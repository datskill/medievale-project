# La Chope d'Étain

Jeu de gestion de taverne médiévale en temps réel, jouable dans le navigateur.

## Jouer

Ouvre `index.html` dans un navigateur, ou active GitHub Pages sur la branche `main` pour y jouer en ligne.

Contrôles : ZQSD ou flèches pour se déplacer, E pour prendre un plat ou servir, R pour préparer une fournée, P pour la pause.

## Boucle de jeu (version 1)

- Le matin : acheter les ingrédients au marché (prix variables chaque jour) et lancer les préparations.
- Le service : les clients (paysans, marchands, chevaliers) s'installent et commandent ; le tavernier va chercher les plats et les sert avant que leur patience s'épuise.
- Le soir : bilan des recettes et de la réputation. Le ragoût et le pain se gardent mal, la bière fermente pendant la nuit.
- Le soir, on dépense ses deniers pour améliorer l'auberge : postes plus grands, tables en plus (jusqu'à six, pour accueillir plus de clients) et packs de décoration (herbes et fleurs, lanternes, tentures, trophées) qui donnent chacun un avantage durable.
- Pas de défaite : en cas de besoin, le seigneur prête de l'argent.

## Technique

Un seul fichier HTML, JavaScript sans dépendance, rendu Canvas 2D. Les ingrédients, recettes, types de clients et équipements sont définis dans l'objet `DATA` en haut du script. Sauvegarde automatique dans le `localStorage` du navigateur.

## Feuille de route

1. Chaîne de production étendue : potager, cultures, moulin, fumoir, qualité des produits.
2. Clients variés avec goûts, budgets et demandes spéciales.
3. Agrandissement et décoration de la taverne.
4. Personnel à embaucher et à gérer.

Voir aussi [docs/conception.md](docs/conception.md) pour le cahier des charges détaillé.
