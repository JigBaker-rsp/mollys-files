# Molly's Files

Moteur de génération d'expériences narratives personnalisées, conçu pour produire automatiquement des jeux d'enquête numériques et physiques à partir de scénarios validés.

## Vision

Molly's Files sépare strictement :

1. les offres commerciales ;
2. les univers narratifs ;
3. les variantes de nombre de joueurs ;
4. le moteur logique ;
5. le gameplay autonome ;
6. les assets et schémas de production.

L'intrigue, la chronologie, les preuves et la solution sont déterministes. La personnalisation modifie l'habillage, jamais la solvabilité de l'enquête.

## Expérience promise

L'organisateur prépare la soirée sans connaître la solution, puis joue comme les autres. Aucun maître du jeu n'est requis.

La progression repose sur des dossiers individuels, des enveloppes collectives, des révélations bornées, des questions collectives, un compagnon numérique léger, un parcours hors ligne et quatre niveaux d'aide.

La spécification commune est dans [`docs/gameplay_experience.md`](docs/gameplay_experience.md).

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
universes/   Univers, contrats de gameplay et variantes
engine/      Génération, progression autonome et validations
assets/      Modèles PDF, graphiques, emails et impression
schemas/     Contrats JSON des entrées, sorties et sessions
docs/        Spécifications produit, gameplay et architecture
```

## Contrats de gameplay

- `engine/autonomous_gameplay.json` : règles communes ;
- `schemas/gameplay_contract.schema.json` : structure obligatoire ;
- `universes/palace_1930_gameplay.json` : édition standard 6/8 joueurs ;
- `universes/palace_1930_4p_gameplay.json` : édition compacte 4 joueurs ;
- `engine/validation_rules.json` : gates empêchant une livraison incohérente.

## Premier MVP

Le premier univers est `palace_1930`, **Le Palace des Ombres**.

Deux profils sont prévus :

| Profil | Joueurs | Durée cible | Préparation |
|---|---:|---:|---:|
| Édition compacte | 4 | 1 h 30, plage 1 h 15–1 h 45 | environ 15 min |
| Édition standard | 6 ou 8 | 2 h 30, plage 2 h–3 h | environ 30 min |

L'édition compacte est une variante dédiée. Elle conserve quatre personnages actifs et transforme les informations des rôles retirés en témoignages et documents autonomes. Elle ne peut pas être obtenue en supprimant simplement deux dossiers de l'édition standard.

La conception détaillée est décrite dans [`docs/palace_1930_four_players.md`](docs/palace_1930_four_players.md).

## Principes non négociables

- une solution unique et démontrable ;
- aucune anecdote personnelle indispensable ;
- organisateur sans spoiler et autorisé à jouer ;
- aucun maître du jeu requis ;
- aucun déclencheur indispensable sans secours ;
- parcours hors ligne complet ;
- variante choisie avant génération ;
- transfert contrôlé des informations lorsqu'un rôle est retiré ;
- aucune version compacte résoluble par simple élimination ;
- aucune retouche manuelle dans le flux normal ;
- livraison uniquement après passage de tous les contrôles ;
- aucune donnée client ou sortie générée committée dans Git.

## Statut

Socle produit, gameplay autonome et profils 4/6/8 joueurs spécifiés. Le contenu narratif complet, le moteur exécutable, le compagnon web, le front de commande et la génération PDF restent à développer.
