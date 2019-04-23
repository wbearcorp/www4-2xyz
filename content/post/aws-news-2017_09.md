+++
title = "AWS : News Septembre 2017"
draft = false
date = "2017-10-01T14:00:00+01:00"
+++

Quelques news AWS issu principalement du mois de septembre :

[AWS S3 data events Cloudtrail](https://aws.amazon.com/fr/about-aws/whats-new/2017/09/aws-cloudtrail-enables-option-to-add-all-amazon-s3-buckets-to-data-events/)  
<i class="fa fa-arrow-circle-right" aria-hidden="true"></i> la possibilité d'activer le login de toutes les actions S3 de base avec Cloudtrail.

[AWS NLB](https://aws.amazon.com/fr/about-aws/whats-new/2017/09/elastic-load-balancing-network-load-balancer-now-supports-load-balancing-to-ip-addresses-as-targets-for-aws-and-on-premises-resources/)  
<i class="fa fa-arrow-circle-right" aria-hidden="true"></i> Le petit nouveau de la famille loadbalancing ajoute 2 semaine après sa naissance la possibilité de faire de l’équilibrage de charge entre aws et on-premise ! (directconnect requis) 

[AWS Stop/Start Spot Instance](https://aws.amazon.com/fr/about-aws/whats-new/2017/09/amazon-ec2-spot-can-now-stop-and-start-your-spot-instances/)  
<i class="fa fa-arrow-circle-right" aria-hidden="true"></i> Ca interessera les amateurs de Spot instances, elles peuvent être arrêté au lieu de terminer, ce qui permet des flottes de SPOT permanentes !

[AWS Codebuild support Github](https://aws.amazon.com/fr/about-aws/whats-new/2017/09/aws-codebuild-now-supports-building-github-pull-requests/)  
<i class="fa fa-arrow-circle-right" aria-hidden="true"></i> Codebuild deviens intéressant en permettant l’utilisation d’autre chose que le repo AWS, c’est une bonne news 

[AWS Security Group rules description](https://aws.amazon.com/fr/blogs/aws/new-descriptions-for-security-group-rules/)  
<i class="fa fa-arrow-circle-right" aria-hidden="true"></i> News qui peut paraitre faiblement intéressante, mais pouvoir ajouter une description derrière une règles de firewall, ça permet de savoir à quoi ça correspond, surtout quand on utilise des ports spécifiques.

[AWS VMWare on Cloud](https://aws.amazon.com/fr/blogs/aws/vmware-cloud-on-aws-now-available/)  
<i class="fa fa-arrow-circle-right" aria-hidden="true"></i> Espérons cette année que ce service soit sec.

[AWS EC2 new instance x1e.large](https://aws.amazon.com/fr/blogs/aws/now-available-ec2-instances-with-4-tb-of-memory/)  
<i class="fa fa-arrow-circle-right" aria-hidden="true"></i> Petite dernière, l’instance x1e.32xlarge, identique à sa petite sœur sauf qu’elle passe à 4Tb de RAM (en DDR4) au lieu de 2Tb, une nouvelle arrivée qui peut être intéressante pour les projets SAP HANA, car comme le reste de la famille des instances x elle est certifié SAP, jusqu’à une mise en cluster pour atteindre 34Tb. En cas de projet HANA arrivant en AVV c’est toujours bon a prendre

[AWS DS AD support LDAP SSL](https://aws.amazon.com/fr/about-aws/whats-new/2017/09/now-you-can-encrypt-ldap-communication-with-aws-directory-service-for-microsoft-active-directory/)  
<i class="fa fa-arrow-circle-right" aria-hidden="true"></i> Dans un optique de sécurisation client, ou de respect de PSSI, on peut maintenant utiliser le LDAPS avec AWS DS for MS Active Directory

Beaucoup d’autres nouveautés, on peut rajouter en bonus :  
* Nouveaux points de connexion pour des direct connect a Houston (USA) et Canberra (Australia)  
* Support de Raspbian OS et Rasperry Pi dans EC2 System Manager

@+ pour d’autres news !