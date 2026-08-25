---
title: "Why Large Projects Always Fall Into Revision Chaos"
date: 2026-08-20
last_modified_at: 2026-08-20
categories:
  - Engineering Information Governance
tags:
  - Revision Control
  - Document Control
  - Information Governance
  - Configuration Management
  - Project Delivery
excerpt: "Revision chaos is not a failure of discipline. It affects projects with numbering standards, enforced workflows, and clean audit trails — because at scale, outdated copies always outnumber current ones."
toc: true
toc_label: "Contents"
toc_sticky: true
series: "Engineering Information Governance"
series_part: 5
---

## It Happens on Well-Run Projects

Imagine a project that does everything right. It has strict numbering rules, approved procedures, and enforced workflows in a shared system. Document deliveries are tracked and balanced monthly, and audits show zero errors in document control.

Eighteen months in, a supplier builds a piece of equipment using an outdated drawing. Fixing it costs six weeks and over a million dollars.

An investigation shows no rules were broken. The document was issued correctly, sent to the right person on time, and they confirmed receiving it. No one was careless. 

Carelessness doesn't explain this mistake. Neither does a lack of training, bad software, or loose rules—the project already had good versions of all three.

**Key Takeaway:** If document chaos only happened on messy projects, it would just be a training issue. Because it happens on highly disciplined projects, it is a system design problem.

---

## Three Concepts, One Field

Most revision problems start when we mix up three different ideas and put them into a single data field.

| | What it asks | Changes when | Who sees it | Who owns it |
|---|---|---|---|---|
| **Version** | Which draft is this? | Any save or edit | Only the creators | The Author |
| **Revision** | Which official release is this? | Formal issue | Everyone | Document Control |
| **Status** | What can we use this for? | Review outcome | Everyone | Approver / Client |

These three concepts are completely separate. A single revision can have many drafts (versions) and change its status over its lifetime.

```text
Rev B  
  ├─ v1  draft       
  ├─ v2  internal check       
  ├─ v3  discipline review       
  └─ v4  →  ISSUED as Rev B, status IFR (Issued for Review)
         ←  returned Code 2

Rev C  
  ├─ v1  comment incorporation       
  └─ v2  →  ISSUED as Rev C, status IFA (Issued for Approval)
```

If you mash these into one field, you can't tell people what the document is *for*. That is the most important question for the person using it. Mixing these up causes two main problems:

**Drafts leak out.** An engineer emails "v3, for information" because the official process takes too long. That file now floats around with no official identity, status, or tracking. Months later, someone might use it without knowing where it came from.

**Revisions don't update.** Someone fixes a "minor typo" and sends the document out again with the same revision number. Now, two different documents have the exact same identity. This is a massive failure. All tracking systems assume one revision number means one specific set of content. When this rule breaks, you lose control without even realizing it.

*A quick tip on naming:* Use letters (A, B, C) for drafts before approval, and numbers (0, 1, 2) once approved for construction. The exact rule comes from your contract—see [Part 4](/engineering-information-governance/document-control-begins-at-the-contract/).

**Key Takeaway:** One field cannot do the job of three. Version, revision, and status answer different questions and belong to different people.

---

## Why the Number of Copies Explodes

Revision chaos always happens on large projects because of simple math, not bad behavior.

Every time you issue a document, you create copies. Those copies stick around until someone actively throws them away. The total number of copies out there looks like this:

```text
Total Copies = Documents × Issued Revisions × People Who Have Them
```

Here is an example to show the math:

| Project scale | Documents | Revisions | Companies | Total copies | Current | Outdated |
|---|---|---|---|---|---|---|
| Mid-size | 5,000 | 4 | 12 | 240,000 | 60,000 | 180,000 |
| Large EPC | 50,000 | 5 | 40 | 10,000,000 | 2,000,000 | 8,000,000 |

If a document has five revisions, **four out of five copies in the real world are wrong**. This isn't a mistake; it happens because old copies were replaced but never destroyed.

Two surprising truths come from this:

- **Being right is rare.** Document control isn't just fixing occasional mistakes; it's fighting a massive flood of outdated files. Outdated is the default.
- **Adding companies creates more chaos than adding documents.** Adding one subcontractor copies the entire document list. A project with 50,000 documents and 8 companies is much easier to manage than a project with 15,000 documents and 40 companies.

[Part 2](/engineering-information-governance/why-engineering-projects-lose-control/) described four companies holding four different revisions of the same drawing. That isn’t a bad project—that is just basic math.

**Key Takeaway:** On large projects, chaos is normal. Control is a structure you have to actively force onto the project.

---

## Having Multiple Active Revisions Is Sometimes Necessary

The obvious fix is to allow only one active revision at a time. But this is wrong. If you try to force this, people will just hide their work.

Having multiple active revisions is often the correct way to work:

| Situation | In use | Being created | Why both are valid |
|---|---|---|---|
| Phased construction | C — Approved for Area 1 | D — In Review for Area 2 | Different physical locations |
| Contractual freeze | C — Approved design | E — Working design | The difference is an unapproved cost change |
| Vendor review | 2 — Approved | 3 — Vendor's draft | Not officially submitted yet |
| Slow procurement | B — Used to order parts | D — Current design | Changing the order would cost too much |

Stopping these parallel revisions would halt work or hide important business negotiations. Having multiple active revisions is not a flaw.

It only becomes dangerous when it’s a secret. If you have Rev C, you need to know if it's the newest, if it's on hold, or if it's outdated. The revision number won't tell you this. Only the *status* tells you this. **The status field is what makes it safe to have multiple active revisions.**

**Key Takeaway:** The problem isn't having multiple active revisions. The problem is having them without telling anyone what they are for.

---

## Replacing a Document Requires Action

Issuing Rev C creates something new. Retiring Rev B destroys something old. Most projects do the first and assume the second happens automatically. It doesn't. Issuing a new revision just creates a competitor to the old one.

After Rev C is issued, Rev B is still:
- Printed and pinned to a wall on the job site
- Attached to a purchase order sent three months ago
- Saved on a supplier's computer network
- Written into an approved testing manual
- Hidden inside 40 different email inboxes

Issuing Rev C doesn't touch any of those. You have to actively hunt them down and retire them.

People often mix up two different actions, which causes expensive mistakes:

| | What it means | Does it replace something? | Urgency |
|---|---|---|---|
| **Supersession (Update)** | A newer version exists | Yes | Routine |
| **Withdrawal (Recall)** | This document is wrong — STOP | No | Immediate |

If you need people to stop using a dangerously wrong document (a withdrawal) but you just send it out like a standard update (a supersession), the bad information will keep being used. It looks like a routine update and gets filed away instead of acted upon.

**The Last Mile.** Control ends as soon as a file is downloaded or printed. It becomes a frozen picture that ignores all future updates. Smart projects manage this actively. They keep a strict list of who has printed copies, use expiring watermarks, and do routine checks to gather old prints.

**Key Takeaway:** If you issue a new revision but don't actively recall the old one, you haven't replaced the document. You have just duplicated it.

---

## Who Gets to Create the Next Revision?

People usually think it's obvious who is allowed to update a document. On projects with many companies, it isn't.

| Document type | Why it gets confusing |
|---|---|
| Vendor document | The vendor makes Rev 3. The project team adds a cover sheet and calls it Rev C. Now one document has two names. |
| Client-commented | When a client adds notes, does that create a new revision, or only when you reply? |
| Shared interfaces | Two contractors share a boundary, and both think they can edit the document. |
| Third-party certified | An inspector updates a document without telling the central control team. |

The rule must be strict: **only one specific group can update a specific document, and they must be named on the Master Document Register (MDL).** As mentioned in [Part 3](/engineering-information-governance/why-mdl-is-the-most-important-document/), this right belongs to a specific person, not a whole department.

**Key Takeaway:** If two different people are allowed to create "Rev D", two different "Rev Ds" will eventually exist. No software will catch this, because both people followed the rules.

---

## Systems That Actually Work

Everyone agrees revisions should be controlled. Successful projects use specific tools to stop specific failures.

| Tool | Problem it stops |
|---|---|
| **One single exit point** — all files must go through Document Control | Drafts leaking out unofficially |
| **Revision is part of the name** — not just an editable tag | Two different documents sharing one name |
| **Pull, not push** — send links to the live system, not email attachments | Old copies piling up everywhere |
| **Updates require action** — make users confirm they saw it | Old revisions silently staying in use |
| **Clear purpose on every document** — state what it's for | Secret multiple revisions |
| **Printed copy register** — list exactly who has physical copies | Unstoppable printed copies |
| **Recall as a major event** — treat bad documents as emergencies | Wrong documents being filed away instead of destroyed |

The choice between "push" (sending files) and "pull" (sending links) is where many projects fail. 
*   **Push:** If you email a file, you create copies everywhere. If the person never reads the email, they keep using their old file, and you never know. 
*   **Pull:** If you send a link, they always get the latest version. 

The best approach is **pull for the document, push for the alert**. Tell them a change happened (push), but make them log in to get it (pull). Doing the reverse creates endless outdated copies.

**Things to measure:**
```text
Outdated copies still in use         Printed documents that haven't been checked
Time it takes to update              Issue date → Date the last person confirmed receipt
Secret overlapping revisions         Active files that don't state their purpose
Duplicate identities                 Two different files sharing one revision number
```

Duplicate identities must be zero. If two different documents share the same number, your entire tracking system is broken.

**Key Takeaway:** Controlling revisions on a large scale isn't about making people work harder. It's about designing a system that doesn't rely on human perfection.

---

## The Limits of Revision Control

Revision control works on one document at a time. It tells you if a document is the newest version. It does **not** tell you if all your newest documents agree with each other.

```text
P&ID Drawing      Rev D   Newest   ✓
Cause & Effect    Rev B   Newest   ✓
Loop diagrams     Rev C   Newest   ✓
                            ↓
Every document is the newest version. 
But the design is broken.
```

Every check passes, and every tracker is accurate. But the Cause & Effect document no longer matches the P&ID drawing, because someone added two parts to Rev D and forgot to update the other files.

This is the line [Part 1](/governance/what-does-document-control-actually-manage/) called Stage 3 — Configuration Management. 
*   Document Control asks: *"Is this file the newest?"* 
*   Configuration Management asks: *"Do all these files actually match the real world?"* 

Revision control only answers the first question. To answer the second, you need a system for change propagation, which we will cover in Part 6.

**Key Takeaway:** Perfect revision control can give you a set of perfectly updated documents that completely contradict each other.

---

## How to Fix Things Mid-Project

If you are already halfway through a messy project, you can still fix it. But you must fix things moving *forward*. Trying to clean up past mistakes costs too much time and money. Start with the easiest steps:

1. **Separate version, revision, and status before you change anything else.** If your system can't tell the difference between these three, adding better data won't help.
2. **Find all active revisions and force a purpose.** Make everyone declare what their active document is being used for (its status).
3. **Start tracking printed/downloaded copies from today onward.** Don't try to track down the past ones. Just track new ones and let the old ones naturally expire.
4. **Stop emailing files for new updates.** Send links instead (pull). Leave old emails alone.
5. **Hunt down duplicate identities.** Look for documents with the same number but different content. Fix these immediately, as they silently destroy your project's data.

**Key Takeaway:** Do not try to fix the past. Control the new documents and let the old ones naturally expire.

---

## Conclusion

Think back to the project at the start of this article. Their rules weren't broken. Their rules simply didn't account for how much data was out there.

```text
Documents × Revisions × Companies
            ↓
Outdated copies always outnumber new ones
            ↓
Control means stopping the flood, not just preventing mistakes
```

A revision rule tells you how a document goes from Rev A to Rev B. It doesn't tell you what to do with the hundreds of thousands of outdated Rev A copies sitting on computers at 40 different companies. That is where the failure actually happens.

People often confuse two questions:
*   *"Is this document the newest version?"* (A revision question)
*   *"Are we all looking at the same reality?"* (A governance question)

Revision control answers the first question reliably. Only the systems mentioned in this article answer the second.

The projects that succeed don't just have stricter rules. They accept that copies will multiply out of control, and they build a system to stop it.

---

## Next in This Series

Revision control makes sure each document is the newest version. It cannot make sure all the documents agree with each other.

Part 6 looks at change propagation — how one approved change ripples across drawings, specifications, vendor documents, testing rules, and final manuals, and why getting the approval is actually the easy part.

**→ [Part 6: Change Propagation — Why Approval Is the Easy Part](/governance/change-propagation-why-approval-is-the-easy-part/)**
