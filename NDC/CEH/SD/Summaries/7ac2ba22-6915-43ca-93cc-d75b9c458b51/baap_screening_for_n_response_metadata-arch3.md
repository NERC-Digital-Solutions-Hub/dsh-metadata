# BAAP_Screen_Aberdeen_0N.csv and BAAP_Screen_Aberdeen_100N.csv

## Overview
- Data collection focused on 229 rice cultivars from the Bengal and Assam Association Panel (BAAP) to assess responses to nitrogen treatment over six weeks.
- Purpose: identify cultivars with high nitrogen use efficiency (NUE) and enable quantitative trait loci (QTL) and candidate gene discovery for NUE.
- Datasets provide raw trait measurements under low (0% N) and high (100% N) nitrogen conditions.

## Experimental context
- Location and timing: School of Biological Sciences, University of Aberdeen; September–October 2020.
- Experimental design: controlled environment room with 28°C day / 25°C night, ~12 h light, ~400 μmol m^-2 s^-1 PAR, and humidity >50%.
- Plant material: 229 BAAP cultivars (genotypes) with an associated 2 million SNP marker dataset; portion of broader BAAP panel described in Norton et al. (2018).
- Growth medium and setup: equal-volume soil/sand mix (Insch soil and builder's sand); boxes 160 cm × 70 cm × 27 cm; ~600 kg soil/sand per box.
- Nitrogen treatments: 0% N (no added nutrients) and 100% N (16.12 g urea per box, representing ~40 kg N ha^-1 in a typical field application); initial moisture, then flooding after two weeks.
- Layout and replication: seeds sown on a 23 × 10 grid with two seeds per genotype, thinned to one plant; four replicates per treatment arranged as paired 0% N and 100% N boxes. One replicate of the 100% N treatment was excluded due to a leak.

## Measured traits and methods
- Traits measured (six weeks): plant height (cm), tiller number (count per plant), nitrogen balance index (NBI), chlorophyll content (Chl) via Dualex; shoot dry biomass (g).
- Measurement schedule: weekly measurements for height, tiller number, NBI, and Chl.
- Harvest: shoots dried at 80°C for 48 hours for dry weight.

## Data structure and contents
- Data format: simple spreadsheets with 11 columns (A–K).
- Key columns:
  - Replicate, Treatment (0 = 0% N, 100 = 100% N)
  - BAAP number (unique BAAP ID) and BAAP name
  - X and Y coordinates for plant position within the experimental box
  - Measured trait data (G–K)
- Files and contents:
  - BAAP_Screen_Aberdeen_0N.csv: raw data for the 0% N treatment across five traits (Plant_height, Tiller_number, NBI, Chl, Shoot_biomass)
  - BAAP_Screen_Aberdeen_100N.csv: raw data for the 100% N treatment across the same five traits
- Data units and descriptions:
  - Plant_height: cm
  - Tiller_number: count (no unit)
  - NBI and Chl: unitless indices
  - Shoot_biomass: g (dry weight)
- References and linkage: BAAP IDs reference Norton et al. (2018) BAAP panel; dataset includes SNPol markers context.

## Quality control and data processing
- Data quality: replication 1 of the 100N treatment excluded due to environmental variance (leak).
- Data checks: initial data entry checked with Minitab for outliers/unusual observations; corrections made only for confirmed data-entry errors.

## Metadata, data governance, and accessibility
- Data are provided as raw CSVs with explicit metadata in the descriptions (treatment, BAAP IDs, coordinates, trait definitions).
- Data structure supports traceability back to individual plants and genotypes, enabling reproducibility and integration with SNP datasets for downstream analyses (e.g., NUE/QTL studies).

## Funding and references
- Funding: UK-funded GCRF project “South Asia Nitrogen Hub”; YH scholarship (Royal Embassy of Saudi Arabia); AT SERB Overseas Visiting Doctoral Fellowship (Government of India).
- Reference: Norton GJ, et al. (2018) Genome-wide association mapping of grain and straw biomass traits in the rice BAAP grown under different irrigation regimes. Frontiers in Plant Science.