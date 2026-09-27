# ALEX — Guide d'infrastructure o2switch
**Agent :** ALEX (Administrateur Système)  
**Date :** 2026-06-03  
**Domaine :** mespoulesaujardin.fr  
**Hébergeur :** o2switch (cPanel)

---

## ÉTAPE 1 — Pointer le domaine vers o2switch

### Chez votre registrar (o2switch, espace client)
O2switch est à la fois registrar et hébergeur — le DNS est donc géré dans le même espace client.

1. Connectez-vous sur **clients.o2switch.fr**
2. Aller dans **Espace client → Domaines → mespoulesaujardin.fr → Gérer les DNS**
3. Vérifier que les nameservers pointent vers o2switch :
   ```
   ns1.o2switch.net
   ns2.o2switch.net
   ```
   (Normalement déjà configuré puisque domaine acheté chez eux)

4. Dans cPanel, aller dans **Domaines → Domaines** → vérifier que `mespoulesaujardin.fr` est bien listé comme domaine principal.

---

## ÉTAPE 2 — Activer SSL (HTTPS gratuit)

1. Dans **cPanel → Sécurité → SSL/TLS Status**
2. Cocher `mespoulesaujardin.fr` et `www.mespoulesaujardin.fr`
3. Cliquer **Run AutoSSL** → Let's Encrypt s'installe automatiquement (~2 min)
4. Vérifier le cadenas vert sur `https://mespoulesaujardin.fr`

---

## ÉTAPE 3 — Installer WordPress via Softaculous

1. Dans **cPanel → Softaculous Apps Installer → WordPress**
2. Cliquer **Install Now**
3. Paramètres :
   ```
   Protocol   : https://
   Domain     : mespoulesaujardin.fr
   Directory  : (vide — installation à la racine)
   Site Name  : Mes Poules au Jardin
   Site Desc  : Élevage de poules, poulaillers et jardinage
   Admin User : (choisir un nom DIFFÉRENT de "admin")
   Admin Pass : (mot de passe fort — 20+ caractères)
   Admin Email: romain.daubras@gmail.com
   Language   : Français
   ```
4. Décocher **Limit Login Attempts Reloaded** (on installera Wordfence à la place)
5. Cliquer **Install** → WordPress installé en 60 secondes

> ⚠️ NOTER les identifiants dans un gestionnaire de mots de passe (Bitwarden recommandé)

---

## ÉTAPE 4 — Configurer les redirections HTTP → HTTPS

Dans **cPanel → Domaines → Redirections** :
- Ajouter : `http://mespoulesaujardin.fr` → `https://mespoulesaujardin.fr` (permanente 301)
- Ajouter : `http://www.mespoulesaujardin.fr` → `https://mespoulesaujardin.fr` (permanente 301)

OU dans WordPress (après installation), ajouter dans **wp-config.php** :
```php
define('FORCE_SSL_ADMIN', true);
```

Et dans **.htaccess** (via cPanel → Gestionnaire de fichiers) :
```apache
RewriteEngine On
RewriteCond %{HTTPS} off
RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
```

---

## ÉTAPE 5 — Configurer les sauvegardes automatiques

O2switch inclut des sauvegardes JetBackup dans cPanel.

1. **cPanel → Fichiers → JetBackup 5**
2. Vérifier que les sauvegardes sont programmées (quotidien, 30 jours)
3. Faire une **sauvegarde manuelle immédiate** avant toute modification

En plus, configurer le plugin WordPress **UpdraftPlus** :
- Sauvegarde vers Google Drive ou Dropbox
- Fréquence : quotidienne (base de données) / hebdomadaire (fichiers)
- Rétention : 30 jours

---

## ÉTAPE 6 — Créer les adresses email professionnelles

Dans **cPanel → Email → Comptes Email** :
```
contact@mespoulesaujardin.fr
romain@mespoulesaujardin.fr  (optionnel)
newsletter@mespoulesaujardin.fr  (pour Brevo)
```

---

## ÉTAPE 7 — Configurer Cloudflare (CDN + protection)

1. Créer un compte gratuit sur **cloudflare.com**
2. Ajouter le site `mespoulesaujardin.fr`
3. Cloudflare détecte les DNS actuels — cliquer **Continue**
4. Choisir le plan **Free**
5. Cloudflare donne 2 nouveaux nameservers (ex: `mia.ns.cloudflare.com`)
6. Dans l'espace client o2switch → Domaines → **changer les nameservers** vers ceux de Cloudflare
7. Propagation DNS : 24–48h

**Configuration Cloudflare recommandée :**
- SSL/TLS : **Full (strict)**
- Speed → **Auto Minify** : JS + CSS + HTML
- Caching → **Cache Level : Standard**
- Security → **Firewall : Medium**

> ⏳ Cloudflare est optionnel en phase 1. Peut être ajouté à J+30 si la priorité est ailleurs.

---

## Checklist de vérification finale

- [ ] mespoulesaujardin.fr accessible en HTTPS
- [ ] www redirige vers non-www
- [ ] WordPress installé (admin ≠ "admin")
- [ ] SSL valide (cadenas vert)
- [ ] Sauvegarde JetBackup active
- [ ] Adresse email contact@ créée
- [ ] Accès wp-admin fonctionnel

---

*ALEX — Administrateur Système | Haiku 4.5*
