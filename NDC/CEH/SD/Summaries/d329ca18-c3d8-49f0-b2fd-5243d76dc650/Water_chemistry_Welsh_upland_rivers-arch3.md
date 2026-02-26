# Water chemistry of Welsh upland rivers

- Overview
  - A dataset of stream water chemistry for selected Welsh upland rivers across 61 catchments (41 WAWS sites; 20 Wye catchment sites).
  - Measured parameters include pH, alkalinity, conductivity, and major ions; Wye includes major anions.
  - Sampling periods: Wye in May 2012; WAWS samples in summer/autumn 2012 and spring/summer 2013.
  - Purpose: characterise water chemistry variation along biodiversity and environmental gradients, such as land-use intensity and recovery from acidification.
  - Project context: part of the DURESS project (NERC NE/J014818/1) under the Biodiversity and Ecosystem Service Sustainability programme; led by Dr Isabelle Durance with sample collection by Dr Hugh Feeley; analyses at Forest Research Laboratories.

- Lineage and data handling
  - Samples were collected in situ (filtered and unfiltered) using standardised procedures.
  - Laboratory analysis conducted at Forest Research Laboratories; results entered into Excel and exported as CSV for ingestion into the Environmental Information Data Centre (EIDC).

- Keywords
  - diversity, aquatic invertebrates, land-use, benthic community, acidity

- Experimental design and sampling regime
  - WAWS: 41 sites sampling to capture acidity gradient across geological settings; four samples per site across 2012–2013 to capture seasonal variation.
  - Wye: 20 sites focusing on nutrient content; one sample per site in May 2013 (with two WAWS sites not sampled on 01/07/2013).
  - Some missing data: two WAWS sites could not be sampled on 01/07/2013.

- Collection and analytical methods
  - Field collection: standardized in situ collection of filtered and unfiltered water samples.
  - Ammonia: Blue book method (ISO 7150/2:1986) with automated spectrophotometry.
  - Anions: US EPA Method 300.0; Dionex systems with appropriate columns and detectors.
  - Total Organic Carbon (TOC) and Dissolved Organic Carbon (DOC): thermal oxidation with CO2 detection; DOC requires filtration and acidification with helium purging; TOC uses non-filtered samples.
  - Instrumentation: specified pH, conductivity, and IC/TOC equipment (e.g., Mettler Inlab, Thermo Orion, Dionex setups).

- Data structure and documentation
  - WAWS dataset: 34 columns; Wye dataset: 13 columns (site_code, site_name, date, pH, Conductivity, Alkalinity_CaCO3, Alkalinity_eq, DOC, Cl, N(NO3), S(SO4), P(PO4), F, N(NO2), plus additional cations/anions and trace elements).
  - Site description: separate CSV with 10 fields (site_code, name, Eastings/Northings, Grid, Latitude/Longitude, Elevation, Survey, Catchment, etc.).

- Supporting documentation and data provenance
  - Additional files: DURESS_CU_site_description.csv (site metadata).
  - Notes reference field methods (Plynlimon methods guidance) and potential ingestion as two datasets due to differing determinands.

- Data availability and governance
  - Data managed for ingestion into the Environmental Information Data Centre (EIDC); implies open sharing and data governance considerations.
  - Metadata and field/method details are provided to facilitate verification, replication, and reuse.
  - Acknowledges need for complete metadata, standardisation, and potential data-sharing barriers (relevant to monitoring framework governance).

- Relevance to monitoring frameworks (archaetype alignment)
  - Demonstrates a structured approach to environmental health monitoring by combining: 
    - standardized field collection and laboratory methods
    - defined sampling regimes to capture spatial and seasonal variation
    - clear data lineage from field collection to central data repositories
    - explicit data structure with metadata and site descriptors
    - governance and sharing through EIDC, enabling transparency and reuse
  - Highlights challenges typical for monitoring frameworks:
    - data gaps (missing samples at some times/sites) and limited temporal coverage for the Wye catchment
    - data access and potential silos across organisations (WAWS vs Wye)
    - need for comprehensive metadata to assess data suitability and compatibility
    - formatting and integration complexities due to differing determinands between WAWS and Wye
    - governance requirements to ensure data quality, openness, and up-to-date storage

- Key takeaways for monitoring practitioners
  - Use of parallel monitoring streams (WAWS and Wye) to explore acidity gradients and land-use effects on water chemistry.
  - Importance of standardized analytical methods and robust field protocols to ensure comparability.
  - Value of central data curation in a recognized data centre (EIDC) to support transparency and future decision-making.
  - Anticipate and document data limitations to inform interpretation and governance decisions.