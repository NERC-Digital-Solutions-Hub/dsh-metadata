# 1/ Collection/generation methods

- Purpose and scope
  - Two CSV sheets (0N and 100N) documenting trait values for 229 BAAP rice cultivars grown for 6 weeks under two nitrogen levels.
  - Traits recorded: plant height (cm), tiller number, nitrogen balance index (NBI), chlorophyll content (ChI), and shoot biomass (g).
  - Goal: assess nitrogen-use response and identify NUE-associated QTLs and candidate genes.

- Experimental design and layout
  - Genetic material: Bengal and Assam Association Panel (BAAP) with ~2 million SNP markers.
  - Environment: controlled room with 28°C day / 25°C night, 12 h light (~400 μmol m^-2 s^-1 PAR), humidity >50%.
  - Growth setup: equal-volume soil mix of Insch soil and builder’s sand; boxes sized 160 cm × 70 cm × 27 cm; each box holds 600 kg of soil/sand mix.
  - Planting: seeds sown in a 23 × 10 grid (7 cm spacing); two seeds per genotype per box, thinned to one plant; 230 genotypes per replicate.
  - Replication and pairing: four replicates per treatment; within each box, 0%N and 100%N boxes paired; one 100N replicate (replicate 1) excluded due to a leak.

- Treatments
  - 0% N (0N): no added nitrogen.
  - 100% N (100N): 16.12 g urea per box to simulate ~40 kg N ha^-1; soil flooded to ~5 cm after two weeks.

- Measurements and harvest
  - Begin two weeks after sowing: weekly measurements of plant height and tiller number; weekly measurements of NBI and chlorophyll content (Dualex) for youngest fully expanded leaf.
  - Harvest at six weeks: shoot dry weight after drying at 80°C for 48 hours.

- Data structure and units
  - Data files contain 11 columns per record:
    - A: Replicate (1–4)
    - B: Treatment (0 = 0N, 100 = 100N)
    - C: BAAP number (unique ID)
    - D: BAAP name (cultivar)
    - E: X (relative position in X)
    - F: Y (relative position in Y)
    - G–K: measured trait data
  - Units:
    - Plant height: cm
    - Tillers: count (no units)
    - NBI, ChI: no units
    - Shoot biomass: g

- Quality control
  - Replicate 1 of the 100N treatment removed due to environmental inconsistency (leak).
  - Data checked with Minitab for unusual observations; corrections only for data-entry errors.

- Files and data content
  - BAAP_Screen_Aberdeen_0N.csv: raw data for 0N with five traits; per-plant records include replicate, treatment, BAAP ID, cultivar name, X, Y.
  - BAAP_Screen_Aberdeen_100N.csv: raw data for 100N with five traits; same structure as 0N.
  - Both files include column headers and per-plant trait values; means summarized in the file descriptions.

- Context and references
  - The BAAP panel is described in Norton et al. (2018) with extensive SNP marker data.
  - Funding acknowledgment: GCRF project South Asia Nitrogen Hub; additional support for YH and AT.

- GIS-relevance and integration notes
  - Each record includes explicit X, Y coordinates within box-level layout, enabling geospatial visualization of trait variation across the planting grid.
  - Data can be joined with BAAP genotype information (SNP markers) for spatial-genotype–phenotype analyses.
  - Suitable as a map-based data product to explore spatial patterns of nitrogen response across cultivars in a controlled layout.