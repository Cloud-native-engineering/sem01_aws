---
layout: default
title: 3.11 Database @ AWS
parent: 3. Learningpath
nav_order: 10
---

# 3.11 Database @ AWS

Damit eine Applikation funktionieren kann, benötigen diese eine Datenbank. AWS die AWS Cloud bietet fast alle Datenbanken als Service an. In den folgenden Kapitel werden die häufigsten Datenbank Typen beschrieben, welche für den AWS Cloud Practitioner geprüft werden.

## 3.11.1 Relationale Datenbanken

Der Amazon Relational Database Service (RDS) ermöglicht relationale Datenbanken als Service zu beziehen. Es werden viele Datenbank Engines unterstützt.

- Amazon Aurora
- MySQL
- PostgreSQL
- MariaDB
- Oracle
- Microsoft SQL Server

## 3.11.2 NoSQL Datenbanken

Eine NoSQL Datenbank hat keine Relationen wie eine Relationale Datenbank. Amazon DynamoDB ist eine serverless key-value NoSQL Datenbank. Sie ist hoch performant und kann skaliert werden.

## 3.11.3 Was ist die richtige Datenbank?

| **Datenbank Typ** | **Beispiel**                                           | **AWS Service**                               |
| :---------------: | ------------------------------------------------------ | --------------------------------------------- |
|    Relational     | Traditionelle Applikationen, CMS Systeme (WordPress)   | Amazon Aurora, Amazon RDS, Amazon Redshift    |
|     Key-value     | Applikationen mit viel Traffic, Skalierbare Datenbank | Amazon DynamoDB                               |
|     In-memory     | Caching, session management, kurze Antwortzeiten       | Amazon ElastiCache, Amazon MemoryDB for Redis |
|     Document      | Files, Setting, Benutzerprofile                        | Amazon DocumentDB                             |
|       Graph       | Betrugserkennung, Soziale Netzwerke                    | Amazon Neptune                                |
|    Time series    | Internet of Things (IoT), DevOps, Monitoring           | Amazon Timestream                             |

Weitere Informationen sind [hier](https://aws.amazon.com/products/databases/) ersichtlich.
