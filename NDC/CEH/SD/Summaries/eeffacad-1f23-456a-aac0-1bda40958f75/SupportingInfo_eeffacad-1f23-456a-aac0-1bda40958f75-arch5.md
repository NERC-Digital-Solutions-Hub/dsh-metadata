# Supporting information for: Chemical and physical data of water and its evolution over incubation experiments for three headwater streams in the Conwy catchment, North Wales (2014)

## Scope and purpose
- Provides supporting information for a dataset describing chemical and physical data of stream water during incubation experiments on three headwater streams in the Conwy catchment (North Wales, 2014) as part of the Turf2Surf project.
- Documents treatments applied (varying light exposure, sterilization, nutrient enrichment) and measured parameters to understand water chemistry evolution under incubation.

## Study sites and timeline
- Sampling locations:
  - Nant y Brwyn (NyB) – peat catchment
  - Glasgwm (Glg) – forested catchment
  - Hiraethlyn (Hir) – improved grassland catchment
- Coordinates provided for each site.
- Field sampling in 2014 on:
  - NyB: May 22 and August 1
  - Glg: June 27 and September 25
  - Hir: June 13 and September 2
- Laboratory work:
  - Incubations at Environmental Centre of Wales (ECW) laboratory, Bangor
  - Experimental setup in Sun Test Box CPS+ for light control
  - Analyses conducted at the Centre for Ecology and Hydrology (CEH) laboratory in ECW

## Experimental design and procedures
- Field sample collection:
  - In-stream sampling using a 5 L bottle; additional 500 mL glass bottles for pH and alkalinity
  - Samples transported to ECW for 6-day incubations
- Treatments during incubation (5-day run):
  - Light vs dark exposure
  - HgCl2 poisoning in some light-exposed samples
  - Nutrient enrichment with nitrogen (as nitrate) and phosphorus (as phosphate)
- Incubation setup:
  - 12–16 subsamples per run, with 3–4 treatments replicated 4–3 times
  - 300 mL water per subsample placed in amber bottles
  - Circulation between a cooling bath and vessels in the Sun Box; dark runs covered
  - Box phases: six phases of 999 minutes at 765 W/m2
- Sample coding and day structure:
  - Subsamples codified by station (NyB, Glg, Hir), run (r1–r3), and amber bottle (b01–b16)
  - Day-specific sampling coded with d0 (initial) and d5 (end); day-by-day subsamples encoded with d0–d5

## Measured parameters and analytical methods
- Chemical and physical measurements:
  - Major ions and conductivities via Ion Chromatography (Dionex DX-120)
  - Cations (Ionpac CS12A) and anions (Ionpac AS4A-SC) with specific eluents
  - Carbon and nitrogen contents:
    - Organic carbon (OC), inorganic carbon (IC), total carbon (TC), non-purgeable organic carbon (NPOC), total nitrogen (TN), and total inorganic carbon (TIC) using a Thermalox TC/TN Analyser
  - pH and alkalinity by titration (0.02 N H2SO4)
  - Conductivity (µS/cm)
  - Absorbance from 200–700 nm; derived indices (E2E3, E4E6, humification index)
  - Particulate Organic Carbon (POC) via mass loss on combustion of filtered samples
- Units and formats:
  - Concentrations in mg/L or µg/L as appropriate
  - Conductivity in µS/cm; pH units; alkalinity in µeq/L
  - Absorbance in 1/m; specific indices as ratios
- Quality controls:
  - Instrument calibration with relevant value ranges prior to analyses
  - Use of control standards and blanks at regular intervals
  - Replicate measurements and evaluation of coefficient of variation (CV)
  - Analyses with high CV repeated; only validated values reported
  - CEH Bangor adheres to Aquacheck International Testing scheme for laboratory reliability
- Storage and handling:
  - If storage required, samples kept dark at <5°C

## Data structure and column definitions
- Primary data structure:
  - Sample descriptor: site abbreviation + run number + sample ID
  - date_of_sampling: date of initial stream sampling (d0)
  - sampled_stream: NyB, Glg, or Hir
  - Treatment: 8 possible combinations of light/dark with optional HgCl2 poisoning and/or nutrient additions (+N, +P, or +N+P)
  - EC_d0, pH_d0, Alk_d0, TC_d0, DOC_d0, Abs254_d0, E2E3_d0, E4E6_d0, TN_d0, Cl_d0, Br_d0, N-NO3_d0, P-PO4_d0, SO4_d0, Li_d0, Na_d0, NH4_d0, K_d0, Mg_d0, Ca_d0, POC_d0
  - Day 1–5 measurements (e.g., Irr_d1, TC_d1, DOC_d1, Abs254_d1, E2E3_d1, E4E6_d1, …, POC_d1; similarly for d2–d5)
  - Day 5 measurements include EC_d5, pH_d5, Alk_d5, TC_d5, DOC_d5, Abs254_d5, E2E3_d5, E4E6_d5, TN_d5, Cl_d5, Br_d5, N-NO3_d5, P-PO4_d5, SO4_d5, Li_d5, Na_d5, NH4_d5, K_d5, Mg_d5, Ca_d5, POC_d5
- Example of coding:
  - Sample codes combine station (NyB, Glg, Hir), run (r1–r3), bottle (b01–b16)
  - Day-specific suffixes d0 for initial, d5 for end, and d1–d4 for intermediate days

## Data quality, provenance, and governance
- Provenance and personnel:
  - Field sampling and incubations conducted by Ophelie Fovet (INRA, France)
  - Coordination by Chris Evans (CEH Bangor, UK)
- Data validation and reliability:
  - Detailed QA/QC steps described (calibration, blanks, standards, replicate analyses)
  - Only validated data reported; re-analysis performed if CV exceeded acceptable thresholds
  - Documentation notes reliability under the Aquacheck scheme and data center practices
- Licensing and access:
  - Data accessibility and licensing information available at the provided DOI
  - Data hosted in the NERC Environmental Information Data Centre; supporting information accompanies the dataset

## Access, licensing, and reuse
- Licensing and use limitations described at: https://doi.org/10.5285/eeffacad-1f23-456a-aac0-1bda40958f75
- Data repository: NERC Environmental Information Data Centre
- Citations and metadata accompany the dataset for proper attribution and reuse

## Notes on data stewardship implications
- Comprehensive metadata and explicit data structure facilitate discoverability, interoperability, and reuse by users with diverse data needs.
- Clear documentation of sampling methods, treatments, instruments, units, and QA enhances data governance and trust.
- The dataset exemplifies robust data management practices: traceable provenance, standardized coding, rigorous QA, and explicit licensing.