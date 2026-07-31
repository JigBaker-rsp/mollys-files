# Instructions aux agents

## Autorité

Les fichiers présents sur `main` sont la source de vérité. Ne pas inventer une règle incompatible avec `engine/`, un champ absent des schémas ou une promesse commerciale absente de `offers/`.

## Séparation des responsabilités

- `offers/` décrit ce qui est vendu.
- `universes/` contient le contenu narratif et ses variantes.
- `engine/` contient la logique générique indépendante des univers.
- `assets/` décrit les supports de restitution.
- `schemas/` définit les contrats de données.
- `runtime/` accueillera plus tard le code et les sorties temporaires, jamais le canon narratif.

## Règles de génération

1. Ne jamais laisser un modèle génératif choisir librement le coupable, les preuves obligatoires ou la solution.
2. Les personnalisations ne doivent pas modifier le graphe logique de l'enquête.
3. Toute génération doit être reproductible depuis un identifiant de version, un scénario et une graine.
4. Les anecdotes doivent rester secondaires, non humiliantes et facultatives pour résoudre le jeu.
5. Toute sortie client doit passer les validations bloquantes définies dans `engine/validation_rules.json`.

## Qualité des changements

- JSON valide et formaté avec une indentation de deux espaces.
- Identifiants en `snake_case`, stables et en anglais.
- Textes commerciaux et narratifs en français par défaut.
- Ajouter ou mettre à jour un schéma lors de l'introduction d'une nouvelle structure de données.
- Un changement de règle moteur doit documenter son impact sur les univers existants.
- Aucun fichier vide uniquement destiné à matérialiser un dossier.

## Sécurité et données

Ne jamais committer :

- données personnelles de clients ou de joueurs ;
- sorties de commandes réelles ;
- clés, tokens, mots de passe ou secrets ;
- fichiers d'impression personnalisés ;
- journaux contenant des données personnelles.

## Discipline produit

Le système doit rester exploitable avec moins d'une heure de supervision quotidienne. Refuser toute fonctionnalité qui introduit implicitement une validation humaine systématique, une rédaction sur mesure ou un support individuel non borné.
