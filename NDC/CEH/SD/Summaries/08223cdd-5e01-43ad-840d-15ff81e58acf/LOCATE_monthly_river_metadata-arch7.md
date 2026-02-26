# Land Ocean Carbon Transfer (LOCATE) Monthly river sampling dataset

## Overview
- LOCATE is a multidisciplinary NERC project involving the National Oceanography Centre, the British Geological Survey, the Centre for Ecology and Hydrology, and the Plymouth Marine Laboratory, with support from several universities and the Environment Agency.
- The dataset focuses on carbon transfer from land to rivers; a companion dataset covers estuaries.
- Monthly sampling across 41 rivers in England, Scotland and Wales during 2017 (Jan–Dec) with additional samples in Nov 2016.
- Rivers were selected to reflect different land-use types; aims to characterise geographical and seasonal variation in carbon fluxes.
- Aimed at enabling GIS-based analysis and map-based visualization of spatial and temporal patterns; a shift to HMS sites was made for easier data integration with EA datasets.

## Scope and Coverage
- Parameters collected monthly from fixed sites on each river (mostly within a 2–3 day window per month); Dorset Stour had a delayed start (April 2017).
- A companion estuarine dataset exists.
- Field coordination led by Andy Tye (BGS).
- Data intended to support understanding of land-to-river carbon flow and its variation with catchment characteristics.

## Sampling Design and Procedures
- After initial test sampling, most sites moved to HMS sites to facilitate data integration with EA data.
- Field sampling practices:
  - In-field filtration and separation into bottles; POC filtered back in the lab.
  - Samples kept in darkness in coolers or freezers.
  - Field measurements for salinity, SEC, and temperature where possible; if salinity probe unavailable, bottles sealed and analysed later.
  - Fixed mid-channel sampling depth (~0–30 cm) when feasible; otherwise from a representative flowing area.
  - Equipment prepared at the sampling institute; field data forms completed with weather and river conditions; upstream and downstream photos taken at each site.
  - Gloves worn; sampling vessels rinsed multiple times; samples transported in appropriate cool storage.
  - Specific sample handling for particulates, nutrients, DOM (fluorescence and absorbance), alkalinity/pH, and salinity.
  - Samples returned to respective laboratories for analyses.
- Field blanks were taken for selected sites/types to test batch quality.

## Measured Parameters
- Physical/chemical water-quality parameters: temperature, salinity, conductivity (SEC).
- Nutrients: NH4-N, NO3-N, PO4-P, total nitrogen (TN), total phosphorus (TP).
- Carbon forms: non-particulate organic carbon (NPOC), total dissolved carbon (TDC), particulate organic carbon (POC), particulate organic nitrogen (PON); 13C and 15N isotopes.
- Alkalinity and pH (RAW_WATER and/or filtered WATER as appropriate).
- Dissolved Organic Matter (DOM) fluorescence (fDOM) and absorbance (abs254, abs340) with PARAFAC modelling (DOMFluor).
- Protein/organic matter characterisation via fluorescence indices and PARAFAC components.
- Molecular analyses planned to be reported separately.

## Data and Metadata Schema
- Data file columns include:
  - Demographic/identification: River_code, Date, Trip_number, Sampling_time_GMT, River_sample_ID.
  - Sample inventory: Number_filters_used, Volume_filtered_for_RNA, Volume_filtered_for_POC.
  - In-situ measurements: Temperature_deg C, Conductivity_uS/cm, Salinity_ppt, Weather, Sampler_comments, Flow_and_level, Additional_logsheet_based_comments.
  - Core chemistry: NH4-N_FILTERED_WATER_mg_per_L, NO3-N_FILTERED_WATER_mg_per_L, NPOC_FILTERED_WATER_ppm, PO4-P_FILTERED_WATER_mg_per_L, TN_RAW_WATER_ppm, TP_RAW_WATER_mg_per_L, TDC_FILTERED_WATER_mg_per_L, Alkalinity_RAW_WATER_mg_per_L, pH_RAW_WATER, etc.
  - DOM/optical properties: Absorbance_abs254, Absorbance_abs340, EEM_Peak_Picking_*, PARAFAC_loading_Component_*, Other_fluorescence_index_*.
  - POC/PON isotopes and related metrics: POC_delta_13C_parts_per_mil, POC_13C_Atom_percent, PON_delta_15N_parts_per_mil, PON_15N_Atom_percent, POC_Amount_C_micro_g, PON_Amount_N_micro_g, POC_Amount_C_micro_g_per_L, POC_PON_Sample_Label, etc.
  - Data quality/QA fields: Nutrients_pH_alkalinity_comments, QA_status, PARAFAC_sample_file_ID, etc.
- River context and catchment context:
  - Land cover and catchment attributes derived from the 2015 CEH Land Cover Map (LCM 2015) including: catchment area, peat soil area, arable & horticulture, various habitat types (acid grassland, bog, calcareous grassland, broadleaf/ coniferous woodland, freshwater, fen/marsh/swamp, heath, various grasslands), urban/suburban, and other land uses.
  - Hydrological and geology features: mean altitude, Base Flow Index (BFI), carbonate rocks presence, and other derived layers.
- Spatial/temporal scale: monthly river-wide dataset for 41 rivers across the UK for 2017 (plus a 2016 trial).

## Laboratory Methods and Quality Assurance
- Carbon and nitrogen concentrations and isotope ratios measured with:
  - Flash EA 1112 Series Elemental Analyser connected to a DeltaPlus XP isotope ratio mass spectrometer (Thermo Finnigan).
  - Calibration against international references USGS40 (carbon and nitrogen) and USGS41a for δ13C/δ15N; δ13CVPDB and δ15NAir-N2 normalization.
  - Analyses performed under UKAS ISO 17025 framework; treated as accredited for QA purposes, though not formally accredited due to repeatability constraints.
- Instrumentation:
  - Fluorescence: Varian Cary Eclipse.
  - Absorbance: Varian Cary 60 (UV–Vis) with 1 cm path length cuvettes.
- Calibration and QA:
  - Blank and Quinine sulphate standards run with every batch.
  - PARAFAC modelling via Matlab DOMFluor toolbox.
  - Long-term precision checks using a standard (dried milled topsoil) for total C, δ13C, total N, and δ15N.
- Quality control:
  - Approximately 5% of samples subjected to additional QA checks within a run (participation in Aquacheck program for CEH Lancaster lab).

## River Information and Land Cover Context
- River catchment context and land-cover-derived metrics prepared using the 2015 CEH Land Cover Map (LCM 2015).
- Variables include:
  - Catchment area, peat soil area, arable land, various habitat types (bog, fen, grasslands, heath), broadleaf and coniferous woodlands, freshwater areas, urban/suburban areas, and other land uses.
  - Hydrological context: mean altitude, Base Flow Index (BFI), and carbonate rock presence.
  - Standardized rainfall data (SAAR 1961–90) and other raster-derived attributes.
- Data organized with River_code, sampling metadata, and a comprehensive set of chemical/optical measurements used for GIS analyses and integration with catchment attributes.

## Practical GIS Relevance
- Enables mapping and spatial analysis of carbon transfer proxies across catchments with different land-use types.
- Facilitates time-series analysis of monthly riverine carbon flux indicators across the UK 2017 dataset.
- Allows integration with land-cover, hydrology, and geology layers (LFIs, BFI, carbonate rocks, altitude) to explore drivers of spatial variability.
- Provides a rich schema for join operations with river networks, catchment polygons, and estuarine datasets (via the LOCATE suite).

## Notes on Data Use and Access
- Molecular analyses are planned but reported elsewhere; primary dataset emphasizes water chemistry, DOM fluorescence/absorbance, POC/PON, isotopes, and derived indices.
- A companion estuary dataset exists for complementary analysis of land-to-sea carbon transfer.
- The sampling regime and site selection were designed to support robust data integration and modelling efforts, with ongoing QA and cross-lab verification.