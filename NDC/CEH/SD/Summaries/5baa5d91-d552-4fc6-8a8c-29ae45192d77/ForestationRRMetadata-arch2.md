# Forestation_RR

- Aim
  - Provide a standardized, time-resolved dataset to assess how forest age influences river flow following forestation, enabling evaluation of environmental health and policy outcomes over time.

- What the dataset includes
  - Two main files in the EIDC catalogue:
    - Forestation_RR_Bibliography.csv: bibliographic data for the primary studies.
    - Forestation_RR_EffectSize.csv: extracted dataset containing river flow response and associated metadata.
  - Variable descriptions are provided in Tables 1 and 2 of the documentation.

- Data content and structure
  - For each selected forestation study, four categories of data are extracted:
    - Catchment descriptors: catchment area (km2), mean annual precipitation (MAP, mm), land cover prior to forestation, etc.
    - Treatment descriptors: forest type (broadleaf, needleleaf, mixed), year of planting.
    - Experiment descriptors: treatment duration, method used to produce the control dataset.
    - Experimental data: time since first planting, area forest planted per year, control river flow, treatment river flow, annual precipitation, hydrological year.
  - Forest age is calculated as an area-weighted mean to reflect non-uniform establishment across the catchment.
  - Data were collected at annual time scales, comparing forested catchments to non-forested controls.
  - Where data were reported graphically, PlotDigitizer was used to extract values.

- Scope and selection of studies
  - Systematic literature search of Web of Science (1990 to 4 January 2018) identified 567 unique data sources.
  - Inclusion criteria: single catchment or paired catchment experiments that isolate the effect of forestation on river flow; treatment excludes deforestation; catchments are hydrologically independent; avoidance of confounding variables; longest available time series used when multiple reports existed.
  - 43 unique catchment experiments met the criteria.

- Data processing and calibration
  - Control river flow data were adjusted in some cases to be comparable with forested data by applying linear calibration regressions using pre-forestation data and/or precipitation and/or forested catchment flow.
  - When precipitation data were missing, climate data (CRU TS4.3) and related variables (potential evapotranspiration, mean annual temperature) were extracted for the catchment location.
  - Climate data were digitized for catchments as needed (30 catchments with direct data; 12 with representative circle sampling; 1 catchment using location-based data only).
  - For each study, four data categories were extracted as described above, including forest age (FA_WM), forestry extent (FC_PD), and year of study.

- Calibration methods and data corrections (Table 4)
  - Calibration options to estimate corrected control flow when not originally calibrated:
    - Single catchment or paired catchments designs.
    - Calibrations using regression of historic precipitation vs. river flow, or forecasted/observed river flow differences.
    - Several options account for pre-forestation conditions and data availability (e.g., with or without pre-forestation data).
  - The calibration approach aims to maximize the explained variance (adjusted R2) when aligning control flow with forested conditions and precipitation.

- Data access and citation
  - Dataset accessible via the EIDC catalogue (Forestation_RR_Bibliography.csv and Forestation_RR_EffectSize.csv).
  - Acknowledgement and recommended citation: Bentley, L. & Coomes, D. (2020) Partial river flow recovery with forest age is rare in the decades following establishment. Global Change Biology. DOI: 10.1111/gcb.14954.

- Related references and background
  - Foundational studies informing methodology and context include:
    - Farley, Jobbágy, & Jackson (2005) on afforestation effects on water yield.
    - Harris et al. (2014) for CRU TS climate data.
  - The dataset synthesizes primary and secondary sources from the literature to quantify river flow responses to forestation across time.