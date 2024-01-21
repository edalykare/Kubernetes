## Mettez à jour le cache des paquets :
sudo apt-get update

## Installez Docker (si ce n'est pas déjà fait) :
sudo apt-get install docker.io

## Installez curl (si ce n'est pas déjà fait) :
sudo apt install curl

## Ajoutez la clé GPG pour le repository Kubernetes :
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -

## Ajoutez le repository Kubernetes :
sudo apt-add-repository "deb http://apt.kubernetes.io/ kubernetes-xenial main"

## Mettez à jour le cache des paquets une fois de plus :
sudo apt-get update

# Installation kubectl
sudo curl -LO "https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl"

## Rendez le binaire exécutable :
chmod +x kubectl

## Déplacez kubectl vers un répertoire dans votre variable d'environnement PATH, par exemple /usr/local/bin :
sudo mv kubectl /usr/local/bin/
