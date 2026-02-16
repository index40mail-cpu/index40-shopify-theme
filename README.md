# INDEX40 — Shopify Theme

Thème Shopify minimal et custom pour INDEX40. Pas de bloat, juste ce qui est nécessaire.

## Structure

```
index40-shopify-theme/
├── layout/
│   └── theme.liquid              # Wrapper HTML (contient content_for_header pour le tracking natif)
├── templates/
│   ├── index.json                # Homepage → section INDEX40
│   ├── product.json              # Page produit (Rapport Complet)
│   ├── cart.json                 # Panier
│   ├── collection.json           # Collection
│   ├── page.json                 # Pages statiques (legal, CGU, etc.)
│   └── 404.json                  # Page 404
├── sections/
│   ├── index40-landing.liquid    # ⭐ Landing page complète (CSS + HTML + JS)
│   ├── product.liquid            # Page produit minimale
│   ├── cart.liquid               # Panier
│   ├── collection.liquid         # Collection
│   ├── page.liquid               # Contenu pages
│   └── 404.liquid                # 404
├── config/
│   ├── settings_schema.json      # Info thème
│   └── settings_data.json        # Settings par défaut
├── locales/
│   └── fr.default.json           # Traductions FR
└── assets/                       # Fichiers statiques (favicon, images, etc.)
```

## Déploiement

1. Push ce repo sur GitHub
2. Shopify Admin → Boutique en ligne → Thèmes → Import theme → **Connect from GitHub**
3. Sélectionne ce repo
4. Chaque `git push` déploie automatiquement

## Tracking

Le tracking est géré **nativement par Shopify** via `{{ content_for_header }}` dans theme.liquid.

Configure tes pixels dans **Settings → Customer events** :
- Meta Pixel + CAPI (server-side) → via l'app Meta & Instagram
- Google Ads + GA4 → via l'app Google & YouTube
- Clarity → custom pixel

## Configuration

Dans le **Theme Editor** (Personnaliser), la section INDEX40 a 2 settings :
- **API Endpoint** : URL de ton API de lookup profil
- **Test URL** : URL de la page quiz
