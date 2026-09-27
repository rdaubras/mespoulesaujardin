# CYPHER — Durcissement sécurité WordPress
**Agent :** CYPHER (Expert Cybersécurité)  
**Date :** 2026-06-03  
**Site :** mespoulesaujardin.fr

---

## Checklist de durcissement WordPress

### 1. Compte administrateur
- [ ] Nom d'utilisateur admin ≠ "admin" / "romain" / nom de domaine
- [ ] Mot de passe : 20+ caractères, lettres + chiffres + symboles
- [ ] Adresse email admin différente de l'email public
- [ ] Activer l'authentification à deux facteurs (Wordfence → Login Security → 2FA)

### 2. Wordfence Configuration
- [ ] **Firewall → Enable Firewall** (mode étendu)
- [ ] **Login Security → Brute Force** : bloquer après 5 tentatives
- [ ] **Login Security → 2FA** : activer pour le compte admin
- [ ] **Scan → Planifier** : scan complet hebdomadaire
- [ ] **Alertes email** : activées pour les blocages et malwares

### 3. Protection de wp-admin
Ajouter dans **.htaccess** (dossier /wp-admin/) :
```apache
# Autoriser uniquement votre IP (remplacer x.x.x.x)
Order Deny,Allow
Deny from All
Allow from x.x.x.x
```
*Ou utiliser Cloudflare Access Rules pour restreindre /wp-admin/*

### 4. Protection wp-config.php
Ajouter dans **.htaccess** (racine du site) :
```apache
<files wp-config.php>
order allow,deny
deny from all
</files>
```

### 5. Désactiver l'éditeur de fichiers WordPress
Dans **wp-config.php** :
```php
define('DISALLOW_FILE_EDIT', true);
define('DISALLOW_FILE_MODS', true); // Bloque aussi les màj plugins/thèmes via admin
```
*Garder DISALLOW_FILE_MODS à false si vous voulez mettre à jour via l'admin*

### 6. Masquer la version WordPress
Rank Math → Général → Avancé → désactiver **Afficher la version WordPress**

OU dans **functions.php** du thème enfant :
```php
remove_action('wp_head', 'wp_generator');
```

### 7. Sécuriser les uploads
Créer un fichier **.htaccess** dans `/wp-content/uploads/` :
```apache
<Files ~ "\.php$">
  Order allow,deny
  Deny from all
</Files>
```

### 8. Cookies de sécurité
Ajouter dans **wp-config.php** (utiliser le générateur WordPress : api.wordpress.org/secret-key/1.1/salt/) :
```php
define('AUTH_KEY',         'clé-unique-ici');
define('SECURE_AUTH_KEY',  'clé-unique-ici');
define('LOGGED_IN_KEY',    'clé-unique-ici');
define('NONCE_KEY',        'clé-unique-ici');
// etc.
```

### 9. Headers de sécurité HTTP
Dans **.htaccess** (racine) :
```apache
Header always set X-Content-Type-Options "nosniff"
Header always set X-Frame-Options "SAMEORIGIN"
Header always set X-XSS-Protection "1; mode=block"
Header always set Referrer-Policy "strict-origin-when-cross-origin"
```
*Cloudflare peut gérer ces headers si activé*

### 10. Mises à jour automatiques
Dans **wp-config.php** :
```php
define('WP_AUTO_UPDATE_CORE', 'minor'); // Mises à jour mineures auto
```
Pour les plugins : **Extensions → Mises à jour automatiques** → activer pour tous les plugins de confiance.

---

## Audit de sécurité initial — Score cible : A

Tester sur **immuniweb.com/websec** ou **observatory.mozilla.org** après mise en ligne.

Score cible minimum : **B+ (70/100)**  
Score cible optimal : **A (90/100)**

---

## Plan de réponse aux incidents

**En cas de piratage :**
1. Passer le site en maintenance (plugin "Under Construction")
2. Changer TOUS les mots de passe (WordPress, FTP, cPanel, base de données)
3. Restaurer depuis la dernière sauvegarde propre (JetBackup o2switch)
4. Scanner avec Wordfence et/ou MalCare
5. Contacter le support o2switch

**Sauvegardes de secours :**
- o2switch JetBackup : 30 jours
- UpdraftPlus → Google Drive : 30 jours
- Sauvegarde manuelle mensuelle : télécharger localement

---

*CYPHER — Expert Cybersécurité | Sonnet 4.6*
