# Water chemistry of Welsh upland rivers

- 61 catchments studied: 41 sites from the Welsh Acid Water Surveys (WAWS) network and 20 sites from the Wye catchment.
- Measurements by dataset:
  - WAWS catchments: pH, alkalinity, conductivity, and major cations and anions.
  - Wye catchment: pH, alkalinity, conductivity, and major anions (plus related variables).
- Purpose: characterize water chemistry variation along gradients in aquatic biodiversity, environmental settings (land-use intensity), and recovery from acidification.
- Project context: part of the DURESS project (Diversity in Upland Rivers for Ecosystem Service Sustainability), funded by NERC (BESS programme).

## Data collection and lineage

- In situ collection of filtered and unfiltered water samples using standardized procedures; samples analyzed at Forest Research Laboratory.
- Data lineage:
  - Samples collected, analyzed, and results entered into an Excel spreadsheet.
  - Data exported as CSVs for ingestion into the Environmental Information Data Centre (EIDC).

## Experimental design / Sampling regime

- WAWS: four samples per site collected across campaigns in July and September 2012, and April and July 2013 (to capture seasonal variation).
  - Note: two WAWS sites (DW20274 and DW57001) had missing sampling on 01/07/2013.
- Wye catchment: one sample per site collected in May 2013 (single time point for this dataset).

## Methods and analyses

- Collection methods: in situ collection of both filtered and unfiltered water samples using standardized procedures.
- Analytical methods:
  - Ammonia: ISO 7150/2 (Blue Book); spectrophotometric indophenol method.
  - Anions: US EPA Method 300.0; Dionex IC methods with appropriate detectors.
  - Total Organic Carbon (TOC) / Dissolved Organic Carbon (DOC): thermal oxidation to CO2 with NDIR detection; DOC measured on filtered, acidified samples; TOC on unfiltered, acidified samples.
  - Instrumentation noted: Chemlab with colorimeter; Dionex equipment; pH and conductivity probes; Thermalox instrument for carbon analyses.
- Data structure:
  - WAWS data: 34 columns (extensive list including pH, conductivity, alkalinity, DOC, Cl, NO3, SO4, PO4, F, NO2, K, Ca, Mg, Na, Al, Fe, Mn, P, S, B, Ba, Cd, Co, Cr, Cu, Ni, Pb, Si, Sr, Zn, plus others).
  - Wye data: 13 columns (site_code, site_name, date, pH, Conductivity, Alkalinity_CaCO3, Alkalinity_eq, DOC, Cl, NO3, SO4, PO4, F, NO2, and additional cations/anions listed similarly).
- Data notes:
  - Possible need to ingest as two datasets due to differences in determinands analysed between WAWS and Wye.
  - Supporting documentation includes field methods and site descriptions.

## Data structure, metadata, and access

- Site description file available with coordinates, elevation, grid references, catchment details, and campaign identifiers.
- Data stored as CSV and prepared for ingestion into the Environmental Information Data Centre (EIDC).
- Campaign identifiers:
  - WAWS (Welsh Acid Water Survey)
  - Wye catchment
  - Plynlimon, Llyn Brianne catchments as referenced in the site metadata

## Provenance, documentation, and caveats

- Supporting documentation requested includes details of Forest Research Laboratory analyses and field methods (Plynlimon methods guidance).
- Data provenance emphasizes two datasets with different determinands; users should consider combining with caution and consulting the supporting methods for alignment.
- Limitations and considerations:
  - Seasonal coverage for WAWS but limited to four campaigns; Wye provides a single May 2013 dataset.
  - Missing samples for two WAWS sites in July 2013.
  - Potential differences in detected variables and measurement depth across datasets.

## Implications for analysis and use

- Suitable for exploring relationships between water chemistry and biodiversity, land-use intensity, and acidification recovery gradients.
- Enables assessment of major ion balances, acidity indicators (pH, alkalinity), and nutrient content across catchments.
- When integrating WAWS and Wye data, plan for harmonization of determinands and time points; use site metadata to align catchment contexts.
- Data provenance and metadata enable reproducibility; consider linking to the DURESS project context and site descriptions for interpretation.