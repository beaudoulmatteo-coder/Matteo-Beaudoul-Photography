# Matteo Beaudoul Photography — mode d'emploi

## Structure
```
index.html (tout le site dans un seul fichier)
le bloc CONFIGURATION en haut du fichier index.html         → VOS PHOTOS (le seul fichier à modifier pour la galerie)
images/hero/         → hero.jpg (accueil), portrait.jpg (à propos)
images/covers/       → couvertures : sport-automobile.jpg, automobile.jpg, nature.jpg, paysages.jpg, divers.jpg
images/sport-automobile/  images/automobile/  images/nature/  images/paysages/  images/divers/
```

## Ajouter des photos
1. Copiez vos photos dans le bon dossier, ex. `images/nature/foret-01.jpg`
2. Ouvrez `le bloc CONFIGURATION en haut du fichier index.html` et ajoutez le nom dans la liste de la catégorie :
   `photos: ["foret-01.jpg", "foret-02.jpg"]`
3. Enregistrez : la galerie, la visionneuse et le compteur se mettent à jour.

Tant qu'une catégorie est vide, des emplacements temporaires s'affichent.

## Optimiser vos photos (important pour la vitesse)
- Format JPG, grand côté ≈ 2000–2400 px, qualité 80–85 %, idéalement < 600 Ko par photo
- Évitez les espaces et accents dans les noms de fichiers (`course-spa-01.jpg`)
- Outils gratuits : Squoosh.app, Lightroom/export web

## Publier gratuitement
**Netlify Drop** : allez sur app.netlify.com/drop et glissez le dossier du site.
**GitHub Pages** : créez un dépôt, envoyez les fichiers, puis Settings → Pages → branche `main`.
**Cloudflare Pages** : même principe, gratuit.

Le site doit être testé via un serveur (ou une fois publié) ; en ouvrant directement `index.html` il fonctionne aussi.
