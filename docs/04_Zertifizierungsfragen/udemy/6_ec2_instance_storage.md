---
layout: default
title: 4.2.4 EC2 - Storage
parent: 4.2 Udemy Ultimate AWS Certified Cloud Practitioner
grand_parent: 4. Zertifizierungsfragen
nav_order: 4
---

# 4.2.4 EC2 - Storage

## 1. Which EC2 Storage would you use to create a shared network file system for your EC2 Instances?

1. EBS Volume
2. EC2 Instance Store
3. EBS Snapshots
4. EFS

<details>
  <summary>Lösung</summary>
  <b>EFS</b>
  <br>
  <p>Elastic File System - NFS or SMB share service</p>
</details>

---

## 2. Which service can be used to automate image management processes?

1. AMI
2. EC2 Image Builder
3. EBS Snapshots
4. IAM

<details>
  <summary>Lösung</summary>
  <b>EC2 Image Builder</b>
</details>

---

## 3. Which of the following is a fully managed native Microsoft Windows file system?

1. EFS
2. FSx
3. EBS

<details>
  <summary>Lösung</summary>
  <b>FSx</b>
  <br>
  <p>Amazon FSx ist eine einfache und kostengünstige Art um gemanaged Filesystem zu beziehen.</p>
</details>

---

## 4. What are AMIs NOT used for?

1. Add your own software license
2. Add your own configuration
3. Add your own operating system
4. Add your own IP addresses

<details>
  <summary>Lösung</summary>
  <b>Add your own IP addresses</b>
</details>

---

## 5. EBS Volumes CANNOT be attached to multiple EC2 instances at a time.

1. True
2. False

<details>
  <summary>Lösung</summary>
  <b>True</b>
</details>

---

## 6. An EBS Volume is a network drive you can attach to your instances while they run, so your instances' data persist even after their termination.

1. True
2. False

<details>
  <summary>Lösung</summary>
  <b>True</b>
</details>

---

## 7. Which statement is CORRECT regarding EC2 Instance Store?

1. It is not good to use as a disk to cache content
2. It has better I/O performance, but the data is lost if the EC2 Instance is terminated
3. Your data is always safe with EC2 Instance Store

<details>
  <summary>Lösung</summary>
  <b>It has better I/O performance, but the data is lost if the EC2 Instance is terminated</b>
  <br>
  <p>Beim EBS Service können die Festplatten Art definiert werden (ssd/hdd/iops).</p>
</details>

---

## 8. What is an EBS Snapshot?

1. The operating-system on an EC2 Instance
2. A backup of your EBS Volume at a point in time
3. The amount of CPU and RAM of an EC2 Instance

<details>
  <summary>Lösung</summary>
  <b>A backup of your EBS Volume at a point in time</b>
</details>

---

## 9. Where can you find a third party's AMI so you can use it to launch your EC2 Instance?

1. Public AMIs
2. My own AMIs
3. AWS Marketplace AMIs

<details>
  <summary>Lösung</summary>
  <b>AWS Marketplace AMIs</b>
</details>

---

## 10. What is an EBS Volume tied to?

1. A region
2. A data center
3. An edge location
4. An availability zone

<details>
  <summary>Lösung</summary>
  <b>An availability zone</b>
  <br>
  <p>Ein EBS Volume ist nur in der eigenen AZ gegen physischen Ausfall einer Festplatte gesichert. Die Verteilung über mehrere AZ oder Regionen ist der Kunde verantwortlich.</p>
</details>
