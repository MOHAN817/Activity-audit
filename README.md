
# EXPERIMENT 4
# NAME  : m mohan
# REGNO : 212224220064

## ASSET-ORIENTED RISK ASSESSMENT OF STORAGE ASSETS IN AWS 

---

## Aim

To identify storage assets in **AWS S3**, identify possible vulnerabilities and threats, and assess their likelihood, impact, and risk level.

---

## Software / Cloud Services Required

- AWS Account
- Microsoft Azure Account
- Web Browser
- Internet Connection

### Cloud Services Used

| Cloud Platform | Storage Service |
|---|---|
| AWS | Amazon S3 |

---

# PART A — AWS S3 STORAGE ASSESSMENT

## Step 1: Login to AWS

1. Open the AWS Management Console.
2. Sign in using your AWS account.
3. Search for **S3**.
4. Select **Amazon S3**.

---

## Step 2: Select the S3 Bucket

1. Click **Buckets**.
2. Select the S3 bucket created in the previous experiment.
3. Record:
   - Bucket name
   - AWS Region
   - Number/type of objects

<img width="1535" height="959" alt="Screenshot 2026-09-04 223312" src="https://github.com/user-attachments/assets/5cfe7340-f3ed-4a75-b3ed-4f3cd32742e8" />

---

## Step 3: Check Block Public Access

1. Open the S3 bucket.
2. Select **Permissions**.
3. Locate **Block public access (bucket settings)**.
4. Check **Block all public access**.

### Record

- **ON** → Secure configuration
- **OFF** → Potential public-access risk

<img width="1535" height="959" alt="Screenshot 2026-09-04 223401" src="https://github.com/user-attachments/assets/a5e3ba73-7476-410d-87a7-65159e130be2" />

---

## Step 4: Check Bucket Versioning

1. Select the **Properties** tab.
2. Locate **Bucket Versioning**.
3. Record whether it is:
   - Enabled
   - Disabled

### Security Purpose

Versioning helps recover previous versions of objects after accidental deletion or modification.

<img width="1535" height="959" alt="Screenshot 2026-09-04 223525" src="https://github.com/user-attachments/assets/b4781e18-3cf6-465e-ad27-b7f3ec960713" />

---

## Step 5: Check Default Encryption

1. Stay in the **Properties** tab.
2. Locate **Default encryption**.
3. Record the encryption type.

### Possible Configurations

- SSE-S3
- SSE-KMS
- DSSE-KMS

### Security Purpose

Encryption protects stored data from unauthorized disclosure.

<img width="1535" height="959" alt="Screenshot 2026-09-04 223543" src="https://github.com/user-attachments/assets/eed07203-422a-45f1-bf55-e9ea9752cdce" />

---

## Step 6: Check Bucket Policy

1. Select **Permissions**.
2. Locate **Bucket policy**.
3. Check whether a bucket policy exists.

### Record

- Policy exists
- No policy

> **Note:** A missing bucket policy is not automatically a vulnerability. Access may be controlled through IAM and other AWS security mechanisms.

<img width="1535" height="959" alt="Screenshot 2026-09-04 223630" src="https://github.com/user-attachments/assets/e54a0157-8c0c-4245-a91e-a7bcbebbdf5a" />

---

## Step 7: Check Object Ownership and ACL

1. In **Permissions**, locate **Object Ownership**.
2. Record the current configuration.

A common secure configuration is:

**Bucket owner enforced**

This means:

- ACLs are disabled.
- Objects are owned by the bucket owner.
- Access is controlled using policies.

<img width="1535" height="959" alt="Screenshot 2026-09-04 223658" src="https://github.com/user-attachments/assets/661060bf-1e47-49cf-862d-5ae4d5ff6048" />

---
## Step 8: Check Server Access Logging

1. Go to **Properties**.
2. Locate **Server access logging**.
3. Record whether it is:
   - Enabled
   - Disabled

### Security Purpose

Logging helps investigate suspicious or unauthorized access to the bucket.

<img width="1535" height="959" alt="Screenshot 2026-09-04 223923" src="https://github.com/user-attachments/assets/77c696ac-af8a-4116-b161-b1f38ef925a3" />

---


## Step 7: Check Object Ownership and ACL

1. In **Permissions**, locate **Object Ownership**.
2. Record the current configuration.

A common secure configuration is:

**Bucket owner enforced**

This means:

- ACLs are disabled.
- Objects are owned by the bucket owner.
- Access is controlled using policies.

<img width="1535" height="959" alt="Screenshot 2026-09-04 224029" src="https://github.com/user-attachments/assets/659bfce7-3794-40ce-bf12-8a9581c48f15" />

---


---

# PART B — AWS RISK ASSESSMENT

After checking the S3 configuration, identify possible vulnerabilities and threats.

## Risk Formula

**Risk Score = Likelihood × Impact**

### Likelihood Scale

| Score | Description |
|---:|---|
| 1 | Very Low |
| 2 | Low |
| 3 | Medium |
| 4 | High |
| 5 | Very High |

## AWS Risk Assessment

> Students must use their actual configuration while preparing the final table.

| Asset | Vulnerability | Threat | Likelihood | Impact | Risk Score | Risk Level | Recommended Mitigation |
|---|---|---|---:|---:|---:|---|---|
| S3 Bucket | Versioning disabled | Accidental/malicious data deletion | 3 | 4 | 12 | High | Enable versioning |
| S3 Bucket | Access logging disabled | Difficult investigation of unauthorized activity | 3 | 3 | 9 | Medium | Enable appropriate logging |
| S3 Bucket | Public access enabled | Unauthorized data access | 4 | 5 | 20 | Critical | Enable Block Public Access |
| S3 Bucket | Weak access permissions | Unauthorized modification/access | 3 | 4 | 12 | High | Apply least privilege |

---

Risk scores were calculated using the **Likelihood × Impact** method, and appropriate security mitigation measures were recommended.


## Result

~~~
AWS S3 security configurations were analyzed and potential risks were identified.
Risk levels were assessed and suitable security measures were recommended. 
~~~



