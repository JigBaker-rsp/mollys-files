# Molly's Files

Moteur de génération d'expériences narratives personnalisées, conçu pour produire automatiquement des jeux d'enquête numériques et physiques à partir de scénarios validés.

## Vision

Molly's Files sépare strictement les offres commerciales, les univers narratifs, les variantes de nombre de joueurs, les personnages, la chronologie canonique, le moteur logique, le gameplay autonome et les assets de production.

L'intrigue, les personnages, la chronologie du crime, les preuves et la solution sont déterministes. La personnalisation modifie les noms et l'habillage, jamais la solvabilité de l'enquête.

## Expérience promise

L'organisateur prépare la soirée sans connaître la solution, puis joue comme les autres. Aucun maître du jeu n'est requis.

La progression repose sur des dossiers individuels, des enveloppes collectives, des révélations bornées, des questions collectives, un compagnon numérique léger, un parcours hors ligne et quatre niveaux d'aide.

## Offres initiales

| Code | Offre | Livraison |
|---|---|---|
| `ready_to_play` | Enquête prête à jouer | Immédiate |
| `named_enquiry` | Enquête à vos noms | Automatique, moins d'une heure |
| `complices_edition` | Édition Complices | Automatique, sous 24 h annoncées |
| `event_box` | Coffret Événement | Impression et expédition à la demande |

## Architecture

```text
offers/      Définition des produits vendus
universes/   Univers, personnages, chronologies, gameplay et variantes
engine/      Génération, attribution, progression et validations
assets/      Modèles PDF, graphiques, emails et impression
schemas/     Contrats JSON des entrées, rôles, chronologies, sorties et sessions
docs/        Spécifications produit et expérience
```

## Premier MVP

Le premier univers est `palace_1930`, **Le Palace des Ombres**.

| Profil | Joueurs | Durée cible | Préparation |
|---|---:|---:|---:|
| Édition compacte | 4 | 1 h 30 | environ 15 min |
| Édition standard | 6 ou 8 | 2 h 30 | environ 30 min |

L'édition compacte est une variante dédiée. Elle conserve quatre personnages actifs et transforme les informations des rôles retirés en témoignages et documents autonomes.

## Casting canonique

Le casting compte huit rôles :

- Camille de Valleroy, l'héritier·ère — coupable canonique ;
- Jeanne Mercier, la directrice du palace ;
- Docteur Gabriel Renaud, le médecin de famille ;
- Lucien Delmas, le secrétaire particulier ;
- Véra Lenoir, la vedette du gala ;
- Armand Keller, le banquier et investisseur ;
- Élise Morel, la journaliste sous couverture ;
- Madeleine Rochefort, l'aviatrice et messagère privée.

Les quatre premiers constituent l'édition compacte. Véra et Armand complètent l'édition 6 joueurs. Élise et Madeleine complètent l'édition 8 joueurs.

Contrats :

- `universes/palace_1930/characters/index.json` : manifeste du casting et transferts de variante ;
- `universes/palace_1930/characters/role_01.json` à `role_08.json` : rôles détaillés ;
- `schemas/character_role.schema.json` : structure obligatoire ;
- `engine/character_system.json` : règles d'attribution et de personnalisation ;
- `docs/palace_1930_characters.md` : présentation lisible du casting.

## Chronologie canonique

La chronologie criminelle est identique dans les versions 4, 6 et 8 joueurs. Les scènes sociales supplémentaires peuvent varier, mais elles ne modifient jamais :

- le prélèvement de la préparation fictive à 15:43 ;
- la substitution du flacon entre 15:57 et 16:02 ;
- l'ingestion à 22:21 ;
- l'entrée dans le bureau verrouillé à 22:45 ;
- la mort à 23:08 ;
- la découverte à 07:55.

Les rôles absents sont remplacés par des documents ou des témoignages ayant la même fonction démonstrative.

Contrats :

- `universes/palace_1930/timeline/canonical_timeline.json` : événements réels et horaires verrouillés ;
- `universes/palace_1930/timeline/variant_delivery.json` : porteurs des preuves et scènes propres aux variantes ;
- `schemas/timeline.schema.json` : structure obligatoire ;
- `docs/palace_1930_timeline.md` : chronologie minute par minute et chaîne de démonstration.

## Principes non négociables

- une solution unique et démontrable ;
- un seul coupable verrouillé ;
- même chronologie criminelle dans toutes les variantes ;
- chaque rôle possède un mobile, un secret, un objectif, une raison de mentir et une information utile ;
- aucun rôle purement décoratif ;
- organisateur sans spoiler et autorisé à jouer ;
- aucun maître du jeu requis ;
- aucun déclencheur indispensable sans secours ;
- transfert contrôlé des informations lorsqu'un rôle est retiré ;
- aucune version compacte résoluble par simple élimination ;
- noms et pronoms personnalisables, fonctions narratives immuables ;
- aucune donnée client ou sortie générée committée dans Git.

## Statut

Socle produit, gameplay autonome, profils 4/6/8 joueurs, huit rôles canoniques et chronologie minute par minute spécifiés. Il reste à écrire les documents, la chaîne de preuves exécutable, les dossiers joueurs finaux, le moteur, le compagnon web et les PDF.
