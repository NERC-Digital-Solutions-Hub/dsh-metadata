# Land Ocean Carbon Transfer (LOCATE) Monthly river sampling dataset

## Overview
- Multidisciplinary NERC project integrating multiple UK institutions to understand carbon transfer from land to the ocean.
- Focus on flow from land to rivers; companion estuary dataset exists.
- 2017 monthly sampling across 41 rivers in England, Scotland, and Wales (plus earlier November 2016 samples).
- Rivers selected to reflect different land-use types; data aimed at capturing geographical and seasonal variation in carbon fluxes.

## Sampling Design and Coordination
- Sampling conducted at fixed sites on each river, typically within the same 2–3 day window each month.
- Dorset Stour (DSTO) had deviations (not sampled until April 2017).
- After a test phase, most sites moved to HMS sites to improve data integration; Environment Agency data to underpin modelling datasets.
- Coordination led by Andy Tye (British Geological Survey).

## Parameters Measured
- Physical and chemical water properties: temperature, specific electrical conductivity (SEC), salinity, pH, alkalinity.
- Nutrients: ammonium (NH4-N), nitrate (NO3-N), phosphate (PO4-P).
- Carbon metrics: non-particulate organic carbon (NPOC), total dissolved carbon (TDC), total carbon (TC) in dissolved and particulate forms.
- Nitrogen and phosphorus: total nitrogen (TN), total phosphorus (TP).
- Particulate and dissolved organic matter: particulate organic carbon (POC), particulate organic nitrogen (PON), 13C, 15N isotopes; dissolved organic matter fluorescence (fDOM) and absorbance.
- Additional: sampling for molecular analyses (to be reported separately).

## Field Sampling Procedure
- Field processing: most filtering/separating done in the field; POC samples filtered in-lab.
- Samples kept in darkness, in cool conditions or freezers.
- In-field measurements: salinity, SEC, and temperature where possible; in cases without a salinity probe, bottle samples sealed to minimize evaporation and analyzed later.
- Sample collection: mid-channel depth ~0–30 cm, representative of main river body; volumes and bottle types specified for each analyte.
- Cleaning and contamination control: bottles rinsed three times; gloves worn; field logs captured weather and river conditions; photos taken upstream and downstream.
- Transport: samples placed in coolers or freezers; some analyses conducted at partner labs with designated handling (POC, NOC; nutrients at CEH Lancaster; pH/alkalinity at CEH Lancaster; fluorescence/absorbance at BGS Wallingford).

## Field Blanks and Quality Assurance
- Field blanks implemented at selected sites to test batch integrity of filters.
- Blanks and procedure specifics handled by the respective analysis groups (BGS for fluorescence, CEH Lancaster for nutrients, NOC for POC).
- QA processes aligned with Aquacheck participation for laboratory analyses.

## Analytical Methods and Instrumentation
- Nutrients and related metrics:
  - NH4-N, NO3-N, PO4-P, TDC, NPOC, TN, TP, pH, alkalinity.
  - Instruments and methods referenced (e.g., SEAL_AQ2, DIONEX_ICS2000, FORMACS, METROHM, SKALAR SP10).
  - Detection limits provided for key nutrients.
- Carbon and isotopes:
  - Carbon and nitrogen concentrations (percent by weight) with δ13C and δ15N isotope ratios.
  - Instrumentation: Flash EA 1112 Series Elemental Analyzer with Conflo III connected to DeltaPlus XP IRMS.
  - Calibration with international standards USGS40, USGS41a; ISO 17025 style QA; long-term precision targets provided.
- Fluorescence and absorbance:
  - Fluorescence: Varian Cary Eclipse; excitation 200–400 nm, emission 250–500 nm; PARAFAC modelling via Matlab DOMFluor.
  - Absorbance: 200–800 nm with blank subtraction; Raman unit reporting; quality control with blanks and quinine sulphate standards.
- River and land-cover context:
  - River catchment and landscape data drawn from 2015 CEH Land Cover Map (LCM 2015) and related GIS derivatives (e.g., drainage area, peat soils, arable/horticulture, various habitat types, woodland types, freshwater bodies, canalization of land cover, etc.).
  - Additional covariates: rainfall (standardised 1961–90), Base Flow Index (BFI), carbonate rocks, mean altitude, and other land-cover metrics.

## Data Structure and Variables
- Data file columns include:
  - Spatial/time identifiers: River_code, Date, Trip_number, Sampling_time_GMT, River_sample_ID.
  - Sampling and process metrics: Number_filters_used, Volume_filtered_for_RNA, Volume_filtered_for_POC, Temperature_degC, Conductivity_uS/cm, Salinity_ppt, Weather, Sampler_comments, Flow_and_level, Additional_logsheet_based_comments.
  - Nutrients and chemistry: NH4-N_FILTERED_WATER_mg_per_L, NO3-N_FILTERED_WATER_mg_per_L, pH_RAW_WATER, NPOC_FILTERED_WATER_ppm, PO4-P_FILTERED_WATER_mg_per_L, TN_RAW_WATER_ppm, TDC_FILTERED_WATER_mg_per_L, TP_RAW_WATER_mg_per_L, Nutrients_pH_alkalinity_comments, Nutrients_pH_alkalinity_Raw_data_file.
  - PARAFAC and fluorescence: PARAFAC_Sample_file_ID, PARAFAC_loading_Component_1..Component_6, PARAFAC_comments, EEM_peak metrics, OHNO indices, McKnight ratios, betalpha ratios.
  - Absorbance and POC/PON isotopes: Absorbance_abs254, Absorbance_abs340, POC-PON sample metadata and isotopic data (e.g., POC_delta_13C_parts_per_mil, POC_13C_Atom_percent, PON_delta_15N_parts_per_mil, PON_15N_Atom_percent).
  - POC/PON loadings and concentrations: POC_Amount_C_micro_g, PON_Amount_N_micro_g, POC_Amount_C_micro_g_per_L, POC_Amount_N_micro_g_per_L.
  - Various PF and quality indicators for sample status and lab checks.

## Ancillary River Information
- Land-cover and hydrological context derived from CEH LCM 2015.
- Key covariates include:
  - Catchment area (ha), NRFA code, peat soil area, arable/horticulture, various habitat and land-cover types (bog, calcareous/grassy, broadleaf/conifer woodlands, freshwater habitats, fen/marsh/swamp, urban/rural mixes), and inland rock data.
  - Hydrological and climatic context: standardised rainfall (1961–1990), Base Flow Index (BFI), carbonate rocks, mean altitude.

## Notes and Considerations for Analysts
- Dataset aims to support analysis of land-to-river carbon transfer with rich chemical, isotopic, and optical characterisation, alongside extensive catchment-level covariates.
- Acknowledges data integration challenges across sites, standardisation of methods, and alignment with broader modelling datasets (EA data emphasized for integration).
- Some elements (e.g., molecular analyses) are reported separately; not all sampling deviations are uniform across all rivers/months.
- Data quality relies on multi-institution QA processes, field blanks, and standardized QA procedures consistent with ISO/17025-style practices.