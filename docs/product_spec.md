# Spécification produit

## Problème résolu

Permettre à un client de commander une expérience narrative personnalisée et de recevoir un jeu complet sans échange préalable, devis ni intervention éditoriale manuelle.

## Proposition de valeur

Le client choisit un univers, un nombre de joueurs et un niveau de personnalisation. Le système sélectionne le contrat de gameplay correspondant, transforme les réponses encadrées en documents prêts à jouer et conserve une enquête conçue, testée et résoluble.

L'organisateur prépare matériellement la soirée, mais il ne devient pas maître du jeu. Il peut incarner un personnage, enquêter et découvrir la solution en même temps que les autres.

## Utilisateur initial

Un adulte organise un dîner, un anniversaire, un week-end, un EVJF/EVG ou une réunion familiale pour 4 à 8 personnes. Il veut une activité mémorable sans écrire le jeu, sans animateur professionnel et sans connaître la solution.

Deux usages initiaux sont couverts :

- petit groupe de quatre personnes recherchant une expérience plus courte ;
- groupe de six à huit personnes souhaitant une soirée longue et immersive.

## Parcours cible

1. Découvrir un univers.
2. Choisir le nombre de joueurs.
3. Charger automatiquement la variante compatible.
4. Choisir l'offre.
5. Visualiser le contenu et la durée.
6. Remplir un formulaire borné.
7. Vérifier les prénoms et contraintes.
8. Payer.
9. Recevoir automatiquement les fichiers.
10. Attribuer les personnages sans lire leurs secrets.
11. Préparer les enveloppes.
12. Lancer le compagnon numérique ou le parcours hors ligne.
13. Jouer sans tâche spéciale.
14. Déposer les accusations avant de déverrouiller la solution.

## Gestion des variantes

Une variante est un contrat de gameplay dédié à un nombre de joueurs ou à un profil de durée.

Elle doit définir :

- ses rôles actifs ;
- les rôles retirés ou convertis ;
- la destination de leurs informations ;
- sa charge de lecture ;
- son budget d'indices ;
- ses durées d'actes ;
- ses aides ;
- ses critères de test.

Une variante ne peut pas être fabriquée en supprimant des dossiers après génération. Elle doit être sélectionnée avant l'attribution des personnages.

## Contrat d'expérience autonome

Un produit commercialisable doit respecter :

- aucun maître du jeu requis ;
- organisateur autorisé à jouer ;
- préparation sans spoiler ;
- règles sans arbitrage extérieur ;
- progression et déverrouillages explicites ;
- informations libres, conditionnelles et obligatoires identifiées ;
- secours pour chaque déclencheur conditionnel ;
- quatre niveaux d'aide ;
- solution inaccessible avant les accusations ;
- parcours hors ligne complet ;
- transfert des informations de tout rôle retiré ;
- version écrite obligatoire de la solution.

La spécification commune se trouve dans `docs/gameplay_experience.md`.

## Profils MVP du Palace des Ombres

### Compact 4 joueurs

- durée recommandée : 90 minutes ;
- plage : 75 à 105 minutes ;
- préparation : environ 15 minutes ;
- quatre rôles actifs ;
- trois actes de 20, 30 et 25 minutes ;
- cinq à sept indices obligatoires ;
- aucune conversion automatique vers trois joueurs.

### Standard 6/8 joueurs

- durée recommandée : 150 minutes ;
- plage : 120 à 180 minutes ;
- préparation : environ 30 minutes ;
- six rôles indispensables et deux rôles optionnels ;
- trois actes de 40, 55 et 45 minutes.

## Hors périmètre initial

- création libre d'une intrigue à la demande ;
- validation manuelle des commandes ;
- retouches illimitées ;
- maître du jeu humain fourni ;
- application mobile native ;
- connexion obligatoire pendant la partie ;
- stockage permanent des profils ;
- expédition physique avant validation du numérique ;
- adaptation improvisée d'une variante en cas d'absence.

## Critères de succès MVP

- un scénario complet pour 4, 6 et 8 joueurs ;
- une solution unique dans chaque variante ;
- au moins trois tests complets par profil ;
- parties terminées sans intervention extérieure ;
- aucune exposition prématurée de la solution ;
- chaque révélation obligatoire distribuée ;
- chaque déclencheur conditionnel doté d'un secours ;
- parcours numérique et hors ligne équivalents ;
- transfert validé des informations des rôles retirés ;
- version quatre joueurs non résoluble par simple élimination ;
- durée compacte observée entre 75 et 105 minutes ;
- génération nominative sans erreur ;
- PDF imprimables sans correction ;
- taux de génération automatique supérieur à 95 % ;
- moins de 5 % de commandes nécessitant une intervention ;
- préparation inférieure à 15 minutes pour le compact et 30 minutes pour le standard, hors impression.
