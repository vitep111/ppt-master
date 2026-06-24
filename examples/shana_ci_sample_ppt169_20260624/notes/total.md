# Speaker Notes — SHANA CI Sample Deck
# Finance & Travel and Expense Workstream — Change Impact Analysis

---

## P01 — Cover

This deck presents the Change Impact Analysis for the Finance and Travel & Expense workstream under the PTTEP S/4HANA and Concur transformation programme. It covers the current-state system landscape, quantified impact areas, the target architecture, and a four-phase delivery timeline running July through October 2026. The analysis was prepared by Accenture DigitalX under the SHANA Change Impact methodology.

---

## P02 — Section Divider: Current State

We begin by establishing where we are today. The current-state section maps the existing systems and processes that are in scope for change.

---

## P03 — As-Is System Landscape

Four systems define the current landscape. SAP ECC 6.0 is the core ERP, handling general ledger, accounts payable and receivable for 140 Finance users — it will be replaced by S/4HANA. The E-Payment Portal handles travel claims and expense reimbursement for 340 staff through manual approval workflows; it is being decommissioned. Concur Legacy is a partial rollout limited to HQ Finance with 60 users and no mobile access; it will be upgraded to the full Concur platform. Finally, the Manual Excel CO Tracker used by 20 CO team members for budget tracking has no ECC integration and will also be decommissioned. Together these four systems represent the baseline from which the transformation is measured.

---

## P04 — Change Impact Summary

The transformation touches three headline numbers. Fifteen business processes are impacted across T&E claims, expense approvals, cost centre coding, month-end close, and AP reconciliation — plus ten additional sub-processes. Three systems are being decommissioned — the E-Payment Portal, the SAP ECC Finance module, and the Manual Excel CO Tracker — all requiring data migration and archival. And 480 end users will need training: 120 in the Finance team, 340 T&E requestors, and 20 AP clerks. These numbers drive the change management, training, and communication plans.

---

## P05 — Impact Area Assessment

Across the five standard CIA dimensions, People and Process carry high impact. 480 users face role changes, a new approval hierarchy, and an estimated 16 hours of training per cohort. Fifteen processes are revised, with manual steps replaced by automated workflows and a projected three-day reduction in month-end close cycle time. Technology carries medium impact: three systems retire and a new SAP BTP integration layer is introduced. Data is also medium: five years of financial history must be migrated, the Chart of Accounts requires mapping, and 4,200 vendor master records need cleansing. Document impact is low: twelve SOPs require updates alongside new user guides for Concur and S/4HANA.

---

## P06 — Section Divider: Target State

We now turn to where we are going — the target architecture and the key actions that will get us there.

---

## P07 — To-Be System Landscape

Each current-state system maps to a clear target. SAP ECC 6.0 transitions to SAP S/4HANA, delivering Universal Journal, Fiori UX, and a target two-day close cycle — go-live October 2026. The E-Payment Portal and Concur Legacy are consolidated into an upgraded SAP Concur platform with mobile access for all staff including field teams — go-live August 2026. The Manual Excel CO Tracker is absorbed into the native S/4HANA Controlling module, providing real-time budget visibility as a single source of truth — go-live October 2026. A new Integration Middleware layer using SAP BTP provides Concur-to-S/4HANA data sync, a net-new capability for the organisation.

---

## P08 — Key Actions & Timeline

The programme runs four phases. Phase 1 in July covers foundation work: kick-off and governance, stakeholder mapping, data migration assessment, training needs analysis, and SOP gap inventory. Phase 2 in August is Concur Go-Live: all-staff T&E launch, E-Payment decommission, Excel tracker retirement, Wave 1 training, and the start of hypercare support. Phase 3 in September is UAT and parallel run for S/4HANA Finance, alongside Wave 2 Finance user training and cutover planning. Phase 4 in October is the S/4HANA Go-Live: ECC decommission, full Finance cutover, and stabilisation review leading to project close-out.

---

## P09 — Ending / Thank You

Thank you for your time. For any questions on the scope of change impacts or the training and communication schedule, please contact the Finance Transformation Lead at shana-ci@pttep.com. This analysis has been prepared under the SHANA CI methodology by Accenture DigitalX.
