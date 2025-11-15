# Garderie Saint-Bruno - Site Web

Site web statique pour la Garderie Saint-Bruno, déployé sur Cloudflare Pages.

## Structure

- `index.html` - Page d'accueil
- `contact.html` - Page de contact
- `styles.css` - Feuille de style principale
- `public/` - Assets statiques (images, fonts)
  - `images/` - Toutes les images du site
  - `font/` - Police de caractères (Fragmentcore)

## Déploiement

Ce site est configuré pour être déployé sur Cloudflare Pages.

### Via l'interface Cloudflare
1. Connecter le dépôt Git à Cloudflare Pages
2. Configurer le build output directory: `/`
3. Déployer

### Via Wrangler CLI
```bash
wrangler pages deploy .
```

## Contact

1435 Roberval, Saint-Bruno, QC J3V 3P7  
514-894-2424

## Technologies

- HTML5
- CSS3 (avec variables CSS et Grid/Flexbox)
- Police personnalisée: Fragmentcore

## Responsive

Le site est entièrement responsive et optimisé pour mobile, tablette et desktop.

