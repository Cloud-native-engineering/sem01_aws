---
layout: default
title: 5.2. Host Website on S3
nav_order: 2
parent: 5. Hands-on-Projekte
has_children: true
---

# 5.2 Host Website on S3

In diesem Projekt will ich meine Semesterarbeit neben dem Hosting auf GitHub Pages auch auf einem S3 publizieren. Das Publishing soll mit der CI/CD-Pipeline von GitHub Actions erfolgen.

Der S3 Service von Amazon AWS ermöglicht [statische Websiten zu hosten](https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html). Dazu muss ein S3 Bucket erstellt werden und die HTML-Files hochgeladen werden. Auch müssen dazu noch die Berechtigungen richtig gesetzt werden.

![2023_S3_Website](../../ressources/images/2023_s3_website.svg)

## 5.2.1 Kostenanalyse

Es ist mit sehr kleinen Kosten zu rechnen. Wenn die HTML-Files und die Bilder kleiner als 5 GB Speicher sind, ist mit keinen Kosten zu rechen. Grund dafür ist das Amazon einen [Free Tier](https://aws.amazon.com/free) anbietet.

# 5.2.2 Umsetzung

In diesem Projekt wird zu allen Ressourcen ein Tag "project_Name" gesetzt. Damit ist besser ersichtlich, welche Ressourcen erstellt wurden.

1. Erstellen eines IAM Benutzer für die
2. Aktivieren des Webhosting
3. Berechtigungen setzen
4. Policy setzen
5. IAM Rolle erstellen
6. IAM Benutzer erstellen
7. CI/CD anpassen
8. Testen

```bash
  # Create an S3 Bucket
  aws s3api create-bucket \
    --bucket <BUCKET-NAME> \
    --region eu-central-2 \
    --create-bucket-configuration LocationConstraint=eu-central-2

  # Disable "public-access-block"
  aws s3api put-public-access-block \
    --bucket <BUCKET-NAME> \
    --public-access-block-configuration "BlockPublicAcls=false,IgnorePublicAcls=false,BlockPublicPolicy=false,RestrictPublicBuckets=false"

  # Upload publicRead Policy
  aws s3api put-bucket-policy \
    --bucket <BUCKET-NAME> \
    --policy file://<PATH-TO-JSON-FILE>

  # Enable static website hosting
  aws s3 website s3://<BUCKET-NAME>/ --index-document index.html --error-document error.html

  
```