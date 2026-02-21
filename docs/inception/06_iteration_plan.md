# Iteration Plan
## Pharmacy Point of Sale System

| Document Information | |
|---------------------|-|
| **Document Name** | Iteration Plan (UP Phases) |
| **Phase** | Inception |
| **Author** | Nixon |
| **Contributors** | Chibinji, Enos, Ruth, Idah |
| **Version** | 1.0 |
| **Date** | 19-02-2026 |

---

## 1. Unified Process Overview

This project follows the **Unified Process (UP)** - an iterative and incremental development methodology. Unlike waterfall, we will:
- Deliver working software in small increments
- Address high-risk items early
- Refine requirements throughout
- Get feedback continuously

---

## 2. Phase Overview

| Phase | Weeks | Purpose | Key Deliverables |
|-------|-------|---------|------------------|
| **Inception** | 1-2 | Vision & Scope | Problem statement, business case, initial use cases, risks |
| **Elaboration** | 3-8 | Architecture & Core Design | Detailed use cases, domain model, SSDs, working architecture |
| **Construction** | 9-12 | Feature Implementation | Working software, tests, integrated features |
| **Transition** | 13-15 | Deployment & Polish | Beta testing, documentation, final demo |

---

## 3. Detailed Iteration Plan

### PHASE 1: INCEPTION (Weeks 1-2)

| Week | Iteration | Focus | Tasks | Deliverables | Owner |
|------|-----------|-------|-------|--------------|-------|
| **Week 1** | Inception | Vision & Scope | • Define problem statement<br>• Create business case<br>• Brainstorm use cases<br>• Initial risk identification | • Problem statement<br>• Business case<br>• 10% use cases (3) | Ruth, Chibinji |
| **Week 2** | Inception | Planning | • Complete risk register<br>• Feasibility study<br>• Create iteration plan<br>• Select tech stack | • Risk register<br>• Feasibility study<br>• Iteration plan<br>• Tech stack | Idah, Enos |

---

### PHASE 2: ELABORATION - ITERATION 1 (Weeks 3-5)

| Week | Iteration | Focus | Tasks | Deliverables | Owner |
|------|-----------|-------|-------|--------------|-------|
| **Week 3** | Elab 1 | Requirements | • Detail UC-01 (Process Sale)<br>• Create SSD for UC-01<br>• Identify domain classes | • 30% use cases detailed<br>• SSD diagrams | Chibinji |
| **Week 4** | Elab 1 | Domain Modeling | • Create domain model<br>• Define relationships<br>• Identify attributes | • Domain class diagram<br>• Relationship documentation | Enos |
| **Week 5** | Elab 1 | Architecture | • Setup project structure<br>• Create proof-of-concept<br>• Test database connection<br>• Update risk list | • Working prototype<br>• Updated risk register | Enos, Idah |

---

### PHASE 2: ELABORATION - ITERATION 2 (Weeks 6-8)

| Week | Iteration | Focus | Tasks | Deliverables | Owner |
|------|-----------|-------|-------|--------------|-------|
| **Week 6** | Elab 2 | Use Cases | • Detail remaining use cases<br>• Create SSDs for critical paths<br>• Define UI requirements | • 70% use cases detailed<br>• Complete SSDs | Chibinji |
| **Week 7** | Elab 2 | Design | • Create design class diagrams<br>• Define interfaces<br>• Design database schema | • Design class diagrams<br>• Database schema | Enos |
| **Week 8** | Elab 2 | UI & Risk | • Create UI prototypes<br>• Review and update risks<br>• Mitigation planning | • UI prototypes<br>• Updated risk register | All |

---

### PHASE 3: CONSTRUCTION - ITERATION 3 (Weeks 9-10)

| Week | Iteration | Focus | Tasks | Deliverables | Owner |
|------|-----------|-------|-------|--------------|-------|
| **Week 9** | Con 3 | Core Features | • Implement UC-01 (Process Sale)<br>• Create database<br>• Basic inventory functions | • Working Process Sale<br>• Database implementation | All |
| **Week 10**| Con 3 | Testing | • Unit tests for core<br>• Integration testing<br>• Bug fixes | • Test cases<br>• Working features | All |

---

### PHASE 3: CONSTRUCTION - ITERATION 4 (Weeks 11-12)

| Week | Iteration | Focus | Tasks | Deliverables | Owner |
|------|-----------|-------|-------|--------------|-------|
| **Week 11**| Con 4 | Advanced Features | • Implement UC-02 (Prescription)<br>• UC-03 (Inventory)<br>• Insurance integration | • Prescription handling<br>• Full inventory | All |
| **Week 12**| Con 4 | Integration | • Complete all features<br>• Full testing<br>• Defect tracking | • Complete feature set<br>• Defect log | All |

---

### PHASE 4: TRANSITION - ITERATION 5 (Weeks 13-14)

| Week | Iteration | Focus | Tasks | Deliverables | Owner |
|------|-----------|-------|-------|--------------|-------|
| **Week 13**| Trans 5 | Testing & Feedback | • Beta testing with users<br>• Collect feedback<br>• Performance testing | • Beta test report<br>• User feedback | All |
| **Week 14**| Trans 5 | Polish | • Performance fixes<br>• Security review<br>• Documentation | • Optimized system<br>• User manual | All |

---

### PHASE 4: TRANSITION - FINAL (Week 15)

| Week | Iteration | Focus | Tasks | Deliverables | Owner |
|------|-----------|-------|-------|--------------|-------|
| **Week 15**| Final | Demo & Submit | • Prepare live demo<br>• Final report<br>• Code cleanup | • Live demo<br>• Final report<br>• GitHub repo | All |

---

## 4. Iteration Planning Guidelines

### Each Iteration Includes:
1. **Planning** (Monday) - What will we deliver?
2. **Development** (Tuesday-Thursday) - Build features
3. **Review** (Friday) - Demo working software
4. **Retrospective** (Friday) - What went well? What to improve?

### Iteration Artifacts:
- Working, tested software
- Updated documentation
- Revised risk register
- Lessons learned

---

## 5. Milestone Summary

| Milestone | Week | Deliverables | Criteria |
|-----------|------|--------------|----------|
| **Inception Complete** | 2 | All Phase 1 docs | Approved by team |
| **Architecture Validated** | 5 | Working prototype | Proof-of-concept works |
| **Design Complete** | 8 | All models, UI prototypes | Ready to build |
| **Core Features Done** | 10 | Process Sale working | Passes tests |
| **All Features Done** | 12 | Complete system | All UC implemented |
| **Beta Tested** | 14 | User feedback incorporated | Ready for demo |
| **Final Delivery** | 15 | Demo, report, code | Submitted |

---

## 6. Risk-Driven Approach

Per Larman's UP methodology, iterations are risk-driven:

| Iteration | High-Risk Items Addressed |
|-----------|---------------------------|
| **Elab 1** | Hardware integration, database performance |
| **Elab 2** | Prescription security, compliance |
| **Con 3** | Core transaction accuracy |
| **Con 4** | Complex prescription rules |
| **Trans 5** | User adoption, performance |

---

## Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 19-02-2026 | Nixon| Initial iteration plan |