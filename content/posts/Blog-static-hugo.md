+++
title = "Gérer un blog serverless avec Hugo, GithUb, Travis CI, slack, S3 et CloudFront"
draft = false
date = "2016-12-14T10:30:30+01:00"
+++

Comme indiqué précedemment, ce site est généré avec **Hugo**, et entièrement stocké sur **S3**

Les pages sont écrites en **MarkDown** et le tout est hébergé sur **GitHub** (https://github.com/wbearcorp/www4-2xyz)

**Travis** est configuré pour vérifier chaque push ou pull sur **github** et un fichier yml a la racine du projet contient le code a éxécuter via **Travis**

**hugo** génère le site a chaque nouvelle mise a jour.

**Hugo** étant en go, **Travis** lance une instance go pour généré le site :

    language: go
    install: go get -v github.com/spf13/hugo
    script:
        - hugo
        - python --version
        - sudo pip install awscli
        - export AWS_DEFAULT_REGION="eu-west-1"
        - export AWS_ACCESS_KEY_ID=$AK
        - export AWS_SECRET_ACCESS_KEY=$SK
        - aws s3 sync public/ s3://www.4-2.xyz/ --delete

    notifications:
        email:
             on_failure: always
        slack: wbearcorp:[cledapislack]

Je n'utilise pas le code natif de **Travis** pour **S3** car il ne sais que copier l'intégralité des données et pas faire de synchronisation, c'est pourquoi j'execute du code pour télécharger le cli AWS et éxecuté des commandes natives **S3**

Au niveau notifications, **Travis** envoie un message sur un channel **Slack** dédié au blog et zou, je suis prévenu du bon déroulement du déploiement.

Le bucket **S3** est configuré en tant que hosting de site static, la page index.html est défini comme page par défaut et la page 404.html comme page d'erreur par defaut.

**Cloudfront** est configuré pour publié, non pas le bucket **S3** mais l'url du website **S3**, derrière mon nom de domaine www.4-2.xyz le tous redirigé uniquement en HTTPS avec un certificat généré gratuitement chez AWS via le service ACM (AWS Certificate Manager)

Et voilà!

A chaque nouvelle page ou mise a jour, un git push upload les modifications sur **github**, déclenche **Travis**, qui génère via **hugo** le site et le publie sur **S3**, le iste est accessible au travers de **CloudFront**, et le résultat du déploiement est annoncé sur **Slack**.

Pour le moment je suis seul a publié sur le site mais tous fonctionnerais de même si on était 2, 5 ou 22 a travailler en parallèle sur le blog ! 