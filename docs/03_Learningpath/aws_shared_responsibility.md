---
layout: default
title: 3.6 Shared Responsibility Model
parent: 3. Learningpath
nav_order: 6
---

# 3.6 Shared Responsibility Model

Bei jedem Betrieb eines Services müssen die Verantwortlichkeiten geklärt sein. So ist es auch bei der Benutzung der AWS Cloud. Amazon hat dazu folgendes Model erstellt. Es Beschreibt die Verantwortung zischen dem Kunde der AWS cloud und AWS, welche die Cloud Infrastruktur betreibt.

![aws_shared_responsibility_model](https://d1.awsstatic.com/security-center/Shared_Responsibility_Model_V2.59d1eccec334b366627e9295b304202faf7b899b.jpg)

## 3.X.X AWS Verantwortlichkeit - Sicherheit der Cloud

> Security **OF** the Cloud

AWS ist für den physischen Schutz der Infrastruktur verantwortlich. Dazu gehören die alle Services der AWS cloud. Die Infrastruktur besteht aus der Hardware, Software, Netzwerk und die Gebäude.

## 3.X.X Kundenverantwortlichkeit - Sicherheit in der Cloud

> Security **IN** the cloud

Der Kunde ist verantwortlich, ist unterschiedlich je nach dem welcher AWS-Service benutzt wird. Wird Beispielweise ein "Infrastructure as Code" (IaC) Dienst wie EC2 verwendet hat der Kunde viel Verantwortung. Es ist so beispielweise für das Gastsystem und das Patching davon verantwortlich. Anders sieht es aus, wenn er zum Beispiel Amazon DynamoDB verwendet. Da ist AWS für das Patching verantwortlich, da dies ein PaaS/SaaS Service ist.
