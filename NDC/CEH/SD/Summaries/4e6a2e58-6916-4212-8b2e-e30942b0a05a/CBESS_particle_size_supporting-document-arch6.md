# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) sediment particle size in mudflat and saltmarsh habitats.

## Overview
- Dataset documenting sediment particle size across mudflat and saltmarsh habitats as part of CBESS.
- Collected from 6 sites over 2 locations (Essex and Morecambe Bay), across 2 habitat types per site.
- Winter and summer 2013 sampling with 3 replicates across 22 quadrats at 4 spatial scales.
- Data prepared for analysis via particle size distributions and related statistics.

## Study design and locations
- Locations:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS)
- Habitat types per location:
  - Saltmarsh and Mudflat (with contrasting soil/sediment types between locations)
- Sampling framework:
  - 3 replicates per combination
  - 22 quadrats total
  - 4 spatial scales (A, B, C, D) representing increasing area coverage
  - Seasons: Winter (W) and Summer (S) 2013

## Data collected and processing
- Measured variable: sediment particle size (PSD) distributions
- Field procedures:
  - Mudflats: surface sediment scrapes
  - Saltmarsh: sediment cut from 2 cm below surface
- Sample handling: all samples frozen at -20°C
- Laboratory analysis: Malvern Mastersizer PSD protocol
- Data coverage:
  - 6 sites × 2 habitats × 2 seasons × 3 reps
- Documentation and references:
  - Calibration/PSD methods linked to external resources
  - Primary reference including Gradistat concepts and related literature

## Dataset structure and key fields
- Data file format: .csv
- Core fields (examples):
  - Row Number: sort order
  - Season: Winter (W) or Summer (S)
  - Location: Morecambe (M) or Essex (E)
  - Site: Morecambe (CS, WS, WP) or Essex (AH, FW)
  - Habitat: Mudflat (MF) or Saltmarsh (SM)
  - Quadrat Number: 1–22
  - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100–upper limit)
  - Replicate: 1–3
  - Measurement Type: PSA (Particle Size Analysis)
  - PSD metrics: d(0.050), d(0.160), d(0.5), d(0.840), d(0.950), D[4,3], inclusive mean (Phi and µm), inclusive kurtosis, skewness, standard deviation, various clay/silt fractions, and size-class percentiles
- Dataset field descriptions provide detailed codings for each variable (locations, sites, habitats, scales, and PSD-derived statistics)

## Quality assurance and provenance
- Data quality references:
  - Procedures and calibration details available via linked external resources
  - Data checking procedures documented in references
- Provenance:
  - Staff: Christina Wood and Martin Solan
  - Data contribution and methodology align with CBESS field campaigns
- Data lineage:
  - Based on established PSD methodology and prior works (e.g., Gradistat, Blott & Pye references)

## Access, formats, and reuse
- Primary format: CSV dataset with accompanying field descriptions
- Reuse potential:
  - Build self-serve insights via dashboards showing PSD across sites/habitats/seasons
  - Compare sediment size distributions between Essex and Morecambe Bay saltmarshes
  - Integrate with biodiversity and ecosystem service indicators to explore habitat relationships
- Documentation provides guidance for interpretation and the equations used for derived metrics (e.g., D[4,3], Phi scales)

## Usage notes and considerations
- Spatial and temporal scope: 2013 winter and summer, with no planned repeat sampling noted
- Variability considerations:
  - Two locations with contrasting sediment/types; two habitat types per site
  - Four spatial scales increase analytical flexibility but require careful aggregation
- Potential caveats:
  - High-dimensional PSD data require appropriate summarization (e.g., select key percentiles or clay fractions for dashboards)
  - Data checks rely on external method references; users should consult linked resources for calibration and processing details

## Roles, contact, and further information
- Staff responsible: Christina Wood and Martin Solan
- Full methodological details and external references available in the dataset documentation
- Suitable for researchers and analysts seeking to compare sediment size characteristics across coastal habitats and management contexts within the CBESS framework