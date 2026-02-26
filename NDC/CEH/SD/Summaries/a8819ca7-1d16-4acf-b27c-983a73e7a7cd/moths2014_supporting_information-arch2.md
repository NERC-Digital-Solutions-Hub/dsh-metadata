# Moth counts on chalk grassland and surrounding arable fields with agri-environment schemes in Hampshire, 2014

## Overview
- Landscape-scale study (2014) in north-west Hampshire, UK, examining interaction between agri-environment schemes (AES) and long-standing chalk grassland (CG) habitat adjacent to arable fields.
- Four landscapes near a large CG patch within or near an SSSI, with >50% surrounding arable land within ~3 km.
- Surveys targeted macro-moths using light traps across 18 locations per landscape (totaling 72 locations), including 2 CG sites and 16 arable-field locations (margins and centres).
- Data capture includes dates, locations, AES management, habitat connectivity, and counts for 180 macro-moth species.
- Aim aligned with demonstrating environmental health and informing AES outcomes for moths, using standardized monitoring data.

## Study design and scope
- Four study landscapes (a–d) adjacent to CG habitat; CG patch visible in all landscapes.
- AES interventions studied: 
  - 6 m wide grassland margins (6m buffer strips; NE 2012; AES type EE3) 
  - Nectar flower mixes (EF4) within margins.
- Layout within landscapes: 18 trap locations per landscape; 2 on CG habitat; 16 on arable fields (across margins and centres of field pairs, with gradient of CG connectivity).
- For arable fields, each pair includes a treatment margin (AES present) and a control margin (AES absent). On CG habitat, margins are not distinguished.
- Survey period: six consecutive good-weather nights per landscape between June 2 and July 22, 2014.
- Sampling: ten light traps deployed each night (one per survey location across landscapes); traps on CG surveyed twice per night; arable field margins alternated between margin and centre positions across nights.

## Data collected and structure
- Data include:
  - date of trapping night (YYYYMMDD)
  - landscape code (three-letter): STO (Stockbridge Down), BUR (Burghclere Beacon), BRO (Broughton Down), DAN (Danebury Hill)
  - field code: five-character field identifier combining landscape code, field number (1–5), and margin type (A = AES intervention margin; B = control margin; or for CG, A/B identify sections)
  - location code: field-specific location (0 = 45 m from boundary; 1 = 5 m from boundary; CG locations use A/B as sections)
  - OS_x, OS_y: Easting/Northing coordinates (GPS-derived, <10 m accuracy)
  - management: habitat type or AES status (chgr, aesi1, ctrl1, aesi0, ctrl0)
  - connect_CG: connectivity to chalk grassland (relative index; derived measure)
  - species: scientific name of each macro-moth recorded
  - specialism: habitat classification per species (cgr = CG-associated; gra = grassland-associated; oth = other)
  - count: number of individuals per species per trap per night
- Connectivity calculation:
  - Uses 100×100 m raster of CG habitat coverage to compute C_i for each cell i via a negative exponential kernel.
  - Formula approximated as C_i ∝ Σ_j A_j e^{-α d_ij}, with α = 2 (implying mean dispersal ~1 km).
  - Connectivity values log2-transformed and centered on the landscape mean for analysis.

## Methods
- Collection methods:
  - Macro-moth sampling with ten Heath-style actinic light traps (15 W) per night; traps solar-activated at sunset and sunrise.
  - Good weather criteria: minimum temperature > 10°C, wind < 20 km/h, low precipitation risk.
  - Identification on-site or via photographs (Waring & Townsend 2009); recapture minimized by moving traps ~50 m on subsequent visits.
  - Trap locations mapped with GPS; equipment and logistics described (batteries, stands, transport).
- Species classification:
  - Specialism assignment using Waring & Townsend (2009): CG species, grassland species, and other.
- Data handling:
  - Fieldwork notes and data coded to facilitate cross-landscape comparison and connectivity analyses.

## Data processing and analysis
- Spatial analysis:
  - CG habitat coverage derived from HBIC/Natural England data; rasterization and GIS processing performed in ArcMap 10.1.
  - Connectivity metrics extracted for each survey location and incorporated into subsequent analyses.
- Data transformation:
  - Connectivity values log2-transformed and centered prior to modelling.
- Software:
  - ArcMap 10.1 (GIS) and R 3.0.3 (statistical analysis).
- Quality control:
  - Macro-moth records cross-checked by a local moth recorder.
  - Three singleton records flagged as likely misidentifications (Apamea анцепs, Ceramica pisi, Photedes fluxa) but retained due to uncertainty and rarity.

## Quality control and data integrity
- Independent verification by local expert confirms general accuracy of identifications.
- Flagged uncertain records preserved to maintain dataset completeness and transparency.
- Qualitative notes indicate data are suitable for robust analysis of AES effects on macro-moths and their habitat connectivity.

## Data availability and reuse
- Data and supporting materials published with DOI references:
  - Main dataset: Moth counts on chalk grassland and surrounding arable fields with agri-environment schemes in Hampshire, 2014
  - Supporting information: Detailed methods and data (e.g., analysis protocols)
- Data are structured for reuse in environmental monitoring and landscape-scale biodiversity assessments.
- References include foundational work on metapopulation dynamics, moth survey methodology, and AES-related ecological studies.

## Practical implications for environmental monitoring
- Demonstrates a standardized, replicable approach to monitoring moth responses to AES in a landscape context.
- Integrates habitat connectivity and management interventions to assess outcomes beyond local site scales.
- Provides a rich, interoperable dataset suitable for meta-analyses and data integration with other monitoring efforts.
- Addresses key challenges for analysts monitoring the environment:
  - Increasing the value of datasets through integration with additional relevant data.
  - Facilitating access to underlying data to enable broader scrutiny and reuse.