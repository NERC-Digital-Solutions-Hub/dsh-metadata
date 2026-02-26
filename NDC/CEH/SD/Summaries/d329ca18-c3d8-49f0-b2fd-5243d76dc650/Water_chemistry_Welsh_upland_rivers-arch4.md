# Water chemistry of Welsh upland rivers

## Overview
- Dataset of stream water chemistry from Welsh upland rivers across 61 catchments (41 WAWS sites; 20 Wye catchment sites).
- Measured variables include pH, alkalinity, conductivity, and major cations/anions (with WAWS providing a more detailed major-ion suite; Wye providing pH, alkalinity, conductivity and major anions).
- Sampling aims to characterize chemical variation along ecological gradients related to biodiversity, land-use, and acidification recovery.
- collection periods: Wye in May 2012; WAWS across summer/autumn 2012 and spring/summer 2013.

## Data scope and design
- Two datasets corresponding to different survey networks:
  - WAWS: 41 sites with extensive major-ion data, four samples per site across 2012–2013 to capture seasonal variation.
  - Wye catchment: 20 sites with pH, alkalinity, conductivity and major anions; single sample in May 2013.
- Experimental design reflects distinct gradients:
  - WAWS: acidity gradient across geological settings and acidic episodes.
  - Wye: gradient in land-use intensification and nutrient content.
- Data gaps: two WAWS sites lacked a July 2013 sample; potential separation into two datasets due to differing determinants.

## Sampling and analytical methods
- Sample collection: filtered and unfiltered water collected in situ using standardized procedures; samples analyzed at Forest Research Laboratories.
- Analytical methods (selected):
  - Ammonia: ISO 7150/2 (Blue book) with automated spectrophotometry.
  - Anions: US EPA Method 300.0; ion chromatography with specific columns and detectors.
  - TOC/DOC: thermal oxidation with CO2 detection (TOC) and DOC via filtration, acidification, and helium purge.
- Documentation: detailed field and laboratory methods referenced (e.g., Plynlimon methods); supporting data on instruments and procedures available in the dataset notes.

## Data structure and metadata
- WAWS dataset: 34 columns (example columns: site_code, site_name, date, pH, Conductivity, Alkalinity_CaCO3, Alkalinity_eq, DOC, Cl, N(NO3), S(SO4), P(PO4), F, N(NO2), K, Ca, Mg, Na, Al, Fe, Mn, P, S, B, Ba, Cd, Co, Cr, Cu, Ni, Pb, Si, Sr, Zn).
- Wye dataset: 13 columns (site_code, site_name, date, pH, Conductivity, Alkalinity_CaCO3, Alkalinity_eq, DOC, Cl, N(NO3), S(SO4), P(PO4), F, N(NO2)).
- Supporting site metadata: DURESS_CU_site_description.csv includes coordinates (Eastings/Northings, Grid, Latitude/Longitude), elevation, catchment, and survey campaign identifiers.
- Data flow: raw samples → Excel records → CSV exports → ingestion into Environmental Information Data Centre (EIDC).

## Data lineage and provenance
- Field collection organized by Dr. Isabelle Durance; sample collection by Dr. Hugh Feeley.
- Analyses conducted by Forest Research Laboratories.
- Project umbrella: Diversity in Upland Rivers for Ecosystem Service Sustainability (DURESS; NERC NE/J014818/1; BESS programme).
- Data processing: standardized formats with in situ collection, laboratory analyses, and subsequent data structuring for repository ingestion.

## Access, usage and governance notes
- Data useful for assessing relationships between water chemistry and biodiversity/land-use gradients, and for cross-site comparisons within upland Welsh catchments.
- Consider potential need to treat WAWS and Wye as separate datasets due to differing determinands and sampling regimes.
- Users should consult supporting documentation for detailed field methods, analytical protocols, and metadata before integration into new analyses.
- Potential data quality considerations include seasonal sampling gaps and differing numbers of samples per site.

## Supporting materials and references
- Supporting documents referenced include detailed field methods (Plynlimon methods), analysis details, and site descriptions.
- Dataset ready for ingestion into EIDC; potential two-file ingestion due to determinand differences.