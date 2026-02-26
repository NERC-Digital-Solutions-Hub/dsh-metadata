# Climoor field site in Clocaenog forest. Supporting documentation for data

## Overview
- Climate change manipulation experiment ( initiated 1998 ) at Clocaenog Forest, Wales, using automated roof technology to implement drought and warming treatments.
- Focuses on delivering long-term environmental health measurements to scrutinise and inform policy and future decisions.
- Provides micro-meteorological, soil and ecosystem data (2016–2021 for the micromet data file) with supporting site context and treatment information.

## Data access and citation
- Data available at: https://doi.org/10.5285/5d90d356-5b2c-4ce0-927a-e26efacff015
- Licensing: Open Government Licence (compliance required).
- Citation: Reinsch, S.; Brooks, M.; Emmett, B.A. (2022). Daily plot level (micro meteorological) data at Climoor field site in Clocaenog Forest 2016-2021. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/5d90d356-5b2c-4ce0-927a-e26efacff015

## Data structure
- Single dataset file: clm_micromet_2016-2021_summaryqa.csv (28 columns).
- Data gaps: entries recorded as "NA"; faulty data replaced by -9999.
- Example variables include:
  - TSoil5cm_Plot1_degC, TSoil5cm_Plot2_degC, etc. (soil temperature at 5 cm depth by plot)
  - TSoil20cm_Plot1_degC, TSoil20cm_Plot2_degC, etc. (soil temperature at 20 cm depth by plot)
  - Soil_moisture_Plot1_m3_per_m-3, Soil_moisture_Plot2_m3_per_m-3, etc. (volumetric soil moisture)

## Site context
- Location: Clocaenog Forest, North East Wales (53°03'19"N, -03°27'55"W)
- Ecosystem: upland west-atlantic moorland dominated by Calluna vulgaris (heather); bryophytes present.
- Vegetation and biomass (1998 baseline): Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum, Deschampsia flexuosa, several bryophytes; bryophytes prominent in 1998 biomass (~73% cover).
- Soil: humo-ferric podzol with horizon variability (E and Bh horizons not always visible); detailed soil chemistry and mineralogy provided (C, N, base cations, CEC, etc.).
- Climate context (1997–2014): mean air temp ~8.0°C; mean soil temp in control ~7.5°C; mean annual rainfall ~1411 mm; total N deposition ~20–25 kg N ha^-1 yr^-1.

## Climate change treatment information
- Experimental design: two treatments (drought and warming), each with three replicate plots; three control plots with scaffolding to mirror shading, total of 9 plots.
- Drought treatment:
  - Mechanism: retractable polyethylene roof triggered by tipping-bucket rainfall sensor; reduces annual rainfall by ~20% (varies by year); ensures exclusion of ~80% of rain during active period.
  - Active period: generally May–September (varied across years; 1999–2011; later adjustments to April–October since 2012).
  - Constraints: roof operation halted in high winds (>10 m s^-1); by 2016 rainfall patterns caused water accumulation on roofs preventing full retraction; replacements planned in 2017.
- Warming treatment:
  - Mechanism: retractable aluminum mesh curtains increasing infrared reflectance (96–97%), reducing night-time heat loss; automatically retracted during rain to preserve rainfall.
  - Control logic: activated after 15 minutes of darkness (below 200 lux); rain detected triggers roof retraction to protect rainfall; some rainfall exclusion remains due to lag.
  - Maintenance: new frames installed on top of old ones in 2017 due to frame degradation; wind safety measures in place.
- Operational details (selected years):
  - Drought: annual reductions in rainfall reported per year (e.g., 1999: 28% annual reduction, 79% growing-season; 2000: 14%/56%; etc.); 2016 onward, drought roofs not in operation due to refurbishments and rainwater accumulation.
  - Warming: reported growing degree days (GDD) changes to quantify warming effect; data for several years show varying % change in GDD due to warming.
- Data and maintenance notes:
  - Frame refurbishment and replacement occurred in 2017.
  - Some years show missing or unreliable data due to sensor issues (e.g., rainfall sensor broken since 2018) and COVID-related disruptions.

## Equipment, protocols and data processing methodology
- Automated Weather Station (AWS) on site providing meteorological data (daily):
  - Sensors measure: air temperature, relative humidity, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction, etc.
  - Data cadence: minute-sampled; hourly averages produced for the dataset.
- Micro-meteorological plot data (plot-level measurements) include soil and air temperatures, soil moisture (TDR sensors since 2008; earlier proxy methods).
- Other measurements (not all stored in EIDC): rainfall volume and chemistry (biweekly), throughfall (plot-level rainfall, biweekly), water table depth (fortnightly), soil respiration, trace gas measurements (CH4, N2O), net ecosystem CO2 exchange, vegetation surveys, canopy reflectance, phenology, vegetation chemistry, litterfall, root biomass, soil microbial biomass, nitrogen mineralisation, soil organic matter and carbon metrics, soil solution chemistry.
- Data quality and processing:
  - Early micro-meteorological data (1997–2008) described; post-2008 data are more standardized.
  - Data quality control primarily via visual/manual checks in Excel; no strict automated limits described in the text.
  - Some data are infrequently collected; not all datasets stored in EIDC; requests for details via contact.

## Data types and storage
- Micro-meteorological plot data: high-frequency measurements (minute sampling, hourly/daily/half-hourly aggregation depending on period).
- AWS and plot datasets: multiple variables with explicit units and sensors listed (temperature, humidity, radiation, rainfall, PAR, etc.).
- Rainfall and throughfall data: separate site-level rainfall (storage gauge, biweekly) and plot-level throughfall (biweekly), with methods to reconcile and compute treatment-specific rainfall totals.

## Data governance, sharing and caveats
- Some datasets not fully stored in the Environmental Information Data Centre (EIDC); contact authors for full details.
- Licensing requires compliance with Open Government Licence; data sharing and metadata quality depend on dataset originators.
- Metadata quality varies; some datasets require contacting data originators to fill gaps or clarify provenance.

## Practical implications for monitoring framework authors
- Demonstrates a comprehensive climate manipulation experiment with clearly defined treatments, replication, and control, useful for testing monitoring metrics and governance workflows.
- Highlights common data governance challenges: data availability, metadata completeness, data standardization, and sharing constraints.
- Provides a concrete example of linking treatment design and resulting environmental measurements (soil temperature, soil moisture, throughfall, rainfall, etc.) to policy-relevant monitoring objectives.
- Illustrates the need for robust data processing, documentation, and transparency around data gaps, sensor failures, and maintenance events that affect long-term datasets.