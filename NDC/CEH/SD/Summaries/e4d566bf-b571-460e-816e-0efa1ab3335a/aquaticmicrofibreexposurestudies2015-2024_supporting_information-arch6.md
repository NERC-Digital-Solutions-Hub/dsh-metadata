# AquaticMicrofibreExposurestudies2015-2024 Supporting information

## Overview
- A dataset comprising extracted data from published laboratory studies on microfibre exposure (<5 mm) and their effects on aquatic organisms.
- Focuses on traits such as development, fecundity, feeding, growth, hatching, health, and survival.
- Created to support meta-analyses comparing petroleum-based vs non-petroleum microfibres.
- Data collected up to 19/06/2024; compiled by Ben Parker.
- Data are extracted from manuscripts, supplementary information, and figures (via plot digitiser) and include final timepoint measurements only.

## Dataset contents
- File name: AquaticMicrofibreExposurestudies2015-2024.csv
- Structure: per-response rows capturing study metadata, organism, exposure details, and outcome measures.
- Key components:
  - Study-level metadata: Reference, Authors, Title, Year, Country of first author affiliation.
  - Organism-level: Species, Source (how organism was obtained), Environment (Freshwater, Marine, Estuarine), Taxonomic grouping.
  - Exposure details: Microfibre category (petroleum-based vs other polymers), Length/Width, Study exposure (non-standardised), Standardised exposure (by mass or fibre number) and units, Time series indicators.
  - Outcome measures: Trait category (Development, Fecundity, Feeding, Growth, Hatching, Health, Survival), Response type, Means and SDs for Control and Experimental conditions, including conversion notes if needed.
  - Data extraction notes: Source of data (MS or SI), Converted.measure flag, Timepoint/lifestage considered (final only), and whether data were part of sequential series.
- Data fields (examples): ID, Study.no, Reference, Authors, Title, Year, FA.country, Species, Source, Environment, Taxonomic.grouping, Days.exposed, Days.cat, MF.category, Length.mm, Length.cat, Width.mm, Study.exposure, Study.exposure.units, Standard.exposure, S.cat, Standard.units, Time.series, Additional.variable, Response, Converted.measure, Response.units, C.N, C.mean, C.SD, E.N, E.mean, E.SD, Data.source.

## Collection and screening
- Data identification: Topic search in Web of Science (as of 19/06/2024) using microfibre/microfiber/textile and effect keywords; document type: Article.
- Screening process:
  - Screening stage 1: Title/abstract relevance to biological responses to microfibre exposure.
  - Screening stage 2: Forward and backward searches of citing/cited studies for relevance.
  - Screening stage 3: Eligibility screening with criteria:
    - Aquatic organism included
    - Controlled microfibre exposure (>1 µm and <5 mm) of a single polymer type (no mixtures)
    - Mean measures with errors available for both exposure and control
    - Data extractable from manuscript/SI/figures
- Outcome: All eligible responses extracted for key traits; only final timepoints included; only positive responses kept (negative responses converted to positive when appropriate).

## Data structure and units
- The resource is a structured CSV with consistent fields to enable cross-study comparisons.
- Extractions include final timepoint data across exposure combinations and life stages, excluding co-contaminants.
- Units and scaling:
  - Standardised exposure may be by mass (µg/L) or fibre number (fibres/L), with categories A–K representing orders of magnitude.
  - Timepoint categorisations (e.g., Days.exposed, Days.cat) standardised to defined bins.
- Data provenance:
  - Data source indicated as MS (manuscript) or SI (supplementary information), with notes on any conversions applied.

## Quality control
- Multi-stage screening to ensure relevance and data suitability:
  - Stage 1 and Stage 2: Relevance screening of titles/abstracts and their citers/cited-by.
  - Stage 3: Full eligibility assessment against predefined criteria.
- Criteria ensure inclusion of controlled exposures to a single polymer and availability of mean ± error estimates for both control and exposure groups.

## Data usage and potential products
- Primary use: meta-analyses comparing biological responses to microfibres across taxa and environments, including petroleum-based vs non-petroleum fibres.
- Data support for building end-user tools:
  - Dashboards to filter by trait, species, polymer type, exposure concentration, and duration.
  - Pivot-style summaries to compare effect directions across taxa and traits.
  - Data dictionaries and provenance trails to facilitate reproducibility and transparency.
- Data preparation notes for end users:
  - Negative responses converted to positive where appropriate to align with the positive-response framework.
  - Only final-timepoint data included for multi-timepoint studies.
  - Exclusion of co-contaminant exposures to maintain single-polymer comparisons.

## Source references
- The dataset aggregates data from numerous primary studies (example references listed in the accompanying document), including but not limited to:
  - Au et al., 2015
  - Blarer & Burkhardt-Holm, 2016
  - Bour et al., 2022
  - Bunge et al., 2022
  - Cheng et al., 2021, 2024
  - Choi et al., 2021, 2022
  - Cole et al., 2020
  - Coppock et al., 2019
  - Cui et al., 2022
  - DiBona et al., 2021, 2022
  - Hu et al., 2020
  - Jabeen et al., 2018
  - Jemec et al., 2016
  - Jiang et al., 2023
  - and many others listed in the resource
- The dataset includes the full bibliographic references and study contexts as compiled in the resource’s “Study references” section.