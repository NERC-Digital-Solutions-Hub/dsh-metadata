# Water chemistry of Welsh upland rivers

## Aim and scope
- Provides stream water chemistry data for 61 sites across Welsh upland rivers (41 WAWS sites; 20 Wye catchment).
- Data collected to characterize variation in water chemistry along gradients of aquatic biodiversity, land-use intensity, and recovery from acidification.
- Supports monitoring and assessment of environmental health and policy performance through standardized outputs.

## Study design and sampling
- Experimental design:
  - WAWS: gradient of acidity across 41 sites; emphasis on detailed major ions.
  - Wye: gradient of land-use intensity; focus on nutrient content.
- Sampling regime:
  - WAWS: four samples per site across July and September 2012, April and July 2013 (seasonal variation).
  - Wye: one sample per site collected in May 2013 (two WAWS sites missing a sample on 01/07/2013).
- Sites:
  - 41 WAWS sites (Welsh Acid Water Survey network) and 20 Wye catchment sites.
- Collection methods:
  - In situ collection of filtered and unfiltered water using standardized procedures.
  - Samples analysed at Forest Research Laboratories; results entered in Excel and exported as CSV for ingestion into EIDC.

## Analytical methods
- Ammonia (NH3):
  - Reference: Blue book method ISO 7150/2 (1986).
  - Indophenol method using salicylate and dichloroisocyanurate, reaction monitored at 650 nm; automated spectrophotometric readout.
- Anions:
  - Reference: US EPA Method 300.0.
  - Dionex IC with appropriate eluents and detection; discusses specific Dionex applications.
- Total Organic Carbon (TOC) and Dissolved Organic Carbon (DOC):
  - TOC: Thermal oxidation to CO2 in a high-temperature furnace; CO2 detected by NDIR.
  - DOC: Sample filtration, acidification, helium purge; separate TOC method without filtration for total carbon.
  - Instrumentation: Analytical Sciences Ltd, Thermalox; pH and conductivity probes for ancillary measurements.
- Supporting measurements:
  - pH (low conductivity electrode) and conductivity (conductivity probe).

## Data structure and content
- WAWS dataset: 34 columns.
- Wye dataset: 13 columns.
- Example columns:
  - site_code, site_name, date, pH, Conductivity, Alkalinity_CaCO3, Alkalinity_eq, Cl, N(NO3), S(SO4), P(PO4), F, N(NO2), plus appended elements (K, Ca, Mg, Na, Al, Fe, Mn, P, S, B, Ba, Cd, Co, Cr, Cu, Ni, Pb, Si, Sr, Zn) for WAWS; Wye includes a subset.
- Supporting documentation:
  - Site description file (site_code, name, coordinates, grid reference, latitude/longitude, elevation, catchment, survey).
  - Data assembled as flat CSV files for ingestion into EIDC.

## Lineage and data management
- Lineage:
  - In situ collection of filtered and unfiltered water samples using standardized procedures.
  - Analysis performed at Forest Research Laboratory.
  - Results recorded in Excel, then exported to comma-separated value files for EIDC ingestion.
- Data management and standards:
  - Data prepared to align with environmental information portals (EIDC) for broad accessibility.
  - Notes indicate potential handling as two datasets due to differing determinands between WAWS and Wye datasets; discussion and finalisation needed.

## Context, usage, and notes
- Keywords: diversity, aquatic invertebrates, land-use, benthic community, acidity.
- Supporting context:
  - Part of the DURESS project (Diversity in Upland Rivers for Ecosystem Service Sustainability), funded by NERC under the BESS programme.
  - Organised by Dr. Isabelle Durance; sample collection by Dr. Hugh Feeley.
- Considerations for analysts:
  - Ensure data quality and standardised processing across sites and campaigns.
  - Facilitate data reuse by combining WAWS and Wye data with other relevant environmental datasets.
  - Prepare for potential dual-dataset ingestion due to methodological differences in determinands.