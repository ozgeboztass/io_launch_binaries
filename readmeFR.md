# Binaires officiels IO-Net

Ce dépôt contient les binaires officiels pour io.net - Suivez les instructions ci-dessous pour configurer et exécuter les binaires sur votre système d'exploitation respectif.

## Prérequis

### Pour Linux
- Docker
- Pilotes Nvidia (dans le cas d'un GPU Worker) (l'exécution de io-setup l'installera automatiquement si nécessaire)
- Nvidia container toolkit (dans le cas de GPU Worker) (l'exécution de io-setup l'installera automatiquement si nécessaire)

### Pour Mac
- Docker Desktop
 - [Télécharger Docker Desktop pour Mac](https://www.docker.com/products/docker-desktop/) - choisissez la version mac - apple chip pour le téléchargement.

## Installation

### Linux

1. **Exécuter IO-Setup (une fois pour le matériel)** (sauter si docker et les pilotes Nvidia sont déjà installés et configurés)
 - Téléchargez le script d'installation : 
```
 curl -L https://github.com/ionet-official/io-net-official-setup-script/raw/main/ionet-setup.sh -o ionet-setup.sh
 ```
 - Exécutez le script :
 ```
 chmod +x ionet-setup.sh && ./ionet-setup.sh
 ```
 ##### Note - au cas où la commande curl échouerait : 
- Installez `curl` : 
```
 sudo apt install curl
 ```

2. **Pour les systèmes avec GPU**
 - Attendez le redémarrage.
 - Après le redémarrage, relancez l'installation avec la commande ci-dessus.

### Démarrer les conteneurs en utilisant binaire

3. **Télécharger et lancer le binaire** :
 ```
 curl -L https://github.com/ionet-official/io_launch_binaries/raw/main/launch_binary_linux -o launch_binary_linux
 chmod +x launch_binary_linux
 ```

- Lancer en mode interactif ou copier la commande générée depuis le site web.
 ```
 ./launch_binary_linux
 ```


### Mac

- **Télécharger et lancer le binaire** :
 ```
 curl -L https://github.com/ionet-official/io_launch_binaries/raw/main/launch_binary_mac -o launch_binary_mac
 chmod +x launch_binary_mac
 ```

- Lancer en mode interactif ou copier la commande générée depuis le site web.
 ```
 ./lancement_binaire_mac
 ```

- Dépannage (optionnel)

 - Si vous rencontrez un message d'erreur tel que "mauvais type de CPU dans l'exécutable", cela indique probablement que vous exécutez un logiciel conçu pour un processeur Intel sur un appareil Apple Silicon. Pour résoudre ce problème, vous devrez installer Rosetta 2, qui permet de supporter les processeurs Intel dans Docker sur les appareils Apple Silicon.
 
```
 softwareupdate --install-rosetta
 ```

 - Une fois l'installation de Rosetta terminée, relancez la commande excute.
 
```
 ./launch_binary_mac
 ```

<!-- ### Windows

1. **Télécharger le binaire** :
- Allez dans votre navigateur et collez :
 ```
 wget https://github.com/ionet-official/io_launch_binaries/raw/main/launch_binary_windows
 ```
- Double-cliquez sur le fichier téléchargé et remplissez les détails en mode interactif. -->


## Support

Pour obtenir de l'aide, veuillez ouvrir un problème ou contacter notre équipe d'assistance sur [discord](https://discord.gg/kqFzFK7fg2)
