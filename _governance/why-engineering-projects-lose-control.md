---
title: "Why Engineering Projects Lose Control: The Real Problem Is Usually Information"
date: 2026-07-30
categories:
  - Engineering Information Governance
  - Document Control
  - EPC
tags:
  - Information Governance
  - Document Control
  - Revision Control
  - Change Management
  - Project Delivery
excerpt: "Delays, rework, and overruns are usually reported as engineering or supply-chain failures. Trace them back far enough and most began as information failures."
toc: true
toc_label: "Contents"
toc_sticky: true
series: "Engineering Information Governance"
series_part: 2
---

*Projects run on decisions. Decisions run on information. When information degrades, execution degrades — regardless of how capable the team is.*

## Symptoms Are Not Causes

When a project slips, the explanations are familiar: the schedule was aggressive, suppliers were late, resources were short, requirements changed, coordination broke down.

These are usually accurate. They are also usually **symptoms**.

| Reported cause | Frequent underlying cause |
|---|---|
| Supplier built the wrong configuration | Superseded revision issued with the purchase order |
| Rework on site | Approved change never reached the field |
| Duplicated engineering effort | Same information held in four disconnected locations |
| Handover delayed after mechanical completion | Final revisions and vendor data never reconciled during execution |

> Execution quality can never exceed information quality.

---

## Four Information Failures Behind Most Project Problems

Different projects, different sectors — the same four patterns.

### 1. Revision Failure

Engineering issues a drawing at **IFC** (Issued for Construction), Revision B. In practice:

```text
Engineering    →  Rev B   (current)
Procurement    →  Rev A   (ordered against)
Supplier       →  Rev A   (manufactured to)
Construction   →  Rev A   (printed copy on site)
```

No one made a technical error. Every party executed correctly against the information they held. That is precisely the problem.

Revision control is not clerical work. It is the mechanism that keeps a distributed project operating from one shared reality.

### 2. Change Failure

Change is not the problem. **Reach** is.

A change can be correctly raised, reviewed, and approved — and still fail, because approval and propagation are separate activities and only one was completed.

```text
Change approved → Drawing updated → Supplier not notified
                                  → Site not notified
                                  → Discovered at FAT (Factory Acceptance Test)
```

> A change that does not reach every affected party is, operationally, an uncontrolled change.

### 3. Integration Failure

As projects scale, information fragments across personal folders, shared drives, email threads, vendor portals, and multiple repositories.

Each team is internally organised. No team holds the complete picture. The result is duplicated work, conflicting interpretations, slow decisions, and knowledge that leaves when individuals rotate off.

Most organisations plan carefully for *technical* integration between systems. Far fewer plan for *information* integration between the parties producing them.

### 4. Handover Failure

Many projects look successful until handover begins. Equipment is installed, construction is complete, commissioning is done — then the questions start:

- Which revision is final?
- Is the as-built package complete?
- Have all vendor documents been received and verified?
- Are all deviations documented?
- Which version does Operations inherit?

Handover failures are not created at handover. They accumulate across the lifecycle and become visible at the end, when the only remaining option is reconstruction — slow, expensive, and rarely complete.

---

## The Common Pattern

The four failures look unrelated. They share one sequence:

```text
Information Failure  →  Execution Failure  →  Project Failure
```

Capable engineers, experienced suppliers, and modern tooling do not interrupt this chain. None of them compensate for people acting on the wrong information.

---

## What Information Governance Actually Does

The objective is not document administration. It is ensuring the right information, at the right version, reaches the right people at the right time.

| Capability | What it guarantees | Failure mode without it |
|---|---|---|
| **Single source of truth** | One authoritative reference per deliverable | Competing versions, none provably correct |
| **Traceability** | Who changed what, when, and why | No basis for audit, claim, or root-cause analysis |
| **Change control** | Structured evaluation, approval, and release | Silent drift between design intent and built reality |
| **Information flow** | Confirmed distribution to all affected parties | Approved changes that never reach the field |

These are the same four capabilities formalised in **ISO 19650** (information requirements and delivery planning) and **ISO 9001 §7.5** (control of documented information). The vocabulary is newer than the discipline.

---

## A Quick Diagnostic

If several of these are true, information control has already degraded:

- Two teams maintain separate deliverable lists because "the master isn't current."
- Nobody can state a drawing's current revision without opening a file.
- Approved changes are communicated primarily by email.
- Vendor documents are tracked outside the main register.
- Progress reporting requires manual assembly from multiple sources.
- The answer to "is this the latest?" is "let me check with the engineer."

Individually, none are critical. Together, they reliably predict rework and delayed handover.

---

## What Separates High-Performing Projects

The usual assumptions are better engineers, better software, larger budgets. Those help. The consistent differentiator is **information discipline**.

```text
High-performing                  Average
────────────────                 ────────────────
One information source           Multiple versions
Shared understanding             Multiple interpretations
Consistent execution             Inconsistent execution
Rework as exception              Continuous correction
Handover as reconciliation       Handover as reconstruction
```

What is reported as an engineering problem is frequently an information problem that surfaced in engineering.

---

## Key Takeaway

Most organisations invest in improving execution. The most mature ones improve information quality first, because everything downstream inherits it.

> Engineering scales through information.

As projects grow larger, faster, and more distributed across parties, engineering capability stops being the constraint. Information control becomes the limiting factor — and when information loses control, the project follows.

That is why information governance is becoming a core engineering capability rather than a support function.

---

## Next in This Series

Newcomers see the **Master Document List (MDL)** as a spreadsheet. It is the operational backbone of everything described above.

Part 2 covers what an MDL is (as distinct from a document register), why it functions as the project's single source of truth, how it underwrites scope, progress, revision control and handover, the six ways MDLs fail, and how to build one that scales.

→ **[Part 3: Why the MDL Is the Most Important Document in a Project](/engineering-information-governance/why-mdl-is-the-most-important-document/)**

If information is the lifeblood of a project, the MDL is what keeps it circulating.
