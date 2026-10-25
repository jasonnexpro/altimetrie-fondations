# Altimétrie des fondations

Outil de terrain pour vérifier l'altimétrie des massifs et calculer les cales à commander.
C'est un outil indépendant, ouvert depuis Suivi Chantier (Outils). Le plan PDF est lu et calculé **sur l'appareil** : rien n'est envoyé.

## Utilisation

1. **📄 Plan** : ouvrir le plan d'implantation PDF du bureau d'études.
2. **Repérage automatique.**
   - L'outil lit le tableau « points d'implantation » (A/1, B/5…, y compris les files intermédiaires comme A1/1 ou B1/12 sur les pignons) et place une pastille sur chaque massif, calée sur les bulles d'axes et de files.
   - Si un massif de file intermédiaire n'est pas dans le tableau, l'outil le cherche sur le plan : il regarde, à chaque croisement entre une file intermédiaire (bulles A1, B1…) et un axe, s'il y a un massif dessiné en couleur.
   - Si les pastilles sont mal placées : **Décaler** (1 touche) ou **Recaler** (2 touches).
   - Les massifs absents du tableau s'ajoutent avec **＋ Massif**.
3. **Point zéro** : toucher le massif de référence (cote 0).
4. **Saisie** : toucher chaque massif et entrer son écart en mm par rapport au zéro (+ plus haut, − plus bas).
5. **Résultat** :
   - le point zéro optimisé, celui qui demande le moins de cales ;
   - la comparaison avec le zéro de départ ;
   - le total de cales à commander ;
   - le détail dans **📋 Tableau**.
6. **📄 PDF** :
   - la zone d'implantation du plan, avec la cote et les cales à côté de chaque massif ;
   - le point zéro optimisé en haut ;
   - le tableau des cales en bas.

Le relevé en cours (plan, point zéro, cotes) est gardé sur l'appareil jusqu'à **↺ Nouveau**.

## Règles de calcul

- **Cales :** 5 mm, une cale par épaisseur. On ne peut que monter un poteau.
- **Arrondi au plus proche :** 2 mm → 0 cale ; 3 ou 4 mm → 1 cale ; 8 mm → 2 cales. L'écart final est toujours entre −2,5 et +2,5 mm.
- **Point zéro optimisé :**
  - toutes les hauteurs possibles sont testées au demi-millimètre ;
  - on garde celle qui demande le moins de cales ;
  - à égalité, celle qui donne les plus petits écarts finaux, puis la plus proche du zéro de départ.

## Vérifications réalisées

- **Calcul :** contrôlé sur 3 000 relevés aléatoires, en le comparant à une recherche exhaustive au 1/10 de mm ; le minimum de cales est toujours trouvé.
- **Plan 12067 DARBOIS :**
  - 38 massifs lus dans le tableau, dont les 4 massifs de pignon (A1/1, A1/12, B1/1, B1/12), placés automatiquement sur les bons massifs ;
  - le repérage de secours par la couleur retrouve seul ces 4 massifs, à environ 1 point près ;
  - le recalage en 2 touches redonne les mêmes positions ;
  - la saisie au clavier fonctionne ;
  - le relevé est retrouvé après rechargement ;
  - l'export PDF est en A3 paysage, avec le plan vectoriel, les étiquettes et le tableau.
