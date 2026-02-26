# Data collected for a study looking at the survival of human pathogens bound to microplastics during transfer through the freshwater-marine continuum

## Overview
- Dataset arises from mesocosm experiments to quantify survival of E. coli, Enterococcus faecalis, and Pseudomonas aeruginosa on polyethylene or glass particles.
- Two experiments simulate: (1) direct WWTP plastic release into freshwater or seawater, and (2) downstream transport from WWTP discharge to beach environments.
- 14 CSV files comprise the dataset, with full descriptions provided in section 8.

## Study design and aims
- Goal: assess survival of human pathogens bound to microplastics during transfer through freshwater–marine continuums.
- Data oriented toward standardised outputs for environmental health monitoring (e.g., CFU counts, biofilm measurements).

## Study site and timing
- Location: University of Stirling, Scotland.
- Experiment 1: conducted April–June 2022; field sampling at three Forth Catchment sites (Dunblane, Bridge of Allan, Kirkcaldy) from June 4–6, 2022.
- Experiment 2: conducted in April 2022; samples collected at four Forth Catchment sites (Dunblane, Bridge of Allan, Torryburn, Kirkcaldy) between April 12–16, 2022.

## Data collection details and methods
- Experiment 1:
  - Direct discharge of WWTP effluent into freshwater or seawater in mesocosms.
  - Bacteria prepared, inoculated into WWTP effluent, then introduced to mesocosms with 12 L tanks and 30 cages containing 100 particles each (plastic and glass).
  - Timepoints: 1–27 days; at each timepoint, two cages (one plastic, one glass) sampled per replicate.
  - Measurements: CFU enumeration on selective media after filtration and washing; pond parameters measured (pH, EC, turbidity, salinity, temperature).
- Experiment 2:
  - Simulated downstream transport: cages moved through a sequence of tanks containing river water, estuary water, seawater, and beach sand.
  - Crystal violet staining used to quantify biofilm on plastic and glass surfaces.
  - Bacterial concentrations quantified post-incubation via CFU counts; sand samples processed to remove bacteria.
  - Timepoints synced with mesocosm sampling; additional measurements for water characteristics and biofilm.
- Conditions and controls:
  - Beads: 2 mm polyethylene and glass beads; sterilised cages; negative controls with virgin plastic and glass.
  - Incubation: 15 °C with gentle shaking; sampling performed under sterile conditions.

## Data contents and file structure
- 14 CSV files cover:
  - Background water characteristics for mesocosms (before experiments)
  - Experiment water characteristics (during experiments)
  - Initial bacteria added (per mesocosm)
  - Bacterial counts in water (WaterCFU)
  - Bacterial counts on plastic (PlasticCFU)
  - Bacterial counts on glass (GlassCFU)
  - Background characteristics and CFU data for mesocosm2 (Experiment 2)
  - Crystal violet biofilm measurements for plastic (CrystalViolet_Plastic_Mesocosm2) and glass (CrystalViolet_Glass_Mesocosm2)
  - Sand dry weight measurements (SandDryWeight_Mesocosm2)
- Data columns are described per file, including:
  - Water type, timepoint, replicate, and measurement values (pH, EC, turbidity, salinity, temperature)
  - Species, material (plastic or glass), dilution factors, and CFU counts
  - Biofilm absorbance (Absorbance_550nm) for crystal violet assays
  - Sand weight metrics (before/after drying, difference, percentage change)

## Data quality and completeness
- Data checked for anomalies; no missing data reported.
- Metadata include dilution factors, plate counts, and timepoints to facilitate reproducible analyses.
- Completeness ensures traceability from background conditions through downstream exposure and biofilm formation.

## Responsibilities and provenance
- Data collection and interpretation led by Rebecca Metcalf.
- Data recording aligns with standardised experimental workflows to support observability and auditability.

## Reuse, governance, and accessibility
- Data support environmental monitoring analyses, enabling assessment of pathogen survival and microplastics as a transport vector.
- Related to UKRI/NERC grants: 
  - Microbial hitchhikers of marine plastics: the survival, persistence & ecology of microbial communities in the Plastisphere (NE/S005196/1)
  - NERC-GCRF SPACES project (NE/V005847/1)
- Datasets stored and managed for portal upload and broader accessibility.

## Key notes for analysts monitoring the environment
- The standardized, multi-site mesocosm design provides time-resolved, organism-specific CFU data on microplastics and glass across freshwater to marine transitions.
- Includes both microbiological counts and biofilm indicators, enabling integrated assessments of microbial hitchhiking potential.
- Data are suitable for cross-dataset linkage with other environmental health metrics (e.g., water quality, salinity, turbidity) and for trend analysis over the freshwater–marine continuum.
- Quality assurance steps and detailed file-level documentation facilitate reproducibility and data quality assessments.