# Molly's Files

Moteur de génération d'expériences narratives personnalisées, conçu pour produire automatiquement des jeux d'enquête numériques et physiques à partir de scénarios validés.

## Vision

Molly's Files n'est pas une collection de PDF générés librement. Le produit sépare strictement :

1. les offres commerciales ;
2. les univers narratifs ;
3. le moteur logique ;
4. le gameplay autonome ;
5. les assets de production ;
6. les entrées et sorties contrôlées par schémas.

L'intrigue, la chronologie, les preuves et la solution sont déterministes. La personnalisation modifie l'habillage, jamais la solvabilité de l'enquête.

## Expérience promise

L'organisateur prépare la soirée sans connaître la solution, puis joue comme les autres. Aucun maître du jeu n'est requis.

La progression repose sur :

- des dossiers individuels par acte ;
- des enveloppes collectives ;
- des révélations libres, conditionnelles et obligatoires ;
- des questions collectives ;
- un compagnon numérique léger ;
- un parcours hors ligne ;
- quatre niveaux d'aide anti-blocage ;
- une solution verrouillée jusqu'aux accusations.

La spécification complète est dans [`docs/gameplay_experience.md`](docs/gameplay_experience.md).

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
universes/   Packs narratifs et gameplay propre à chaque univers
engine/      Génération, progression autonome et validations
assets/      Modèles PDF, graphiques, emails et impression
schemas/     Contrats JSON des entrées, sorties et sessions
docs/        Spécifications produit, gameplay et architecture
```

## Contrats de gameplay

- `engine/autonomous_gameplay.json` : règles communes à tous les jeux ;
- `schemas/gameplay_contract.schema.json` : structure obligatoire d'un contrat d'univers ;
- `universes/palace_1930_gameplay.json` : progression autonome du premier univers ;
- `engine/validation_rules.json` : gates empêchant la livraison d'un jeu non autonome.

## Premier MVP

Le premier univers est `palace_1930`, **Le Palace des Ombres**. La cible de production est une enquête numérique pour 6 à 8 joueurs, en trois actes, d'environ 2 h 30, déclinable en offre prête à jouer puis à vos noms.

Le contenu narratif détaillé reste à produire, mais le cadre, le contrat d'enquête et le fonctionnement autonome sont désormais spécifiés.

## Principes non négociables

- une solution unique et démontrable ;
- aucune anecdote personnelle indispensable à la résolution ;
- organisateur sans spoiler et autorisé à jouer ;
- aucun maître du jeu ou animateur extérieur requis ;
- aucun déclencheur indispensable sans solution de secours ;
- parcours hors ligne complet ;
- aucune donnée client durablement stockée sans nécessité ;
- aucune retouche manuelle prévue dans le flux normal ;
- une commande n'est livrée que si tous les contrôles bloquants passent ;
- aucun secret, fichier client ou sortie générée n'est committé dans Git.

## Statut

Socle produit et gameplay autonome spécifiés. Le contenu narratif complet, le moteur exécutable, le compagnon web, le front de commande et la génération PDF restent à développer.
