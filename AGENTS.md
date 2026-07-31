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
3. Toute génération doit être reproductible depuis un identifiant de version, un scénario, une variante et une graine.
4. Les anecdotes doivent rester secondaires, non humiliantes et facultatives pour résoudre le jeu.
5. Toute sortie client doit passer les validations bloquantes définies dans `engine/validation_rules.json`.

## Chronologie canonique

1. Chaque univers doit posséder une chronologie canonique validée par `schemas/timeline.schema.json`.
2. Le coupable, le mobile, la méthode, les fenêtres d'accès, l'ingestion, la mort et la découverte sont identiques dans toutes les variantes.
3. Une variante peut modifier le porteur d'une information, jamais le fait matériel ni son horaire verrouillé.
4. Les scènes sociales d'un rôle optionnel peuvent être supprimées ou remplacées uniquement si elles ne changent pas la chaîne du crime.
5. Toute scène ajoutée doit préciser si elle est canonique ou constitue un overlay de variante.
6. Les alibis, révélations, documents et horaires des personnages doivent rester compatibles avec la chronologie canonique.
7. Toute modification d'un horaire verrouillé exige une nouvelle version du contrat narratif, une mise à jour des rôles, des indices, des documents et de toutes les variantes.
8. Une preuve transférée doit conserver la même fonction démonstrative que dans la variante d'origine.
9. Aucun événement optionnel ne peut devenir nécessaire à la résolution d'une autre variante sans mécanisme de transfert explicite.
10. La chronologie réelle et la chronologie de jeu doivent rester séparées : la partie commence après la découverte du corps.

## Gestion des variantes

1. La variante compatible doit être résolue avant l'attribution des personnages.
2. Ne jamais créer une variante en supprimant des dossiers d'une version déjà générée.
3. Toute suppression de rôle doit produire une carte de transfert de ses informations indispensables.
4. Les informations transférées doivent être livrées par un autre personnage, un document collectif ou le compagnon, sans intervention humaine.
5. Une variante compacte doit conserver plusieurs suspects crédibles et ne peut pas être résolue par simple élimination.
6. Chaque variante possède ses propres durées, budgets d'indices, limites d'absence et tests.
7. Une variante ne peut pas être déclarée `playtest_ready` sur la base des tests d'une autre variante.

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

Les règles génériques sont dans `engine/autonomous_gameplay.json`. Chaque univers et chaque variante doivent fournir un fichier `*_gameplay.json` conforme à `schemas/gameplay_contract.schema.json`.

## Qualité des changements

- JSON valide et formaté avec une indentation de deux espaces.
- Identifiants en `snake_case`, stables et en anglais.
- Textes commerciaux et narratifs en français par défaut.
- Ajouter ou mettre à jour un schéma lors de l'introduction d'une nouvelle structure de données.
- Un changement de règle moteur doit documenter son impact sur les univers existants.
- Aucun fichier vide uniquement destiné à matérialiser un dossier.
- Ne pas déclarer un univers ou une variante `playtest_ready` tant que son gameplay autonome, ses aides, son mode hors ligne, sa chronologie et ses tests dédiés ne sont pas complets.

## Sécurité et données

Ne jamais committer :

- données personnelles de clients ou de joueurs ;
- sorties de commandes réelles ;
- clés, tokens, mots de passe ou secrets ;
- fichiers d'impression personnalisés ;
- journaux contenant des données personnelles.

## Discipline produit

Le système doit rester exploitable avec moins d'une heure de supervision quotidienne. Refuser toute fonctionnalité qui introduit implicitement une validation humaine systématique, une rédaction sur mesure, une animation humaine ou un support individuel non borné.
