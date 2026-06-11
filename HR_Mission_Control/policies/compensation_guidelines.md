# Reliance Jio Compensation & Pay Review Guidelines

This document outlines the corporate guidelines for the annual salary review process. Any automated calculations or agentic reviews must adhere to these policies.

## 1. Budget and General Increase Caps
- The overall department salary increase budget must not exceed **8.0%** of the current total payroll.
- Individual salary increases are calculated based on performance ratings and market positioning.

## 2. Performance-Based Salary Increase Grid
Increases are calculated based on the employee's performance rating:

| Performance Rating | Recommended Salary Increase Range |
| :--- | :--- |
| **Outstanding** | 12% to 15% increase |
| **Exceeds Expectations** | 8% to 10% increase |
| **Meets Expectations** | 4% to 6% increase |
| **Needs Improvement** | 0% (No increase, eligible for Performance Improvement Plan) |

## 3. Market Alignment (Compa-Ratio) Policy
- **Compa-Ratio Formula**: `Current Salary / Market Midpoint`
- **Under-Market Adjustment**: If an employee's current salary is below the `market_min` for their Grade and their rating is at least "Meets Expectations", apply a **Market Correction Adjustment** of up to **10%** (or the amount needed to bring them to `market_min`, whichever is lower) *before* applying the performance-based increase.
- **Over-Market Cap**: If an employee's current salary is above `market_max`, their total performance increase must be capped at **3%** to avoid salary compression, regardless of rating.

## 4. Human-in-the-Loop Governance & Audit Checkpoints
- **Review Checkpoint 1**: The HR Manager must review and sign off on all compa-ratio calculations *before* proposed increases are drafted.
- **Review Checkpoint 2**: Any final increase that violates the budget cap (8% overall) or falls outside the standard performance grid must be flagged for manual approval.
- **Review Checkpoint 3**: Before salary letters are finalized, they must be audited for accuracy and tone.

## 5. HR Data Privacy and Information Security
- **Data Confidentiality**: Salary data and employee emails are classified as **Highly Confidential**.
- **No External Leakage**: Do not upload this data to public models, web services, or search engines.
- **Access Control**: Keep all files locally within the `HR_Mission_Control` sandbox.
- **No PII in Shared Logs**: Ensure that no highly sensitive personal identifiers (like Aadhaar, PAN, bank account numbers, or home addresses) are processed or logged.
