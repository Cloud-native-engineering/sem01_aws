---
layout: default
title: 3.10 Storage @ AWS
parent: 3. Learningpath
nav_order: 9
---

# 3.10 Storage @ AWS

Amazon Webservices hat verschiedene Möglichkeiten Daten von EC2-Instanzen und Services.

## 3.10.1 Elastic Block Storage - EBS

> Drive Management

Elastic Block Storage sind genauer gesagt einzelne Festplatten. Jede EC2 Instanz hat ein EBS-Root Volume mit welchem sich das System bootet. Es können aber weitere Festplatten/Volumes erstellt werden und den einzelnen Maschinen angebunden werden. Grünsatzlicht kann ein Volume nur einer EC2-Instanz zugewiesen werden.

## 3.10.2 Elastic File System - EFS

> Network File Shares

Der Elastic File Service ist ein Service, welcher im Hintergrund mit den Protokollen NFS und SMB arbeitet. Somit ist dieser Service nichts anderes als ein Fileshare.

## 3.10.3 Simple Storage Service - S3

> Object Storage

Amazon S3 ist ein Objekt Speicher. Er ermöglicht über ein API Dateien hochzuladen. Einen klassischen Anwendungsfall ist ein File, welche die Applikation einem User teilen will. Es kann nun den Report generieren und auf einem S3 ablegen und der Benutzer kann diesen später herunterladen.

Es können auch einfache und statische Websites mit einem S3 gehostet werden.
