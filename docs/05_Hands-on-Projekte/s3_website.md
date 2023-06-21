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

1. IAM
    1. Erstellen eines IAM users für die CI/CD Pipeline
    2. generieren von access keys
    3. Erstellen einer IAM Policy. [iam-policy](../../ressources/artifacts/s3_website/s3_iam_policy_write.json)
    4. Hinzufügen der Policy am IAM user
2. S3 Bucket
    1. Erstellen eines S3 Bucket
    2. Deaktivieren vom "Public access block"
    3. Hinzufügen der bucket Policy. [s3-bucket-policy](../../ressources/artifacts/s3_website/s3_bucket_policy.json)
    4. Object Ownership auf Object writer setzen.
3. CI/CD Pipeline
    1. Erstellen eines GitHub Actions environment (secrets & vars definieren)
    2. Pipeline ins GitHub Repository setzen unter ".github/workflows/s3.yml". [workflow-example](../../ressources/artifacts/s3_website/s3.yml)
4. Nun wird bei einem Push auf das Repository die Pipeline ausgeführt und die Website auf den S3 publiziert.

<details>
  <summary>aws cli commands</summary>
  <code>
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

    # Create IAM Policy
    aws iam create-policy \
      --policy-name s3_website_write \
      --policy-document file://<PATH-TO-JSON-FILE>
  
    # Create user for CI/CD access
    aws iam create-user \
      --user s_s3_website
  
    # Attach policy to user
    aws iam attach-user-policy \
      --policy-arn arn:aws:iam:<ACCOUNT-ID>:aws:policy/s3_website_write \
      --user-name Alice
  </code>
</details>

## 5.2.3 Testing

## 5.2.4 Reflexion