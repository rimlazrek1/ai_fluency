# French M2 Data Science Application Evaluator Agent

An AI-driven application workspace built on Claude designed to evaluate and align candidate motivation letters and academic profiles with French Master 2 (M2) Data Science program syllabi and Campus France prerequisites.

## Overview
Applying to French M2 Data Science programs through Campus France requires tight alignment between a student's prior academic coursework (e.g., engineering degree background) and specific program requirements. This project configures a custom workspace using Claude to act as an automated application evaluator.

## System Architecture & Workspace Structure
The workspace relies on structured context ingestion and systemic prompt evaluation:

1. **Context Knowledge Base (`m2_data_science_programs.json`):** A curated JSON database containing M2 Data Science program syllabi (Université Paris-Saclay, Institut Polytechnique de Paris, Université Grenoble Alpes), prerequisite competencies, and university-specific expectations.
2. **Evaluation Framework (`system_prompt.md`):** Systemic instructions guiding Claude to adopt the persona of a French academic admissions committee reviewer.
3. **Candidate Input:** Draft motivation letters and academic history logs submitted in plain text.



[Candidate Motivation Letter] + [m2_data_science_programs.json]
│
▼
[Claude Custom Workspace Environment]
│
▼
[Structural Scorecard & Alignment Analysis]



## Setup & Usage Instructions

### Prerequisites
* Access to Claude (Anthropic) or Claude Workspace.
* The repository files: `m2_data_science_programs.json` and your application drafts.

### Execution Steps
1. **Load Context:** Upload `m2_data_science_programs.json` into your Claude conversation/workspace context.
2. **Apply System Instructions:** Copy the evaluation system prompt into the instructions or initial prompt window.
3. **Input Draft:** Paste your draft motivation letter or module history.
4. **Run Evaluation:** Trigger the audit to output a structural match report.

## Transparency Diligence (AI Building Disclosure)
> **AI Usage Disclosure:** Built using Claude as the core intelligence engine. Custom system prompts, JSON database structures, and evaluation rubrics were designed, verified, and audited manually against real Campus France and M2 Data Science application guidelines.

## Evaluation Results & Limitations

### Evaluation Capability (v2)
* Successfully flags missing technical prerequisites (e.g., highlighting missing explicit mentions of optimization or distributed systems).
* Rates alignment on a 1–5 scale with actionable rewrite suggestions tailored to French academic tone.

### System Limitations
* **Prerequisite Over-Fitted Matching:** Claude occasionally over-indexes on exact keyword matches from the JSON syllabus (e.g., demanding "PyTorch" explicitly when general "Deep Learning" is stated).
* **Context Window Boundaries:** When evaluating more than 5 university syllabi simultaneously, response latency increases and evaluation granularity drops.
