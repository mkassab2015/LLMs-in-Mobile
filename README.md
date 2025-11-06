# Mapping the Patent Frontier of On-Device LLMs in Mobile Software Engineering — Supplementary Materials

This repository hosts the **supplementary materials** accompanying the manuscript  
**“Mapping the Patent Frontier of On-Device LLMs in Mobile Software Engineering.”**  
It contains the curated patent dataset, analysis scripts, and reproducibility assets supporting all figures, tables, and analyses described in the paper.

> The study analyzes **8,630 global patents (1995–2025)** at the intersection of **large language models (LLMs)** and **mobile/on-device software systems**, using **topic modeling**, **CPC/IPC mining**, and **temporal + applicant trend analysis**.

---

## 📁 Repository Structure

Patents Data Set.csv --- Canonical dataset exported from Lens (family-grouped), including title, abstract, publication/filing dates, jurisdiction, assignee, inventor(s), CPC/IPC, and legal status.

Patents Mapped to Topics.csv --- Each patent mapped to its LDA posterior and dominant topic (k=17), used for topic-level analytics and CPC rollups.

CPC Analysis/ -- -Scripts/notebooks to compute (i) top-15 CPC subclasses overall (count once per family) and (ii) top-5 CPC subclasses per topic (using patents with dominant topic ≥ 0.5). Outputs include CSV tables and plots.

LDA/ --- Text preprocessing and topic modeling assets (Gensim LDA, coherence search, pyLDAvis, word clouds), plus the document–topic matrix.

Overall statistics on ntire Patents Set/ --- Corpus-level analytics: yearly filings/publications, CAGR, jurisdictional distribution, applicant concentration, legal maturity, and high-level IPC/CPC sections; exports CSV + PNG figures.

Patents-Topics Analysis/ --- Topic-level aggregations (counts, citations, family size/diffusion), macro-category summaries, and tables mirroring manuscript Tables/Figures (e.g., topic summaries and distributions).

Top-level items visible in the GitHub tree: CPC Analysis/, LDA/, Overall statistics on ntire Patents Set/, Patents-Topics Analysis/, Patents Data Set.csv, Patents Mapped to Topics.csv. 
GitHub

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
