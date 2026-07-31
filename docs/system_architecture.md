# Architecture du système

## Couches

### Produit

`offers/` définit les promesses, entrées, sorties, délais et limites de chaque offre. Cette couche ne contient aucune intrigue.

### Contenu

`universes/` contient les packs narratifs versionnés : cadre, rôles, chronologie, indices, fausses pistes et preuve de solution.

### Moteur

`engine/` orchestre l'attribution des rôles, l'application des personnalisations, les contrôles et la livraison. Il ne dépend d'aucun univers particulier.

### Assets

`assets/` définit les modèles de documents, les formats de sortie et les exigences d'impression.

### Contrats

`schemas/` valide les données reçues et produites. Les formulaires futurs doivent être générés ou vérifiés à partir de ces contrats.

## Architecture cible

```text
Storefront / Marketplace
          |
          v
Order API -> Input validation -> Generation queue
                                  |
                                  v
                  Offer + Universe + Engine version
                                  |
                                  v
                     Deterministic role assignment
                                  |
                                  v
                        Controlled personalization
                                  |
                                  v
                         Document rendering
                                  |
                                  v
                     Logic and file validation gates
                                  |
                     +------------+------------+
                     |                         |
                     v                         v
              Digital delivery        Print fulfillment API
```

## Données

Les données personnelles doivent être isolées du dépôt et des packs narratifs. Une commande conserve uniquement ce qui est nécessaire à sa génération, son support limité et ses obligations commerciales. Une suppression automatique doit être planifiée.

## Déploiement envisagé

Le Raspberry Pi peut servir au développement, aux tests, à l'orchestration et à la supervision. La production commerciale devra pouvoir migrer vers un hébergement redondant sans modification des formats de contenu.

## Étapes techniques suivantes

1. choisir le langage du moteur ;
2. créer un validateur JSON automatisé ;
3. modéliser les rôles et indices du premier univers ;
4. construire le graphe de preuve ;
5. créer le renderer PDF ;
6. exposer une commande locale de génération ;
7. ajouter des tests de non-régression ;
8. connecter ensuite formulaire, paiement et livraison.
