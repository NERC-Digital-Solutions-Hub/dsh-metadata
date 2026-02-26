# Header Descriptions for Dataset "CO2_Flux_Data" and "CH4_N2O_Flux_Data"

- Purpose and scope
  - Provides metadata header descriptions for two flux datasets: CO2_Flux_Data and CH4_N2O_Flux_Data.
  - Defines how fields are identified, dated, and linked to plots/sites and sampling events.
  - Enables consistent data interpretation, discovery, and integration for analysis and dashboarding.

- Core metadata fields (CO2_Flux_Data)
  - Identifier: Sample Identification for measurement of each plot/gas chamber ring at each sampling time.
  - Date: Date data was collected.
  - DateNumber: Sequential sampling day identifier (1, 2, …).
  - SamplingPeriod: Sequential sampling period (e.g., June 2012 = 1, Sept 2012 = 2, June 2013 = 3, July 2014 = 4).
  - Site: Site name.
  - Age: Site age since last wildfire (years).
  - Plot: Plot/chamber number.
  - Biomass: Final dry biomass in plot (g).
  - Temperature: Air temperature at sampling time (°C; Tinytag by Gemini Data Loggers).
  - PAR (Par): Photosynthetically Active Radiation (μmol m^-2 s^-1; Skye Instruments PAR Quantum Sensor).
  - Respiration: Ecosystem respiration (CO2 emitted from plot) (mg CO2-C m^-2 h^-1; measured with EGM-4 IR gas analyser, dark chamber).
  - NEE: Net Ecosystem Exchange (net CO2 emitted or gained; mg CO2-C m^-2 h^-1; EGM-4, light chamber). Positive = emitted; negative = uptake.
  - Photosynthesis: Gross CO2 uptake (mg CO2-C m^-2 h^-1); calculated as Respiration − NEE.
  - BD: Bulk density of soil organic horizon (g cm^-3).
  - PercentC: Percent total carbon in soil organic horizon.
  - PercentN: Percent total nitrogen in soil organic horizon.
  - CN: Carbon to nitrogen ratio (C:N) in soil organic horizon.
  - OrgDepth: Depth of organic horizon (cm).
  - SM1, LWCount1, Soil1cm1, Soil5cm1, AirTemp1: Soil moisture (m^3/m^3), Leaf Wetness Count, soil temperatures at 1 cm and 5 cm, and air temperature, each averaged over 1 hour prior to sampling; devices: Decagon/related instruments.
  - SM24, LWCount24, Soil1cm24, Soil5cm24, P.Schreberi, V.myrtillus, V.vitis-idaea, V.uliginosum, D.flexuosa, P.commune, Lichen, Daisy, Equisetum, Galium, Luzula, Cladonia, E.angustifolium, Vicia, L.borealis, Moss, Shrub: Vegetation cover and community composition metrics (percent cover per species; some totals may exceed 100% for moss/shrub aggregations).
  - Notes on field labels: Some entries (particularly species cover fields) may contain labeling inconsistencies that require careful QA when mapping to species names.

- Additional data fields (CH4_N2O_Flux_Data)
  - All fields from CO2_Flux_Data (most are the same) plus new flux-specific columns:
  - Ch4Flux: CH4 flux from the plot (μg CH4-C m^-2 h^-1).
  - Co2Flux: CO2 flux from the plot (μg CO2-C m^-2 h^-1).
  - N2oFlux: N2O flux from the plot (μg N2O-N m^-2 h^-1).

- Measurement context and units
  - Temperature, PAR, soil and air temperatures, soil moisture, and leaf wetness are measured with specified instruments (e.g., Tinytag loggers, Decagon devices, EGM-4 IR gas analyser).
  - Fluxes are reported in micrograms or micro-moles per square meter per hour, with CO2 and CH4 fluxes differentiated by gas and method (dark vs light chamber contexts noted in CO2 measurements).

- Data quality and integration considerations
  - Consistency across datasets is aided by shared keys: Date, DateNumber, SamplingPeriod, Site, Plot.
  - Potential labeling issues in vegetation/species fields require cross-checking with field notes or species lists.
  - The CH4_N2O_Flux_Data set extends the CO2 framework by adding multi-gas flux measurements for integrated greenhouse gas analysis.

- How this supports data work
  - Enables scientists and analysts to build self-serve dashboards and reports for carbon and greenhouse gas flux.
  - Facilitates data cleaning, merging, and transformation by providing explicit header descriptions and units.
  - Supports QA checks, data provenance, and reproducibility by tying measurements to sampling times, plots, sites, and environmental conditions.