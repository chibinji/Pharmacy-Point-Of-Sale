# Risk Register
## Pharmacy Point of Sale System

| Document Information | |
|---------------------|-|
| **Document Name** | Risk Register |
| **Phase** | Inception |
| **Author** | Idah |
| **Contributors** | Chibinji, Enos, Ruth, Nixon |
| **Version** | 1.0 |
| **Date** | 19-02-2026 |

---

## 1. Risk Management Approach

This document identifies, assesses, and plans responses to project risks. Risks will be reviewed weekly and updated throughout the project lifecycle.

**Risk Rating Matrix:**
| Impact / Probability | Low | Medium | High |
|---------------------|-----|--------|------|
| **High** | Medium | High | Critical |
| **Medium** | Low | Medium | High |
| **Low** | Low | Low | Medium |

---

## 2. Risk Register

### 2.1 Technical Risks

| ID | Risk Description | Probability | Impact | Rating | Mitigation Strategy | Owner | Status |
|----|------------------|-------------|--------|--------|---------------------|-------|--------|
| **R-01** | **Database performance degrades with large inventory** | Medium | High | **High** | • Index key fields<br>• Implement pagination<br>• Optimize queries<br>• Plan for 10,000+ products | Enos | Planned |
| **R-02** | **Hardware compatibility issues** (scanners, printers, cash drawers) | Medium | High | **High** | • Research common pharmacy hardware<br>• Test with at least 3 brands<br>• Use standard drivers/APIs<br>• Have manual fallback | Enos | Planned |
| **R-03** | **System crashes during peak hours** | Low | High | **Medium** | • Load testing<br>• Error handling<br>• Automatic recovery<br>• Graceful degradation | Enos | Planned |
| **R-04** | **Data loss or corruption** | Low | Critical | **High** | • Daily automated backups<br>• Transaction logging<br>• Database integrity checks<br>• Recovery procedures | Enos | Planned |
| **R-05** | **Integration with insurance APIs fails** | Medium | Medium | **Medium** | • Design adapter pattern<br>• Start with mock data<br>• Manual entry fallback<br>• Research APIs early | Enos | Planned |

### 2.2 Regulatory & Compliance Risks

| ID | Risk Description | Probability | Impact | Rating | Mitigation Strategy | Owner | Status |
|----|------------------|-------------|--------|--------|---------------------|-------|--------|
| **R-06** | **Prescription data security breach** | Low | Critical | **High** | • Encrypt all patient data<br>• Role-based access control<br>• Audit trails<br>• Follow pharmacy regulations | Idah | Planned |
| **R-07** | **Non-compliance with controlled substance tracking** | Medium | Critical | **Critical** | • Consult pharmacy regulations<br>• Involve pharmacist in design<br>• Implement DEA requirements<br>• Regular compliance reviews | Idah | Researching |
| **R-08** | **Failure to meet audit trail requirements** | Medium | High | **High** | • Log all prescription access<br>• Immutable audit logs<br>• Regular compliance checks<br>• Legal review | Idah | Planned |
| **R-09** | **Expired medication still sold** | Low | Critical | **High** | • Auto-block expired items<br>• Expiry alerts at scan<br>• Daily expiry reports<br>• Visual warnings | Idah | Planned |

### 2.3 Project Management Risks

| ID | Risk Description | Probability | Impact | Rating | Mitigation Strategy | Owner | Status |
|----|------------------|-------------|--------|--------|---------------------|-------|--------|
| **R-10** | **Scope creep - too many features** | High | Medium | **High** | • Strict prioritization<br>• Must-have vs nice-to-have<br>• Weekly scope review<br>• MVP focus | Nixon | Active |
| **R-11** | **Team member unavailability** | Medium | Medium | **Medium** | • Cross-train tasks<br>• Document everything<br>• Regular communication<br>• Backup assignments | Nixon | Planned |
| **R-12** | **Missed deadlines** | Medium | High | **High** | • Realistic estimates<br>• Buffer time<br>• Weekly progress tracking<br>• Early warning system | Nixon | Active |
| **R-13** | **Poor communication among team** | Medium | Medium | **Medium** | • Daily standups<br>• WhatsApp group<br>• Shared documents<br>• Clear assignments | Nixon | Active |

### 2.4 User & Adoption Risks

| ID | Risk Description | Probability | Impact | Rating | Mitigation Strategy | Owner | Status |
|----|------------------|-------------|--------|--------|---------------------|-------|--------|
| **R-14** | **Staff resistance to new system** | Medium | High | **High** | • Involve staff in testing<br>• Gather feedback early<br>• Provide training<br>• Show benefits clearly | Chibinji | Planned |
| **R-15** | **Training takes too long** | Medium | Medium | **Medium** | • Intuitive UI design<br>• Quick reference guides<br>• Video tutorials<br>• Phased rollout | Chibinji | Planned |
| **R-16** | **System too complex for cashiers** | Medium | High | **High** | • User testing with cashiers<br>• Simplify common tasks<br>• Keyboard shortcuts<br>• Clear error messages | Chibinji | Planned |

### 2.5 Business & Operational Risks

| ID | Risk Description | Probability | Impact | Rating | Mitigation Strategy | Owner | Status |
|----|------------------|-------------|--------|--------|---------------------|-------|--------|
| **R-17** | **System doesn't handle peak load** | Medium | High | **High** | • Load testing<br>• Optimize performance<br>• Queue management<br>• Monitor during peak | Enos | Planned |
| **R-18** | **Inventory inaccuracies persist** | Medium | High | **High** | • Real-time updates<br>• Regular cycle counts<br>• Audit logs<br>• Discrepancy reports | Idah | Planned |
| **R-19** | **Customer data migration fails** | Low | High | **Medium** | • Export/import testing<br>• Data validation<br>• Backup original data<br>• Phased migration | Enos | Planned |

---

## 3. Top 5 Critical Risks

| Rank | ID | Risk | Rating | Mitigation | Owner |
|------|----|------|--------|------------|-------|
| **1** | R-07 | Controlled substance compliance | Critical | Consult regulations, involve pharmacist | Idah |
| **2** | R-06 | Data security breach | High | Encryption, access control | Idah |
| **3** | R-01 | Database performance | High | Indexing, optimization | Enos |
| **4** | R-10 | Scope creep | High | Strict prioritization | Nixon |
| **5** | R-14 | Staff resistance | High | Involve users early | Chibinji |

---

## 4. Risk Response Plan

### For Critical/High Risks:
1. **Weekly review** in team meetings
2. **Mitigation actions** assigned and tracked
3. **Contingency plans** prepared
4. **Early warning indicators** monitored

### Risk Monitoring Schedule:
- **Daily:** Team members monitor assigned risks
- **Weekly:** Full risk review in team meeting
- **Phase-end:** Comprehensive risk reassessment

---

## 5. Risk Log (Updates)

| Date | Risk ID | Update | New Status | Updated By |
|------|---------|--------|------------|------------|
| [Date] | All | Initial risk identification | Planned | Idah |
| | | | | |

---

## Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 19-02-2026 | Idah | Initial risk register |