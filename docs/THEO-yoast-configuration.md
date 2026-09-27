# Configuration Yoast SEO — Mes Poules au Jardin
**Agent :** THÉO (Développeur WordPress)  
**Plugin :** Yoast SEO (gratuit)

---

## ÉTAPE 1 — Assistant de configuration initial

Après activation, Yoast propose un assistant de configuration. Si vous ne l'avez pas fait :
**Yoast SEO → Tableau de bord → Assistant de configuration**

Réponses à donner dans l'assistant :
```
Type de site        : Blog
Représente un       : Personne (pas une organisation)
Nom de la personne  : Romain
Nom du site         : Mes Poules au Jardin
Logo                : uploader votre favicon (logo.svg converti en PNG)
```

---

## ÉTAPE 2 — Réglages généraux

**Yoast SEO → Réglages → Général**

```
Nom du site         : Mes Poules au Jardin
Slogan alternatif   : Poulaillers, élevage et jardinage au naturel
Séparateur          : · (point médian — plus élégant que le tiret)
```

---

## ÉTAPE 3 — Titres & métas (le plus important)

**Yoast SEO → Réglages → Titres & métas**

### Onglet "Général"
```
Titre du site       : %%sitename%% · Mes Poules au Jardin
```

### Onglet "Types de contenus" → Articles
```
Format du titre     : %%title%% · %%sitename%%
Méta description    : (laisser vide — à remplir manuellement sur chaque article)
Indexable           : Oui ✅
```

### Onglet "Types de contenus" → Pages
```
Format du titre     : %%title%% · Mes Poules au Jardin
Indexable           : Oui ✅
```

### Onglet "Taxonomies" → Catégories
```
Format du titre     : %%term_title%% · Conseils et guides · Mes Poules au Jardin
Indexable           : Oui ✅
```

### Onglet "Taxonomies" → Étiquettes (Tags)
```
Indexable           : Non ❌ (évite le contenu dupliqué)
```

### Onglet "Archives" → Archives auteur
```
Indexable           : Non ❌ (blog solo, inutile)
```

### Onglet "Archives" → Archives par date
```
Indexable           : Non ❌
```

---

## ÉTAPE 4 — Réseaux sociaux

**Yoast SEO → Réglages → Réseaux sociaux**

### Onglet "Comptes"
```
TikTok              : https://www.tiktok.com/@mespoulesaujardin
(les autres : remplir si vous avez les comptes)
```

### Onglet "Facebook" (Open Graph)
```
Activer Open Graph  : Oui ✅
Image par défaut    : uploader votre logo horizontal (logo.svg en PNG)
```

### Onglet "Twitter"
```
Activer Twitter Card : Oui ✅
Format de carte      : Carte récapitulative avec grande image
Nom utilisateur      : (votre compte Twitter si vous en avez un)
```

---

## ÉTAPE 5 — Sitemap XML

**Yoast SEO → Réglages → Avancé → XML Sitemaps**

```
Activer le sitemap XML : Oui ✅
```

Votre sitemap sera disponible à l'adresse :
```
https://mespoulesaujardin.fr/sitemap_index.xml
```

→ Copier cette URL et aller la soumettre dans **Google Search Console → Sitemaps**.

---

## ÉTAPE 6 — Schema (données structurées)

**Yoast SEO → Réglages → Site → Représentation du site**

```
Ce site représente   : Une personne
Nom complet          : Romain
Description          : Passionné d'élevage de poules et de jardinage, je partage mon expérience avec mes 3 ISA Brown sur ma chaîne TikTok et ce blog.
Image de profil      : votre photo (ou photo de vos poules si vous préférez rester anonyme)
```

---

## ÉTAPE 7 — Outils de webmaster

**Yoast SEO → Réglages → Avancé → Outils de webmaster**

```
Google Search Console : coller le code de vérification HTML
(récupérer le code dans Search Console → Paramètres → Vérification de propriété → Balise HTML)
```

---

## ÉTAPE 8 — Robots.txt

**Yoast SEO → Outils → Éditeur de fichiers → robots.txt**

Remplacer le contenu par :
```
User-agent: *
Disallow: /wp-admin/
Allow: /wp-admin/admin-ajax.php
Disallow: /wp-login.php
Disallow: /cart/
Disallow: /mon-compte/

Sitemap: https://mespoulesaujardin.fr/sitemap_index.xml
```

---

## ÉTAPE 9 — Configuration par article (à faire à chaque publication)

Dans chaque article, le panneau Yoast (en bas de l'éditeur) doit être rempli :

### Onglet "SEO"
```
Mot-clé principal   : ex. "avis poulailler eglu go up"
Titre SEO           : Avis poulailler Eglu Go UP : mon test honnête avec 3 poules [2025]
Méta description    : J'ai 3 ISA Brown et un Eglu Go UP depuis plusieurs mois. Mon avis complet : ce qui change vraiment au quotidien, ce qui coûte cher, et pour qui c'est fait.
```

Objectif : feux tricolores **verts** ou au minimum **oranges** avant publication.

### Onglet "Réseaux sociaux"
```
Titre Open Graph    : (laisser identique au titre SEO)
Image Open Graph    : uploader l'image à la une de l'article
Description OG      : (laisser identique à la méta description)
```

---

## Checklist avant de publier chaque article

- [ ] Mot-clé principal renseigné dans Yoast
- [ ] Titre SEO < 60 caractères
- [ ] Méta description entre 120 et 156 caractères
- [ ] Image Open Graph définie
- [ ] Score Yoast : orange minimum, vert idéal
- [ ] Image à la une définie
- [ ] Catégorie sélectionnée
- [ ] URL (permalien) vérifiée

---

*THÉO — Développeur WordPress | Sonnet 4.6*
