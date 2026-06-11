# WSDL / XSD Mapper

Application web autonome (un seul fichier HTML, **100 % local, hors-ligne, aucune donnée envoyée**) pour comparer et mapper des schémas WSDL/XSD — pensée pour les travaux de la réforme de la facturation électronique (CII, UBL, Factur-X, Chorus Pro…).

## Utilisation

Ouvre simplement [`index.html`](index.html) dans un navigateur (double-clic). Aucune installation, aucun serveur.

Démo en ligne : **https://samy-che.github.io/wsdl-xsd-mapper/**

## Fonctionnalités

- **Chargement multi-fichiers par côté** — dépose un schéma et ses `import`/`include` ; les références croisées sont résolues, les schémas embarqués dans `<wsdl:types>` sont extraits automatiquement.
- **Vue Mapping** — arborescence des champs côte à côte, reliée par des lignes façon SAP CPI. Types et occurrences (`minOccurs..maxOccurs`) affichés.
- **Mapping manuel** — clic gauche puis clic droit pour relier deux champs ; bouton pour désactiver le mapping automatique.
- **Détection des écarts** — un champ présent des deux côtés mais avec un **type** (feuilles) ou une **cardinalité** différents est signalé ⚠️ (orange).
- **Vue Comparaison** — tableau triable/filtrable : appariés, écarts, uniquement F1, uniquement F2 (avec types et occurrences).
- **Validateur** — bonne formation XML (avec ligne/colonne de l'erreur) + contrôles structurels XSD : références non résolues, `import`/`include` non chargés, doublons de noms, types définis mais inutilisés.
- **Exports CSV / JSON** du résultat de comparaison.
- **Thème clair / sombre** (préférence mémorisée).

## Confidentialité

Tout le traitement se fait dans le navigateur. Aucun fichier n'est téléversé ni transmis à un serveur — adapté aux schémas confidentiels.
