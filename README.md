# Securing Generative AI in a Managed Service Provider Environment# Securing Generative AI in a Managed Service Provider Environment


Capstone project for WGU D833 — Cybersecurity and Information Assurance Capstone.
Author: Brent (John Brent) Petty. Instructor: John Jamison.

## What this project is about

Front Range Managed Services (FRMS), a mid-sized managed service provider, had employees using generative AI tools (Microsoft Copilot, browser-based AI assistants) during troubleshooting and client support with no governance, no Data Loss Prevention controls, and no monitoring. This capstone identifies that risk, proposes a fix, and then implements and reports on it, using Microsoft Purview (DLP), Microsoft Defender for Endpoint, and Microsoft Sentinel (SIEM).

The three tasks walk through the same problem from three different points in time:

| Task | Phase | What it covers |
| --- | --- | --- |
| **Task 1** | Before | Defines the cybersecurity problem, proposes a control, and scopes the project. |
| **Task 2** | During (the plan) | The full project proposal: risk assessment, technical solution, standards alignment, cost, timeline, and implementation plan for rolling the controls out. |
| **Task 3** | After (the results) | The technical report on what happened once the controls were implemented: results, residual risks, monitoring/maintenance plan, and recommendations. |

## Repository structure

```
├── README.md
├── task-1-problem-proposal/
│   └── Task1_Cybersecurity_Problem_Proposal.docx      ← Task 1 (only version — no separate final exists)
├── task-2-project-proposal/
│   ├── Task2_Project_Proposal_FINAL.docx              ← Task 2, the finished/graded version
│   └── drafts/
│       ├── Task2_Outline_Draft.docx                   ← early skeleton pass of the whole proposal
│       └── Task2_Appendices_Fragment_Draft.docx       ← leftover fragment (just Appendix A/B)
├── task-3-technical-report/
│   ├── Task3_Technical_Report_FINAL.docx              ← Task 3, the finished/graded version
│   └── drafts/
│       ├── Task3_Detailed_Draft.docx                  ← mid-stage draft, rubric-labeled (Section A–G)
│       └── Task3_Early_Stub_Draft.docx                ← short early stub (despite old filename, NOT the final)
└── reference/
    └── All_Tasks_Combined_Working_Draft.docx          ← combined working draft of all 3 tasks, kept for reference
```

Each task folder's top-level file is the one to treat as "the" document for that task. Everything under `drafts/` or `reference/` is earlier work, kept for history — not duplicate deliverables.

## Where each file came from

The original files (in the source project) had names that didn't reliably describe their contents — a couple of "final" files were actually early drafts, and a couple of "appendix" files actually contained the whole proposal. This table maps old → new so nothing gets lost:

| Original filename | Renamed to | Why |
| --- | --- | --- |
| `Capstone_Task1_Draft_v2.docx` | `task-1-problem-proposal/Task1_Cybersecurity_Problem_Proposal.docx` | Only Task 1 document that exists; treated as the Task 1 deliverable. |
| `Task_2_Proposal_v1.docx` | `task-2-project-proposal/Task2_Project_Proposal_FINAL.docx` | Fully formatted with cover page, TOC, references, and appendices, dated April 6 — the actual finished proposal. |
| `Task2_Appendix.docx` | `task-2-project-proposal/drafts/Task2_Outline_Draft.docx` | Despite the name, it's a terse outline of the *entire* proposal (Background through Conclusion), not just an appendix. Superseded by the final. |
| `Task2_Full_Draft.docx` | `task-2-project-proposal/drafts/Task2_Appendices_Fragment_Draft.docx` | Despite the name, it only ever contained Appendix A and B. Those same appendices, more complete, are already in the final. |
| `Technical Report Task_3 V1.docx` | `task-3-technical-report/Task3_Technical_Report_FINAL.docx` | Fully formatted with cover page, TOC, references, and appendix, dated April 20 (the latest date of any file) — the actual finished report. |
| `Task 3.docx` | `task-3-technical-report/drafts/Task3_Detailed_Draft.docx` | Detailed mid-stage draft organized under rubric section letters (A–G); same narrative as the final, less polished. |
| `Task3_Final_Report.docx` | `task-3-technical-report/drafts/Task3_Early_Stub_Draft.docx` | Named "final" but is a short stub dated **March** — earlier than the real final (dated April 20). Kept only as draft history. |
| `All_Tasks_All_Sections_Draft.docx` | `reference/All_Tasks_Combined_Working_Draft.docx` | A single working document combining all three tasks under rubric section codes (A1, A2, B1…). The Task 2 section here is the most granular of any draft and likely fed the final proposal. Kept as reference. |

## Safe to delete from the original project

Nothing here was deleted — everything was archived instead, per your request. If you want to trim the original uploads later, the two files below add no unique content once this structure exists (their content is fully superseded elsewhere):

- `Task2_Full_Draft.docx` — content is just Appendix A/B, already included (in fuller form) in the Task 2 final.
- `Task3_Final_Report.docx` — an early, much shorter stub; the real final report supersedes it entirely.

`Task2_Appendix.docx`, `Task 3.docx`, and `All_Tasks_All_Sections_Draft.docx` are lower-value duplicates too, but were kept as drafts/reference rather than flagged for deletion since they contain some phrasing not preserved verbatim anywhere else.

## Using this with GitHub

This folder is ready to become a repository as-is:

```
cd task-1-problem-proposal   # (or wherever you unzipped this)
git init
git add .
git commit -m "Organize capstone into Task 1/2/3 structure"
git remote add origin <your-repo-url>
git push -u origin main
```

## Note on formatting

The `.docx` files in this folder were regenerated from the text content of the originals so they could be cleanly renamed and organized (the source Word files themselves were project uploads that can't be renamed or moved in place). Wording, structure, section order, tables, and references were preserved; original manual formatting flourishes (exact fonts, page-number fields, etc.) were rebuilt using a clean, consistent style rather than pixel-matched. If you need the byte-identical original files, they remain in the Claude project this was organized from.
