---
layout: default
title: 3.3 Globale AWS-Infrastruktur
parent: 3. Learningpath
nav_order: 3
---

# 3.3 Globale AWS-Infrastruktur

Damit Amazon den AWS Dienst betreiben existiert ein ausgeklügeltes System für die AWS-Cloud. Die Cloud besteht aus folgenden zwei Teilen. Die physikalische und die virtuelle Infrastruktur. Die Physikalische kann der Kunde nur sehr bedingt beeinflussen, die virtuelle kann der Kunde selbst nach seinen Bedürfnissen verwalten. Neben diesen zwei Punkte betreibt AWS ein globales privates Netzwerk um eine hohe Datenaustauschrate zwischen ihren Rechenzentren zu ermöglichen.

Wegen diesem Aufbau ist es möglich in AWS hochverfügbare und kritische Services zu betreiben, welche die Daten in verschiedenen Physischen Rechenzentren gespeichert hat.

![2023_aws_structure](../../ressources/images/2023_aws_structure.svg)

## 3.3.2 Rechenzentrum

Ein Rechenzentrum ist ein physikalisches Gebäude in welchem die Server stationiert sind. Die AWS Rechenzentren werden diskret betrieben und besitzen redundante Stromversorgung, Netzwerke und Kühlung.

## 3.3.3 Regionen

Eine Region ist einen physischen Standort, an welchem AWS mehrere Rechenzentren in einem Cluster betreibt. Jede Region hat mindestens drei Verfügbarkeitszonen.

## 3.3.4 Verfügbarkeitszonen (Availability Zonen)

Eine Verfügbarkeitszone besteht aus einem oder mehreren Rechenzentren. Die Verfügbarkeitszonen sind untereinander physisch getrennt und mittels eines hochverfügbaren und ausfallsicheren Netzwerks verbunden.

Durch die Aufteilung von Availability Zones können Applikationen hochverfügbar mit einer niedrigen Latenz betrieben werden. Die Verfügbarkeitszonen sind jeweils voneinander physisch und logisch getrennt. Die Einzelnen Verfügbarkeitszonen stehen jeweils mehrere Kilometer auseinander, sind aber nicht weiter als 100km voneinander entfernt.

## 3.3.5 Local Zones

AWS verfügt über ein Netzwerk von Edge Standorte und Local Zones. Es ermöglicht dass Anwendungen mit niedriger Latenz dem Endkunde zur Verfügung gestellt werden können.

## 3.3.6 Points of Presence

Points of Presence sind Netzwerk Endpunkte, mit welchen sich AWS an verschiedenen Internetknotenpunkte anbindet. (peering.)

## 3.3.7 Netzwerk

AWS betreibt ein globales privates ultraschnelles Netzwerk um Datensicherheit zu gewährleisten. Mit diesem Netzwerk werden die Regions/AZ/Rechenzentren untereinander verbunden und der Kunde kann seine Daten über mehrere Rechenzentren verteilen.

## 3.3.8 Compliance und Sicherheit

Die Sicherheit der Cloud hat für Amazon höchste Priorität. Die Rechenzentrum und Netzwerkarchitektur entspricht ebenfalls den Anspruch Firmen

## 3.3.9 Nachhaltigkeit

Der Betrieb von Server und Rechnerzentren benötigt sehr viel Strom. Dies kann die CO2 Bilanz einer Firma sehr beeinflussen. Um den Unterhalt und den Betrieb sehr umweltbewusst zu betreiben hat AWS eigene Solar Farmen und Windkraftwerke gebaut.

Weitere und genauere Informationen über die Massnahmen, welche AWS ergriffen hat ist auf folgender Website ersichtlich: [Nachhaltigkeit der AWS Cloud](https://nachhaltigkeit.aboutamazon.de/umwelt/die-cloud)
