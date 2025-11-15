# Instructions de déploiement - Cloudflare Pages

## Étape 1: Installer Git (si pas déjà installé)

Téléchargez Git depuis: https://git-scm.com/download/win

## Étape 2: Initialiser le dépôt Git local

Ouvrez PowerShell ou Git Bash dans le dossier du projet et exécutez:

```bash
git init
git add .
git commit -m "Initial commit - Garderie Saint-Bruno website"
```

## Étape 3: Créer un dépôt sur GitHub

1. Allez sur https://github.com
2. Cliquez sur le bouton "+" en haut à droite
3. Sélectionnez "New repository"
4. Nom du dépôt: `gargeriesaintbruno` (ou votre choix)
5. Laissez-le **public** ou **private** (votre choix)
6. **NE PAS** cocher "Initialize with README" (on a déjà nos fichiers)
7. Cliquez sur "Create repository"

## Étape 4: Connecter le dépôt local à GitHub

GitHub vous donnera des commandes. Utilisez celles-ci (remplacez `votre-username` par votre nom d'utilisateur GitHub):

```bash
git branch -M main
git remote add origin https://github.com/votre-username/gargeriesaintbruno.git
git push -u origin main
```

Si vous utilisez SSH au lieu de HTTPS:
```bash
git remote add origin git@github.com:votre-username/gargeriesaintbruno.git
```

## Étape 5: Autoriser Cloudflare Pages sur GitHub

1. Allez sur https://github.com/settings/installations
2. Trouvez "Cloudflare Pages" dans la liste
3. Cliquez sur "Configure"
4. Assurez-vous que votre dépôt `gargeriesaintbruno` est sélectionné
5. Cliquez sur "Save"

## Étape 6: Déployer sur Cloudflare Pages

1. Retournez sur Cloudflare Pages: https://dash.cloudflare.com
2. Cliquez sur "Create a project"
3. Sélectionnez "Connect to Git"
4. Choisissez "GitHub"
5. Autorisez Cloudflare si demandé
6. Votre dépôt `gargeriesaintbruno` devrait maintenant apparaître dans la liste
7. Sélectionnez-le
8. Cliquez sur "Begin setup"

## Configuration du build dans Cloudflare Pages

- **Project name**: `garderiesaintbruno` (ou votre choix)
- **Production branch**: `main`
- **Framework preset**: `None` (ou `Static HTML`)
- **Build command**: (laisser vide)
- **Build output directory**: `/` (racine)
- **Root directory**: `/` (racine)

Cliquez sur "Save and Deploy"

## Vérification

Une fois déployé, votre site sera disponible sur:
- `https://garderiesaintbruno.pages.dev` (ou le nom que vous avez choisi)

## Problèmes courants

### Le dépôt n'apparaît pas dans Cloudflare Pages
- Vérifiez que vous avez poussé le code sur GitHub (étape 4)
- Vérifiez que Cloudflare Pages a accès au dépôt (étape 5)
- Rafraîchissez la page Cloudflare Pages

### Erreur de build
- Vérifiez que "Build output directory" est `/`
- Vérifiez que tous les fichiers sont bien dans le dépôt GitHub

