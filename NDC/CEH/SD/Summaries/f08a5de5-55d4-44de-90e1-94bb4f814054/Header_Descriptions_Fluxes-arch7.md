# Header Descriptions for Dataset "CO2_Flux_Data" and "CH4_N2O_Flux_Data"

## Header Descriptions for Dataset "CO2_Flux_Data"
- Purpose: Defines the meaning and units of header fields for CO2 flux measurements across plots and sampling times, enabling data interpretation and GIS-based visualization.
- Temporal identifiers:
  - Date: Date data were collected.
  - DateNumber: Sequential sampling day identifier (1, 2, …).
  - SamplingPeriod: Identifier for sampling period (e.g., June 2012 = 1, Sept 2012 = 2, June 2013 = 3, July 2014 = 4).
- Spatial and site information:
  - Site: Site name.
  - Age: Site age since last wildfire (years).
  - Plot: Plot or chamber number.
- Flux measurements and derived metrics:
  - Respiration: Ecosystem respiration (mg CO2-C m-2 h-1) measured with EGM-4 IR gas analyser (dark chamber).
  - NEE: Net Ecosystem Exchange (mg CO2-C m-2 h-1); positive = net CO2 emission, negative = net CO2 uptake; measured with EGM-4 IR gas analyser (light chamber).
  - Photosynthesis: Gross CO2 uptake (mg CO2-C m-2 h-1), derived from Respiration and NEE.
- Biomass and soil properties:
  - Biomass: Final dry biomass in plot (g).
  - BD: Bulk density of soil organic horizon (g cm-3).
  - PercentC, PercentN, CN: Carbon, nitrogen, and carbon-to-nitrogen ratio in soil organic horizon.
  - OrgDepth: Depth of the organic horizon (cm).
- Environmental and microclimate variables:
  - Temperature: Air temperature at sampling (°C) using Tinytag data loggers.
  - Par: Photosynthetically Active Radiation (μmol m-2 s-1) using Skye Instruments PAR sensor.
  - Soil-related temperatures and moisture:
    - Soil1cm1, Soil5cm1, Soil1cm24, Soil5cm24: Soil temperatures at 1 cm and 5 cm below ground for 1-hour and 24-hour averaging, respectively (°C).
    - SM1, SM24: Soil moisture averaged over 1 hour and 24 hours (m3/m3).
  - AirTemp1: Air temperature averaged over 1 hour (°C).
  - LWCount1, LWCount24: Leaf Wetness Count averaged over 1 hour and 24 hours.
- Vegetation cover (% cover by species and groups):
  - P.Schreberi, V.myrtillus, V.vitis-idaea, V.uliginosum, D.flexuosa, P.commune, Lichen, Daisy, Equisetum, Galium, Luzula, Cladonia, E.angustifolium, Vicia, L.borealis, Moss, Shrub (percent cover by respective species or groups; note totals can exceed 100% for some groups like Moss or Shrub).
- Measurement devices and conventions:
  - Tinytag by Gemini Data Loggers for temperature.
  - Skye Instruments PAR Quantum Sensor for light.
  - EGM-4 infrared gas analyser with dark/light chambers for respiration, NEE, and CO2 flux measurements.
- Notes:
  - Data are organized to support GIS-based mapping of CO2 flux features by site and plot with accompanying environmental and vegetation covariates.

## Header Descriptions for Dataset "CH4_N2O_Flux_Data"
- Note: Most fields are the same as in the CO2 flux data, enabling consistent linkage and GIS visualization across gas flux datasets.
- New columns (specific to CH4_N2O data):
  - Ch4Flux, 1: CH4 flux from the plot, μg CH4-C m-2 hr-1.
  - Co2Flux, 1: CO2 flux from the plot, μg CO2-C m-2 hr-1.
  - N2oFlux, 1: N2O flux from the plot, μg N2O-N m-2 hr-1.
- Usage: These CH4 and N2O fields augment the CO2 dataset, allowing multi-gas flux analyses and spatial visualization alongside the same temporal, spatial, and environmental covariates described for CO2.
- Format consistency: Leverages the same header definitions for dates, sites, plots, sampling periods, environmental measurements, soil properties, and vegetation cover to ensure cohesive GIS-ready data products.