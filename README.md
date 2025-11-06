# Mapping the Patent Frontier of On-Device LLMs in Mobile Software Engineering — Supplementary Materials

This repository hosts the **supplementary materials** accompanying the manuscript  
**“Mapping the Patent Frontier of On-Device LLMs in Mobile Software Engineering.”**  
It contains the curated patent dataset, analysis scripts, and reproducibility assets supporting all figures, tables, and analyses described in the paper.

> The study analyzes **8,630 global patents (1995–2025)** at the intersection of **large language models (LLMs)** and **mobile/on-device software systems**, using **topic modeling**, **CPC/IPC mining**, and **temporal + applicant trend analysis**.

---

## 📁 Repository Structure

LLMs-in-Mobile/
│
├── CPC Analysis/
│ └── Scripts and notebooks for CPC code frequency, top 15 overall, and per-topic analysis.
│
├── LDA/
│ └── LDA preprocessing and topic modeling assets (Gensim, coherence plots, pyLDAvis, word clouds).
│
├── Overall statistics on ntire Patents Set/
│ └── Global-level analytics (temporal growth, jurisdictions, applicant concentration, legal status, IPC/CPC sections).
│
├── Patents-Topics Analysis/
│ └── Aggregated topic-level statistics, citation means, and macro-category summaries.
│
├── Patents Data Set.csv
│ └── Canonical Lens.org export — grouped by simple families, including metadata fields.
│
└── Patents Mapped to Topics.csv
└── Each patent mapped to its dominant LDA topic (k=17) with posterior probabilities.

## Run the Pipeline

Load the dataset:
Open Patents Data Set.csv (Lens export; includes family ID, title, abstract, CPC/IPC, legal status, etc.)

Generate corpus-level statistics:
Run notebooks in Overall statistics on ntire Patents Set/ to reproduce:

Yearly filings and publications

CAGR trends

Jurisdiction and applicant distributions

Legal status breakdowns

Perform topic modeling:

Use the LDA/ folder to preprocess abstracts (tokenization, stopword removal).

Train LDA with k=17 topics using Gensim.

Export topic-word tables, coherence plots, and visualizations (pyLDAvis).

Map patents to topics:

Assign dominant topic IDs (highest posterior probability).

Save as Patents Mapped to Topics.csv.

Enrich topics with CPC codes:

Run CPC Analysis/ scripts to extract CPC subclasses.

Generate:

Top 15 CPC codes overall

Top 5 CPC codes per topic (dominant prob ≥ 0.5)

Aggregate topic-level insights:

Execute scripts in Patents-Topics Analysis/ to produce:

Topic-wise patent counts, citation stats, diffusion, and macro categories.

Tables and figures corresponding to the paper.


## Data Description

Source: Lens.org (academic export)
Time span: 1995–2025 (partial)
Scope: Global (US, CN, KR, JP, EPO, WIPO, etc.)
Granularity: Simple patent families (to avoid duplication)
Fields:

Patent ID, Title, Abstract, Publication/Filing Dates

Assignee(s), Inventor(s), CPC/IPC Codes, Legal Status

Topic ID (if mapped)

Why abstracts only?
Abstracts offer concise representations of patent content, balancing coverage and interpretability. 
Boilerplate phrases (e.g., “The invention discloses...”) were removed to mitigate stylistic noise. 
Topic validity was ensured through manual reading and CPC-based triangulation.
