+++
title = "AWS : How to backup EFS to S3"
draft = false
date = "2016-11-24T14:00:00+01:00"
+++

#### <i class="fa fa-amazon" aria-hidden="true"></i> AWS Elastic File System

<i class="fa fa-hdd-o" aria-hidden="true"></i> **Amazon Elastic File System** fournit un stockage de fichiers simple et évolutif à utiliser avec les instances Amazon EC2 dans AWS. 
La capacité de stockage d'EFS est élastique : elle augmente ou diminue automatiquement au fur et à mesure que vous ajoutez et supprimez des fichiers.
EFS se monte en NFS sur les instances, s'utilise au sein d'un VPC, avec plusieurs points de connexions possibles (par AZ) et la découverte des points de montage peut se faire pour les instances AWS via les metadata.

Le problème d'EFS, c'est qu'il ne propose pas de système de backup des données, ni snapshot, ni système de copie vers S3 intégré.
L'autre problème c'est que les données ne sont accessible que via un montage NFS, pas de manière programmatique comme S3 (via API).

La seul solution est donc de gérer soit même le backup, au travers d'une instance EC2 dans le VPC (On oublie l'utilisation de Lambda, car il n'est pas possible d'acceder a EFS via Lambda même dans un VPC, et même si c'etait faisable, le temps d'execution de Lambda ne permettrait son utilisation que sur des volumetrie faible).

Par contre dédié et payer une instance EC2 24/24 pour cela c'est pas viable, et utiliser une machine existante pas toujours possible et pas forcement recommander.

Il est par contre possible de lancer selon une planification une instance EC2, qui monterait l'EFS et le backuperait soit sur du S3, doit sur un autre EFS, selon vos besoin.
Avec potentiellement une rétention, etc..

Pour se faire, le plus efficace est d'utiliser le service :

#### <i class="fa fa-cog" aria-hidden="true"></i> **AWS datapi Pipeline**

<i class="fa fa-cog" aria-hidden="true"></i> **AWS datapi Pipeline** est un service Web qui  permet de traiter et de transférer des données de manière fiable entre différents services AWS de stockage et de calcul et vos sources de données sur site, selon des intervalles définis.
Ce service permet de créer dans notre cas, un worflows très simple et réutilisable pour pleins d'autres tache:

1- Créer une EC2 dans le bon sous reseau et le bon Security Group
2- lancer une commande sur l'EC2 pour aller télécharger et lancer un script héberger sur S3

Ne reste ensuite qu'a faire le script pour qu'il monte l'EFS sur l'EC2 et un s3 sync vers un bucket dédié au backup.

Amazon fourni un exemple de EFS to EFS:
http://docs.aws.amazon.com/efs/latest/ug/efs-backup.html

Il suffit de reprendre le json du datapipeline et de le modifier & de refaire le script pour qu'il copie sur S3 plutot que sur EFS

(La suite bientôt)
