# Molly's Files

Moteur de génération d'expériences narratives personnalisées, conçu pour produire automatiquement des jeux d'enquête numériques et physiques à partir de scénarios validés.

## Vision

Molly's Files sépare strictement les offres, les univers, les variantes, les personnages, la chronologie, les preuves, le gameplay autonome et les assets de production.

La personnalisation modifie les noms et l'habillage. Le coupable, les faits, les horaires et la solution restent déterministes.

## Expérience promise

L'organisateur prépare la soirée sans connaître la solution, puis joue comme les autres. Aucun maître du jeu n'est requis.

## Premier MVP — Le Palace des Ombres

En 1934, le propriétaire d'un palace alpin est retrouvé mort dans son bureau verrouillé. L'enquête immédiate cache une seconde histoire : le Belladone a été construit sur l'effacement d'Émile Mercier, associé oublié de la famille de Valleroy.

Cette histoire cachée crée des mobiles concurrents mais ne constitue pas une seconde enquête criminelle : Émile est mort accidentellement en 1920.

| Profil | Joueurs | Durée cible |
|---|---:|---:|
| Édition compacte | 4 | 1 h 30 |
| Édition standard | 6 ou 8 | 2 h 30 |

## Casting

- Camille de Valleroy — héritier·ère et coupable canonique ;
- Jeanne Mercier — directrice et fille du fondateur effacé ;
- Docteur Gabriel Renaud — médecin lié aux archives de 1920 ;
- Lucien Delmas — secrétaire et copiste des dossiers ;
- Véra Lenoir — vedette du gala et détentrice des lettres d'Auguste ;
- Armand Keller — banquier à l'origine du montage financier ;
- Élise Morel — journaliste enquêtant sur l'effacement d'Émile ;
- Madeleine Rochefort — messagère transportant l'acte de 1919.

Camille peut être soupçonné tôt, mais ne doit jamais être prouvé coupable par une pièce unique. L'emprunt de la clé possède une justification réelle, le témoin du couloir ne l'identifie pas formellement et le mobile complet n'apparaît qu'à l'acte III.

## Sources de vérité

- `universes/palace_1930.json` : manifeste de l'univers ;
- `universes/palace_1930/lore/foundation_secret.json` : mensonge fondateur ;
- `universes/palace_1930/characters/index.json` : manifeste des rôles ;
- `universes/palace_1930/characters/role_01.json` à `role_08.json` : rôles détaillés ;
- `universes/palace_1930/timeline/index.json` : autorité de version ;
- `universes/palace_1930/timeline/canonical_timeline_v0_6.json` : chronologie réelle ;
- `universes/palace_1930/timeline/variant_delivery_v0_6.json` : diffusion 4/6/8 joueurs ;
- `docs/palace_1930_characters.md` : casting lisible ;
- `docs/palace_1930_timeline_v0_6.md` : chronologie lisible ;
- `engine/validation_rules.json` : contrôles bloquants.

Les anciens fichiers de chronologie v0.5 restent présents pour l'historique mais sont explicitement dépassés dans `timeline/index.json`.

## Principes non négociables

- solution unique et démontrable ;
- un seul coupable verrouillé ;
- aucun rôle purement décoratif ;
- aucun indice unique suffisant pour condamner ;
- histoire cachée distincte de la chaîne du meurtre ;
- aucun second meurtre historique ;
- organisateur sans spoiler et autorisé à jouer ;
- aucun maître du jeu requis ;
- transfert contrôlé des preuves selon le nombre de joueurs ;
- aucune donnée client ou sortie générée committée dans Git.

## Statut

Socle produit, variantes 4/6/8 joueurs, casting rééquilibré, histoire cachée et chronologie v0.6 spécifiés. Il reste à produire le graphe de preuves, les documents, les fiches joueurs finales, les aides, le moteur exécutable, le compagnon web et les PDF.
