# 1/ Collection/generation methods

- Summary of data: Two CSV data sheets capturing trait measurements for 229 rice BAAP cultivars grown for 6 weeks under two nitrogen treatments (0N and 100N). Traits recorded per plant include plant height, number of tillers, nitrogen balance index (NBI), chlorophyll content (ChI), and shoot biomass.
- Purpose: Evaluate rice cultivars’ responses to nitrogen treatment to identify high nitrogen use efficiency (NUE) candidates and to support quantitative trait loci (QTL) and candidate gene identification for NUE.

## Experimental context

- Location and timing: School of Biological Sciences, University of Aberdeen, Aberdeen, UK; September–October 2020.
- Materials: 229 BAAP cultivars (Bengal and Assam Aus Panel); soil mix of equal volumes Insch soil and builder’s sand.
- Experimental setup: 
  - Containers: Boxes of internal dimensions 160 cm (L) × 70 cm (W) × 27 cm (H) containing 600 kg soil/sand mix.
  - Treatments: 0% N (no added nitrogen) and 100% N (16.12 g urea per box; ~40 kg N ha^-1 first split; first two weeks aerobic, then flooded).
  - Plant layout: 23 × 10 grid per box, two seeds per genotype thinned to one plant; 230 genotypes per box; four replicates per treatment paired as 0N/100N; replicate 1 of 100N excluded due to a leak.
  - Environment: Controlled room with 28°C day/25°C night, 12 h light (≈400 μmol m^-2 s^-1 PAR), humidity >50%.
- Measurements and harvest: 
  - Weekly measurements starting week 2 for plant height, tiller number, and Dualex-based NBI and chlorophyll index (ChI) on the youngest fully expanded leaf.
  - Harvest at 6 weeks; shoot dry weight determined after drying at 80°C for 48 h.

## Data collected and units

- Plant height: centimeters (cm) from soil to tip of the tallest leaf.
- Tillers: count per plant (no units).
- Nitrogen Balance Index (NBI) and Chlorophyll Index (ChI): no units (from Dualex).
- Shoot biomass: grams (g) of the above-ground part after drying.

## Quality control

- Replicate 1 of the 100N treatment discarded for analysis due to environmental discrepancy (leak).
- Data entry quality checks performed with Minitab to flag unusual observations; corrections only applied for identified data-entry errors.

## Data structure and content

- Format: Simple spreadsheets with 11 columns.
- Columns:
  - Replicate (1–4)
  - Treatment (0 = 0N, 100 = 100N)
  - BAAP number (unique ID as in Norton et al., 2018)
  - BAAP name (cultivar name)
  - X (relative position in X)
  - Y (relative position in Y)
  - G–K: measured trait data (Plant_height, Tillers, NBI, Chl, Shoot_biomass)
- Data files:
  - BAAP_Screen_Aberdeen_0N.csv: raw data for 0N treatment across five traits.
  - BAAP_Screen_Aberdeen_100N.csv: raw data for 100N treatment across five traits.
- Trait summaries provided in the files include means for each trait (e.g., Plant_height mean ~74.1 cm for 0N; NBI mean ~17.0; Chl mean ~12.2; Shoot_biomass mean ~0.70 g).
- Columns also include a BAAP ID and cultivar name to link phenotypes to genetic material.

## Context and references

- Genetic material: BAAP (Bengal and Assam Aus Panel) with an associated 2 million SNP marker database; described in Norton et al., 2018.
- Use case: Data can support analyses for NUE and related traits, and be integrated with SNP data for GWAS or candidate gene studies.

## Funding and acknowledgments

- Funding acknowledged from the UK GCRF project South Asia Nitrogen Hub.
- YH supported by a Royal Embassy of Saudi Arabia scholarship; AT by SERB Overseas Visiting Doctoral Fellowship (Government of India).