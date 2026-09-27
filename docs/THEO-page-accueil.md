# Page d'accueil — Mes Poules au Jardin
**Agent :** THÉO (Développeur WordPress)
**Page :** Accueil (statique)

Dans WordPress : Pages → Accueil → modifier
Supprimer tout le contenu importé existant.
Coller les blocs HTML ci-dessous un par un dans l'ordre.

---

## BLOC 1 — HERO

Bloc : HTML personnalisé

```html
<div style="background:linear-gradient(140deg,#2C5F4A 0%,#4A8C6F 100%);border-radius:16px;padding:56px 40px;text-align:center;margin-bottom:8px;">
  <p style="font-size:11px;font-weight:700;letter-spacing:4px;text-transform:uppercase;color:#A8D5BA;margin:0 0 16px;">Élevage de poules au naturel</p>
  <h1 style="font-family:Georgia,serif;font-size:42px;font-weight:700;color:#FFFFFF;line-height:1.15;margin:0 0 20px;max-width:640px;margin-left:auto;margin-right:auto;">Élever des poules heureuses,<br>c'est plus simple<br>qu'on ne le croit</h1>
  <p style="font-size:17px;color:rgba(255,255,255,0.8);line-height:1.7;max-width:520px;margin:0 auto 32px;">Conseils pratiques, avis de poulaillers et guides d'achat — partagés chaque semaine sur TikTok et ce blog.</p>
  <div style="display:flex;gap:12px;justify-content:center;flex-wrap:wrap;">
    <a href="/mes-recommandations/" style="display:inline-block;background:#D4724A;color:#fff;padding:14px 28px;border-radius:50px;font-size:15px;font-weight:700;text-decoration:none;letter-spacing:0.3px;">Mes recommandations →</a>
    <a href="/blog/" style="display:inline-block;background:rgba(255,255,255,0.15);color:#fff;padding:14px 28px;border-radius:50px;font-size:15px;font-weight:700;text-decoration:none;border:1px solid rgba(255,255,255,0.3);">Voir les articles</a>
  </div>
</div>
```

---

## BLOC 2 — BANDE DE CONFIANCE

Bloc : HTML personnalisé

```html
<div style="background:#F0E8D8;border-radius:12px;padding:24px 32px;display:flex;justify-content:center;gap:48px;flex-wrap:wrap;text-align:center;margin-bottom:8px;">
  <div>
    <p style="font-family:Georgia,serif;font-size:28px;font-weight:700;color:#2C5F4A;margin:0 0 4px;">[X]K</p>
    <p style="font-size:12px;color:#7A6250;margin:0;letter-spacing:1px;text-transform:uppercase;">Abonnés TikTok</p>
  </div>
  <div style="width:1px;background:#E8E2D8;"></div>
  <div>
    <p style="font-family:Georgia,serif;font-size:28px;font-weight:700;color:#2C5F4A;margin:0 0 4px;">3</p>
    <p style="font-size:12px;color:#7A6250;margin:0;letter-spacing:1px;text-transform:uppercase;">ISA Brown au jardin</p>
  </div>
  <div style="width:1px;background:#E8E2D8;"></div>
  <div>
    <p style="font-family:Georgia,serif;font-size:28px;font-weight:700;color:#2C5F4A;margin:0 0 4px;">100%</p>
    <p style="font-size:12px;color:#7A6250;margin:0;letter-spacing:1px;text-transform:uppercase;">Testé personnellement</p>
  </div>
</div>
```

Remplacer `[X]K` par votre nombre d'abonnés TikTok.

---

## BLOC 3 — TITRE DE SECTION "Derniers articles"

Bloc : **Titre** (H2 natif Gutenberg)

```
Derniers articles
```

Style : H2, couleur `#2A1F16`, alignement gauche.

Puis ajouter un bloc **Séparateur** (ligne fine, couleur `#E8E2D8`).

---

## BLOC 4 — GRILLE D'ARTICLES

Bloc : **Derniers articles** (bloc natif WordPress)
OU si Kadence Blocks installé : **Kadence Posts** (meilleur rendu)

Réglages du bloc :
```
Nombre d'articles    : 3
Colonnes             : 3
Afficher image       : Oui
Afficher extrait     : Oui (150 caractères)
Afficher date        : Oui
Afficher catégorie   : Oui
```

---

## BLOC 5 — MES RECOMMANDATIONS OMLET

Bloc : HTML personnalisé

```html
<div style="background:#2C5F4A;border-radius:16px;padding:48px 40px;margin:8px 0;">
  <p style="font-size:11px;font-weight:700;letter-spacing:4px;text-transform:uppercase;color:#A8D5BA;margin:0 0 8px;">Produits que j'utilise vraiment</p>
  <h2 style="font-family:Georgia,serif;font-size:32px;font-weight:700;color:#FFFFFF;margin:0 0 8px;">Mes recommandations</h2>
  <p style="font-size:15px;color:rgba(255,255,255,0.7);margin:0 0 36px;">Je ne recommande que ce que j'utilise personnellement. Liens affiliés Omlet.</p>

  <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:16px;">

    <!-- CARTE 1 — Eglu Go UP -->
    <div style="background:rgba(255,255,255,0.08);border-radius:12px;padding:24px;border:1px solid rgba(255,255,255,0.12);">
      <p style="font-size:10px;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:#A8D5BA;margin:0 0 8px;">Mon poulailler</p>
      <p style="font-family:Georgia,serif;font-size:18px;font-weight:700;color:#fff;margin:0 0 10px;">Eglu Go UP</p>
      <p style="font-size:13px;color:rgba(255,255,255,0.65);margin:0 0 20px;line-height:1.6;">Léger, facile à nettoyer, résistant aux renards. Parfait pour 2-3 poules.</p>
      <a href="/recommande/eglu-go-up/" rel="sponsored nofollow" target="_blank" style="display:inline-block;background:#D4724A;color:#fff;padding:10px 20px;border-radius:50px;font-size:13px;font-weight:700;text-decoration:none;">Voir sur Omlet →</a>
    </div>

    <!-- CARTE 2 — Eglu Cube -->
    <div style="background:rgba(255,255,255,0.08);border-radius:12px;padding:24px;border:1px solid rgba(255,255,255,0.12);">
      <p style="font-size:10px;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:#A8D5BA;margin:0 0 8px;">Pour 4-6 poules</p>
      <p style="font-family:Georgia,serif;font-size:18px;font-weight:700;color:#fff;margin:0 0 10px;">Eglu Cube</p>
      <p style="font-size:13px;color:rgba(255,255,255,0.65);margin:0 0 20px;line-height:1.6;">Le modèle premium. Isolation supérieure, enclos extensible.</p>
      <a href="/recommande/eglu-cube/" rel="sponsored nofollow" target="_blank" style="display:inline-block;background:#D4724A;color:#fff;padding:10px 20px;border-radius:50px;font-size:13px;font-weight:700;text-decoration:none;">Voir sur Omlet →</a>
    </div>

    <!-- CARTE 3 — Walk-In Run -->
    <div style="background:rgba(255,255,255,0.08);border-radius:12px;padding:24px;border:1px solid rgba(255,255,255,0.12);">
      <p style="font-size:10px;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:#A8D5BA;margin:0 0 8px;">Enclos</p>
      <p style="font-family:Georgia,serif;font-size:18px;font-weight:700;color:#fff;margin:0 0 10px;">Walk-In Run</p>
      <p style="font-size:13px;color:rgba(255,255,255,0.65);margin:0 0 20px;line-height:1.6;">Grand enclos modulaire. Solide, extensible, pour laisser vos poules se dépenser.</p>
      <a href="/recommande/walk-in-run/" rel="sponsored nofollow" target="_blank" style="display:inline-block;background:#D4724A;color:#fff;padding:10px 20px;border-radius:50px;font-size:13px;font-weight:700;text-decoration:none;">Voir sur Omlet →</a>
    </div>

  </div>

  <p style="text-align:center;margin:28px 0 0;">
    <a href="/mes-recommandations/" style="color:#A8D5BA;font-size:14px;font-weight:600;text-decoration:none;">Voir toutes mes recommandations →</a>
  </p>
</div>
```

---

## BLOC 6 — À PROPOS (bande courte)

Bloc : HTML personnalisé

```html
<div style="display:flex;gap:32px;align-items:center;background:#FAF6EF;border-radius:12px;padding:32px;border:1.5px solid #E8E2D8;flex-wrap:wrap;">
  <div style="flex:1;min-width:200px;">
    <p style="font-size:11px;font-weight:700;letter-spacing:3px;text-transform:uppercase;color:#4A8C6F;margin:0 0 8px;">Qui suis-je ?</p>
    <h3 style="font-family:Georgia,serif;font-size:22px;font-weight:700;color:#2A1F16;margin:0 0 12px;">Romain, éleveur amateur et créateur TikTok</h3>
    <p style="font-size:15px;color:#7A6250;line-height:1.7;margin:0 0 20px;">J'ai 3 ISA Brown dans mon jardin et un Eglu Go UP. Sur TikTok je partage mon quotidien avec elles — ici je vais plus loin avec des guides, des comparatifs et des avis honnêtes.</p>
    <a href="/a-propos/" style="display:inline-block;background:transparent;color:#2C5F4A;padding:10px 22px;border-radius:50px;font-size:14px;font-weight:700;text-decoration:none;border:2px solid #2C5F4A;">En savoir plus →</a>
  </div>
</div>
```

---

## BLOC 7 — NEWSLETTER

Bloc : HTML personnalisé + Formulaire Brevo

```html
<div style="background:linear-gradient(135deg,#F0E8D8 0%,#FAF6EF 100%);border-radius:16px;padding:48px 40px;text-align:center;border:1.5px solid #E8E2D8;">
  <p style="font-size:32px;margin:0 0 12px;">🐔</p>
  <h2 style="font-family:Georgia,serif;font-size:28px;font-weight:700;color:#2C5F4A;margin:0 0 12px;">Recevez mes conseils chaque semaine</h2>
  <p style="font-size:15px;color:#7A6250;margin:0 0 24px;max-width:460px;margin-left:auto;margin-right:auto;line-height:1.7;">Conseils d'élevage, nouveaux articles et bons plans Omlet — directement dans votre boîte mail.</p>
  [FORMULAIRE BREVO ICI]
  <p style="font-size:12px;color:#7A6250;margin:16px 0 0;">Pas de spam. Désinscription en 1 clic.</p>
</div>
```

Pour le formulaire Brevo :
1. Connectez-vous sur brevo.com
2. Contacts → Formulaires → Créer un formulaire
3. Champ email uniquement → Copier le code HTML
4. Remplacer `[FORMULAIRE BREVO ICI]` par le code copié

---

## Dans WordPress : régler la page d'accueil statique

Réglages → Lecture :
```
La page d'accueil affiche : Une page statique
Page d'accueil : Accueil
Page des articles : Blog  ← créer cette page vide si pas encore fait
```

---

*THÉO — Développeur WordPress | Sonnet 4.6*
