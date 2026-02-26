# Overview

- A dataset describing field sensor physicochemical and optical/fluorescence measurements, plus laboratory microbiological and chemical analyses, for urban surface water samples in Kolkata, India.
- Data collected across three field surveys (June 2018, March 2019, December 2019) with GPS coordinates provided for all sample locations.
- Purpose: to develop and test a prototype multichannel fluorimeter for identifying waters with high bacterial load and contamination events via Peak T fluorescence; used to inform sensing technology adaptations for India.

## Spatial and sampling coverage

- Urban Kolkata focus with sampling sites in three main watercourse types: Hooghly River (Ganga), East Kolkata Wetlands, and open sewage canals.
- Some samples outside Kolkata urban area used as marine and groundwater controls (RS1_DHG and RS1_NLH).
- Sampling locations selected for safe access; some sites revisited for seasonal/diurnal comparisons.
- Total of 40 samples analyzed over two years (across three surveys).

## Data collected and parameters

- In-field measurements: electrical conductivity (EC), pH, dissolved oxygen concentration (DO_c) and temperature; field equipment varied by survey.
- Laboratory analyses: nutrients (ammonia, ammonium, phosphate, nitrate, nitrite; with total phosphorus, soluble reactive phosphorus, dissolved organic carbon; major ions such as fluoride, chloride, sulphate), and dissolved nutrients (e.g., DOC, TDN).
- Microbiology: Escherichia coli and total coliforms (plus total coliforms excluding presumptive E. coli) via membrane filtration; total bacterial cells counted by flow cytometry after glutaraldehyde fixation.
- Fluorescence and optical measurements: prototype in-situ fluorimeter data (Peak T fluorescence, Peak C fluorescence, chlorophyll-a, tryptophan, CDOM, turbidity, absorbance at 280 nm) with averaging over 1 minute (n = 60) or single readings where logging issues occurred.
- Controls/reference samples included municipal water supply and laboratory deionised water.
- Samples collected in 2 L subsamples; subsequent subsampling for field measurements and laboratory analyses.

## Field and laboratory methods

- Field collection: ~1 m from water edge, 2 L bucket; triple rinse prior to sampling; time, date, and GPS recorded.
- In-field physicochemical monitoring: DO, conductivity, and pH measured in June 2018 and March 2019 with HOBO/analog meters; December 2019 used Ultrameter 6Pfc for EC, TDS, ORP, pH, and temperature.
- Nutrient and chemical analyses: Palintest photometer for ammonium, ammonium, phosphate, nitrate, nitrite; CEH (UK) for total phosphorus, total dissolved phosphorus, soluble reactive phosphorus, dissolved ammonium, DOC, and major ions via ion chromatography.
- Microbiological analyses: filtration onto MLGA plates for E. coli and coliforms; flow cytometry for total bacteria counts on fixed samples with SYBR Green I staining and bead calibration.
- In-situ fluorimeter: 2018 Chelsea single-channel sensors; 2019 onward VLux five-channel fluorimeter with internal corrections for absorbance, turbidity, and temperature; data logged at depth (30 cm) or by custom data loggers; averages computed over 1 minute (n=60) unless noted.

## Data structure and files

- Three CSV files:
  - File 1: 1_KolkataWQ_Jun2018.csv (20 columns). Includes date, time, sample ID, latitude, longitude, EC, pH, DO, Temp, phosphate, nitrate, E. coli, coliforms, total coliforms, and fluorescence/turbidity/absorbance fields with average and standard deviation over 1 minute.
  - File 2: 2_KolkataWQ_Mar2019.csv (37 columns). Expanded set of fields including additional nutrient measurements, nitrite, ammonia, and total/bacterial fluorescence metrics; includes total bacterial cells and chlorophyll-a data with 1-minute averages and SD.
  - File 3: 3_KolkataWQ_Dec2019.csv (33 columns). Similar structure with field measurements, DO, temperature, nutrients, E. coli, coliforms, TCs, fluorescence channels, turbidity, absorbance, and 1-minute averaged metrics.
- Columns typically include: Date, Time, Sample_ID, Latitude, Longitude, EC, pH, DO_c, Temp, NH4, PO4, NO2, NO3, E_coli, Coliforms, TCs, Total_bact_cells, V_Chl-a, V_TRYP, V_TRYP_SD, V_CDOM, V_CDOM_SD, V_Turbidity, V_Turbidity_SD, V_Abs280, V_Abs280_SD, SRP, TP, NH4_N, F, Cl, NO2, NO3, SO4, DOC, SRP, TP, NH4_N, and related SD columns for each parameter.
- Note: Completeness issues include discarded Aqualog excitation-emission data due to sample integrity concerns; some File 3 logging entries are single values due to field data logging issues; NA used for missing values.

## Data quality, limitations, and nuances

- Aqualog fluorescence data (excitation-emission matrices) discarded due to sample age/storage/transport concerns.
- Field logging issues in December 2019 led to some single-value records instead of averages; some data recorded by hand.
- Missing values labeled as NA; Spanish-like standard data structure with explicit SD values where possible.
- Prototyping context: data collected to support sensor development and validation for real-world deployment in Indian urban waters.

## GIS relevance and potential use

- Geospatial context established via latitude and longitude for all sampling sites, enabling mapping of water quality by location and watercourse type.
- Multimodal dataset supports spatial analysis of nutrients, microbial contamination, and fluorescence-based indicators across Hooghly River, East Kolkata Wetlands, and sewage canals.
- Can be integrated with environmental layers (morphology, land use, hydrology) to identify pollution sources and temporal-spatial trends.
- Suitable for creating map-based data products and dashboards that communicate bacterial risk indicators and nutrient status to policy colleagues, clients, or the public.

## Provenance and references

- Bowes, M.J., Read, D.S., Joshi, H., et al., 2020. Nutrient and microbial water quality of the upper Ganga River, India: identification of pollution sources. Environmental Monitoring and Assessment, 192. https://doi.org/10.1007/s10661-020-08456-2.