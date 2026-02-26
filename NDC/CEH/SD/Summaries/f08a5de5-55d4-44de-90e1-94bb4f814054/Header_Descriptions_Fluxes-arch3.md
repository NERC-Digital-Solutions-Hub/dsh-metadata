# Header Descriptions for Dataset "CO2_Flux_Data" and "CH4_N2O_Flux_Data"

## Overview
- Defines the header fields and data types for gas flux measurements (CO2, CH4, N2O) from plots across sites and sampling periods.
- Captures both flux measurements and rich environmental context to support assessment of ecosystem carbon exchange and drivers, informing monitoring and policy scrutiny.

## CO2_Flux_Data: Key Fields

- Sampling metadata
  - Identifier, Date, DateNumber, SamplingPeriod
  - Site, Age (years since last wildfire), Plot
  - Biomass

- Flux measurements
  - Respiration: mg CO2-C m-2 h-1
  - NEE (Net Ecosystem Exchange): mg CO2-C m-2 h-1
    - Positive value = net CO2 emitted; negative = net CO2 taken up
  - Photosynthesis: mg CO2-C m-2 h-1
  - Derived relationships (where applicable): Photosynthesis calculated as Respiration − NEE

- Environmental context
  - Temperature: air temperature (°C)
  - PAR: Photosynthetically Active Radiation (μmol m-2 s-1)
  - AirTemp1 (°C)

- Instrumentation and methods
  - Tinytag data logger (air temperature measurements)
  - Skye Instruments PAR sensor
  - EGM-4 infrared gas analyser
    - Dark chamber lid (for respiration)
    - Light chamber lid (for NEE)

- Soil and organic horizon properties
  - BD: Bulk density (g cm-3)
  - PercentC: Percent total carbon
  - PercentN: Percent total nitrogen
  - CN: Carbon-to-nitrogen ratio
  - OrgDepth: Depth of organic horizon (cm)

- Soil microclimate and moisture
  - SM1 / SM24: Soil moisture (m3/m3), averaged over 1 hour and 24 hours prior to sampling
  - LWCount1 / LWCount24: Leaf Wetness Count (dimensionless), averaged over 1 hour and 24 hours
  - Soil1cm1 / Soil5cm1: Soil temperature at 1 cm and 5 cm below ground (°C), 1-hour averages
  - Soil1cm24 / Soil5cm24: Soil temperature at 1 cm and 5 cm below ground (°C), 24-hour averages

- Vegetation cover (percent cover by species)
  - P.Schreberi, V.myrtillus, V.vitis-idaea, V.uliginosum
  - D.flexuosa, Dicranum sp., P.commune, Lichen, Daisy, Equisetum
  - Galium, Luzula, Cladonia, E.angustifolium, Vicia, L.borealis
  - Moss, Shrub
  - (Numerous additional taxa indicating overall vegetation composition and cover)

## CH4_N2O_Flux_Data: Key Fields

- Shared fields with CO2_Flux_Data
  - Most columns are described as the same as in CO2 Flux Data, providing consistent metadata and environmental context

- New flux measurements (per plot)
  - Ch4Flux: CH4 flux from the plot (μg CH4-C m-2 h-1)
  - Co2Flux: CO2 flux from the plot (μg CO2-C m-2 h-1)
  - N2oFlux: N2O flux from the plot (μg N2O-N m-2 h-1)

- Units and interpretation
  - CH4Flux uses μg CH4-C m-2 h-1
  - N2oFlux uses μg N2O-N m-2 h-1
  - Co2Flux uses μg CO2-C m-2 h-1

## Data Use and Monitoring Implications
- The datasets provide a comprehensive suite of environmental health measures:
  - CO2 flux dynamics (respiration, net exchange, and gross photosynthesis)
  - CH4 and N2O flux measurements to broaden greenhouse gas assessment
  - Environmental covariates (temperature, moisture, PAR, leaf wetness) and soil/vegetation context to interpret flux variability
- Rich metadata supports data governance, traceability, and cross-site/time comparisons, aligning with monitoring framework needs for transparency and policy scrutiny.