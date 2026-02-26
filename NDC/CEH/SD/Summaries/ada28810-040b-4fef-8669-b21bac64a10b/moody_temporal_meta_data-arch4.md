# Spatial and temporal variations in aquatic organic matter composition in UK surface waters

## Overview
- Scientific study (2018–2021) examining how aquatic organic matter (DOM) composition varies across space and time in UK surface waters.
- Data collected from multiple water bodies (peat/organic soils) across four locations in England and Scotland.
- Aims to characterize DOM composition, its drivers, and how it changes seasonally and spatially.
- Findings intended to support data-driven understanding of aquatic biogeochemistry and inform water quality management.

## Study design and sampling approach
- Fieldwork conducted between 2018 and 2021 at diverse catchments: pools, headwaters, streams/inlets, reservoirs, lakes, and outlets.
- Site-level measurements taken in situ: pH, conductivity, dissolved oxygen, temperature; air temperature, pressure, humidity also recorded.
- Water sampling protocol:
  - Grab water samples collected at each site.
  - 50 mL samples filtered in the field (0.45 µm) and kept cold (cool bag → cool box) for lab analysis.
  - Filtered samples stored at 4 °C for chemistry analyses.
- DOM sampling and processing:
  - Large volume collected for particulate organic matter (POM); filtration and concentration steps used to isolate colloidal and dissolved organic matter (DOM).
  - DOM analyzed for elemental composition (CHNO) using an Elementar Vario MICRO and a subset analyzed by negative-mode FT-ICR MS.
  - Organic matter extraction and handling described in detail, following methods aligned with Moody (2020).
- Quality assurance:
  - 10% of samples analyzed in replicate; instrument calibration and repeated checks throughout runs.
  - Replicate data compared; averages used if within 95% agreement; otherwise samples re-analyzed.
  - Derived metrics restricted based on physical properties to ensure data integrity.

## Data architecture and datasets
- Datasets created to capture site context, DOM composition, and contemporaneous water chemistry:
  - UK_Sites: site metadata and visit history
  - UK_DOM: composition metrics derived from DOM data
  - UK_Water: environmental variables and water chemistry for each sample

### UK_Sites
- Purpose: provide site-level metadata and visit chronology without revealing exact locations.
- Key fields and purpose:
  - ID: alphanumeric site code
  - Visit: sequence number for each site (1–24)
  - Month/Year: sampling calendar month and year
  - Group: location-based grouping
  - PEAT_AREA: categorical descriptor of peatland area (e.g., Peak District, Western Isles, etc.)
  - Elevation: level of elevation information
  - Type_4: classification of sampled water body (e.g., reservoir, stream, peat pool, lake)
  - LAND_USE, VEG_COVER, POSITION, CATCHMENT_AREA, HOSTPEAT, DISTANCE_SEA: contextual environmental attributes (land use, vegetation, catchment characteristics, peat coverage, proximity to sea)

### UK_DOM
- Purpose: metrics describing DOM composition and chemistry derived from element content and mass spectrometry.
- Key fields:
  - ID, Visit: site and visit identifiers
  - DOM_PROP_C: proportion of total carbon that is organic carbon
  - DOM_COX: carbon oxidation state
  - DOM_OR: oxidative ratio
  - DOM_DBEC: double bond equivalent per carbon
  - DOM_C_N, DOM_H_C, DOM_O_C: elemental ratios
  - Assigned_formula: number of formulas assigned by FT-ICR MS
  - Mean_mz, Std_mz: mean and SD of mass-to-charge ratios
  - Mean_ai, Mean_nosc: aromatic index and nominal oxidation state
  - Simpson, Shannon: diversity indices
  - PERC_LIPID, PERC_CARBO, PERC_AMINO, PERC_PEPTI, PERC_OXYAR: fraction of compound classes
  - MS_DBEC: mean double bond equivalents per carbon from MS
- Nature of data: derived composition metrics from DOM, enabling comparisons of chemical character across sites and times.

### UK_Water
- Purpose: contemporaneous water chemistry and environmental variables for each sample.
- Key fields:
  - ID, Visit: site and visit identifiers
  - pH, CONDUCTIVITY, DISS_O2, WATER_TEMP, AIR_TEMP, HUMIDITY, AIR_PRES
  - BANK_TEMP (soil/probe temperature)
  - DOC/ DON, DIN, DOP, DIP, CL, SO4, CA, K, MG, NA, AL, MN, FE, PB, CD, CO, CU, NI, ZN, LI: dissolved/ total chemical constituents and cations/anions
  - Note: two sets of values (1 and 2) for many variables reflect replicate measurements or alternate measurement methods
- Accessibility: site locations not disclosed to maintain anonymity due to access agreements with water companies

## Analytical methods and provenance
- DOM extraction and analysis procedures closely follow the referenced Moody (2020) methodology for DOM extraction from freshwaters.
- Analytical instruments:
  - Elementar Vario MICRO for CHNO and total carbon/nitrogen/hydrogen/oxygen with inorganic carbonates removed
  - FT-ICR MS for a subset of DOM samples to obtain high-resolution molecular information
- Data provenance and quality control documented to support reproducibility and traceability across datasets.

## Data accessibility and governance
- Spatial anonymization: exact site locations withheld to protect access agreements with water companies.
- Data organization emphasizes clear linkage between site context (UK_Sites), DOM composition (UK_DOM), and water chemistry/environmental variables (UK_Water).
- QA protocols are explicitly described, including replicate analysis and criteria for accepting derived metrics.

## Key implications for data leaders
- Holistic data view: integration of site context, DOM composition, and water chemistry supports end-to-end data governance and system-wide data strategy.
- Metadata richness: extensive site-level metadata (environmental context, catchment attributes, peat coverage, etc.) enhances discoverability and reusability for cross-site analyses and networks.
- Data quality and provenance: rigorous QA steps enable trustworthy analytics and reproducibility across studies or networks of partners.
- Access constraints: anonymization of location data should be considered in organizational data sharing policies and governance, balancing transparency with stakeholder confidentiality.
- Provenance and standards: clear documentation of DOM extraction methods and analytical pipelines (with reference to Moody 2020) aids interoperability and cross-study comparisons.
- Potential for collaboration: structured datasets (UK_Sites, UK_DOM, UK_Water) facilitate collaboration across institutions and support wider communities of practice in water quality and organic matter research.