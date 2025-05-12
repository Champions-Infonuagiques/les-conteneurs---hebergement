# IaaS - Déployer les conteneurs

## Prérequis
- 3 machines virtuelles linux avec Docker installé. Guides: [Créer une machine virtuelle](https://github.com/Champions-Infonuagiques/vscode-developpement-distant#installation-manuelle), [Installation de Docker](https://github.com/Champions-Infonuagiques/vscode-developpement-distant/blob/main/VSCode%20-%20Ubuntu%20-%20Docker%20Installation.md)
- [Activer Swarm mode](https://docs.docker.com/engine/swarm/swarm-mode/)

## Déployer un stack à partir de GitHub vers des machines virtuelles distantes

1. **Configurer l'accès SSH aux machines virtuelles**  
  Assurez-vous que vous pouvez accéder à vos machines virtuelles via SSH. Par exemple :  
  ```bash
  ssh user@<IP_DE_LA_MACHINE>
  ```

2. **Cloner le dépôt GitHub contenant le stack Docker**  
  Sur une des machines virtuelles, exécutez la commande suivante pour cloner le dépôt :  
  ```bash
  git clone <URL_DU_DEPOT>
  cd <NOM_DU_REPERTOIRE>
  ```
3. **Déployer le stack sur le cluster Swarm**  
  Depuis la machine virtuelle principale (manager du cluster Swarm), exécutez la commande suivante :  
  ```bash
  docker stack deploy --compose-file docker-compose.yml <NOM_DU_STACK>
  ```

4. **Vérifier le déploiement**  
  Utilisez la commande suivante pour vérifier que les services sont correctement déployés :  
  ```bash
  docker stack services <NOM_DU_STACK>
  ```

5. **Gérer le stack**  
  - Pour mettre à jour le stack :  
    ```bash
    docker stack deploy --compose-file docker-compose.yml <NOM_DU_STACK>
    ```
  - Pour supprimer le stack :  
    ```bash
    docker stack rm <NOM_DU_STACK>
    ```
