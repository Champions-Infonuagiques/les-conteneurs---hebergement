# L'hébergement de conteneurs
## IaaS - Swarm
Pour la mise en production de conteneurs, il est recommandé d'utiliser au minimum 3 nodes. Ce qui assure l'élection d'une node de gestion en cas de panne.
### Les requis
- Minimum 3 machines virtuelles avec Docker
### Recommandé
- Un service de proxy inversé (reserve proxy) pour les ports exposés web.
- Un service de balance de charge pour les ports exposés non-web.

### Procédures
[Déployer les conteneurs](./doc/IaaS%20-%20Déployer%20les%20conteneurs.md)

## Amazon Elastic Container Service (ECS)
[Démarrez avec Amazon ECS](https://aws.amazon.com/fr/ecs/getting-started/?pg=ln&cp=bn)

## AWS Fargate for Amazon ECS
[Deploy Docker Containers on Amazon ECS - HOW-TO GUIDE](https://aws.amazon.com/fr/getting-started/hands-on/deploy-docker-containers/?nc1=h_ls)

## Azure Container Instances (ACI)
[Démarrage rapide : Déployer un instance de conteneur dans Azure à l’aide du portail Azure](https://learn.microsoft.com/fr-ca/azure/container-instances/container-instances-quickstart-portal)
