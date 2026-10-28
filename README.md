# Bus & Car Archives — prototype gratuit

Application statique de test pour OCRiser les PDF, rechercher le texte et construire progressivement un index thématique des articles.

## Utilisation
1. Publier `index.html` sur un hébergement statique HTTPS (ex. GitHub Pages).
2. Ouvrir l’URL dans un navigateur moderne.
3. Sélectionner un PDF depuis l’appareil ou iCloud Drive et lancer l’analyse OCR.
4. Dans « Sommaires et index thématique », choisir une page susceptible de contenir le sommaire et consulter son texte OCR.
5. Recopier le titre exact, choisir la rubrique, renseigner le numéro du magazine et la page de début de l’article (page imprimée dans le magazine/PDF selon ton repérage), puis valider l’entrée. Coche « vérifié » uniquement après contrôle dans le PDF original.
6. Exporter régulièrement le JSON : il contient désormais les pages OCR et les entrées thématiques. Importer ce JSON sur un autre appareil pour transférer les données.

## Index thématique
- Rubriques proposées : essais de véhicules, circuits/voyages, dossiers, salons/expositions, réseaux/transports urbains, technique, actualités, portraits/interviews, marché de l’occasion/petites annonces et autre.
- Les entrées sont filtrables par rubrique et recherchables par numéro, titre, véhicule, thème et notes.
- Les pages de sommaire proposées automatiquement sont des candidates, pas une détection garantie. L’extraction des titres et la suggestion de rubrique utilisent des règles heuristiques ; les pages imprimées et les intitulés doivent être vérifiés manuellement. Les propositions ne sont jamais marquées comme vérifiées automatiquement.
- Les données sont stockées localement dans IndexedDB ; aucun PDF n’est envoyé à un serveur par cette application.

## Technologie et limites
- PDF.js : lecture des couches texte et rendu des pages.
- Tesseract.js : OCR français côté navigateur lorsque le PDF est un scan.
- IndexedDB : stockage local de l’index.
- Export/import JSON : sauvegarde manuelle et transfert.
- Les bibliothèques et le modèle OCR sont téléchargés depuis des CDN ; une connexion Internet est nécessaire.
- Pas encore de synchronisation automatique entre appareils ou avec Notion, ni d’ouverture directe du PDF à la page recherchée.
- Ne publie pas les magazines eux-mêmes sur GitHub : seul le code doit être publié.
