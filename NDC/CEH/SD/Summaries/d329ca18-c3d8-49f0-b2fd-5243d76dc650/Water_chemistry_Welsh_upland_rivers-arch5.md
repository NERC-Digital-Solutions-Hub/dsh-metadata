# Water chemistry of Welsh upland rivers

## Overview
- Dataset of stream water chemistry for selected Welsh upland rivers across 61 catchments (41 WAWS sites + 20 Wye catchment sites).
- WAWS data: pH, alkalinity, conductivity, and major cations/anions. Wye data: pH, alkalinity, conductivity, major anions.
- Sampling periods: Wye in May 2012; WAWS in summer/autumn 2012 and spring/summer 2013 (calendar year timing with some gaps).
- Purpose: characterize water chemistry variation along biodiversity gradients, land-use intensity, and recovery from acidification.
- Project context: part of the DURESS project (NERC Biodiversity and Ecosystem Service Sustainability program).

## Data scope and content
- WAWS: 41 sites with detailed major ion chemistry; 4 samples per WAWS site across 2012–2013 to capture seasonal variation.
- Wye: 20 sites with fewer measurements (limited to a subset of major parameters) collected in May 2013.
- Key variables include pH, conductivity, alkalinity (as CaCO3 and equivalent), and concentrations of major ions (e.g., Cl, NO3, SO4, PO4, F) plus site metadata.
- Data are provided as two flat CSV files (WAWS and Wye) with differing column sets.

## Provenance and lineage
- In situ collection using standardized procedures; samples sent to Forest Research Laboratory for analysis.
- Results recorded in an Excel workbook and exported to CSV for ingestion into the Environmental Information Data Centre (EIDC).

## Sampling and analytical methods
- Experimental design:
  - WAWS: 41 sites with four samples per site (Jul/Sep 2012 and Apr/Jul 2013) to capture seasonal variation.
  - Wye: single sample collected in May 2013 (limited temporal coverage).
  - Note: two WAWS sites (DW20274 and DW57001) lacked one WAWS sample in July 2013.
- Collection methods: filtered and unfiltered water samples collected in situ using standardized procedures.
- Analytical methods:
  - Ammonia: Blue book method (ISO 7150/2:1986), automated spectrophotometric method.
  - Anions: US EPA Method 300.0; ion chromatography with specified columns and detectors.
  - TOC/DOC: thermal oxidation for TC; DOC via filtration/acidification and helium purging; instruments include Thermalox system and CO2 detection.
  - Supporting instrumentation: pH and conductivity measurements with specified electrodes and probes.
- Data structure details:
  - WAWS: 34 columns; Wye: 13 columns.
  - Example WAWS columns include site_code, site_name, date, pH, Conductivity, Alkalinity_CaCO3, Alkalinity_eq, DOC, Cl, NO3, SO4, PO4, F, NO2, K, Ca, Mg, Na, Al, Fe, Mn, P, S, B, Ba, Cd, Co, Cr, Cu, Ni, Pb, Si, Sr, Zn.
  - Wye columns limited to site_code, site_name, date, pH, Conductivity, Alkalinity_CaCO3, Alkalinity_eq, DOC, Cl, NO3, SO4, PO4, F, NO2, plus a subset of cations/anions.
- Supporting documentation:
  - Plan to document analysis details from Forest Research Laboratory.
  - Field methods guidance (Plynlimon methods) attached.
  - Consideration to ingest as two datasets due to differences in determinands analyzed.
  - Data ingestion planning notes (columns listing or CAST-like reference).

## Metadata, governance, and data management
- Data were prepared for ingestion into the Environmental Information Data Centre (EIDC); emphasizes standardization and interoperability.
- Supporting data include a site description file (DURESS_CU_site_description.csv) with location, grid references, elevation, and catchment information.
- Documentation indicates need for detailed method notes and potential dual-dataset ingestion to reflect differing analytes across WAWS and Wye.
- Data stewardship considerations:
  - Ensure complete metadata for each column (units, method, detection limits, QA/QC notes).
  - Maintain traceability from field collection through laboratory analysis to CSV formats and EIDC ingestion.
  - Manage updates and ensure any embargoes or access restrictions are respected.

## Data access, usage, and integration
- Data intended for public dissemination via EIDC as part of the DURESS project outputs.
- Useful for analyses linking water chemistry to biodiversity gradients, land-use patterns, and acidification recovery.
- The presence of a separate WAWS vs. Wye dataset requires careful data integration, including harmonization of columns, units, and provenance.

## Quality assurance and challenges
- Quality assurance steps implied: in situ standardized collection, laboratory analyses, and data curation into CSV with clear lineage.
- Potential challenges for data stewards:
  - Incomplete sampling in a few WAWS and Wye sites, seasonal gaps, and missing data (e.g., two WAWS samples uncollected).
  - Differences in determinands between WAWS and Wye necessitating separate datasets or careful harmonization.
  - Handling large, multi-parameter datasets (including trace ions) and ensuring consistent metadata across platforms.
  - Ensuring timely availability and proper documentation of methods from the Forest Research Laboratory.

## Key takeaways for Data Stewards
- Maintain comprehensive metadata for all columns, including units and analytical methods.
- Preserve lineage: field collection procedures, laboratory analyses, and data transformations to CSV for EIDC.
- Consider dual-ingest strategy to accommodate differing determinations across WAWS and Wye.
- Ensure accessibility through EIDC with clear documentation and site-level metadata (location, catchment, survey campaign).
- Plan for updates and data governance around embargoes and data sharing limitations.
- Include supporting site descriptions to enable spatial analyses and reproducibility.