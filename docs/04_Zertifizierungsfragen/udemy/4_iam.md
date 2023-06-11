---
layout: default
title: 4.2.2 Identity and Access Management
parent: 4.2 Udemy Ultimate AWS Certified Cloud Practitioner
grand_parent: 4. Zertifizierungsfragen
nav_order: 1
---

# 4.2.2 Identity and Access Management

## 1. What is a proper definition of IAM Roles?

1. An IAM entity that defines a set of permissions for making AWS service requests, that will be used by AWS services
2. IAM Users in multiple Groups
3. A password policy
4. Permissions assigned to Users to perform actions

<details>
  <summary>Lösung</summary>
  <b>An IAM entity that defines a set of permissions for making AWS service requests, that will be used by AWS services</b>
  <br>
  <p>IAM Roles bestehen können mehrere Berechtigungen beinhalten. Somit könnte man eine Policy einrichte, welche dem Engineering read-only Rechte auf die Produktionsserver gibt.</p>
</details>

---

## 2. Which of the following is an IAM Security Tool?

1. IAM Credentials Report
2. IAM Root Account Manager
3. IAM Services Report
4. IAM Security Advisor

<details>
  <summary>Lösung</summary>
  <b>IAM Credentials Report</b>
  <br>
  <p>Dieses Tool ermöglicht einen Überblick zu erhalten, welche Credentials und Keys existieren.</p>
</details>

---

## 3. Which answer is INCORRECT regarding IAM Users?

1. IAM Users can belong to multiple groups
2. IAM Users don't have to belong to a group
3. IAM Users can have policies assigned to them
4. IAM Users access AWS with the root account credentials

<details>
  <summary>Lösung</summary>
  <b>IAM Users access AWS with the root account credentials</b>
  <br>
  <p>Mit Hilfe der root-account-id, dem iam-username und dem iam-password kann sich ein IAM user anmelden.</p>
</details>

---

## 4. Which of the following is an IAM best practice?

1. Don't use the root user account
2. Create several users for a physical person
3. Share credentials so a colleague can perform a task for you
4. Do not enable MFA for easier access

<details>
  <summary>Lösung</summary>
  <b>Don't use the root user account</b>
  <br>
  <p>Der Root account soll nuc verwendet werden, um erste User zu erstellen. Danach soll mit IAM User gearbeitet werden.</p>
</details>

---

## 5. What are IAM Policies?

1. AWS services performable actions
2. JSON documents to define Users, Groups or Roles' permissions
3. Rules to set up a password for IAM Users

<details>
  <summary>Lösung</summary>
  <b>JSON documents to define Users, Groups or Roles' permissions</b>
  <br>
  <p>IAM Policies werden als json geschrieben und ermöglichen Berechtigungen zu definieren, wenn diese zu einer Identität oder Ressource angehängt wurde.</p>
</details>

---

## 6. Under the shared responsibility model, what is the customer responsible for in IAM?

1. Infrastructure security
2. Compliance validation
3. Configuration and vulnerability analysis
4. Assigning users proper IAM Policies

<details>
  <summary>Lösung</summary>
  <b>Assigning users proper IAM Policies</b>
  <br>
  <p>Der Kunde ist selbst verantwortlich Berechtigungen richtig zu setzen.</p>
</details>

---

## 7. Which of the following statements is TRUE?

1. The AWS CLI can interact with AWS using commands in your command-line shell, while the AWS SDK can interact with AWS programmatically.
2. The AWS SDK can interact with AWS using commands in your command-line shell, while the AWS CLI can interact with AWS programmatically.

<details>
  <summary>Lösung</summary>
  <b>The AWS CLI can interact with AWS using commands in your command-line shell, while the AWS SDK can interact with AWS programmatically.</b>
</details>

---

## 8. Which principle should you apply regarding IAM Permissions?

1. Grant most privilege
2. Grant least privilege
3. Grant permissions if your employee asks you to
4. Restrict root account permissions

<details>
  <summary>Lösung</summary>
  <b>Grant least privilege</b>
  <br>
  <p>Die IAM User sollten immer nur so viel Berechtigungen haben, wie sie auch benötigen. Es kann eingesehen werden, welche Policies ein User schon lange nicht mehr gebraucht hat.</p>
</details>

---

## 9. What should you do to increase your root account security?

1. Enable Multi-Factor Authentication (MFA)
2. Remove permissions from the root account
3. Use AWS only through the Command Line Interface (CLI)

<details>
  <summary>Lösung</summary>
  <b>Enable Multi-Factor Authentication (MFA)</b>
  <br>
  <p>Der Root user sollte bestmöglich geschützt werden, da dieser am meisten Berechtigungen hat.</p>
</details>
