---
layout: default
title: 3.9 Elastic Compute 2
parent: 3. Learningpath
nav_order: 9
---

# 3.9 Elastic Compute Cloud - EC2

Amazon EC2 ist ein Cloud Computing Dienst von AWS, der ermöglicht virtuelle Maschine zu betreiben. Die Virtuellen Maschinen (EC2 Instances) können auf das ganze globale Netzwerk von AWS deployed werden. Jede Region hat aber eigene Kosten. Die Instances können automatisch skaliert werden, wenn die Last einen Richtwert überschritten hat.

> EC2 Instance = AMI (OS) + Instance Size (CPU + RAM) + Storage + Security Groups + EC2 User Data (Cloud-init)

## 3.9.1 Instance OS

Amazon bietet eine grosse liste mit Amazon Machine Images (AMIs) an. In der AMI Liste sind unter anderem:

- Windows
- Ubuntu
- Debian
- Amazon Linux
- Redhat Enterprise Linux
- etc.

## 3.9.2 Instance Type

Die Rechenleistung und RAM kann nicht komplett selbst gesetzt werden. Man muss sich einen Instance Type aussuchen. Um bei der Auswahl zu unterstützen existieren Folgende Instance-Type-groups:

- General Purpose
- Compute Optimized
- Memory Optimized
- Accelerated Computing
- Storage Optimized
- HPC Optimized (High performance computing)

[AWS Instance Types](https://aws.amazon.com/ec2/instance-types/)

## 2.9.3 Storage

Der Storage kann frei gewählt werden. Es kann normale Harddrive, oder SSDs gewählt werden. Jeder Typ hat eigene Kosten.

## 3.9.4 Security Groups

Eine Security Group kann mit einer Firewall verglichen werden.

Es kann zum Beispiel eine Security Group erstellt werden um SSH Access von einer spezifischen IP zu erlauben, oder einen Webserver im Internet freizuschalten.

## 3.9.5 Purchasing Options

- On-Demand Instances
  - Kurze Rechenleistungs Dauer
  - Kosten:
    - Linux & Windows Abrechnung in Sekunden
    - Alle anderen Betriebssysteme in Stunden
  - Höchste Kosten aber keine Vorauszahlungen
  - keine Langjährigen Verpflichtungen
- Reserved Instance (1 & 3 years)
  - Reservierte Rechenleistung für lange Workloads
  - Options:
    - Standard
    - Convertible
    - Scheudled
- Saving Plans (1 & 3 years)
  - Zusage zu einer fixen bezogenen Leistung an Ressourcen
- Spot Instances
  - kurze Rechenleistung, sehr günstig, Rechenleistung kann durch AWS entzogen werden
- Dedicated Hosts
  - Mieten eines ganzen physikalischen Server
- Deticated Instance
