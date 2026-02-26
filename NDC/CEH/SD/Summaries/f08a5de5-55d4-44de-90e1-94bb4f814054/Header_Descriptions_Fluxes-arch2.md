# Header Descriptions for Dataset "CO2_Flux_Data"

- Purpose: Defines the header fields for CO2 flux measurements across plots/soil chambers, enabling standardized recording of gas exchange and related environmental context over time.
- Scope: Includes core flux metrics, environmental drivers, soil and vegetation characteristics, and temporal/site metadata to support monitoring and analysis of environmental health and policy performance.

## Key fields and what they capture

- Sampling and time metadata
  - Date: Date data were collected.
  - DateNumber: Sequential sampling day identifier (1, 2, …).
  - SamplingPeriod: Identifier for sampling period (e.g., June 2012 = 1, Sept 2012 = 2, June 2013 = 3, July 2014 = 4).
- Site and plot context
  - Site: Site name.
  - Age: Site age since last wildfire (years).
  - Plot: Plot or chamber number.
- Gas exchange and derived fluxes
  - Respiration: Ecosystem respiration from the plot (mg CO2-C m-2 h-1) measured with EGM-4 IR gas analyser (dark chamber).
  - NEE: Net Ecosystem Exchange (mg CO2-C m-2 h-1); positive = net emission, negative = uptake; measured with light/dark chamber setup.
  - Photosynthesis: Gross CO2 uptake (mg CO2-C m-2 h-1), derived from Respiration and NEE (calculated as Respiration - NEE).
- Biomass and soil properties
  - Biomass: Final dry biomass in plot (g).
  - BD: Bulk density of soil organic horizon (g cm-3).
  - PercentC / PercentN: Percent total carbon and nitrogen in the soil organic horizon.
  - CN: Carbon-to-nitrogen ratio.
  - OrgDepth: Depth of the organic horizon (cm).
- Microclimate and soil thermal metrics
  - Temperature: Air temperature at the time of sampling (°C); measured by Tinytag.
  - Par: Photosynthetically Active Radiation (μmol m-2 s-1); measured by Skye PAR sensor.
  - Soil1cm1 / Soil5cm1: Soil temperature at 1 cm and 5 cm depth, averaged over 1 hour prior to sampling (°C).
  - Soil1cm24 / Soil5cm24: Soil temperature at 1 cm and 5 cm depth, averaged over 24 hours prior to sampling (°C).
  - AirTemp1: Air temperature averaged over 1 hour prior to sampling (°C).
  - SM1 / SM24: Soil moisture averaged over 1 hour and 24 hours prior to sampling (m3/m3); Decagon devices.
  - LWCount1 / LWCount24: Leaf wetness count averaged over 1 hour and 24 hours (0–heavy range; 445 dry to 1400 heavy rain) from Decagon devices.
- Vegetation cover (percent cover)
  - P.Schreberi, V.myrtillus, V.vitis-idaea, V.uliginosum, D.flexuosa, Dicranum, P.commune, Lichen, Daisy, Equisetum, Galium, Luzula, Cladonia, E.angustifolium, Vicia, L.borealis, Moss, Shrub: Percent cover for individual species or groups; totals can exceed 100% for moss/shrub categories.
- Ground flora and moss summaries
  - Moss: Total percentage cover by all moss species.
  - Shrub: Total percentage cover by all shrub species.

## CH4 and N2O flux extension

- Note: Most header fields are the same as CO2_Flux_Data.
- New columns (CH4_N2O_Flux_Data)
  - Ch4Flux: CH4 flux from the plot (μg CH4 cm-2 h-1).
  - Co2Flux: CO2 flux from the plot (μg CO2 cm-2 h-1).
  - N2oFlux: N2O flux from the plot (μg N2O-N cm-2 h-1).

## Data quality, standardization, and delivery

- Standardized data handling: Data are understood, verified, quality assured, cleaned, and transformed to enable comparable outputs.
- Outputs: Facilitates the production of clear reports, maps, and charts to communicate environmental health and policy performance over time.
- Data governance: Datasets are stored and uploaded to appropriate portals to ensure accessibility and reusability.

## How this supports environmental monitoring and analysis

- Provides a comprehensive, time-series-ready set of flux measurements (CO2, CH4, N2O) with rich environmental and vegetation context.
- Supports cross-dataset integration by using common sampling and site metadata (DateNumber, SamplingPeriod, Site, Age, Plot).
- Enables scrutiny of ecosystem carbon balance and greenhouse gas flux drivers across time and wildfire-affected sites.
- Aligns with the Analysts Monitoring the Environment approach: verified, standardized, and accessible datasets suitable for reporting and policy evaluation.