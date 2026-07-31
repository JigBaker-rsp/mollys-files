# Molly's Files

Moteur de génération d'expériences narratives personnalisées, conçu pour produire automatiquement des jeux d'enquête numériques et physiques à partir de scénarios validés.

## Vision

Molly's Files n'est pas une collection de PDF générés librement. Le produit sépare strictement :

1. les offres commerciales ;
2. les univers narratifs ;
3. le moteur logique ;
4. les assets de production ;
5. les entrées et sorties contrôlées par schémas.

L'intrigue, la chronologie, les preuves et la solution sont déterministes. La personnalisation modifie l'habillage, jamais la solvabilité de l'enquête.

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
universes/   Packs narratifs indépendants
engine/      Règles de génération et de validation
assets/      Modèles PDF, graphiques, emails et impression
schemas/     Contrats JSON des entrées et sorties
docs/        Spécifications produit et architecture
```

## Premier MVP

Le premier univers amorcé est `palace_1930`. La première cible de production est une enquête numérique pour 6 à 8 joueurs, déclinable en offre prête à jouer puis à vos noms.

## Principes non négociables

- une solution unique et démontrable ;
- aucune anecdote personnelle indispensable à la résolution ;
- aucune donnée client durablement stockée sans nécessité ;
- aucune retouche manuelle prévue dans le flux normal ;
- une commande n'est livrée que si tous les contrôles bloquants passent ;
- aucun secret, fichier client ou sortie générée n'est committé dans Git.

## Statut

Socle produit initialisé. Le contenu narratif complet, le moteur exécutable, le front de commande et la génération PDF restent à développer.
