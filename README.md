# Mon doux planning

PWA statique prête à déployer. Ouvrez `index.html` via un serveur web (et non en double-cliquant le fichier) : le service worker, l'installation et les notifications requièrent `https` ou `localhost`.

## Déploiement sur GitHub Pages

1. Créez un nouveau dépôt GitHub vide, par exemple `mon-doux-planning`.
2. Dans ce dossier, exécutez les commandes suivantes en remplaçant `VOTRE-PSEUDO` :

   ```powershell
   git init
   git add .
   git commit -m "Publier mon doux planning"
   git branch -M main
   git remote add origin https://github.com/VOTRE-PSEUDO/mon-doux-planning.git
   git push -u origin main
   ```

3. Dans GitHub : **Settings** → **Pages** → **Build and deployment** → sélectionnez **GitHub Actions**.
4. Attendez la fin du workflow « Déployer sur GitHub Pages ». Le lien sera de la forme `https://VOTRE-PSEUDO.github.io/mon-doux-planning/`.
5. Ouvrez ce lien sur iPhone dans Safari, puis utilisez Partager → « Sur l’écran d’accueil ».

L’application sera automatiquement republiée à chaque `git push` vers `main`.

Les créneaux sont enregistrés uniquement dans le `localStorage` du navigateur. Le bouton d'export génère les événements récurrents chaque semaine avec une alarme au début de chaque activité.
