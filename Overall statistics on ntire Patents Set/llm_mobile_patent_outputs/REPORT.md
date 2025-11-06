# LLMs for Mobile Patents — Landscape Report (Analyses 1–7)
This report summarizes quantitative patterns in your Lens.org dataset. Each section lists outputs and how to read them.

## A1. Temporal Trends
- Files: `A1_temporal_trends_by_year.csv`, `A1_temporal_trends_line.png`
- Interpretation: Filings vs. publications show pipeline dynamics; CAGR summarizes growth.
  - CAGR (Filings): 28.278%
  - CAGR (Publications): 34.085%
## A2. Geographic Distribution
- Files: `A2_top20_jurisdictions.csv`, `A2_top20_jurisdictions_bar.png`, plus `A2_family_internationalization_*` if family IDs exist.
- Interpretation: Top jurisdictions indicate key protection markets; family internationalization shows breadth of protection across countries.
## A3. Applicants & Inventors
- Files: `A3_top20_applicants.csv`, `A3_top20_applicants_bar.png`, `A3_top20_inventors.csv`, `A3_top20_inventors_bar.png`
- Concentration: Top-10 applicants’ share of patents ≈ 19.7% (higher ⇒ more concentrated).
## A4. Legal Status & Maturity
- Files: `A4_legal_status_distribution.csv`, `A4_legal_status_bar.png`
- Average age (active/granted/pending, by pub year): ~0.51 years.
## A5. Technological Focus (IPC/CPC Sections)
- Files: `A5_ipc_cpc_section_counts.csv`, `A5_sections_aggregated_counts.csv`, `A5_sections_aggregated_bar.png`
- Interpretation: Section letters (A–H) summarize domains (e.g., G = Physics; G06 = Computing). Peaks show where innovation clusters.
## A6. Citation Analysis
- Files: `A6_top25_most_cited_patents.csv`, `A6_top25_citations_per_year.csv`, `A6_citation_histogram_bins.csv`, `A6_citation_histogram_bar.png`
- Interpretation: Most-cited = high impact; citations/year normalizes for recency; histogram shows skew/long tail.
## A7. Family Analysis
- Files: `A7_family_sizes.csv`, `A7_top25_families.csv`, `A7_top25_families_bar.png`