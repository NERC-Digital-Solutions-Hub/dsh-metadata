# Climoor field site in Clocaenog forest. Supporting documentation for data

## Overview
- Describes the Climoor/Clocaenog climate change manipulation experiment (initiated 1998) using automated roof technology to create drought and warming treatments reflecting near-future climate scenarios.
- Data assets include meteorological, abiotic, and biotic measurements from drought and warming plots, with a primary data file (CLM_AWS_2024_summaryQA.csv) plus associated site metadata and protocols.
- Intended for monitoring framework authors to assess data provenance, quality, accessibility, and governance for environmental health monitoring.

## Data access
- Data available from the Environmental Information Data Centre (EIDC) under the dataset: Daily automated weather station (AWS) data from Climoor field site in Clocaenog forest.
- Access link: https://catalogue.ceh.ac.uk/documents/198980ac-8f5e-4a16-b1c0-bc6d61516b99

## Data structure
- One CSV file: CLM_AWS_2024_summaryQA.csv
- Size: 10 columns, 367 rows
- Data coding: missing values as NA; faulty data replaced with -9999
- Column descriptions include: Date (YYYY-MM-DD), Mean air temperature (degC), Min/Max air temperature (degC), Rainfall (mm), Air pressure (mbar), Solar radiation (kW/m2), Photosynthetically active radiation (µmol m-2 s-1), Wind speed (m s-1), Wind direction (degrees)

## Site information
- Location: Clocaenog Forest, North East Wales (53°03'19''N, -03°27'55''W)
- Habitat: upland moorland dominated by Calluna vulgaris (heather); bryophyte-rich understory
- Climate (1997–2014): mean air temperature ~8.0°C; mean soil temperature ~7.5°C; mean annual rainfall ~1411 mm
- Nitrogen deposition: ~20–25 kg N ha-1 yr-1
- Soil: humo-ferric podzol with variable horizons (Eg and Bh present where visible); soil metrics (N, C, C:N, base cations) provided by horizon
- Vegetation & litter: annual litterfall ~177 g m-2; detailed species composition and biomass data for Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum, Deschampsia flexuosa, bryophytes
- Chemistry: species-specific C, N, C:N, P, K, Ca, Mg, lignin, tannin, α-cellulose, and carbohydrate content in vegetation and litter
- Site characteristics: replicated drought and warming treatments; remote/solar- and wind-powered infrastructure; typical growing season June–August; winter dormancy

## Climate change treatment information
- Treatments: drought and warming, each with three replicated plots; plus three control plots (total n=9) mirrored by scaffolding to equal shading
- Drought treatment: retractable polyethylene roof reduces ~20% annual rainfall; active May–Sept (1999–2011), extended Apr–Oct since 2012; occasional rain-event misses due to detector limits; roofs can be hindered by heavy rainfall accumulation since 2016
- Warming treatment: retractable aluminum mesh curtains reduce infrared loss; night-time warming triggered by light sensor after 15 minutes of darkness with rain-triggered retraction to maintain rainfall; annual rainfall reduction ~14%
- Operational notes: wind >10 m s-1 disables curtain operation; frames upgraded in 2017 (new frames installed atop old ones); some years show incomplete data due to refurbishment, rainfall dynamics, or COVID-related access
- Long-term data: tabled records (Table 6) document annual drought reductions 1997–2014; warming GDD changes (Table 6b) present percent change and calculation method; GDD is computed from plot-level air temperature data

## Equipment, protocols and data processing methodology
- Instrumentation: Automated Weather Station (AWS) plus micro-meteorological sensors inside treatment plots; broad suite of abiotic and biotic measurements
- Data categories (Table 7 overview): AWS meteorological data (humidity, temperature, rainfall, air pressure, net radiation, solar radiation, PAR, wind); plot-level soil and air temperature, soil moisture; rainfall and rain chemistry (ground gauge and throughfall); water table depth; soil respiration; trace gas fluxes (CH4, N2O); net ecosystem CO2 exchange; photosynthesis; vegetation surveys; canopy reflectance; phenology and pathology; vegetation chemistry; litterfall; root and microbial biomass; nitrogen mineralisation; SOC/SOM; soil solution chemistry
- Data cadence: varies by dataset; many sensors log per minute with hourly or half-hourly aggregation; data quality control primarily via manual visual checks in spreadsheets
- Data storage and access: some data stored with EIDC; not all post-2015 data are guaranteed to be in EIDC
- AWS micro-meteorological specifics: sensors for air temperature (HMP 45C), relative humidity (HMP 45C), solar radiation (Skye SP1110), PAR (SKP215), net radiation (NR-Lites), barometric pressure (CS100), rainfall (ARG100 tipping bucket), wind (Windsonic 2D)
- Data handling practices: visual QC in Excel; plots and trends examined; loggers and power interruptions acknowledged

## Data quality, gaps and governance
- Data quality challenges and gaps:
  - Incomplete or missing data in several datasets; some years show data INFILL or exclusion due to measurement issues
  - Rainfall measurement issues: tipping bucket sensor limitations; site-born rainfall sensor broken since Jan 2018
  - Throughfall datasets: occasional data loss when funnels fall off or bottles overflow; missing third replicate data in some periods
  - Drought roof operations interrupted starting 2016 due to water accumulation and refurbishments; COVID-19 affected field access in 2020–2021
  - Some years feature non-availability or formatting gaps in site rainfall data (indicated as "**" for unknown)
- Data governance considerations:
  - Metadata and data sharing practices documented; some data require direct contact with site contacts (Sabine Reinsch, Bridget Emmett) for details
  - Data management standards applied at source for new datasets; open sharing of underlying data prioritized
  - Data accessibility is enabled via EIDC for the primary AWS dataset; other data may require coordinated access or direct inquiry

## Appendix and figures
- Site layout and quadrat schematic provided (Figures 2–4) to illustrate plot arrangement and measurement areas
- Appendix notes include detailed plot mappings and quadrat placements to support reproducibility of measurements and analyses