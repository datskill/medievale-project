# La Chope d'Étain

Jeu de gestion de taverne médiévale en temps réel, jouable dans le navigateur.

## Jouer

Ouvre `index.html` dans un navigateur, ou active GitHub Pages sur la branche `main` pour y jouer en ligne.

Contrôles : ZQSD ou flèches pour se déplacer, E pour prendre un plat ou servir, R pour préparer une fournée, P pour la pause.

## Boucle de jeu (version 1)

- Le matin : acheter les ingrédients au marché et lancer les préparations. Les prix fluctuent chaque jour ; une petite courbe et une flèche indiquent si une denrée est moins chère ou plus chère que sa moyenne des sept derniers jours.
- La réserve a une place limitée (25, 50 puis 90 ingrédients, agrandie le soir). La viande se garde 2 jours, le pain 3, le fromage 4 : au-delà, elle pourrit.
- Le service : les clients (paysans, marchands, chevaliers) s'installent et commandent ; le tavernier va chercher les plats et les sert avant que leur patience s'épuise.
- Le soir : bilan des recettes et de la réputation. Le ragoût et le pain se gardent mal, la bière fermente pendant la nuit.
- Le soir, on dépense ses deniers pour améliorer l'auberge : postes plus grands, réserve plus grande, tables en plus (jusqu'à six, pour accueillir plus de clients) et packs de décoration (herbes et fleurs, lanternes, tentures, trophées) qui donnent chacun un avantage durable.
- Pas de défaite : en cas de besoin, le seigneur prête de l'argent.

## Les tavernes

On commence dans une petite taverne de hameau. Quand la réputation et la bourse le permettent, le bilan du soir propose d'acheter la taverne suivante. L'ancienne est confiée à un gérant et verse une rente chaque soir, selon la réputation qu'on y a laissée et ce qu'on y a investi. Dans la nouvelle, on repart à 30 de réputation, avec des postes de base.

| Taverne | Prix | Réputation | On y sert | Clients | Airs |
|---|---|---|---|---|---|
| La Chope d'Étain, le hameau | départ | – | bière, ragoût, pain et fromage | paysans, marchands, chevaliers | La Danse du Tonneau, La Complainte de l'Aubergiste, Le Branle de la Chope |
| Le Relais du Bourg | 500 d | 75 | hydromel, potée au lard, tourte aux pommes | paysans, pèlerins, marchands, chevaliers | La Gigue du Relais, Le Pas du Pèlerin |
| L'Hostellerie du Lion d'Or | 1 500 d | 80 | vin, civet de lapin, fromages et noix | marchands, pèlerins, bourgeois, chevaliers, dames | La Pavane des Bourgeois, La Ronde des Marchands |
| La Grande Salle du Château | 4 000 d | 85 | hypocras, sanglier aux champignons, massepain | bourgeois, chevaliers, dames, seigneurs | La Fanfare du Seigneur, La Basse Danse de la Reine |

Chaque taverne a ses denrées au marché, son décor et ses prix : les améliorations y coûtent plus cher, mais les plats rapportent davantage. Tout est défini dans `DATA.tavernes`.

## Technique

Un seul fichier HTML, JavaScript sans dépendance, rendu Canvas 2D. Les ingrédients, recettes, types de clients et équipements sont définis dans l'objet `DATA` en haut du script. Sauvegarde automatique dans le `localStorage` du navigateur.

## Feuille de route

1. Chaîne de production étendue : potager, cultures, moulin, fumoir, qualité des produits.
2. Clients variés avec goûts, budgets et demandes spéciales.
3. Agrandissement et décoration de la taverne.
4. Personnel à embaucher et à gérer.

Voir aussi [docs/conception.md](docs/conception.md) pour le cahier des charges détaillé.
