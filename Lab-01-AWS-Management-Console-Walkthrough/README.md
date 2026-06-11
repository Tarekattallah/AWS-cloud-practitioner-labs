# Lab 01 — AWS Management Console Walkthrough

## Objective
Get familiar with the AWS Management Console interface, understand account identity, and explore the myApplications section.

---

## Account Details

| Field | Value |
|-------|-------|
| **Account ID** | 4370-5716-9050 |
| **IAM Username** | voclabs/user4680518=Altarek_Mohamed_Alsaied_T... |
| **Region** | us-east-1 (N. Virginia) |

---

## Steps Performed

1. Logged in to the AWS Management Console using the lab credentials.
2. Located the **Account ID** and **IAM Username** from the top-right account menu.
3. Navigated to the **myApplications** section from the Console home.
4. Observed an `Access Denied` error for `servicecatalog:ListApplications` — expected behavior in a restricted lab environment.
5. Identified the **Create Application** button and the **Region selector**.

---

## Access Denied — Explanation

> **Error:** `Access denied to servicecatalog:ListApplications`

This error occurred because the lab IAM role does not have permission to list Service Catalog applications.

| Field | Details |
|-------|---------|
| **User ARN** | `arn:aws:sts::437057169050:assumed-role/voclabs/user4680518=Altarek_Mohamed_Alsaied_Tawfiek` |
| **Action** | `servicecatalog:ListApplications` |
| **Resource** | `arn:aws:servicecatalog:us-east-1:437057169050:/applications/*` |
| **Context** | No identity-based policy allows the action |

✅ This is **normal** in lab environments — IAM permissions are intentionally restricted.

---

## Screenshots

### 1. Account Identity Panel
![Account ID](screenshots/annotated_account_id.png)
> Shows the Account ID and IAM Username (Lab User) from the AWS Console top menu.

### 2. myApplications — Access Denied
![myApplications](screenshots/annotated_my_applications.png)
> Shows the myApplications console section with the Access Denied error and the Create Application button.

---

## What I Learned

- How to locate **Account ID** and **IAM Username** in the AWS Console.
- How AWS uses **IAM Roles** to control access to services.
- What an **Access Denied** error means and why it happens in restricted lab environments.
- How to navigate the **myApplications** section and understand its purpose.
- The importance of **Regions** and how to identify the current region (us-east-1).

---

## Key Takeaways

> The AWS Management Console is the central hub for managing all AWS services.
> Understanding **IAM permissions** is essential — not all users can access all services.
> Always check your **Region** before creating or managing resources.

---

*Lab completed as part of AWS Certified Cloud Practitioner (CLF-C02) preparation.*
