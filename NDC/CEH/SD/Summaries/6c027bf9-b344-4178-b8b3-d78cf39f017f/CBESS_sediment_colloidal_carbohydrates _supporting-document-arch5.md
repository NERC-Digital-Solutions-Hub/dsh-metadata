# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) surface sediment colloidal carbohydrate concentration in saltmarsh and mudflat habitats

## Overview
- Dataset reports concentration of colloidal carbohydrates in surface sediments, expressed as glucose equivalents (µg g-1).
- Focused on saltmarsh and mudflat habitats, collected during CBESS field campaigns in winter and summer 2013.
- Staff: Jack Maunder.

## Sampling design and locations
- Locations:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
- Habitat contrast:
  - Saltmarsh sites representing two contrasting soil types (clay in Essex; sandy in Morecambe Bay)
  - Mudflat sites with cohesive clays/sediments in Essex and coarser sediments in Morecambe Bay
- Sampling intensity:
  - Five replicates per quadrat, for both mudflat and saltmarsh across winter and summer 2013
  - 22 quadrats per site (1 x 1 m), randomly allocated
  - Four spatial scales (A: 1 quadrat; B: 3 quadrats 1–10 m apart; C: 6 quadrats 10–100 m apart; D: 12 quadrats 100–1000 m apart)
  - Random quadrat allocation and scale configuration implemented in R
- Monitoring plan:
  - Part of the general CBESS field campaign; no repeat sampling planned

## Methods and measurements
- Primary variable: Colloidal carbohydrate concentration (µg g-1, as glucose equivalents)
- Sample collection and processing:
  - Surface sediment collected with contact cores; top 2 mm frozen with liquid nitrogen
  - Freeze-dried; wet weight recorded; water removed
  - Concentration determined using the Dubois phenol-sulphuric assay
  - Sub-sample (50–500 mg) extracted with known volume of distilled water; vortexed and centrifuged; color developed with acid and phenol; absorbance read at 486.5 nm
  - Concentrations calculated from regression standards; reported as µg g-1
  - Zeros indicate concentrations below detectable level
- Quality checks:
  - Spectrophotometer accuracy verified using dilutions of glucose standards
  - Data checked and recorded in spreadsheets; standard lab procedures followed
- Metadata and formats:
  - Location descriptions provide habitat and site context to aid interpretation

## Data structure and formats
- File format: Comma-separated values (.csv)
- Key fields (example):
  - Row Number (sorting anchor)
  - Season (Winter W, Summer S)
  - Location (Essex E, Morecambe M)
  - Site (AH, FW, TM, CS, WS, WP)
  - Habitat (Mudflat MF, Saltmarsh SM)
  - Quadrat Number (1–22)
  - Scale (A–D; spatial scheme)
  - Colloidal Carb (µg g-1) (mean concentration)
  - StDev (standard deviation)
- Data notes:
  - NA indicates missing data due to quadrat inaccessibility
  - Units and naming conventions aligned to facilitate cross-site comparisons

## Data quality, provenance, and governance
- Provenance:
  - Observations tied to CBESS field campaign with clearly documented sites, habitats, and quadrat design
  - Responsible individual listed: Jack Maunder
- Data quality:
  - Multiple replicates per quadrat; calibration and quality-control steps explicitly described
  - Metadata includes sampling season, location, site, habitat, scale, and sample processing details
- Access and reuse:
  - Data stored as CSV with explicit variable definitions and context to enable reuse by data users and other stakeholders
  - No repeat sampling planned, which is relevant for data freshness and update expectations

## Notes for data stewards and users
- The dataset uses standardized units and a transparent lab method (Dubois assay) to enable comparability across sites and times.
- Clear documentation of sampling design (random quadrats, scales) supports reproducibility and meta-analyses.
- QCs and metadata support data quality assessment and governance; ensure ongoing cataloguing and linkage to CBESS portals for discoverability.