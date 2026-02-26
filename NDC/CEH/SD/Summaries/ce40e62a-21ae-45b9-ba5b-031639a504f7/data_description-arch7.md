# SARS-CoV-2 qPCR and water chemistry data from wastewater at six sites in England and Wales between March and July 2020, with associated Covid-19 positive test and related-death data collated from other sources

## Data Access and Licensing
- Data accessible at: https://doi.org/10.5285/ce40e62a-21ae-45b9ba5b-031639a504f7
- Licensed under the Open Government Licence (OGL)
- Citation required: Hillary et al. (2021). NERC Environmental Information Data Centre. Dataset DOI: https://doi.org/10.5285/ce40e62a-21ae-45b9-ba5b-031639a504f7

## Data Description
- Two CSV files included:
  - data_table.csv: main dataset with temporal and wastewater chemistry variables
  - cases.csv: clinical testing data for the same period
- Key columns in data_table.csv include: Week, Date, Site_Name, Flow, gc_100ml, E_gene_100ml, Crass_gc_100, Crass_Recovery, NO3, NH4, PO4, pH, EC, Deaths, Deaths_100k, Daily_Cases_100k, Rolling_Sum_100k, Local_Authority_Population, cov_class, cov_detect, E_class
- Key columns in cases.csv include: Site_Name, Date, Local_Authority_Population, Daily_Cases, Cumulative_Cases, Rolling_Sum, Daily_Cases_100k, Rolling_Sum_100k, Week

## Sampling Sites and Time Frame
- Six wastewater treatment plants (WWTPs) across Wales and Northwest England
- Served urban areas in Gwynedd, Cardiff, Liverpool, Manchester, the Wirral, and Wrexham
- Combined population equivalent served: ~3 million
- Sampling period: weekly from March to July 2020 (first UK-wide COVID-19 wave)
- Sample types and timing:
  - Untreated influent collected as grab samples (weekday 08:00–09:00) for all sites
  - Wirral site: 24-hour composite sample using an autosampler
  - Treated effluent sampled periodically at the same times
- Sample handling: immediate transport, 4 °C storage, processing within 24 hours; aliquots frozen at -80 °C for further analyses

## Laboratory and Analytical Methods
- Wastewater processing:
  - Pasteurisation of samples (60 °C for 90 min) before analyses
  - Physicochemical analyses: ammonium, nitrate, phosphate, EC, pH (colorimetric and standard meters)
- Concentration and nucleic acid extraction:
  - Influent: 50–100 mL, centrifuged; supernatant concentrated to 500 µL
  - Effluent: tangential flow ultrafiltration (100 kDa) followed by concentrator steps
  - Internal control: murine norovirus (MNV) spike-in to monitor extraction and inhibition
  - Nucleic acids extracted with NucliSENS MiniMag system; elution 50–100 µL
  - Extractions and qPCR setups performed in separate labs to minimize contamination
- q(RT-)PCR assays:
  - SARS-CoV-2 targets: N1 and E gene
  - CrAssphage quantified as a marker of human fecal loading
  - MNV used as process control
  - Reactions run in duplicate; 5 µL of extract used per reaction (with adjustments if inhibition detected)
  - Standards: plasmids for SARS-CoV-2 targets; synthetic oligos for MNV and CrAssphage
- Assay performance:
  - LoD for N1, E, and MNV: 1.7, 3.8, and 3.1 gc µL^-1 respectively
  - LoQ for N1, E, and MNV: 11.8, 25.1, and 32.1 gc µL^-1 respectively

## Assays and Detection Details
- SARS-CoV-2 (N1) primers and probes specified; E gene primers and probe specified
- MNV used as an extraction/control and quantified in triplex or duplex formats
- CrAssphage qPCR follows established protocols; specific primer/probe sets and cycling conditions provided
- Detection status fields: cov_class, cov_detect (N gene concentration above LoD/LoQ vs. detection below LoD)
- E_class provides analogous classification for E gene

## Data Columns and Quality Flags
- Covariate fields indicate detection/quantification status (e.g., Quantified, Detected, Low amplification, No amplification)
- Local authority population and population equivalents enable normalization and spatial comparisons
- Rolling sums (7-day) for clinical data allow temporal trend analysis

## Spatial and Epidemiological Context
- Data linked to six WWTP sites and their corresponding local authorities
- Clinical data include daily cases, cumulative cases, and 7-day rolling sums
- Population context provided via Local_Authority_Population and Population_Equivalent
- Spatial reference implied by site locations (Gwynedd, Cardiff, Liverpool, Manchester, Wirral, Wrexham) and supplementary mapping in the source document

## Potential GIS Uses
- Map-based visualization of SARS-CoV-2 RNA concentrations (N1 and E) by site over time
- Spatial analysis by local authority boundaries to explore correlations with clinical cases, deaths, and 7-day rolling sums
- Normalization analyses using CrAssphage as a human fecal marker to compare across sites with different wastewater loadings
- Integrate wastewater metrics with physico-chemical parameters (NO3, NH4, PO4, pH, EC) to identify environmental drivers
- Temporal GIS analyses combining site-level data with calendar weeks and dates for dashboards and policy-facing tools

## Licensing and Citation
- Open Government Licence required for data use
- Proper citation of Hillary et al. (2021) dataset in any outputs or analyses

## References
- Centers for Disease Control and Prevention (2020)
- Corman et al. (2020)
- Farkas et al. (2019, 2021)
- Kitajima et al. (2010)
- Miranda et al. (2001)
- Mulvaney (1996)
- Murphy & Riley (1962)
- Stachler et al. (2017, 2018)