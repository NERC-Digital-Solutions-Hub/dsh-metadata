# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) macrofaunal abundance in mudflat and saltmarsh habitats.

## Overview
- A CBESS dataset documenting macrofaunal abundance (individuals per m²) across mudflat and saltmarsh habitats.
- Aimed at enabling consistent environmental health assessment and policy performance monitoring over time through standardized outputs.

## Study design and scope
- Field campaign: winter and summer 2013.
- Sites: 6 sites across 2 locations (Essex and Morecambe Bay).
- Habitats: two per site (mudflat and saltmarsh).
- Replication and sampling: 3 replicates per quadrat across 22 quadrats, measured at 4 spatial scales.
- Output: abundance data for numerous macrofaunal taxa, suitable for comparisons across space and time.

## Locations and habitats
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS).
- Saltmarsh contrast: Essex (clay soils) vs Morecambe Bay (sandy soils); differences in inundation, creek structure, and vegetation.
- Mudflat contrasts: Essex with cohesive clays, mud, silt vs Morecambe with coarse, mobile sediments.

## Data collection methods
- Core sampling: three sediment cores per quadrat (10 cm depth, 10 cm diameter).
- Preservation: cores fixed in 4% buffered formalin in seawater; sieved through 0.5 mm mesh; residues preserved in 70% IMS.
- Identification: species-level (or appropriate taxon) identification using stereo microscope; damaged specimens categorized or excluded from species counts.
- Abundance calculation: counts converted to per m² using a factor of 127.323955 and rounded to the nearest whole number.
- Quality checks: data input by two people with double checks; cross-validated against CBESS_macrofauna_biomass.csv; species names validated against World Register of Marine Species (WoRMS).

## Variables and data structure
- Primary variable: species abundance (number of individuals) per m².
- Key metadata fields (example): Season (Winter W, Summer S), Location (Morecambe M, Essex E), Site (e.g., CS, WS, AH, FW, TM), Habitat (Mudflat MF, Saltmarsh SM), Quadrat Number (1–22), Scale (A: 1 m, B: 1–10 m, C: 10–100 m, D: 100–upper limit), Replicate (C/D coding for spatial subsampling), Measurement Type (Macrofauna, Maf).
- Taxa listed for abundance (examples include Arenicola marina, Ampharete lindstroemi, Capitella sp., Hediste diversicolor, Mya arenaria, Cerastoderma edule, Crangon crangon, various crustaceans, molluscs, and debris categories for major groups).
- Debris and miscellaneous presence/absence fields accompany taxa (e.g., Annelid debris, Crustacea debris, Mollusc debris, etc.).

## Data quality and management
- Procedures include: duplicate data entry, cross-checks with biomass dataset, taxonomic verification, and standardized field formats.
- File formats: CSV for primary data.
- Data management practice: data prepared for submission to appropriate portals; linkage to biomass data enhances interpretability and comparability.

## Accessibility and integration
- Data designed to be combined with other data sources for broader insights (as per monitoring challenges).
- Underlying data are stored and made accessible via standard portals; dataset cross-links to CBESS macrofauna biomass data for integrated analyses.

## Practical implications for analysts
- Provides standardized, site-comparative macrofaunal abundance data across habitat types and seasons, enabling temporal trend analysis and policy performance evaluation.
- Facilitates cross-site and cross-habitat comparisons, with explicit site descriptors, habitat types, and sampling scales.
- Supports data fusion with biomass and other CBESS datasets to enhance ecosystem health assessments and service sustainability analyses.