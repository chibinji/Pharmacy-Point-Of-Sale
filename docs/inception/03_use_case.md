# Use Cases Documentation
## Pharmacy Point of Sale System

| Document Information | |
|---------------------|-|
| **Document Name** | Use Cases Specification |
| **Phase** | Inception |
| **Author** | Chibinji |
| **Contributors** | Nixon, Enos, Ruth, Idah |
| **Version** | 1.0 |
| **Date** | 19-02-2026 |

---

## 📋 Table of Contents
1. [Introduction](#introduction)
2. [Use Case Diagram](#use-case-diagram)
3. [Actor List](#actor-list)
4. [Prioritized Use Cases (Top 10%)](#prioritized-use-cases-top-10)
5. [Full Use Case List](#full-use-case-list)
6. [Glossary](#glossary)

---

## 1. Introduction
This document captures the functional requirements of the Pharmacy Point of Sale (POS) system using use cases. Following the Unified Process methodology, we have identified approximately 25 use cases and prioritized the top 10% (3 use cases) for detailed development in the Inception phase.

---

## 2. Use Case Diagram
https://github.com/chibinji/Pharmacy-Point-Of-Sale/blob/main/docs/inception/images/use_case_diagram.png?raw=true



---

## 3. Actor List

| Actor | Description | Responsibilities |
|-------|-------------|------------------|
| **Cashier** | Pharmacy staff responsible for processing customer sales | • Scan items<br>• Process payments<br>• Issue receipts<br>• Basic customer service |
| **Pharmacist** | Licensed pharmacist who handles prescriptions | • Verify prescriptions<br>• Enter prescription details<br>• Check drug interactions<br>• Authorize prescription sales |
| **Manager** | Store manager who oversees operations | • Manage staff access<br>• View reports<br>• Override transactions<br>• Handle complex issues |
| **Customer** | End user purchasing medications | • Purchase items<br>• Present prescriptions<br>• Make payments<br>• Request refills |
| **System Administrator** | IT support personnel | • Maintain system<br>• Backup data<br>• User management<br>• System configuration |
| **Insurance Provider** (External) | External insurance companies | • Verify coverage<br>• Process claims<br>• Provide eligibility info |

---

## 4. Prioritized Use Cases (Top 10%)

Based on the 10% rule for Inception phase, we have identified the top 3 most critical use cases (out of approximately 25 total).

---

### UC-01: Process Sale

| Element | Description |
|---------|-------------|
| **Use Case Name** | Process Sale |
| **ID** | UC-01 |
| **Priority** | **HIGH** (Core Business Function) |
| **Primary Actor** | Cashier |
| **Stakeholders** | Cashier, Customer, Manager, Pharmacist |
| **Description** | Cashier processes a customer's purchase of pharmacy items |
| **Trigger** | Customer arrives at checkout with items to purchase |
| **Preconditions** | • Cashier is logged into system<br>• Items are in inventory<br>• POS terminal is operational |
| **Postconditions** | • Sale is recorded<br>• Inventory is updated<br>• Payment is processed<br>• Receipt is generated |

#### Basic Flow
| Step | Action |
|------|--------|
| 1 | Cashier starts new sale |
| 2 | Cashier scans or enters item barcodes |
| 3 | System displays item details and price |
| 4 | System calculates running total |
| 5 | Repeat steps 2-4 until all items scanned |
| 6 | Cashier indicates end of sale |
| 7 | System displays total amount due |
| 8 | Customer provides payment |
| 9 | Cashier enters payment details |
| 10 | System processes payment |
| 11 | System updates inventory |
| 12 | System prints receipt |
| 13 | System records sale transaction |

#### Alternative Flows

| Condition | Alternative Flow |
|-----------|------------------|
| **Item not found** | System displays error; cashier manually enters item details |
| **Invalid barcode** | System alerts cashier; cashier manually enters or looks up item |
| **Payment declined** | System notifies cashier; customer provides alternate payment method |
| **Price override** | Manager approval required for price changes; system prompts for manager credentials |
| **Prescription item** | System flags item; requires pharmacist verification before completion |
| **Age-restricted item** | System prompts for age verification; cashier checks ID and confirms |

#### Business Rules
| Rule ID | Rule Description |
|---------|------------------|
| BR-01 | Prescription items require pharmacist verification before sale completion |
| BR-02 | Age-restricted items (e.g., certain cough medicines) require ID check |
| BR-03 | Discounts apply only to eligible items and require manager approval for overrides |
| BR-04 | Returns must be processed within 30 days with receipt |
| BR-05 | Controlled substances have separate tracking requirements |

---

### UC-02: Handle Prescription

| Element | Description |
|---------|-------------|
| **Use Case Name** | Handle Prescription |
| **ID** | UC-02 |
| **Priority** | **HIGH** (Critical Pharmacy Function) |
| **Primary Actor** | Pharmacist |
| **Stakeholders** | Pharmacist, Customer, Manager, Insurance Provider, Doctor |
| **Description** | Pharmacist processes a new or refill prescription |
| **Trigger** | Customer presents a new prescription or requests a refill |
| **Preconditions** | • Pharmacist is logged into system<br>• Prescription is valid (if new)<br>• Customer profile exists (or can be created) |
| **Postconditions** | • Prescription is recorded in system<br>• Inventory is updated (if dispensed)<br>• Label is printed<br>• Customer is notified when ready |

#### Basic Flow
| Step | Action |
|------|--------|
| 1 | Pharmacist selects "New Prescription" option |
| 2 | System prompts for customer information |
| 3 | Pharmacist selects existing customer or creates new profile |
| 4 | System prompts for prescription details |
| 5 | Pharmacist enters medication details (drug name, dosage, quantity) |
| 6 | Pharmacist enters prescribing doctor information |
| 7 | Pharmacist enters instructions for use |
| 8 | System checks for drug interactions with existing medications |
| 9 | Pharmacist reviews interaction alerts |
| 10 | Pharmacist verifies insurance coverage (if applicable) |
| 11 | System calculates cost |
| 12 | Pharmacist dispenses medication |
| 13 | System updates inventory |
| 14 | System prints prescription label |
| 15 | System records prescription transaction |

#### Alternative Flows

| Condition | Alternative Flow |
|-----------|------------------|
| **New customer** | Create customer profile first with name, contact, DOB, insurance info |
| **Refill request** | Locate existing prescription, verify refills remaining, check last fill date |
| **Drug interaction found** | System displays severity; pharmacist consults with doctor before dispensing |
| **Insurance issue** | Handle as cash transaction; provide receipt for customer to file claim |
| **Out of stock** | Create special order; notify customer when available (typically 24 hours) |
| **Expired prescription** | Inform customer; require new prescription from doctor |
| **Controlled substance** | Verify DEA number; additional documentation required |

#### Business Rules
| Rule ID | Rule Description |
|---------|------------------|
| BR-06 | All prescriptions must be verified by licensed pharmacist |
| BR-07 | Controlled substances have additional tracking requirements per DEA regulations |
| BR-08 | Prescription records must be kept for minimum 5 years (regulatory requirement) |
| BR-09 | Expired prescriptions ( > 1 year) cannot be filled |
| BR-10 | Refill limits must be enforced based on doctor's instructions |
| BR-11 | Drug interaction checks must include OTC medications patient is taking |

---

### UC-03: Manage Inventory

| Element | Description |
|---------|-------------|
| **Use Case Name** | Manage Inventory |
| **ID** | UC-03 |
| **Priority** | **HIGH** (Operational Necessity) |
| **Primary Actor** | Manager, Pharmacist |
| **Stakeholders** | Manager, Pharmacist, Cashier, Suppliers |
| **Description** | Staff manages product inventory including adding, updating, and tracking items |
| **Trigger** | • New shipment arrives<br>• Stock runs low<br>• Product information needs updating |
| **Preconditions** | • User is logged in with inventory management privileges<br>• Product data is accessible |
| **Postconditions** | • Inventory records are updated<br>• Stock alerts are triggered if needed<br>• Product information is current |

#### Basic Flow
| Step | Action |
|------|--------|
| 1 | User selects "Inventory Management" option |
| 2 | System displays inventory dashboard |
| 3 | User selects action (Add/Update/Check Stock) |

**For adding new product:**
| Step | Action |
|------|--------|
| 4a | User enters product details (name, manufacturer, price) |
| 5a | User enters stock keeping unit (SKU) or barcode |
| 6a | User sets reorder threshold |
| 7a | User enters expiry date (for medications) |
| 8a | System saves product information |

**For updating existing product:**
| Step | Action |
|------|--------|
| 4b | User searches for product |
| 5b | User modifies relevant fields |
| 6b | System saves changes |

**For checking stock:**
| Step | Action |
|------|--------|
| 4c | User views current stock levels |
| 5c | System displays items below threshold |
| 6c | User can generate reorder report |

| 9 | System confirms successful operation |

#### Alternative Flows

| Condition | Alternative Flow |
|-----------|------------------|
| **Duplicate product** | System alerts user; verify before adding or update existing |
| **Expired stock** | Flag for removal; mark as unsellable; move to quarantine |
| **Recall alert** | Flag affected products; remove from sale; notify customers if dispensed |
| **Bulk import** | Upload spreadsheet for multiple products; validate before import |
| **Low stock alert** | System automatically flags; add to reorder list |
| **Inventory count discrepancy** | Record actual count; investigate variance; adjust if approved |

#### Business Rules
| Rule ID | Rule Description |
|---------|------------------|
| BR-12 | Expired medications cannot be sold and must be removed from active inventory |
| BR-13 | Controlled substances require separate inventory log and counts |
| BR-14 | Refrigerated items must have temperature logs maintained |
| BR-15 | Reorder points based on 30-day average sales velocity |
| BR-16 | Inventory counts must be verified monthly for controlled substances |
| BR-17 | Products on recall must be immediately removed from sale |

---

## 5. Full Use Case List

Below is the complete list of all identified use cases (approximately 25). Those marked with **[DETAILED]** are the top 10% elaborated above.

| ID | Use Case Name | Priority | Primary Actor | Status |
|----|---------------|----------|---------------|--------|
| **UC-01** | **Process Sale** | **HIGH** | Cashier | **[DETAILED]** |
| **UC-02** | **Handle Prescription** | **HIGH** | Pharmacist | **[DETAILED]** |
| **UC-03** | **Manage Inventory** | **HIGH** | Manager/Pharmacist | **[DETAILED]** |
| UC-04 | Process Return | MEDIUM | Cashier | Pending |
| UC-05 | Apply Insurance | MEDIUM | Pharmacist | Pending |
| UC-06 | Generate Reports | MEDIUM | Manager | Pending |
| UC-07 | Manage Customer Records | MEDIUM | Cashier/Pharmacist | Pending |
| UC-08 | Process Refill Request | MEDIUM | Pharmacist | Pending |
| UC-09 | Handle Special Orders | LOW | Pharmacist | Pending |
| UC-10 | Manage User Accounts | LOW | Manager/Admin | Pending |
| UC-11 | Perform End-of-Day Reconciliation | MEDIUM | Manager | Pending |
| UC-12 | Track Expiring Medications | HIGH | Pharmacist | Pending |
| UC-13 | Manage Suppliers | LOW | Manager | Pending |
| UC-14 | Process Credit Applications | LOW | Manager | Pending |
| UC-15 | Handle Controlled Substances | HIGH | Pharmacist | Pending |
| UC-16 | Print Prescription Labels | MEDIUM | Pharmacist | Pending |
| UC-17 | Send Refill Reminders | LOW | System | Pending |
| UC-18 | Manage Discounts/Promotions | LOW | Manager | Pending |
| UC-19 | View Sales History | MEDIUM | Cashier/Manager | Pending |
| UC-20 | Perform Inventory Count | MEDIUM | Pharmacist/Manager | Pending |
| UC-21 | Handle Insurance Claims | MEDIUM | Pharmacist | Pending |
| UC-22 | Manage Tax Settings | LOW | Manager/Admin | Pending |
| UC-23 | Backup/Restore Data | LOW | Admin | Pending |
| UC-24 | Audit Trail Review | MEDIUM | Manager/Admin | Pending |
| UC-25 | Customer Feedback Collection | LOW | Cashier | Pending |

---

## 6. Glossary

| Term | Definition |
|------|------------|
| **POS** | Point of Sale - The system/terminal where sales transactions occur |
| **SKU** | Stock Keeping Unit - Unique identifier for each product |
| **Barcode** | Machine-readable code representing product information |
| **Prescription** | A doctor's written order for medication |
| **Refill** | Subsequent dispensing of an existing prescription |
| **Controlled Substance** | Medication with potential for abuse, requiring special tracking (e.g., opioids) |
| **DEA Number** | Drug Enforcement Administration number for prescribers |
| **NDC** | National Drug Code - Unique 10-digit identifier for medications |
| **OTC** | Over The Counter - Medications that don't require prescription |
| **Formulary** | List of medications covered by insurance |
| **Dispense** | To prepare and give out medication to a patient |
| **Inventory Turnover** | Rate at which inventory is sold and replaced |
| **Reorder Point** | Stock level that triggers new order |
| **Expiry Date** | Date after which medication cannot be sold/used |
| **Drug Interaction** | When two or more drugs react adversely together |
| **SSD** | System Sequence Diagram - Shows events between actor and system |
| **UML** | Unified Modeling Language - Standard for software modeling |
| **HIPAA** | Health Insurance Portability and Accountability Act - Privacy regulations |

---

## 7. Use Case Prioritization Rationale

| Use Case | Why Top Priority |
|----------|------------------|
| **UC-01 Process Sale** | Core business function; without this, pharmacy cannot operate |
| **UC-02 Handle Prescription** | Unique to pharmacy; critical for patient safety and legal compliance |
| **UC-03 Manage Inventory** | Essential for knowing what's in stock and preventing expired sales |

---

## 📝 Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | Feb 17, 2026 | Chibinji | Initial draft with 3 detailed use cases |
| 0.2 | Feb 19, 2026 | Team | Added full use case list and glossary |
| 1.0 | Feb 19, 2026 | Chibinji | Final version for Inception phase |

---

## ✅ Review Checklist

- [x] All 3 prioritized use cases are fully detailed
- [x] Actors are clearly defined
- [x] Use case list includes 25 items
- [x] Glossary terms are defined
- [x] Format is consistent
- [x] Business rules included for each use case
- [x] Alternative flows documented
- [x] Approved by team

**Reviewers:** Nixon, Ruth, Idah, Enos  
**Approval Date:** 19-02-2026
