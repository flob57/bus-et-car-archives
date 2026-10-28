# Bus & Car Archives — prototype gratuit

Application statique de test pour extraire le texte des PDF et rechercher des occurrences page par page.

## Utilisation
1. Publier `index.html` sur un hébergement statique HTTPS (ex. GitHub Pages).
2. Ouvrir l’URL dans un navigateur moderne.
3. Sélectionner un PDF depuis l’appareil/iCloud Drive et lancer l’analyse.
4. Rechercher un terme puis exporter régulièrement l’index JSON.

## Technologie
- PDF.js : lecture des couches texte et rendu des pages.
- Tesseract.js : OCR français côté navigateur lorsque le PDF est un scan.
- IndexedDB : stockage local de l’index dans le navigateur.
- Export/import JSON : sauvegarde manuelle et transfert de l’index.

## Limites
- Les PDF originaux ne sont pas copiés et ne sont pas envoyés à un serveur par l’application.
- Le traitement est local au navigateur ; l’index n’est pas synchronisé automatiquement entre appareils.
- Les bibliothèques et le modèle OCR sont téléchargés depuis des CDN ; une connexion Internet est nécessaire.
- Les mots-clés sont des suggestions statistiques, pas une analyse IA. Pas encore de découpage en articles, de thèmes automatiques ou de synchronisation Notion.
- Tester d’abord un seul numéro. Les PDF longs peuvent consommer beaucoup de mémoire.
- N’ajoute pas les magazines au dépôt GitHub : seul le code doit être publié.
