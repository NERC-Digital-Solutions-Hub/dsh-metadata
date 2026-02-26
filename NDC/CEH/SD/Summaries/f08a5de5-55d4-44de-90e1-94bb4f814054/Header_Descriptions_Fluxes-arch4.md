# Header Descriptions for Dataset CO2_Flux_Data and CH4_N2O_Flux_Data

## Overview
- The document provides header descriptions (data dictionary) for two datasets: CO2_Flux_Data and CH4_N2O_Flux_Data.
- CH4_N2O_Nflux dataset notes that most headers are the same as CO2_Flux_Data, with three new flux columns.

## CO2 Flux Data: Key Header Fields
- Time and sampling identifiers: Identifier, Date, DateNumber, SamplingPeriod.
- Location and plot context: Site, Age, Plot.
- Biological and environmental measurements: Biomass, Temperature (air), Par (PAR), Respiration, NEE (Net Ecosystem Exchange), Photosynthesis, BD (bulk density), PercentC, PercentN, CN (C:N ratio), OrgDepth.
- Instrumentation: Temperature sensors and PAR/measurement devices (Tinytag, Skye PAR Sensor, EGM-4 IR gas analyzer with dark lid).
- Flux components and calculations: Respiration (mg CO2-C m-2 h-1), NEE (mg CO2-C m-2 h-1; sign convention given), Photosynthesis (mg CO2-C m-2 h-1).
- Soil and physical properties: Soil moisture (SM1, SM24), Leaf Wetness (LWCount1, LWCount24), Soil temperatures at 1 cm and 5 cm (Soil1cm1, Soil5cm1; and 24-hour versions Soil1cm24, Soil5cm24), AirTemp1.
- Soil chemistry and depth: PercentC, PercentN, CN, OrgDepth (as above).
- Vegetation and ground cover: Extensive set of percent cover fields for many species and vegetation types (e.g., P.Schreberi, V.myrtillus, V.vitis-idaea, V.uliginosum, Deschampsia flexuosa, Dicranum, Polytrichum commune, Lichen, Daisy, Equisetum, Galium, Luzula, Cladonia, Eriophorum, Linnaea borealis, Moss, Shrub). Notes that certain lines indicate total cover can exceed 100%.

## CH4/N2O Flux Data: New and Shared Fields
- New fields specific to CH4/N2O dataset: Ch4Flux (μg CH4 m-2 h-1), Co2Flux (μg CO2 m-2 h-1), N2oFlux (μg N2O-N m-2 h-1).
- Most headers are shared with CO2_Flux_Data (time, site, plot, environmental measurements, and vegetation cover fields).

## Common Data Characteristics and Units
- CO2-related fields use mg CO2-C m-2 h-1 for respiration, NEE, and photosynthesis calculations.
- CH4/N2O fields use flux units in μg per m2 per hour for the three gases.
- Data capture relies on specific instruments:
  - EGM-4 infrared gas analyzers (with dark and light chamber lids) for CO2/Net CO2 flux measurements.
  - Decagon devices for soil moisture, soil temperature, and leaf wetness.
  - Tinytag and Skye Instruments sensors for temperature and PAR.
- Extensive metadata on sampling periods, site age, plot identifiers, and vegetation composition.

## Data Management and Quality Considerations
- The dataset structure emphasizes time- and location-specific context (DateNumber, SamplingPeriod, Site, Plot).
- Detailed coverage of soil properties, microclimate, and vegetation indicates a need for careful standardization of units and naming to ensure cross-dataset compatibility.
- Presence of numerous vegetation cover fields (some with notes on potential >100% totals) suggests attention to data validation and consistency.
- Alignment between CO2, CH4, and N2O datasets is important for integrated analyses (shared fields vs. gas-specific flux fields).

## Implications for Data Strategy (Data Leaders)
- Ensure consistent data standards across CO2 and CH4/N2O datasets to enable seamless integration and comparison.
- Prioritize metadata completeness and clear unit definitions to support discoverability and reuse.
- Address potential data gaps and quality issues arising from the extensive vegetation cover taxonomy and measurement instruments.
- Foster data governance around shared header schemas to support co-ownership and cross-network collaboration.