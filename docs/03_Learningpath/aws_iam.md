---
layout: default
title: 3.8 Identity and Access Management
parent: 3. Learningpath
nav_order: 7
---

# 3.8 Identity and Access Management - IAM

Mit Hilfe von der Identity and Access Management Plattform von AWS können Berechtigungen auf Ressourcen und Services eingeschränkt werden. In folgenden Kapitel wird beschrieben wir das IAM aufgebaut ist.

![AWS_IAM](https://d1.awsstatic.com/product-marketing/IAM/iam-how-it-works-diagram.04a2c4e4a1e8848155840676fa97ff2146d19012.png)

## 3.8.1 IAM User

Eine Person oder Applikation, welche sich mit AWS mit einem IAM Account verbinden kann.

## 3.8.2 IAM Group

Eine Gruppe von mehreren IAM-Benutzer, welche die selben Rechte haben.

## 3.8.3 IAM Policy

Die IAM Policy wird als JSON-Dokument beschrieben. Es Beschreibt auf welche Ressourcen und Services mit welchen Rechten zugegriffen werden kann.

## 3.8.4 IAM Role

Eine IAM Rolle ist ähnlich wie ein IAM User. Eine Rolle kann mehreren Benutzer zugeordnet werden und ermöglicht ihnen ihnen in diese Rolle zu wechseln, somit können sie andere Aktionen ausführen.

## 3.8.5 Multi-Factor Authentication - MFA

AWS empfiehlt den Usern zusätzlich Multifactor Authentication zu aktivieren. Somit ist der AWS Account sicher, wenn der Username und as Passwort komprimiert sind. Zum Beispiel, wenn die Credentials ausersehen in ein Git Repository gepusht werden. Die AWS Cloud unterstützt folgende Protokolle und 2-Factor Arten:

- FIDO Security Keys (Yubikeys, etc.)
- Virtual Authenticator Apps (Google Authenticator, Microsoft Authenticator)
- TOTP Hardware Tokens
- TOTP Hardware Tokens for the AWS GovCloud (US) Regions

## 3.8.6 IAM Access Analyzer

Das Konzept "Least Privilage" muss stetig überarbeitet und überprüft werden. Nicht mehr benötigte Berechtigungen können zum Beispiel entfernt werden.

![AWS_IAM_Access_Analyzer](https://d1.awsstatic.com/setverifyrefine_SEC207_brigidkaren_1067x397.24e6fa3dd3dc4b7e701fcd9c25a3bf47ef34688d.png)

Der IAM Access Analyzer ermöglicht diese analysen genauer durchführen zu können. Er ermöglicht einzusehen, welche Rechte ein Benutzer nicht mehr benötigt hat. Zum Beispiel, der Benutzer X hat seit 3 Monaten seine Read-Only Rechte auf einen S3 nicht mehr benötigt. Somit kann der Administator sich überlegen, ob er dem Benutzer diese Berechtigungen entfernen will.
