---
title: "From Contract to Handover: Where Document Control Actually Begins"
date: 2026-08-13
categories:
  - Engineering Information Governance
  - Document Control
  - EPC
tags:
  - Document Control
  - Contract Management
  - Information Governance
  - MDL
  - Project Delivery
excerpt: "Document Control does not begin with the first document. It begins at tender, when documentation obligations are priced, and at award, when they become legally binding."
toc: true
toc_label: "Contents"
toc_sticky: true
series: "Engineering Information Governance"
series_part: 4
---

*By the time the first drawing exists, a project's information obligations have already been fixed — negotiated, priced, and made binding. Document Control that starts at the first document has inherited decisions it never saw.*

## The Question Nobody Asks Early Enough

Early in execution, ask a simple question: **how does this project know what it has to deliver?**

The answers are revealing, because every one of them defers accountability to somebody else.

| Asked | Typical answer | What it actually means |
|---|---|---|
| Engineering | "It will become clear as the design develops" | Scope will be discovered, not planned |
| Procurement | "We have a list attached to the POs" | Partial, package-level, disconnected |
| Client | "It's in the specification" | True — and never consolidated by anyone |
| Document Control | "I'll build the register once documents start arriving" | The register will reconstruct the past, not control the future |

The answer already exists. It was agreed at signature, distributed across several hundred pages, and nobody has extracted it.

> Document Control does not begin with documents. It begins with obligations.

Articles [1](/engineering-information-governance/what-does-document-control-actually-manage/) and [2](/engineering-information-governance/why-engineering-projects-lose-control/) established that projects run on information rather than documents, and that most execution failures begin as information failures. [Article 3](/engineering-information-governance/why-mdl-is-the-most-important-document/) established the Master Document List as the instrument of control. This article addresses what comes before the MDL — and determines whether it is correct.

---

## Obligations Are Priced Before They Are Binding

The conventional view is that documentation requirements arrive with the contract. The more accurate view is that they arrive with the tender, and are either priced or absorbed.

```text
Tender        →  Obligations are priced (or mispriced)
Award         →  Obligations become legally binding
Mobilisation  →  Obligations must be interpreted and structured
First document →  Obligations are already immovable
```

Bid teams price steel, equipment, labour, and construction risk with considerable rigour. Documentation obligations are routinely treated as overhead — a document controller and a licence. Several common clauses carry material cost that never appears in the estimate.

| Clause type | Commercial exposure |
|---|---|
| Review period with no cap on resubmission cycles | Unbounded rework; every rejection consumes engineering hours and schedule float |
| Client-nominated EDMS or CDE with mandated metadata | Parallel systems, manual re-keying, licences, and training outside the contractor's own toolset |
| Native file and model deliverables | Intellectual property exposure, format conversion, additional tooling |
| Approval required before fabrication or construction release | Client review duration sits directly on the critical path |
| Retention and access obligations after completion | Multi-decade custodianship, unbudgeted |
| Documentation tied to payment milestones | Cash flow becomes dependent on review turnaround the contractor does not control |

None of these are exotic. All of them are standard in EPC, power, and infrastructure contracts, and all of them are cheaper to price than to discover.

> An unpriced documentation obligation is a margin leak that presents, two years later, as a schedule problem.

The practical implication is organisational. If Document Control is not consulted during tender review, the function will spend the project discharging commitments it had no opportunity to assess.

---

## Where Obligations Are Actually Buried

Information requirements are never located in one place. They are distributed across the contract structure, frequently inconsistent between documents, and occasionally contradictory. Consolidating them is not administrative preparation — it *is* the first deliverable of the function.

| Source document | What to extract |
|---|---|
| Conditions of Contract | Review periods, approval authority, notice provisions, retention, intellectual property |
| Scope of Work / Employer's Requirements | Deliverable categories, phase gates, submission stages |
| Technical Specifications | Discipline-level document requirements, applicable standards, formats |
| Documentation Exhibit or Appendix | Explicit deliverable schedule, review codes, transmittal protocol |
| Coordination Procedure | Numbering convention, metadata, nominated EDMS/CDE, distribution matrix |
| Quality Requirements / ITP | Records, certificates, inspection and test documentation |
| Commercial Schedule | Documentation-linked payment milestones, liquidated damages |
| Handover / Completion Requirements | As-built scope, O&M dossier structure, data handover format |

Two observations from practice.

First, these documents frequently disagree. The Coordination Procedure specifies one numbering convention; a technical specification assumes another. The Conditions of Contract state a 14-day review; the Documentation Exhibit states 21. These conflicts must be surfaced and resolved formally, in writing, during mobilisation — not settled informally at the first rejected submission.

Second, and more consequential:

> If no single named individual has read all of these end to end, the project does not know its own information scope.

---

## The Extraction: Clause to Obligation to Deliverable

The mechanism that converts a contract into a controlled register is a traceability matrix. It is unglamorous and it is the most defensible artifact the function produces.

```text
Contract Clause  →  Information Obligation  →  Deliverable(s)  →  MDL Line(s)
```

A worked extract:

| Clause ref | Information obligation | Deliverable | MDL entry | Owner |
|---|---|---|---|---|
| SOW 4.3.2 | Submit system design basis for approval before detail design commences | Design Basis Report | NEA-0000-PRO-RPT-0001 | Process Lead |
| Spec E-102 §7 | Provide short-circuit and protection coordination study | Study report with calculations | NEA-1200-ELE-CAL-0014 | Electrical Lead |
| Spec I-204 §3.2 | Provide loop diagrams for all control loops prior to commissioning | Loop diagrams (per loop) | NEA-1200-ICT-DWG-0201 → 0388 | I&C Lead |
| Cond. 12.4 | Client review 14 days; resubmission within 10 days of return | *No deliverable* — schedule and workflow constraint | Applied as MDL date logic | Document Control |
| Exhibit F §5 | Native CAD files provided at handover in client-specified format | As-built native package | Handover dossier item HO-07 | Document Control |
| QR 8.1 | Material certificates for all pressure-retaining components | Certificate package, per PO | Vendor register, flowed to MDL | QA/QC + Procurement |

Two rules make the matrix defensible rather than decorative:

1. **Every MDL line traces to a clause reference.** If a deliverable cannot be traced to an obligation, it is either internal scope or unpriced work — and the distinction should be a deliberate decision, not an accident.
2. **Every clause maps to at least one MDL line, or to a recorded decision that no deliverable is required.** Unmapped clauses are the mechanism by which handover gaps are created.

The commercial value runs in both directions. The matrix defends against scope creep by making additions visible as additions. It also prevents the contractor from quietly absorbing obligations that were never priced — which is the more common and more expensive error.

---

## The Obligations That Are Not Deliverables

This is the section most projects omit, and the omission is systemic rather than local.

Contracts do not only specify *which* documents must be delivered. They specify rules *about* documents: how they are identified, formatted, exchanged, reviewed, and retained. These obligations produce no MDL lines. They configure the entire information system, and they cannot be retrofitted without touching every deliverable already produced.

| Obligation type | Example requirement | Cost if discovered late |
|---|---|---|
| Numbering convention | Client-mandated document numbering structure | Renumber the entire register; every cross-reference breaks |
| Metadata and attributes | Mandatory tag, system, and asset linkage on every document | Re-attribute thousands of documents during handover |
| Format and native files | PDF/A archival format, native CAD, model deliverables | Bulk conversion; potential IP renegotiation |
| Review codes | Client-specific Code 1–4 definitions differing from internal practice | Status mapping errors propagate through all progress reporting |
| Review durations and resubmission limits | 14-day review, maximum two resubmissions | Schedule and engineering hours built on wrong assumptions |
| Transmittal protocol | Formal transmittal through nominated CDE only | Parallel email trail with no contractual standing |
| Language, units, certification | Bilingual issue, wet signature, licensed engineer stamp | Full resubmission of already-approved documents |
| Retention and access | Documents available for ten years after completion | Unbudgeted long-term custodianship |

> A deliverable submitted in the wrong format has not been submitted.

There is a strict sequence here, and inverting it is the most common front-end failure:

```text
Contractual rules  →  Numbering & metadata standard  →  MDL  →  Documents
```

Article 3 makes the point that document numbering is the primary key of the entire information system and cannot be changed mid-project. This is where that key comes from. The numbering convention is not designed by Document Control according to preference — it is derived from contractual obligation, and only then extended to cover what the contract leaves open.

---

## Flow-Down: Making Vendors Contractually Bound

An EPC contractor holds documentation obligations to the client for information it does not produce. Vendor and subcontractor deliverables typically account for 40–60% of the total register. The contractor cannot discharge those obligations unless they have been passed through, back to back, into every subcontract and purchase order.

```text
Client Contract  →  EPC Obligations  →  Subcontract / PO VDRL  →  Vendor Deliverables
```

The Vendor Document Requirements List (VDRL, or SDRL in some sectors) is the flow-down instrument. It is a contractual attachment to the purchase order, and it must specify not only *what* the vendor delivers, but the same non-deliverable obligations the contractor holds: numbering, format, metadata, language, review turnaround, and resubmission duties.

Three failures recur, and all three are timing failures:

- **Flow-down occurs after award.** The vendor is asked to comply with requirements not priced into their quotation. Compliance becomes a commercial negotiation rather than an obligation.
- **The VDRL is generic.** A standard template is attached without tailoring to the actual scope, generating deliverables nobody needs and omitting ones the client requires.
- **MDL entries are created on first submission rather than at award.** Until the vendor submits something, the deliverable does not exist in the register — so it cannot be reported as late, and its absence is invisible until handover.

The control is simple and rarely applied: **every purchase order requiring documentation generates MDL entries at the moment of award.** Article 3 explains why unregistered vendor documents surface as handover gaps. This is the upstream reason they were never registered.

---

## What This Phase Actually Produces

The output of contract-to-delivery translation is not the MDL alone. It is three artifacts, produced in a specific order, each dependent on the one before it.

| # | Artifact | Question it answers | Owner |
|---|---|---|---|
| 1 | **Document Control Plan / Information Delivery Plan** | How will information be produced, reviewed, exchanged, controlled, and handed over? | Document Control |
| 2 | **Numbering and Metadata Standard** | How is every deliverable uniquely identified and classified? | Document Control + Engineering |
| 3 | **Baselined MDL** | What is owed, by whom, by when? | Document Control |

Building the register first is the common shortcut, and it guarantees rework of all three. A register built before the numbering standard will be renumbered. A numbering standard built before the plan will conflict with the client's exchange requirements. Sequence is not bureaucracy here; it is the difference between a system and an accumulation.

For the construction of the MDL itself — required fields, ownership, baselining, and reconciliation — see [Article 3](/engineering-information-governance/why-mdl-is-the-most-important-document/). This article stops at the point where the register is derived; that one takes it forward.

---

## How This Fails, and When It Surfaces

Front-end failures share a characteristic that makes them uniquely expensive: **detection lag**. Each one is cheap to prevent, invisible for months, and costly to correct once visible.

| Failure | Where it surfaces | Cost of correction |
|---|---|---|
| Document Control mobilised after engineering starts | First client submission rejected on format or numbering | Moderate — rework of early deliverables |
| No single party read the contract end to end | Mid-execution scope dispute | High — commercial exposure, weak position |
| MDL copied from a precedent project without validation | Handover gap analysis | Very high — no schedule float remaining |
| Non-deliverable obligations never extracted | First formal review cycle, or at handover | Very high — systemic rework across all deliverables |
| No flow-down to purchase orders | Vendor data gap at handover | Highest — no contractual remedy against the vendor |

> Most missed deliverables are not execution failures. They are requirement-interpretation failures that took eighteen months to become visible.

The pattern from Article 2 holds precisely: the information failure occurs first, execution proceeds correctly against it, and the problem is reported as something else entirely.

---

## Delivery Assurance: Stage 3 to Stage 4 at the Front End

Article 1 set out a four-stage maturity curve. Contract-derived delivery planning is what the upper stages look like *before any document exists*.

| Question the function can answer | Maturity stage |
|---|---|
| "What documents exist?" | Stage 1 — Document Filing |
| "What status are they in?" | Stage 2 — Document Control |
| "Does the documentation match the built asset?" | Stage 3 — Configuration Management |
| **"Will we discharge our contractual obligations?"** | **Stage 4 — Information Governance** |

Only the last question is answerable at award, and only if the extraction has been done. It is also the only one the Project Manager, the Commercial Manager, and the client actually care about.

This is the same discipline formalised by **ISO 19650** as the progression from exchange information requirements to an information delivery plan, and by **ISO 9001 §7.5** as the control of documented information. The standards describe the destination. The contract determines the route.

---

## Conclusion

The chain is short and each link is derived from the one before it:

```text
Contract  →  Obligations  →  Deliverables  →  MDL  →  Delivery Governance
```

Break the first link and everything downstream is guesswork with a register attached. Projects that treat Document Control as a function that starts when documents start have already skipped the only phase in which the outcome could have been designed.

> Projects do not deliver documents. They discharge obligations.

### First Thirty Days After Award

- [ ] All contract documents assembled and read end to end by a named individual
- [ ] Conflicts between contract documents logged and formally resolved with the client
- [ ] Clause → obligation → deliverable traceability matrix drafted
- [ ] Non-deliverable obligations extracted: numbering, metadata, format, review codes and durations, transmittal protocol, retention
- [ ] Numbering and metadata standard issued and approved
- [ ] Document Control Plan issued for client acceptance
- [ ] MDL baselined and reconciled against the project schedule
- [ ] VDRL template prepared and mandated for flow-down into all purchase orders
- [ ] Documentation-linked payment milestones and liquidated damages identified and communicated to Project Management and Commercial

If this list is complete before the first deliverable is produced, the project has information control. If it is completed afterwards, the project has documentation.

---

## Next in This Series

Article 2 identified revision failure as one of four information failures. The next article treats it as an engineering problem in its own right — because on large projects, revision control does not fail through carelessness. It fails through scale.

Part 5 covers:

- Revision, version, and status — three concepts routinely conflated, with different owners
- Why concurrent revision streams emerge and why they are sometimes legitimate
- How superseded information stays in circulation despite formal control
- Designing revision discipline that survives 50,000 documents and 40 organisations

→ **[Part 5: Why Large Projects Always Fall Into Revision Chaos](/engineering-information-governance/why-large-projects-fall-into-revision-chaos/)**
