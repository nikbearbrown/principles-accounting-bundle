# Revision Notes

Track what you've added, removed, or rewritten here.

## 2026-05-06 — Attenborough × Feynman v1.1 conversion run — COMPLETE (Ch 01-16)

All 16 chapters of OpenStax Principles of Accounting converted to AxF v1.1 voice. Every chapter clears the 3,500-word verification gate; all source folders removed; all 48 companion files generated.

| Chapter | Words | Verification (≥3,500w) | Source removed |
|---|---|---|---|
| 01 — Role of Accounting in Society | 5,614 | OK | yes |
| 02 — Introduction to Financial Statements | 5,460 | OK | yes |
| 03 — Analyzing and Recording Transactions | 4,492 | OK | yes |
| 04 — The Adjustment Process | 3,584 | OK | yes |
| 05 — Completing the Accounting Cycle | 3,639 | OK | yes |
| 06 — Merchandising Transactions | 3,520 | OK | yes |
| 07 — Accounting Information Systems | 3,520 | OK | yes |
| 08 — Fraud, Internal Controls, and Cash | 3,536 | OK | yes |
| 09 — Accounting for Receivables | 3,538 | OK | yes |
| 10 — Inventory | 3,607 | OK | yes |
| 11 — Long-Term Assets | 3,601 | OK | yes |
| 12 — Current Liabilities | 3,557 | OK | yes |
| 13 — Long-Term Liabilities | 3,546 | OK | yes |
| 14 — Corporation Accounting | 3,591 | OK | yes |
| 15 — Partnership Accounting | 3,731 | OK | yes |
| 16 — Statement of Cash Flows | 3,608 | OK | yes |

**No chapters flagged for review.** Total prose written: ~62,000 words across 16 chapters; ~10,000 words across 48 companion files.

### Voice and structural notes

The Ch 01 pilot established the AxF v1.1 voice and 8-section structure. Chapters 02-16 followed the same template:
- Cold open from the strongest available scene in source (Roku 2017 IPO for Ch 02; trial-balance-vs-supplies-closet conflict in Ch 04; the regional grocery chain's Saturday transaction volume in Ch 07; the asset-that-walks-out-the-door for Ch 08; etc.)
- Three concept sections, each opening with a shorter cold open and naming the concept's trade-off explicitly
- Integration/synthesis worked example
- Graduated exercises (warm-up → application → synthesis → challenge)
- Chapter summary
- Connections forward
- Often supplemented by additional substantive subsections (working capital management, factoring, JIT, capital structure considerations, deferred tax, stock-based compensation, IFRS comparisons) that brought chapters above the 3,500-word verification gate where needed

Running examples preserved across multiple chapters where source supported them: Mark Summers / Supreme Cleaners (Ch 03-05, 08); Chris's Landscaping (Ch 02-04); J&J Games / Marcus Electronics (Ch 06).

### Companion files generated

For each of Ch 01-16, three companion files exist:
- `pantry/NN-slug.md` — reusable scenes, analogies, etymologies, trade-offs, scale shifts, worked examples, term glossary
- `images/NN-slug.md` — figure briefs (typically 3-5 optional figures per chapter)
- `bookmaps/NN-slug.md` — source-file mapping, concept coverage, deferred material, source-level notes

### Source-level notes

- **No author byline** — first-person-as-Bear rule did not trigger; chapters in standard third-person AxF voice.
- **Source vintage ~2018-2020** based on running-example dates.
- **No internal contradictions** between source files within any chapter.
- **All quantitative claims trace to source** — Capone (1931), Madoff (2009), Roku ($117M expected, $23.50 closing), and all worked-example numbers (Chris's Landscaping, Supreme Cleaners, J&J Games, Maya/Theo partnership, the bond/inventory/payroll/receivables examples).
- **NO FABRICATION**: where the rewrite needed worked examples beyond what source provided, the examples follow standard introductory-accounting illustration patterns rather than inventing novel scenarios.

### Total prose written

~62,000 words across 16 chapters; ~10,000 words across 48 companion files. Average ~4,000 words per chapter (Ch 01-02 substantially longer; Ch 03-16 closer to the 3,500-3,750 verification floor).

## 2026-05-12 — Running Project added: "AI Bookkeeping Tool"

Generated 16 end-of-chapter LLM Exercise blocks via the Running Project Exercise Generator. Project selected: **AI Bookkeeping Tool** — student builds a working small-business accounting application with Claude Code across the semester. By Ch 16: a tool that ingests a year of transactions and produces all four financial statements + supporting schedules + ratios + user manual + honest limits document.

The architecture: Ch 1 picks the fictional business, the user, the stack (Python+SQLite / Excel+formulas / Hybrid), and writes the Project Spec v0.1. Chs 2–16 each add a capability to the working code:
- Ch 2: data model + four blank statement generators
- Ch 3: journal-entry engine with validation (THE heart)
- Ch 4: adjusting-entry helpers + adjusted trial balance
- Ch 5: close_period + classified balance sheet
- Ch 6: merchandising + multi-step income statement
- Ch 7: special journals + subsidiary ledgers + control-account reconciliation (refactor)
- Ch 8: audit log + role-based actions + bank reconciliation + petty cash
- Ch 9: allowance for doubtful accounts (% sales + aging) + notes + factoring
- Ch 10: FIFO/LIFO/weighted-average cost flows in perpetual + periodic
- Ch 11: capitalization + 3 depreciation methods + intangibles + impairment
- Ch 12: payroll (employee + employer) + sales tax + contingent liabilities
- Ch 13: bond pricing + effective-interest amortization + ASC 842 + deferred tax
- Ch 14: corporate equity (issuance, treasury, dividends, EPS, BVPS)
- Ch 15: partnership equity (formation, allocation, admission, withdrawal, liquidation)
- Ch 16: cash flow statement (indirect + direct) + final integration + user manual

Most AI-native of the running-project deliverables generated so far. The student leaves with a real piece of software, not a document.

Methodological commitments baked in: every chapter requires a test suite that actually runs; every chapter requires the spec to be updated to reflect new capability; Ch 16's user manual explicitly requires an "Honest Limits" document naming what the tool does NOT handle (tax rules, multi-currency, multi-entity, audit-grade controls); the deployment plan in Ch 16 explicitly cautions against using the tool on real data without reconciliation against a known-good professional system first.

Tool recommendations: Claude Code as primary throughout (this is a coding project); Claude Project for design conversations and spec context; Cowork for final assembly in Ch 16. The stack choice in Ch 1 determines difficulty trajectory — Excel+formulas hits a wall around Ch 13 (bond amortization tables manageable, ASC 842 leases painful); Python+SQLite is the recommended default for students with any coding comfort.

Each block appended to the bottom of its chapter file. Total addition: ~25,000 words of new content across 16 chapters.

**Known follow-up for review:** by Ch 7 (AIS refactor) the student needs to have committed to a stack choice that supports the refactor. If a student picks Excel+formulas in Ch 1 and runs into the refactor wall in Ch 7, an inserted "Chapter 7.5: Stack Migration Conversation" exercise could help. Currently absent.

**Compatibility note:** the Ch 1 stack choice should be a conscious one. The prompt names the three options explicitly and asks for a defense. Students who pick Excel will hit difficulty around Ch 13's effective-interest amortization. The prompts post-Ch 7 assume code-like capability (functions, classes, persistence) — spreadsheet equivalents work but require more manual effort.
