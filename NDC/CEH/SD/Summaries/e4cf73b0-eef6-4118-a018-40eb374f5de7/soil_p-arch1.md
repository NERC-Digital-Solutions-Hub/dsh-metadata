# Soil survey of Moor House, 1965.

## Overview
- Dataset from a soil survey at Moor House, Cumbria, UK, conducted by Mike Hornung as part of his PhD.
- The PhD thesis is available in the supporting documentation and online; the survey database is described in Cuthbertson (1993).

## Data files and structure
- D2SOIL_P.csv — Site Locations
  - PROF_NO: unique profile number (primary key)
  - EASTING, NORTHING: coordinates
  - LOCATION, REL_DATA, ALTITUDE: location description, relief data, altitude (m)
  - GEO_DATA, VEG_DATA: references to geological data and vegetation
- D3SOIL_P.csv — Horizon analysis
  - PROF_NO: links to D2SOIL_P
  - HORIZON: horizon code (as defined in Hornung thesis)
  - FDEPTH, TDEPTH: start and end depths of horizons (cm)
  - REM1, REM2: remarks
  - TYPE: ORGANIC or MINERAL horizon type
- D4SOIL_P.csv — Chemical analysis and soil mineralogy
  - PROF_NO, SMPL_NO: profile and sample identifiers
  - FDEPTH, TDEPTH: sample depth interval (cm)
  - PH, CAC03 (CaCO3), FE203, US_SAND, I_SAND, I_SILT, CLAY, US_SILT, BS, and numerous extractable and elemental measures
  - CEC, SAT, LOI, P2O5, C, N, C_N, SI, AL, FE, MG, CA, NA, K, TI, MN, H2O, P
  - Each variable appears with two sets (1 and 2), indicating duplicate measurements or alternative methods; SAT is marked as not in use

## Linking between datasets
- PROF_NO serves as the key linking D2 (site), D3 (horizon), and D4 (chemistry) data
- D3 horizons correspond to depth ranges within each PROF_NO and relate to the profile information from D2
- D4 uses PROF_NO and SMPL_NO to tie chemical results to specific samples within profiles

## Key variables and interpretation
- Location metadata: coordinates, altitude, location descriptions, vegetation
- Horizon data: horizon code, depth range, horizon type (organic/mineral), and remarks
- Chemical and mineralogical data: soil pH, carbonate content, major elements, texture (US_SAND, I_SAND, US_SILT, I_SILT, CLAY), base saturation (BS), extractable cations (Ca, Mg, Na, K), organic matter indicators (LOI), nutrients (P2O5, P), carbon (C), nitrogen (N), carbon-to-nitrogen ratio (C_N), silica (SI), aluminum (AL), iron (FE), cation exchange capacity (CEC), and soil water content (H2O)
- Replication/duplicate measurements: suffixes 1 and 2 indicate paired measurements for many fields

## Potential analyses and questions
- How horizon type (organic vs mineral) relates to pH, CEC, base saturation, or organic matter indicators
- Depth profiles: how chemical properties vary across FDEPTH–TDEPTH within horizons
- Texture–chemistry relationships: links between particle-size fractions (SAND/SILT/CLAY) and CEC, LOI, or nutrient contents
- Spatial patterns when integrating with coordinates (elevation/altitude vs soil chemistry)
- Predictive modeling: estimate pH, CEC, or fertility indicators from depth and site attributes

## Data quality considerations and limitations
- Date: 1965; measurement methods may differ from modern standards
- Units: ensure consistent interpretation across fields; dual 1/2 columns require explicit handling
- Completeness: some records may be sparse; horizon coding relies on the Hornung thesis
- Local scale: data are site-specific to Moor House; caution when generalizing beyond the site

## Processing and best practices
- Harmonize units and resolve the 1/2 replication columns (decide on using full data or a chosen replicate)
- Merge D2, D3, D4 on PROF_NO; align horizon depth definitions with depth intervals
- Standardize coordinate data as needed for spatial analyses
- Maintain provenance: document data sources, replication scheme, and any transformations
- Consider publishing derived, cleaned datasets with metadata to enhance discoverability

## Practical takeaways
- Rich, multi-dimensional soil dataset enabling horizon-level chemistry and mineralogy analyses tied to site attributes
- Suitable for exploring soil formation processes, fertility indicators, and depth-related changes within a historical UK soil context