# Ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, 2022

## Purpose and scope
- Report initial results from a study to determine the uptake rate for ALPHA® passive samplers used to measure ammonia (NH3) in air.
- Samplers prepared and analyzed at UKCEH Edinburgh; local site operator duties conducted by UKCEH, AFBI Hillsborough, and Ricardo AEA; analysis by CEH Edinburgh.
- Samplers exposed in monthly cycles at the start of each month; data provide an ammonia concentration in air for specified exposure periods.

## UKCEH ALPHA® sampler method
- Passive sampler design: citric acid coated filter to capture NH3, protected by a white PTFE membrane; membrane faces downward during exposure; exposed end sealed with protective cap when not exposed.
- Deployment: replicate samplers mounted on shelters on poles/posts at about 1.5 m above ground; multiple replicates for reliable concentration estimates.
- Analysis workflow: exposed samplers extracted into deionised water; NH3 concentration determined by SEAL AA3 colorimetry; concentration in air calculated using a known uptake rate (0.0038422 m3 hr-1) and exposure duration.
- Data quality notes: measurements flagged if concerns arise (details on page 4).

## Data quality and handling
- QA rules applied to raw data to assess validity:
  - Coefficient of variation (CV) of replicates: CV < 15% deemed acceptable; if >15%, replicates reviewed, some may be discarded; data flagged as valid (103) if representative.
  - Calibrations: values above calibration range may be reported if dilution/reanalysis not possible due to instrument failure.
  - Missing data: represented as -9999 in measurement field or missing date/time metadata; such entries render concentration calculations impossible.
- Final data product: submissions_ED_UR_NH3_2022.csv containing accepted data values with appropriate flags; site names and spatial identifiers provided (see page 5 and page 3 for dataset contents).
- Data flags and metadata explained:
  - EMEP flags detail data status and quality (codes listed, e.g., data capture, validation status, data issues, etc.).
  - Examples of EMEP flag meanings include: CV-related validity (e.g., 103), detection/quantification considerations (e.g., 781, 780), contamination or local influence notes, sampling period adjustments, and other validity notes.
- Dataset structure highlights:
  - Each row represents one month of data for a single site.
  - Columns include: site_id, site_name, network_id (ED_UR), parameter_id (e.g., alpha_NH3_g), measurement start and end dates/times, measurement value (ammonia concentration in µg NH3 m-3), less-than flag, verification id, unit id (µg NH3 m-3), data capture, validity, EMEP code, Month-Year, and Comments.

## Dataset and field details
- Final dataset name: submissions_ED_UR_NH3_2022.csv
- Measurement units: micrograms of NH3 per cubic metre of air (µg NH3 m-3); all concentrations are average values for the specified exposure period.
- Key fields and meanings:
  - Site id, Site name, network_id (ED_UR), parameter_id (alpha_NH3_g)
  - Measurement start date/time; measurement end date/time
  - Measurement (ammonia concentration)
  - Less than (<) flag for values below detection limit (0.03 µg NH3 m-3)
  - Verification id (Not verified, Preliminary verified, Verified)
  - Unit id (24 = µg NH3 m-3)
  - Data capture percentage; Validity_id (1 = valid, -1 = not valid)
  - EMEP code and related flags (data status and quality indicators)
  - Month-Year and Comments

## Site information and spatial context
- Four Edinburgh uptake rate sites (collocated with UKEAP identifiers):
  - Edinburgh uptake rate OTC
    - Start: 01/03/2020; End: ongoing
    - Latitude: 55.863150; Longitude: -3.209845
    - Inlet height: 1.5 m above ground
    - Details: Collocated with UKEAP UKA00128
  - Edinburgh uptake rate Auch
    - Start: 01/03/2020; End: ongoing
    - Latitude: 55.792160; Longitude: -3.242900
    - Inlet height: 1.5 m
    - Details: Collocated with UKEAP UKA00451
  - Edinburgh uptake rate Hills
    - Start: 01/03/2020; End: ongoing
    - Latitude: 54.452500; Longitude: -6.083340
    - Inlet height: 1.5 m
    - Details: Collocated with UKEAP UKA00293
  - Edinburgh uptake rate Chilbolton
    - Start: 01/01/2021; End: ongoing
    - Latitude: 51.149617; Longitude: -1.438228
    - Inlet height: 1.5 m
    - Details: Collocated with UKEAP UKA00614
- Spatial identifiers and coordinates are provided to enable GIS mapping and spatial analysis of NH3 concentrations across sites.

## GIS-relevant takeaways
- Data are organized for map-ready presentation: monthly NH3 concentrations per site with precise coordinates and metadata.
- Replicate sampling and HQA QA rules improve data reliability for spatial analyses and policy-relevant mapping.
- Clear data flags, metadata, and EMEP codes facilitate filtering by data quality for GIS visualization and downstream analyses.
- The dataset supports monitoring ammonia in UK climates and can be integrated into spatial dashboards showing temporal trends and site-specific emissions assessment.