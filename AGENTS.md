# Instructions aux agents

## Autorité

Les fichiers présents sur `main` sont la source de vérité. Ne pas inventer une règle incompatible avec `engine/`, un champ absent des schémas ou une promesse commerciale absente de `offers/`.

## Séparation des responsabilités

- `offers/` décrit ce qui est vendu.
- `universes/` contient le contenu narratif, les contrats de gameplay spécifiques et leurs variantes.
- `engine/` contient la logique générique indépendante des univers.
- `assets/` décrit les supports de restitution.
- `schemas/` définit les contrats de données.
- `docs/` explique les décisions produit et l'expérience attendue.
- `runtime/` accueillera plus tard le code et les sorties temporaires, jamais le canon narratif.

## Règles de génération

1. Ne jamais laisser un modèle génératif choisir librement le coupable, les preuves obligatoires ou la solution.
2. Les personnalisations ne doivent pas modifier le graphe logique de l'enquête.
3. Toute génération doit être reproductible depuis un identifiant de version, un scénario et une graine.
4. Les anecdotes doivent rester secondaires, non humiliantes et facultatives pour résoudre le jeu.
5. Toute sortie client doit passer les validations bloquantes définies dans `engine/validation_rules.json`.

## Autonomie de jeu

1. Aucun univers commercialisable ne peut exiger un maître du jeu.
2. L'organisateur doit pouvoir préparer et jouer sans connaître la solution.
3. Aucune révélation obligatoire ne peut dépendre de l'intuition ou de l'improvisation de l'organisateur.
4. Chaque information conditionnelle doit avoir un déclencheur explicite et un secours.
5. Chaque acte doit avoir une question collective et une condition de déverrouillage.
6. La solution doit rester verrouillée jusqu'au dépôt des accusations.
7. Un parcours hors ligne doit permettre de terminer la partie sans service distant.
8. Le compagnon numérique rythme et débloque ; il ne remplace pas les interactions physiques.
9. Le coupable peut mentir loyalement, mais ne peut pas contredire les faits immuables ou bloquer une preuve.
10. Toute suppression de rôle doit transférer ses informations indispensables.

Les règles génériques sont dans `engine/autonomous_gameplay.json`. Chaque univers doit fournir un fichier `*_gameplay.json` conforme à `schemas/gameplay_contract.schema.json`.

## Qualité des changements

- JSON valide et formaté avec une indentation de deux espaces.
- Identifiants en `snake_case`, stables et en anglais.
- Textes commerciaux et narratifs en français par défaut.
- Ajouter ou mettre à jour un schéma lors de l'introduction d'une nouvelle structure de données.
- Un changement de règle moteur doit documenter son impact sur les univers existants.
- Aucun fichier vide uniquement destiné à matérialiser un dossier.
- Ne pas déclarer un univers `playtest_ready` tant que son gameplay autonome, ses aides et son mode hors ligne ne sont pas complets.

## Sécurité et données

Ne jamais committer :

- données personnelles de clients ou de joueurs ;
- sorties de commandes réelles ;
- clés, tokens, mots de passe ou secrets ;
- fichiers d'impression personnalisés ;
- journaux contenant des données personnelles.

## Discipline produit

Le système doit rester exploitable avec moins d'une heure de supervision quotidienne. Refuser toute fonctionnalité qui introduit implicitement une validation humaine systématique, une rédaction sur mesure, une animation humaine ou un support individuel non borné.
