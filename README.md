# POS Suite Serveur

Serveur de boutique POS Suite : caisse, commandes, stock et finances sur le réseau local.
L'application installe sur la machine principale de la boutique une base PostgreSQL embarquée,
l'API et le client web ; les autres postes (caisse, accueil, magasin) utilisent simplement un navigateur.

## Téléchargement

Les paquets sont publiés dans les [releases](https://github.com/IsmaelRAJAOMANIRY/pos-suite-desktop/releases) :

- Linux (Debian, Ubuntu, Mint) : `pos-suite-serveur_<version>_amd64.deb`
- Windows 10/11 : `pos-suite-serveur_<version>_x64-setup.exe`

Vérifier les fichiers : `sha256sum -c SHA256SUMS`.

## Installation

Linux :

```
sudo apt install ./pos-suite-serveur_<version>_amd64.deb
```

Windows : lancer l'installateur (installation pour l'utilisateur courant). Windows peut
afficher « éditeur inconnu » : l'installateur n'est pas signé Authenticode.

Au premier lancement, l'écran « Configuration initiale » crée la boutique et le compte
administrateur (une boutique par serveur).

## Mises à jour

L'application vérifie les nouvelles versions au démarrage puis toutes les 6 heures, et propose
de les installer (menu Paramètres > Mises à jour). Chaque paquet est vérifié avec la signature
POS Suite avant installation ; la base est sauvegardée automatiquement avant toute migration.

## Statut

Versions de test (prototype). Le code source n'est pas publié dans ce dépôt.
