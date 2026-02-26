# BAAP_Screen_Aberdeen_0N.csv and BAAP_Screen_Aberdeen_100N.csv

## Overview
- Two CSV data sheets containing trait values for 229 rice cultivars from the Bengal and Assam Association Panel (BAAP).
- Experiments conducted over 6 weeks under two nitrogen treatments: 0N (no added N) and 100N (added N).
- Traits measured per plant: plant height (cm), number of tillers, nitrogen balance index (NBI), chlorophyll content (Chl), and shoot dry biomass (g).
- 0N and 100N raw data are provided separately.

## Purpose and Context
- Aim: identify rice cultivars with high nitrogen use efficiency (NUE) and enable quantitative trait loci (QTL) and candidate gene exploration for NUE.
- Location: School of Biological Sciences, University of Aberdeen, UK.
- Date: September–October 2020.
- Material: 229 BAAP cultivars (linked to an existing BAAP database of ~2 million SNPs).
- Experimental setup references prior BAAP work (Norton et al., 2018).

## Experimental Design and Setting
- Growth environment: controlled environment room with 28°C day / 25°C night, 12 h light (~400 μmol m^-2 s^-1 PAR), >50% humidity.
- Layout: seeds sown in a 23 x 10 grid; 2 seeds per genotype, thinned to one plant; four replicates per treatment forming paired 0N/100N boxes within each pair.
- Treatment details:
  - 0N: no added nitrogen.
  - 100N: 16.12 g urea per box to simulate 40 kg N ha^-1 (first split of a typical field application of 120 kg N ha^-1 in three splits).
  - Two-week period before measurements; 100N box replicate 1 removed due to a small liner leak causing environmental differences.
- Substrate: equal-volume soil/sand mix, using Insch soil and builder’s sand.

## Measurements and Harvest
- Measurements started two weeks after sowing; weekly data collection.
- Traits measured weekly: plant height, tiller number, NBI, chlorophyll index (ChI) from Dualex.
- Harvest: six weeks after sowing; shoots dried at 80°C for 48 hours; shoot dry weight recorded.

## Nature and Units of Recorded Values
- Plant height: cm (soil to tip of highest leaf).
- Tillers: count (no units).
- NBI and ChI: unitless.
- Shoot biomass: g (shoot dry weight).

## Quality Control
- Replicate 1 of the 100N treatment excluded from analysis due to experimental anomaly.
- Data checked for unusual observations (via Minitab) and corrected only when errors were identified.

## Data Structure and Files
- Data format: simple spreadsheets with 11 columns.
- Columns (A–K):
  - Replicate (1–4)
  - Treatment (0 = 0N, 100 = 100N)
  - BAAP number (unique BAAP ID as in Norton et al., 2018)
  - BAAP name (cultivar)
  - X (position in X)
  - Y (position in Y)
  - G–K: measured trait data
- Files:
  - BAAP_Screen_Aberdeen_0N.csv: raw 0N data for five traits; includes per-plant measurements and descriptive metadata (means listed in summary descriptions).
  - BAAP_Screen_Aberdeen_100N.csv: raw 100N data for five traits; same structure; note a minor naming inconsistency in the description (Shoot_biomas s) likely a typographical artifact.
- Trait reporting in files includes per-trait description, unit, and mean values for reference.

## Provenance, Funding, and References
- Funding: UK GCRF South Asia Nitrogen Hub; YH supported by Saudi Arabian scholarship; AT by SERB Overseas Visiting Doctoral Fellowship (India).
- Data lineage: BAAP cultivar IDs linked to Norton et al. (2018) genome-wide association study context; dataset referenced for subsequent QTL/candidate gene analyses.

## Governance and Reuse Considerations for Data Stewards
- Interoperability: two separate CSV files with a consistent 11-column structure and shared BAAP identifiers; ensure linking with the BAAP SNP database for integrated analyses.
- Metadata integrity: preserve replicate, treatment, BAAP ID, cultivar name, and coordinate data to enable traceability and reproducibility.
- Data quality: document the excluded replicate in 100N and any future data curation steps; maintain versioning if updates occur.
- Accessibility: provided as raw data; suitable for re-analysis, meta-analysis, and cross-study integration with QTL mapping efforts, subject to standard data governance and any collaboration-specific restrictions.