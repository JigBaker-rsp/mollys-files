# Molly's Files

Moteur de génération d'expériences narratives personnalisées, conçu pour produire automatiquement des jeux d'enquête numériques et physiques à partir de scénarios validés.

## Vision

Molly's Files sépare strictement les offres commerciales, les univers narratifs, les variantes de nombre de joueurs, les personnages, le moteur logique, le gameplay autonome et les assets de production.

L'intrigue, les personnages, la chronologie, les preuves et la solution sont déterministes. La personnalisation modifie les noms et l'habillage, jamais la solvabilité de l'enquête.

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
universes/   Univers, personnages, gameplay et variantes
engine/      Génération, attribution, progression et validations
assets/      Modèles PDF, graphiques, emails et impression
schemas/     Contrats JSON des entrées, rôles, sorties et sessions
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

## Principes non négociables

- une solution unique et démontrable ;
- un seul coupable verrouillé ;
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

Socle produit, gameplay autonome, profils 4/6/8 joueurs et huit rôles canoniques spécifiés. Il reste à écrire la chronologie minute par minute, les documents, la chaîne de preuves, les dossiers joueurs finaux, le moteur exécutable, le compagnon web et les PDF.
