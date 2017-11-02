+++
title = "AWS : News Octobre 2017"
draft = false
date = "2017-11-01T14:00:00+01:00"
+++

Quelques news AWS issu du mois d'octobre :

[AWS EC2 Facture à la seconde](https://aws.amazon.com/fr/about-aws/whats-new/2017/10/announcing-amazon-ec2-per-second-billing/)  
<i class="fa fa-arrow-circle-right" aria-hidden="true"></i> Arrivé sur AWS de la facturation a la seconde! (Sauf pour les instances avec licences : windows RHEL, Suse)

[AWS EC2 Microsoft SQL 2017](https://aws.amazon.com/fr/about-aws/whats-new/2017/10/amazon-ec2-instances-now-support-microsoft-sql-server-2017/)  
<i class="fa fa-arrow-circle-right" aria-hidden="true"></i> Prise en charge de MS SQL 2017, et donc possibilité de créer des clusters Always On multi AZ... 

[AWS DMS S3 Azure SQL](https://aws.amazon.com/fr/about-aws/whats-new/2017/10/aws-database-migration-service-adds-amazon-s3-and-azure-sql-database-as-sources/)  
<i class="fa fa-arrow-circle-right" aria-hidden="true"></i> Pour les projets de migrations, AWS DMS prend en charge maintenant des sources sur S3 et sur AzureSQL

[AWS ELB/ALB multi SSL](https://aws.amazon.com/fr/about-aws/whats-new/2017/10/elastic-load-balancing-application-load-balancers-now-support-multiple-ssl-certificates-and-smart-certificate-selection-using-server-name-indication-sni/)  
<i class="fa fa-arrow-circle-right" aria-hidden="true"></i> Grosse grosse news : La possibilité de mettre plusieurs listener HTTPS avec des certificats différents sur les LB AWS! 

[AWS SES Email templates](https://aws.amazon.com/fr/about-aws/whats-new/2017/10/amazon-ses-introduces-email-templates-for-sending-personalized-email/)  
<i class="fa fa-arrow-circle-right" aria-hidden="true"></i> Nouveauté coté envoie d'email, la possibilité de créer des modèles : pratiques quand plusieurs applications doivent respecter la meme charte d'emailing.

[AWS ElasticSearch VPC](https://aws.amazon.com/fr/about-aws/whats-new/2017/10/amazon-elasticsearch-service-announces-support-for-amazon-virtual-private-cloud-vpc/)  
<i class="fa fa-arrow-circle-right" aria-hidden="true"></i> Intégration dans un VPC possible pour les noeuds ElasticSearch, pour sécuriser ou limiter l'accès a ce service.

[AWS ActiveDirectory Standard](https://aws.amazon.com/fr/about-aws/whats-new/2017/10/introducing-aws-directory-service-for-microsoft-active-directory-standard-edition/)  
<i class="fa fa-arrow-circle-right" aria-hidden="true"></i> Version plus adaptée pour PME de sa grande soeur la version entreprise de AWS DS ActiveDirectory

[AWS EC2 System Manager](https://aws.amazon.com/fr/about-aws/whats-new/2017/10/amazon-ec2-systems-manager-now-integrates-with-github/)  
<i class="fa fa-arrow-circle-right" aria-hidden="true"></i> Possibilité maintenant d'éxecuter des scripts depuis github ou S3 directement avec EC2 System Manager

Beaucoup d’autres nouveautés, on peut rajouter en bonus :  
* Les RDS Oracles supportent de nouveaux types d'instances : R4, T2 et M4  
* Sortie des nouvelles instances de types P3 (du GPU du NVIDIA pour 14 fois plus de puissance que les P2)  
* Elasticache Redis supporte maintenant le chiffrement des données en transit et au repos  
* Sortie d'Amazon Aurora avec compatibilité PostgreSQL, et dans la foulée d'une nouvelle fonctionnalité RDS Performance Insights (preview pour aurora PostGre seulement)  

@+ pour d’autres news !