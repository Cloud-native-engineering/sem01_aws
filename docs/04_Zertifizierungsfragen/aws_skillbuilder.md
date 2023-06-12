---
layout: default
title: 4.3 AWS Skillbuilder
nav_order: 3
parent: 4. Zertifizierungsfragen 
---

# 4.3 AWS Skillbuilder

## 1. A company is hosting a static website from a single Amazon S3 bucket. Which AWS service will achieve lower latency and high transfer speeds?

1. AWS Elastic Beanstalk
2. Amazon DynamoDB Accelerator (DAX)
3. Amazon Route 53
4. Amazon CloudFront

<details>
  <summary>Lösung</summary>
  <b>Amazon CloudFront</b>
  <br>
  <p>Amazon CloudFront ist ein Content Delivery Service. Er ermöglicht die Ladezeit von statischen und dynamischen Webcontent zu verkürzen. Dies ermöglicht er indem er die Daten in Edge Locations cached.</p>
</details>

---

## 2. A company needs phone, email, and chat access 24 hours a day, 7 days a week. The response time must be less than 1 hour if a production system has a service interruption. Which AWS Support plan meets these requirements at the LOWEST cost?

1. AWS Basic Support
2. AWS Developer Support
3. AWS Business Support
4. AWS Enterprise Support

<details>
  <summary>Lösung</summary>
  <b>AWS Business Support</b>
  <br>
  <p>Der Business Support Plan ermöglicht: Telefon, email und chat support 24h/7d pro Woche. Die Antwortzeit für Produkionssysteme beträgt unter einer Stunde.</p>
</details>

---

## 3. Which AWS Cloud architecture design principle supports the distribution of workloads across multiple Availability Zones?

1. Implement automation.
2. Design for agility
3. Design for failure.
4. Implement elasticity.

<details>
  <summary>Lösung</summary>
  <b>Design for failure.</b>
  <br>
  <p>Amazon empfiehlt dass kritische Applikationen verteilt kommunizieren. Die Server sollten dazu über mehrere Verzugsarbeitszonen verteilt werden. Somit dass die Applikation immernoch verfügbar ist, wenn es ein Problem in einer Verfügbarkeitszone gibt.</p>
</details>

---

## 4. Which aspect of AWS infrastructure provides global deployment of compute and storage?

1. Multiple Availability Zones in an AWS Region
2. Multiple AWS Regions
3. Tags
4. Resource groups

<details>
  <summary>Lösung</summary>
  <b>Multiple AWS Regions</b>
  <br>
  <p>Eine Region ist ein physikalischer Ort an welchem Datencenter Cluster existieren. Mit Hilfe der AWS Regionen können Services (Compute, Storage, Databases) weltweit deployed werden.</p>
</details>

---

## 5.A company wants a dedicated private connection to the AWS Cloud from its on-premises operations. Which AWS service or feature will provide this connection?

1. AWS VPN
2. AWS PrivateLink
3. APC endpoint
4. AWS Direct Connect

<details>
  <summary>Lösung</summary>
  <b>AWS Direct Connect</b>
  <br>
  <p>AWS Direct Connect ermöglicht eine private Verbindung (Glassfaser) direkt zu AWS zu erhalten. Es ist eine alternative um auf AWS Ressourcen zuzugreifen (Internet)</p>
</details>

---

## 6. Which AWS service provides a simple and scalable shared file storage solution for use with Linux-based Amazon EC2 instances and on-premises servers?

1. AWS Managed Services (AMS)
2. Amazon S3 Glacier
3. Amazon Elastic Block Store (Amazon EBS)
4. Amazon Elastic File System (Amazon EFS)

<details>
  <summary>Lösung</summary>
  <b>Amazon Elastic File System (Amazon EFS)</b>
  <br>
  <p>Amazon Elastic File System (Amazon EFS) ermöglicht Netzwerkshares zu erstellen. Diese Shares können über NFS und SMB angesprochen werden. Amazon stellt dieser Share als Service zu Verfügung. Auch vergrössert oder verkleinern Sie den Share, je nach Bedarf.</p>
</details>

---

## 7. Which recommendations are included in the AWS Trusted Advisor checks? (Select TWO.)

1. Amazon S3 bucket permissions
2. AWS service outages for services
3. Multi-facor authentication (MFA) use on the AWS account root user
4. Available software patches for Amazon EC2 instances
5. Number of users in the account

<details>
  <summary>Lösung</summary>
  <b>1 & 3</b>
  <br>
  <ol>
    <li>Der AWS Trusted Advisor prüft die Berechtigungen auf einem S3 bucket, welche offene Zugriffsberechtigungen haben. Wenn Berechtigungen zur Liste öffentlich sind, kann das zu erhöhten Kosten führen, in dem ungewünschte Besucher das Dokument X Mal herunterladen. Bucket, welche noch mehr Berechtigungen offen haben (upload, delete, modify, remove) bieten einen grossen Angriffsfaktor um Schwachstellen auszunutzen.</li>
    <li>Tusted Advisor prüft auch, ob der Root account Multi-factor enabled hat. Grundsätzlich sollte dies eingeschalten werden, da dieser Account alle Rechte hat!</li>
  </ol>
</details>

---

## 8. Which of the following are advantages of the AWS Cloud? (Select TWO.)

1. AWS manages the maintenance of the cloud infrastructure.
2. AWS manages the security of application built on AWS.
3. AWS manages capacity planning for physical servers.
4. AWS manages the development of applications on AWS.
5. AWS manages cots planning for virtual servers.

<details>
  <summary>Lösung</summary>
  <b>1 & 3</b>
  <br>
  <ol>
    <li>AWS ist verantwortlich für die Sicherheit VON der Cloud. Somit ist AWS auch für das Warten der physischen Server und Netzwerkgeräte verantwortlich.</li>
    <li>AWS ist verantwortlich für die Sicherheit VON der Cloud. Dazu gehört auch die Kapazitätsplanung der physischen Hardware.</li>
  </ol>
</details>

---

## 9. Which of the following is a responsibility of AWS under the AWS shared responsibility model?

1. Design a customer's application for disaster recovery.
2. Update the guest operating systems on deployed Amazon EC2 instances.
3. Configure new resources within an AWS account.
4. Secure the physical infrastructure.

<details>
  <summary>Lösung</summary>
  <b>Secure the physical infrastructure.</b>
  <br>
  <p>AWS hat die Verantwortung und Hoheit über die ganze physikalische Infrastruktur.</p>
</details>

---

## 10. Which of the following are benefits of the AWS Cloud? (Select TWO.)

1. Companies need increased IT staff.
2. Capital expenses are replaces with variable expenses.
3. Customers receive the same monthly bill regardless of which resources they use.
4. Companies gain increased agility
5. AWS holds responsibility for security in the cloud.

<details>
  <summary>Lösung</summary>
  <b>2 & 4</b>
  <br>
  <ol>
    <li>Mit der AWS Cloud profitiert man von dem "Economics of Scale". Eigene Server müssen nicht mehr angeschafft werden, da diese ins OpEX genommen wurden, da diese jetzt als Service ins OpEX gerutscht sind.</li>
    <li>Mit dem Verwenden der AWS Cloud ist ein Unternehmen viel agiler und kann sich schneller anpassen. "Go global in minutes"</li>
  </ol>
</details>

---

## 11. A company has an application server that runs on an Amazon EC2 instance. The application server needs to access contents within a private Amazon S3 bucket. What is the recommended approach to meet this requirement?

1. Creates an IAM role with the appropriate permissions. Associate the role with the EC2 instance.
2. Configure a VPC peering connection to allow private communication between the EC2 instance and the S3 bucket.
3. Create a shared access key. Configure EC2 instance to use the hardcoded key.
4. Configure the application to read an access key from a secured source.

<details>
  <summary>Lösung</summary>
  <b>Creates an IAM role with the appropriate permissions. Associate the role with the EC2 instance.</b>
  <br>
  <p>IAM Rollen ermöglicht temporär auf Ressourcen zuzugreifen. Diese Credentials aktualisieren sich stetig, dadurch sind sie gegen versehentliches veröffentlichen geschützt.</p>
</details>

---

## 12. A company requires physical isolation of its Amazon EC2 instances from the instances of other customers. Which instance purchasing option meets this requirement?

1. Dedicated Hosts
2. Reserved Instances
3. On Demand Instances
4. Spot Instances

<details>
  <summary>Lösung</summary>
  <b>Dedicated Hosts</b>
  <br>
  <p>Dedizierte Hosts sind in AWS physikalische Server, welche nicht mit anderen Kunden geteilt werden. Dedicated Hosts ermöglichen zu entscheiden, auf welchem Physischen Server eine EC2 Instanz deployed werden soll.</p>
</details>

---

## 13. Which AWS service can create an alarm that sends a notification when a billing threshold is exceeded?

1. AWS Trusted Advisor
2. AWS CloudTrail
3. Amazon CloudWatch
4. Amazon QuickSight

<details>
  <summary>Lösung</summary>
  <b>Amazon CloudWatch</b>
  <br>
  <p>Service Soflimits können mit Hilfe von CloudWatch überwacht werden.</p>
</details>

---

## 14. A company needs to monitor and receive alerts about AWS Management Console sign-in events that involve the AWS account root user. Which AWS service can the company use to meet these requirements?

1. Amazon CloudWatch
2. AWS Config
3. AWS Trusted Advisor
4. AWS Identity and Access Management (IAM)

<details>
  <summary>Lösung</summary>
  <b>Amazon CloudWatch</b>
  <br>
  <p>CloudWatch überwacht AWS Ressourcen in Echtzeit. Es kann Aletring eingeschaltet werden, damit man informiert wird.</p>
</details>

---

## 15.Which AWS services or features support data replication across AWS Regions? (Select TWO.)

1. Amazon S3
2. Amazon Elastic block Store (Amazon EBS)
3. Amazon EC2 Instance store
4. AWS Storage Gateway
5. Amazon RDS

<details>
  <summary>Lösung</summary>
  <b>1 & 5</b>
  <br>
  <ol>
    <li>Amazon S3 unterstützt X-Region Replikationen. Dafür muss ein Bucket in einer anderen Region erstellt werden und dieser als sync Ziel ausgewählt werden.</li>
    <li>Mit dem RDS Datenbank Service können ein Read-write Node in der Haupt Region erstellt werden. Danach können sogenannte Read Replicas Regionenweit verteilt werden.</li>
  </ol>
</details>

---

## 16. Which of the following is an advantage of consolidated billing on AWS?

1. Volume pricing qualification
2. Shared access permissions
3. Multiple bills for each account
4. Elimination of the need to tag resources

<details>
  <summary>Lösung</summary>
  <b>Volume pricing qualification</b>
  <br>
  <p>Konsolidierte Rechnungen ermöglichen AWS Organisationen die Benutzung zusammenzufassen unf vom "volume pricing" zu profitieren. Somit kann die Organisation von einem Rabatt profitieren.</p>
</details>

---

## 17. Which security-related services or features does AWS offer? (Select TWO.)

1. Complete PCI compliance for customer applications that run on AWS
2. AWS Trusted Advisor security checks
3. Data encryption
4. Automated penetration testing
5. Amazon S3 copyrighted content detection

<details>
  <summary>Lösung</summary>
  <b>2 & 3</b>
  <br>
  <ol>
    <li>Der AWS Trusted Advisor hat von hunderten Kunden gelernt. Diese Best Practices umfassen auch Sicherheitschecks.</li>
    <li>Viele AWS Services unterstützen Verschlüsselung.</li>
  </ol>
</details>

---

## 18. Which Amazon EC2 pricing model adjusts based on supply and demand of EC2 instances?

1. On-Demand Instances
2. Reserved Instances
3. Spot Instances
4. Convertible Reserved Instances

<details>
  <summary>Lösung</summary>
  <b>Spot Instances</b>
  <br>
  <p>Spot Instanzen sind günstiger, wenn es viele nicht gebraucht Rechenleistung (CPU & RAM) noch in einer Verfügbarkeitszone hat.</p>
</details>

---

## 19. Which of the following describes a security best practice that can be implemented by using AWS Identity and Access Management (IAM)?

1. Turn off AWS Management Console
2. Generate secrets keys for every IAM user.
3. Grant permissions to users who are required to perform a specific task only.
4. Store AWS credentials within Amazon EC2 Instances.

<details>
  <summary>Lösung</summary>
  <b>Grant permissions to users who are required to perform a specific task only.</b>
  <br>
  <p>Die Berechtigungen sollten nach dme "least privilege" Prinzip verteilt werden.</p>
</details>

---

## 20. Which AWS Cloud architecture principle states that systems should reduce interdependencies?

1. Scalability
2. Service, not servers
3. Automation
4. Loose coupling

<details>
  <summary>Lösung</summary>
  <b>Loose coupling</b>
  <br>
  <p>Loose Kupplung mit anderen Diensten. Eine Komponente soll bestmöglich eigenständig und isoliert sein. Eine Änderung oder ein Ausfall in einer der Komponenten sollte sich nicht auf andere Komponenten auswirken.</p>
</details>
