# THÉO — Configuration WordPress complète
**Agent :** THÉO (Développeur WordPress)  
**Date :** 2026-06-03  
**Site :** mespoulesaujardin.fr  
**Thème :** Kadence

---

## ÉTAPE 1 — Configuration initiale WordPress

### Réglages généraux (Réglages → Général)
```
Titre du site      : Mes Poules au Jardin
Slogan             : Poulaillers, élevage et jardinage au naturel
URL WordPress      : https://mespoulesaujardin.fr
URL du site        : https://mespoulesaujardin.fr
Adresse e-mail     : romain.daubras@gmail.com
Fuseau horaire     : Paris
Format de date     : 3 juin 2026
Format d'heure     : 10:25
Langue             : Français
```

### Réglages des permaliens (Réglages → Permaliens)
Choisir : **/%postname%/**
(URLs propres, optimales pour le SEO)

### Réglages de lecture (Réglages → Lecture)
- Page d'accueil : **Une page statique** (créer "Accueil" plus tard)
- Décourager les moteurs : **DÉCOCHÉ** (important !)

### Réglages des discussions (Réglages → Discussion)
- Décocher **Permettre aux visiteurs de poster des commentaires** (anti-spam)
- Ou garder les commentaires et activer l'approbation manuelle

---

## ÉTAPE 2 — Installer le thème Kadence

### Installation
1. **Apparence → Thèmes → Ajouter**
2. Rechercher **"Kadence"**
3. Installer + Activer

### Configuration Kadence (Apparence → Personnaliser)

**Identité du site :**
- Logo : à créer avec IRIS
- Favicon : petit logo carré

**Couleurs (charte IRIS) :**
```
Couleur principale  : #2D6A4F (vert forêt profond)
Couleur secondaire  : #95D5B2 (vert menthe clair)
Couleur accent      : #F4A261 (orange chaud / terre cuite)
Texte               : #1B1B1B
Fond                : #FAFAF8 (blanc cassé naturel)
```

**Typographies recommandées :**
```
Titres  : Playfair Display (serif, élégant, autorité)
Corps   : Lato (sans-serif, lisible, moderne)
```
*À configurer dans Kadence → Design → Typographie*

---

## ÉTAPE 3 — Installer Kadence Starter Template

1. Installer le plugin **Kadence Starter Templates**
2. **Apparence → Starter Templates**
3. Choisir un template "Blog / Nature" proche de la charte
4. Importer uniquement la **structure** (ne pas écraser le contenu)

Ou partir de zéro avec Kadence Blocks directement.

---

## ÉTAPE 4 — Plugins essentiels à installer

### Groupe 1 — SEO (PRIORITÉ 1)
```
Plugin          : Rank Math SEO
Version         : Pro (59€/an) ou gratuit pour débuter
Installation    : Extensions → Ajouter → "Rank Math"
Configuration   : Wizard de configuration → Mode "Custom"
```
*Réglages Rank Math prioritaires :*
- Connecter Google Search Console
- Activer Schema : Article, FAQ, Product
- Sitemap XML : activé, soumettre dans Search Console
- Robots.txt : configuré automatiquement

### Groupe 2 — Performance (PRIORITÉ 1)
```
Plugin          : WP Rocket
Version         : Pro (59€/an) — FORTEMENT recommandé
Alternative     : LiteSpeed Cache (gratuit, excellent sur o2switch)
```
*Si budget limité, utiliser **LiteSpeed Cache** (o2switch utilise LiteSpeed) :*
- Cache activé
- Minification CSS/JS
- Lazy load images
- Preload activé

### Groupe 3 — Sécurité (PRIORITÉ 1)
```
Plugin          : Wordfence Security (gratuit)
Configuration   : Firewall activé, scan hebdomadaire, alertes email
```

### Groupe 4 — Images (PRIORITÉ 2)
```
Plugin          : ShortPixel Image Optimizer
Usage           : Compression automatique des images
Quota           : 100 images/mois gratuit
Alternative     : Imagify (25 crédits/mois gratuit)
```

### Groupe 5 — Sauvegardes (PRIORITÉ 2)
```
Plugin          : UpdraftPlus
Configuration   : Google Drive, quotidien BDD, hebdo fichiers
```

### Groupe 6 — Affiliation (PRIORITÉ 1)
```
Plugin          : ThirstyAffiliates (gratuit)
Usage           : Gérer et masquer les liens Omlet
Exemple         : /recommande/eglu-cube/ → lien Omlet
```

### Groupe 7 — Email (PRIORITÉ 2)
```
Plugin          : Brevo (ex-SendinBlue) — Plugin officiel
Usage           : Formulaires d'inscription, envoi d'emails
Compte Brevo    : Gratuit jusqu'à 300 emails/jour
```

### Groupe 8 — Anti-spam (PRIORITÉ 2)
```
Plugin          : Akismet Anti-Spam (gratuit pour blogs perso)
```

### Groupe 9 — Divers utiles
```
Plugin          : WP Cookieyes (RGPD, bandeau cookies)
Plugin          : Redirection (gérer les 301, éviter les 404)
Plugin          : Duplicate Page (dupliquer des articles/pages)
```

---

## ÉTAPE 5 — Structure des pages à créer

### Pages statiques (menu principal)
```
/                          → Page d'accueil
/blog/                     → Tous les articles
/poulaillers/              → Catégorie poulaillers (SEO pilier)
/races-de-poules/          → Catégorie races
/sante-alimentation/       → Catégorie santé
/jardin-autonomie/         → Catégorie jardin
/mes-recommandations/      → Page hub affiliation Omlet ⭐
/a-propos/                 → Présentation de Romain + la chaîne TikTok
/contact/                  → Formulaire de contact
/mentions-legales/         → Obligatoire RGPD
/politique-confidentialite/ → Obligatoire RGPD
```

### Structure des catégories WordPress
```
Poulaillers & Enclos
  ├── Avis & Comparatifs
  ├── Guides d'achat
  └── Installation

Races de poules
  ├── Races pondeuses
  ├── Races ornementales
  └── Débutants

Santé & Alimentation
  ├── Alimentation
  ├── Maladies & Parasites
  └── Soins naturels

Jardin & Autonomie
  ├── Permaculture
  ├── Potager avec poules
  └── Autonomie alimentaire

Débuter avec des poules
  ├── Premiers pas
  ├── Installation
  └── Législation
```

---

## ÉTAPE 6 — Configuration des URLs de catégories

Dans Rank Math → Titres & Métas → Catégories :
- Format : `%category% - Mes Poules au Jardin`
- Description : rédiger une description unique par catégorie

---

## ÉTAPE 7 — Page d'accueil — Structure recommandée

```
[HEADER]
  Logo | Menu principal | Bouton CTA "Mes Recommandations"

[HERO]
  Titre H1 : "Élevez des poules heureuses dans votre jardin"
  Sous-titre : "Conseils pratiques, avis de poulaillers et guides d'achat pour créer votre élevage familial"
  CTA principal : "Découvrir les meilleurs poulaillers →"
  Image : Poulailler Eglu dans un joli jardin

[BANDE DE CONFIANCE]
  🐔 X abonnés TikTok | ✅ Testé et approuvé | 📝 X articles

[ARTICLES RÉCENTS]
  Grille 3 colonnes — 6 derniers articles

[SECTION RECOMMANDATIONS OMLET]
  "Mes produits préférés" — cards avec liens affiliation
  Eglu Cube | Eglu Go | Walk-In Run | Accessoires

[SECTION NEWSLETTER]
  "Recevez mes conseils chaque semaine"
  Formulaire Brevo intégré
  Lead magnet : "Téléchargez le guide gratuit du débutant"

[FOOTER]
  Liens rapides | Catégories | Mentions légales | Réseaux sociaux
```

---

## ÉTAPE 8 — Configuration GA4 + Search Console (avec DATA)

1. Créer propriété **Google Analytics 4** sur analytics.google.com
2. Ajouter le code GA4 via Rank Math (Rank Math → Général → Analytics)
   OU via plugin **Site Kit by Google**
3. Créer propriété **Google Search Console**
   - Vérification : via DNS (CNAME chez o2switch) ou balise HTML
4. Connecter GA4 à Search Console dans les deux interfaces

---

## Checklist de mise en ligne

- [ ] WordPress configuré (permaliens /%postname%/)
- [ ] Thème Kadence installé et paramétré
- [ ] Couleurs et typographies définies
- [ ] Rank Math installé et configuré
- [ ] Sitemap XML généré et soumis
- [ ] LiteSpeed Cache / WP Rocket configuré
- [ ] Wordfence activé
- [ ] ThirstyAffiliates configuré (liens Omlet masqués)
- [ ] UpdraftPlus + sauvegarde Google Drive
- [ ] Pages légales créées (Mentions légales, RGPD)
- [ ] Page d'accueil publiée
- [ ] GA4 + Search Console connectés
- [ ] Test PageSpeed Insights > 80

---

*THÉO — Développeur WordPress | Sonnet 4.6*
