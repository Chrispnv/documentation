Installation de VSphere 5.5
=======================

Télécharger VSphere depuis l'adresse du serveur dédié (https://x.x.x.x).

Installer VSphere sur un poste local.

Récupérer un licence VMWare pour VSphere : https://www.vmware.com/tryvmware/p/landing.php?p=free-esxi5

* Créer un compte sur VMWare  
* Récupérer la clé de licence : https://my.vmware.com/group/vmware/evalcenter?p=free-esxi5&source=dwnp, onglet Licence & Download

Installer la clé de licence dans VSphere
::
Configuration dans l'écran central > Fonctions autorisées > Modifier ... (haut gauche) 
  > Affecter une nouvelle clé de licence

Virtualisation d'une VM
=======================

Téléchargement de Ubuntu 14.04 Server 64 bits : http://releases.ubuntu.com/14.04/

En SSH aller sur l'ESXI en root (IP et identifiant fourni par l'hébergeur).

cd /vmfs/volumes/datastore1

wget http://releases.ubuntu.com/14.04/ubuntu-14.04.2-server-amd64.iso

Dans VSphere > Fichier > Nouvelle machine virtuelle
::
Configuration = Installation personnalisée
Nom et emplcement stockage = par défaut
version de machine virtuelle = vs de machine virtuelle 8
système d'exploitatoin = Ubuntu linux 64
CPU = 1 et 1
RAM = 4 Go
Réseau = par défaut (carte NIC, VM network, WMXNET 3)
Controleur SCSI = LSI Logic parallel
Choisir un disque = créer un disque virtuel
Créer un dique = 300 Go / provisionnement disque = Thin provision / Emplacement = stocker avec la machine virtuelle
Options avancées = par défaut
prêt à terminer = cocher Editer les param de la VM avant
