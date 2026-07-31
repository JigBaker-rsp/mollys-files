# Spécification produit

## Problème résolu

Permettre à un client de commander une expérience narrative personnalisée et de recevoir un jeu complet sans échange préalable, devis ni intervention éditoriale manuelle.

## Proposition de valeur

Le client choisit un univers et un niveau de personnalisation. Le système transforme ses réponses encadrées en documents prêts à jouer, tout en conservant une enquête conçue, testée et résoluble.

L'organisateur prépare matériellement la soirée, mais il ne devient pas maître du jeu. Il peut incarner un personnage, enquêter et découvrir la solution en même temps que les autres.

## Utilisateur initial

Un adulte organise une soirée, un anniversaire, un week-end, un EVJF/EVG ou une réunion familiale pour 6 à 8 personnes. Il veut une activité mémorable sans écrire lui-même le jeu, sans animateur professionnel et sans connaître la solution à l'avance.

## Parcours cible

1. Découvrir un univers.
2. Choisir le nombre de joueurs et l'offre.
3. Visualiser précisément le contenu livré.
4. Remplir un formulaire borné.
5. Vérifier les prénoms et contraintes.
6. Payer.
7. Recevoir automatiquement les fichiers.
8. Attribuer les personnages sans lire leurs secrets.
9. Préparer les enveloppes à l'aide d'une checklist courte.
10. Lancer le compagnon numérique ou le parcours hors ligne.
11. Jouer comme les autres sans tâche spéciale.
12. Déposer les accusations avant de déverrouiller la solution.

## Contrat d'expérience autonome

Un produit Molly's Files commercialisable doit respecter les exigences suivantes :

- aucun maître du jeu requis ;
- organisateur autorisé à jouer ;
- préparation sans spoiler ;
- règles lisibles sans arbitrage extérieur ;
- progression par actes, questions collectives et déverrouillages explicites ;
- informations libres, conditionnelles et obligatoires identifiées ;
- mécanisme de secours pour chaque déclencheur conditionnel ;
- quatre niveaux d'aide anti-blocage ;
- solution inaccessible avant les accusations ;
- parcours hors ligne complet ;
- transfert des informations indispensables en cas de retrait d'un rôle optionnel ;
- version écrite obligatoire de la solution.

La spécification détaillée se trouve dans `docs/gameplay_experience.md`. Les règles génériques exécutables se trouvent dans `engine/autonomous_gameplay.json`.

## Hors périmètre initial

- création libre d'une intrigue à la demande ;
- validation manuelle des commandes ;
- retouches illimitées ;
- maître du jeu humain fourni par Molly's Files ;
- application mobile native ;
- dépendance obligatoire à une connexion pendant la partie ;
- stockage permanent des profils de joueurs ;
- expédition physique avant validation du produit numérique.

Le compagnon numérique collectif est prévu comme une interface web légère de progression. Il ne doit pas devenir un jeu en temps réel nécessitant que chaque participant reste sur son téléphone.

## Critères de succès MVP

- un scénario complet pour 6 et 8 joueurs ;
- une solution unique validée ;
- une partie testée au moins trois fois ;
- trois parties terminées sans intervention extérieure ;
- aucune exposition prématurée de la solution à l'organisateur ;
- chaque acte jouable sans improvisation d'un facilitateur ;
- chaque révélation obligatoire distribuée avant son échéance ;
- chaque déclencheur conditionnel doté d'un secours testé ;
- parcours numérique et hors ligne menant à la même solution ;
- une génération nominative sans erreur ;
- des PDF imprimables sans correction ;
- un taux de génération automatique supérieur à 95 % ;
- moins de 5 % de commandes nécessitant une intervention ;
- préparation cible inférieure à 30 minutes hors impression.
