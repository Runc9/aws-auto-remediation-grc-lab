# AWS Compliance-as-Code Lab: Auto-Remediation with AWS Config, Lambda & EventBridge

![AWS](https://img.shields.io/badge/Built%20With-AWS-orange)
![Automation](https://img.shields.io/badge/Focus-Auto--Remediation-blue)
![GRC](https://img.shields.io/badge/GRC-Aware-brightgreen)
![Compliance](https://img.shields.io/badge/Compliance-as--Code-yellow)
![NIST](https://img.shields.io/badge/Mapped%20to-NIST%20800--53%20%7C%20CIS%20Controls-lightgrey)

---

## 🧠 Overview

**Imagine your organization just onboarded 12 new AWS accounts under a multi-account structure.** You're tasked with ensuring every environment continuously enforces compliance baselines such as no publicly accessible S3 buckets, secure security group configurations, and no disabled CloudTrail logs. Manually tracking and remediating these issues isn't scalable.

This lab simulates a real-world scenario where your GRC/security team codifies compliance guardrails using AWS Config and EventBridge, then automatically remediates violations using AWS Lambda. This is a foundational step toward achieving "compliance as code" across cloud environments.

---

## 🎯 Objectives

By completing this lab, you will:

- Understand how AWS Config rules detect compliance violations
- Learn how EventBridge captures compliance state change events
- Implement auto-remediation via AWS Lambda functions
- Link actions to compliance frameworks (e.g., NIST 800-53, CIS v8)
- Build audit-ready controls with logs and structured findings

---

## 🔧 Prerequisites

Before starting:

- AWS Account with admin-level permissions (or IAM roles that allow Config, Lambda, EventBridge, and S3 operations)
- AWS CLI configured locally
- Basic familiarity with:
  - AWS Config rules (managed + custom)
  - Lambda function creation and permissions
  - CloudFormation (optional if deploying via template)

---

## 🧱 Lab Components

| Component | Description |
|----------|-------------|
| `code/cloudformation/compliance-remediation-stack.yaml` | Full IaC template to deploy Config, EventBridge, Lambda |
| `README.md` | Documentation (this file) |
| `docs/architecture-diagram.png` | (Optional) Architecture diagram for visual explanation |
| `docs/validation-checklist.md` | Manual test plan (to be created) |

---

## 🚀 Lab Steps

1. **Deploy AWS Config Managed Rule via CloudFormation**
2. **Create EventBridge Rule**
3. **Deploy Remediation Lambda Function**
4. **Simulate Noncompliance**
5. **Observe Automation**
6. **Deploy Full Stack via CloudFormation**

---

## 💪 Skills Demonstrated

- Compliance-as-Code strategy
- Event-driven automation in AWS
- Lambda security and permissions scoping
- Cloud audit readiness (CloudTrail + CloudWatch Logs)
- Framework mapping to NIST, CIS Controls, ISO 27001

---

## 📚 Resources

- [AWS Config Rules Documentation](https://docs.aws.amazon.com/config/latest/developerguide/evaluate-config.html)
- [AWS Security Hub Compliance Standards](https://docs.aws.amazon.com/securityhub/latest/userguide/securityhub-standards.html)
- [EventBridge + Lambda Pattern](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-troubleshooting.html)
- [CIS AWS Foundations Benchmark v1.5](https://www.cisecurity.org/benchmark/amazon_web_services)
- [NIST 800-53 Rev. 5 Controls](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final)

---

> Developed by [Runc9](https://github.com/Runc9) as part of a growing AWS Cloud Security GRC engineering portfolio.
