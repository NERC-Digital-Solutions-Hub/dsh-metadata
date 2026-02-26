# Lolium and Trifolium solardomes

## Overview
- Investigates the effects of ozone exposure on Lolium perenne and Trifolium repens grown in monocultures and mixtures.
- Plants derived from pasture turf near Edinburgh; randomized by parent origin and treatment.
- Experimental timeline: 12-week exposure with two harvests (6 weeks and 12 weeks).
- Measured physiological responses (photosynthesis), biomass partitioning, and tissue chemistry.

## Experimental design and treatments
- Large pots (drainage holes) with 12 plants each: 4 central plants surrounded by 8 colleagues.
- Four solardomes in a randomized block design; two control domes (ozone-free air) and two ozone-exposed domes.
- Ozone regime:
  - Control: continuous 30 ppb.
  - Ozone: maximum 80–100 ppb on days 1–4, ramping up and down; 30 ppb otherwise.
  - In addition, two domes received an episodic rural ozone profile (O3(30+peaks)).
- Plant configurations:
  - Monocultures of L. perenne and T. repens.
  - A mixed canopy with central T. repens and surrounding L. perenne.
- Maintenance: well-watered via mist system; standard environmental controls in solardomes.

## Harvesting and sample processing
- Harvests on 6 September and 16 October; plants cut to 7 cm.
- Layered harvesting to separate canopy components:
  - Material outside pot, >14 cm above soil, 7–14 cm, and 0–7 cm for final harvest.
  - Species‑level separation (T. repens: stolons, flowers, leaves; L. perenne: leaves and stems only; all >7 cm considered leaves).
- Biomass determination: dried at 65°C (minimum 4 days).
- Subset analyses: C and N content in L. perenne leaf material via CHNS analyzer after grinding.

## Physiological measurements
- Leaf sampling:
  - Leaf 1: newest fully expanded leaf; Leaf 2: second newest.
  - Minimum six leaves per measurement day, same physiological stage.
- Photosynthesis measurements:
  - A-Ci curves: net CO2 assimilation (A) vs substomatal CO2 (Ci) using CIRAS I with 1000 μmol m−2 s−1 PAR; CO2 steps from 0 to 2000 ppm.
  - AQ curves: measured at 1000 ppm CO2 with varying PAR from 0 to 2000 μmol m−2 s−1.
- Derived parameters:
  - Jmax from A-Ci asymptote (Ci > 500 ppm) using Farquhar model and the specified equation.
  - Vcmax estimated from the initial slope of A-Ci (Ci up to 300 ppm).
  - Data processed per plant; mean values per solardome used for analyses.

## Data and variables collected
- ACi data: Lolium_and_Trifolium_solardomes_ACi_Curve_data.csv
  - Columns include Species, Leaf number, Weeks since start, Treatment, dome.pot, Ci (ppm), A corrected for leaf area (μmol m−2 s−1).
- Biomass data: Lolium_and_Trifolium_solardomes_biomass_data.csv
  - Harvest, Species, Monoculture or mixture, Ozone treatment, dry weight (g per pot), standard error.
- Clover distribution: Lolium_and_Trifolium_solardomes_clover_distribution_data.csv
  - Harvest, Monoculture or mixture, part of canopy, Ozone treatment, Dry weight per pot, standard error.
- Lolium distribution: Lolium_and_Trifolium_solardomes_Lolium_distribution_data.csv
  - Harvest, Monoculture or mixture, part of canopy, Ozone treatment, Dry weight per pot, standard error.

## Data processing and analysis
- Relationships and models:
  - A-Ci and AQ curves used to estimate photosynthetic capacity parameters (Jmax, Vcmax).
  - Jmax derived from A-Ci curve asymptotes; Vcmax from initial slope (Ci up to 300 ppm).
- Statistical approaches:
  - One-way ANOVA (Minitab) for Jmax (ozone effect; monoculture vs mixture not compared in this analysis).
  - GLM regression (SPSS) for A vs Ci across treatments.
  - Split-plot and split-split-plot ANOVA (Genstat) with:
    - Main factor: ozone treatment.
    - Subplot: monoculture vs mixture.
    - Sub-subplot: canopy position for biomass partitioning.

## Data governance and stewardship notes
- Data organization:
  - Data are structured by solardome, pot, species, treatment, and harvest/timepoint.
  - Clear naming and separation of datasets for ACi, biomass, and canopy distribution support traceability.
- Metadata and provenance:
  - Experimental origin and location described (pasture samples near Edinburgh; grid ref provided for plant material).
  - Instrumentation and calibration details noted (ozone analyzer Dasibi; ozone generation and LabView control).
  - Measurement conditions documented (PAR, CO2 levels, temperature considerations implicit in design).
- Reproducibility and interoperability:
  - Detailed data structures with explicit column names facilitate reuse and metadata alignment.
  - Data files and processing steps enable reconstruction of Jmax, Vcmax, and related parameters.
- Considerations for data sharing and governance:
  - Ensure versioning and persistent identifiers for CSV files.
  - Include metadata dictionaries and instrument calibration records with any data release.
  - Maintain clear documentation of treatments, canopy configurations, and harvest layers to aid downstream users and data users.

## Key takeaway for data stewards
- The study yields a well-structured, multi-faceted dataset linking ozone exposure to physiological performance and biomass allocation in two pasture species, with explicit data files, measurement protocols, and analysis methods suitable for reproducibility, re-use, and integration with broader datasets on plant responses to air pollutants.