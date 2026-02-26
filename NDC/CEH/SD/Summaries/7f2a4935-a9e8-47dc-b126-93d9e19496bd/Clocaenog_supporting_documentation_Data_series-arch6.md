# Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- A climate change manipulation experiment (Climoor) using automated roof technology to simulate drought and warming over upland moorland species for the next 20–30 years.
- Established in 1998 at Clocaenog Forest, North East Wales; replicated drought and warming treatments with three replicates each plus three control plots (total of 9 plots).
- Studies a wide range of abiotic and biotic responses, with data collected across multiple years and along a suite of ecological processes.

## Site information
- Location: Clocaenog Forest, North East Wales (53°03′19″N, 03°27′55″W); upland west-Atlantic moorland dominated by Calluna vulgaris (heather) with Vaccinium myrtillus and Empetrum nigrum present.
- Soil: Humic ferric podzol with variable eluvial (E) and illuvial (Bh) horizons; depth of apparent horizons typically 6–17 cm for E, Bh below.
- Ecosystem type and vegetation: Wet upland heath, with a diversity of bryophytes and vascular plants; shrubs and grasses tracked for biomass and phenology.
- Climate context: Site experiences mean annual rainfall around 1411 mm and N deposition typical of the region; specific microclimate responses are captured via on-site instrumentation.

## Climate change treatments
- Drought (D): Retractable polyethylene roof over plots (4 m x 5 m) triggered by tipping-bucket rainfall sensor; May–Sept (1999–2011) and April–October since 2012; reduces site rainfall by ~20% and excludes ~80% of rainfall during treatment periods; curtains do not operate in winds >10 m/s.
- Warming (W): Retractable aluminum mesh curtains that reduce infrared loss at night, reflecting 96–97% of IR; rain retraction occurs during rain events to minimize rainfall loss; annual rainfall reduction ~14%; curtains not operated in high winds.
- Experimental design: 3 warming plots, 3 drought plots, and 3 control plots; arranged in blocks to account for spatial variation.
- Treatment timing and changes over years are detailed in year-by-year tables.

## Data collection and data management

- Data types and datasets (high-level)
  - Climate and meteorology
    - AWS daily meteorological data (Daily automated weather station data_1999to2015_Clocaenog.csv)
    - Micro-meteorological plot data (Daily micromet data_1998to2015_Clocaenog.csv)
  - Hydrology and rainfall
    - Rainfall at site (Rainfall_Clocaenog.csv)
    - Throughfall (Throughfall_Clocaenog.csv)
    - Rainfall chemistry (pH, NO3, Cl, SO4, DOC, NH4)
  - Soil and groundwater
    - Water table depth (Water table depth_Clocaenog.csv)
  - Soil respiration and trace gases
    - Fortnightly soil respiration (Fortnightly soil respiration_Clocaenog.csv)
    - Automated soil respiration (Automated soil respiration_Clocaenog.csv)
    - Trace gases CH4 and N2O (Trace gases_Clocaenog.csv)
  - Ecosystem fluxes
    - Net ecosystem CO2 exchange (Net ecosystem exchange_Clocaenog.csv)
  - Plant physiology and vegetation
    - Photosynthesis (Photosynthesis_Clocaenog.csv)
    - Vegetation surveys for biomass (Vegetation survey_Clocaenog.csv)
    - Canopy reflectance (Canopy reflectance_Clocaenog.csv)
    - Phenology, growth, pathogens (Phenology Growth Pathogens_Clocaenog.csv)
    - Vegetation chemistry (Vegetation chemistry_Clocaenog.csv)
    - Litterfall (Litterfall.csv)
    - Root biomass (Root biomass.csv)
    - Soil microbial biomass (Soil microbial biomass.csv)
    - Nitrogen mineralisation (Nitrogen mineralisation.csv)
    - SOM, SOC and bulk density (Soil organic matter carbon density.csv)
    - Soil solution and leachate chemistry (Water chemistry.csv)

- Data processing and methodology
  - Equipment and sensors: On-site AWS met data (1-min sampling, hourly averages from a mast-mounted station after 2007); plot-level micro-met data; various soil and forest canopy sensors.
  - Data quality and curation: Visual quality control in Excel; legacy data sometimes lack modern, automated QC; some datasets have detailed calibration and unit-conversion notes to standardize across instruments and years.
  - Unit conversions and data calibration: Detailed conversion rules between raw instrument outputs and reported fluxes (e.g., soil respiration in mg CO2-C m^-2 h^-1 or µmol m^-2 s^-1; NEE converted to mg CO2-C m^-2 h^-1; biomass adjustments in NEE via pin-hit biomass calibrations).
  - Pin-point vegetation measurements: 3 quadrats per plot with 100-pin grids; biomass calibrations established via destructive sampling; conversion factors provided (Table 6) for translating pin hits to biomass (g m^-2).
  - Throughfall and rainfall processing: Throughfall data used to derive plot-level rainfall reductions by applying percent differences to site rainfall data; data gaps and occasional infill with average reductions noted.
  - Data stewardship: Not all data are stored in the Environmental Information Data Centre (EIDC); contact CEH Bangor staff (Sabine Reinsch, Bridget Emmett) for access details.

- Data limitations and notes
  - Legacy data: Documentation and processing reflect past practices; some methods or calibrations may not meet current best-practice standards, particularly for trace gases and certain soil measurements.
  - Data gaps: Occasional data loss due to instrument issues (e.g., canopy sampling losses, funnel misplacements, or equipment downtime); treatment means may be calculated with less than full replicates in some years.
  - Storage and availability: While many datasets are listed, not all are stored in the EIDC; contact project contacts for access and permissions.

## Data accessibility and contacts
- Primary contacts for data access and details: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor.
- Note: Some data are not stored within the EIDC; follow up with CEH Bangor for data provision and provenance.

## Appendices
- Appendix 1: Site layout
- Appendix 2: Quadrat layout with experimental plots (including LYS, PQ, SS codes)
- Appendix 3: Plot layout with quadrats and measurement areas

## Summary of data stewardship implications for Data Support
- The Climoor dataset collection is extensive and multidisciplinary, spanning climate manipulation, hydrology, soil processes, vegetation dynamics, and ecosystem fluxes.
- Data are historically rich but heterogeneous in methods, instruments, and documentation, requiring careful harmonization, provenance tracking, and clear metadata.
- Data quality control relies heavily on manual, ad hoc QC practices in some periods; future work should enhance automated QC, standardize units, document processing steps, and centralize storage (preferably within a common data center like EIDC) to facilitate long-term reuse.
- Users should account for treatment-specific data gaps and potential biases due to methodological changes over time when conducting cross-epoch analyses.