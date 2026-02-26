# Details of data structure to HF_NW_herbage_quality.csv

- This document is a supplement describing the data structure for HF_NW_herbage_quality.csv, a dataset derived from the 2016 grassland fertiliser trials at Henfaes Research Station (Bangor University) and North Wyke Research Station (Rothamsted Research). The dataset contains 13 columns and 96 rows.

- Data provenance and sampling
  - Sites: HF = Henfaes; NW = North Wyke.
  - Trials: grassland fertiliser trial conducted in 2016.
  - Lab processing: Henfaes samples were pre-dried and sent to Sciantec Analytical (Stockbridge Technology Centre, UK); North Wyke samples were processed from fresh material and sent to Trouw Nutrition GB (Blenheim House, UK).
  - Analytical methods: dry matter, acid-detergent fibre (ADF), ash, crude protein, metabolisable energy (ME), and neutral detergent fibre (NDF) measured using near-infrared spectrometry.
  - Digestibility metric: D = ME/0.16.
  - Units: all measurements expressed as g kg-1 on a dry weight basis, except where noted for ME (MJ kg-1) and D (percent).

- Dataset scope and layout
  - Columns: 13 total; 96 rows.
  - Data origin: grassland plots harvested in 2016 as part of a fertiliser trial.
  - Plot structure: Plots arranged in blocks; Plot numbers 1–16; each plot measures 2 × 6 m.

- Column headers and definitions (with units)
  - Date: Date of grass cut
  - Site: HF | NW (location of trial; HF = Henfaes, NW = North Wyke)
  - N_app: 1 | 2 | 3 (fertiliser application number; 1st & 2nd applications at 90 kg ha-1, 3rd application at 60 kg ha-1)
  - Block: 1 | 2 | 3 | 4 (randomised block design)
  - Plot: 1 – 16 (plot harvested within the block; each plot size 2 × 6 m)
  - Treatment: AN | U | IU | C (N fertiliser type; AN = ammonium nitrate, U = urea, IU = inhibited urea, C = 0 N control)
  - Dry_matter: g kg-1
  - ADF: g kg-1 (acid detergent fibre; measure of lignin, cellulose and lignified N)
  - Ash: g kg-1 (total mineral content)
  - Crude_Protein: g kg-1 (protein content)
  - ME: MJ kg-1 (metabolisable energy)
  - NDF: MJ kg-1 (neutral detergent fibre)
  - D: % (digestibility)

- Relevance for environmental monitoring
  - Provides a standardized, traceable dataset of herbage quality linked to specific fertiliser treatments and plot design, suitable for longitudinal environmental health and policy performance evaluations.
  - Data are designed for verification, quality assurance, and comparison across sites and time, aligning with standardised monitoring practices and enabling broader data integration.