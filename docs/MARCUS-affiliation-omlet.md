# MARCUS — Configuration Affiliation Omlet
**Agent :** MARCUS (Expert Marketing d'Affiliation)  
**Date :** 2026-06-03

---

## ÉTAPE 1 — Récupérer vos liens Omlet

Dans votre tableau de bord affilié Omlet, récupérez les liens pour ces produits prioritaires :

| Produit | Priorité | Prix indicatif | Commission estimée |
|---------|----------|---------------|-------------------|
| Eglu Cube + enclos | ⭐⭐⭐⭐⭐ | ~700–900€ | 35–72€ |
| Eglu Go UP + enclos | ⭐⭐⭐⭐⭐ | ~400–600€ | 20–48€ |
| Eglu Go + enclos | ⭐⭐⭐⭐ | ~300–500€ | 15–40€ |
| Walk In Chicken Run | ⭐⭐⭐⭐ | ~300–600€ | 15–48€ |
| Mangeoire Omlet | ⭐⭐⭐ | ~30–60€ | 1.5–5€ |
| Abreuvoir Omlet | ⭐⭐⭐ | ~30–60€ | 1.5–5€ |
| Porte automatique | ⭐⭐⭐⭐ | ~150–200€ | 7–16€ |
| Accessoires divers | ⭐⭐ | ~10–50€ | 0.5–4€ |

---

## ÉTAPE 2 — Configurer ThirstyAffiliates

### Créer les catégories de liens
Dans **ThirstyAffiliates → Liens → Ajouter une catégorie** :
- Poulaillers Omlet
- Enclos Omlet
- Accessoires Omlet
- Autres partenaires (pour l'avenir)

### Ajouter chaque lien (Ajouter un lien affilié)
Exemple pour l'Eglu Cube :
```
Nom           : Eglu Cube - Poulailler Omlet
URL de dest.  : [votre lien affilié Omlet]
URL cloakée   : /recommande/eglu-cube/
Catégorie     : Poulaillers Omlet
Nofollow      : ✅ Oui (obligatoire pour Google)
Sponsored     : ✅ Oui
```

Faire pareil pour chaque produit :
```
/recommande/eglu-go/
/recommande/eglu-go-up/
/recommande/walk-in-run/
/recommande/porte-automatique/
/recommande/mangeoire-omlet/
/recommande/abreuvoir-omlet/
/recommande/accessoires-omlet/
```

### Activer le tracking des clics
**ThirstyAffiliates → Options → Général → Enable Link Click Tracking** ✅

---

## ÉTAPE 3 — Créer la page "Mes Recommandations"

C'est votre **page hub affiliation** — la plus importante du site.

### URL : mespoulesaujardin.fr/mes-recommandations/

### Structure de la page

```
[H1] Mes recommandations de produits pour vos poules

[INTRO PERSONNELLE]
"Voici les produits que j'utilise vraiment dans mon jardin et que 
je recommande à ma communauté TikTok. J'ai testé chacun d'eux."

⚠️ Note de transparence : certains liens sont affiliés (je touche
une commission sans surcoût pour vous). Cela m'aide à maintenir
ce blog gratuit. Je ne recommande que ce que j'utilise vraiment.

---

[SECTION 1] 🏠 Les poulaillers que je recommande

[CARD PRODUIT — EGLU CUBE]
  Image officielle Omlet
  ⭐⭐⭐⭐⭐ "Mon préféré"
  "Le meilleur poulailler pour 4-6 poules. Design, facile à nettoyer,
   isolation thermique excellente."
  ✅ Pour qui : familles, jardins de taille moyenne
  💰 Prix : à partir de XXX€
  [Bouton CTA] "Voir le prix sur Omlet →"

[CARD PRODUIT — EGLU GO UP]
  Image officielle Omlet  
  ⭐⭐⭐⭐⭐ "Idéal pour débuter"
  "Perché, léger, parfait pour 2-3 poules. Mon conseil pour les débutants."
  ✅ Pour qui : débutants, petits jardins
  [Bouton CTA] "Voir le prix sur Omlet →"

[CARD PRODUIT — EGLU GO]
  ⭐⭐⭐⭐
  "La version au sol, très accessible."
  [Bouton CTA] "Voir le prix sur Omlet →"

---

[SECTION 2] 🔒 Les enclos

[CARD — WALK IN CHICKEN RUN]
  "L'enclos que j'ai acheté pour mes poules. Grande taille, solide."
  [Bouton CTA] "Voir sur Omlet →"

---

[SECTION 3] 🌾 Accessoires indispensables

[LISTE] Mangeoire | Abreuvoir | Porte automatique | Thermomètre

---

[SECTION 4] 📚 Mes autres ressources

[Liens internes] vers les meilleurs articles du site
```

### Boutons CTA — Style recommandé (Kadence)
- **Couleur :** #F4A261 (orange chaud) avec texte blanc
- **Texte :** "Voir le prix sur Omlet →" (jamais "Acheter ici")
- **Taille :** large, bien visible, espacé
- **Position :** après chaque description produit ET en fin de card

---

## ÉTAPE 4 — Disclosure légale (obligatoire)

Ajouter en haut de **chaque article avec liens affiliés** :

> *Cet article contient des liens d'affiliation. Si vous achetez via ces liens, je perçois une commission sans frais supplémentaires pour vous. Je ne recommande que des produits que j'utilise et approuve personnellement.*

Créer un shortcode dans WordPress pour l'insérer facilement :
```
[disclosure_affiliation]
```

---

## KPI à suivre (DATA)

| Métrique | Outil | Fréquence |
|---------|-------|-----------|
| Clics par lien Omlet | ThirstyAffiliates | Hebdomadaire |
| Conversions (achats) | Dashboard Omlet | Hebdomadaire |
| CTR des CTA | GA4 Events | Mensuel |
| Revenue par article | Dashboard Omlet | Mensuel |

---

*MARCUS — Expert Marketing d'Affiliation | Sonnet 4.6*
