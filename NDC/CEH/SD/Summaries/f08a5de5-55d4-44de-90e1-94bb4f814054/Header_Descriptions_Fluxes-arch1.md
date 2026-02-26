# Header Descriptions for Dataset "CO2_Flux_Data"

- Purpose: Define the metadata fields describing measurements of CO2 flux in plots across sampling times.
- Key identifying fields
  - Identifier, Date, DateNumber, SamplingPeriod (sampling day and period identifiers)
  - Site, Age (years since last wildfire), Plot
- Measurements and flux variables
  - Biomass (final dry biomass in g)
  - Temperature and light
    - Temperature (air temperature at sampling; Tinytag °C)
    - Par (Photosynthetically Active Radiation; μmol m^-2 s^-1)
  - Gas fluxes
    - Respiration (ecosystem respiration; mg CO2-C m^-2 h^-1; using EGM-4 infrared gas analyser with dark chamber lid)
    - NEE (Net Ecosystem Exchange; mg CO2-C m^-2 h^-1; positive = emission, negative = uptake)
    - Photosynthesis (gross CO2 uptake; mg CO2-C m^-2 h^-1; derived from Respiration − NEE)
- Soil and chemical properties
  - BD (Bulk density of soil organic horizon; g cm^-3)
  - PercentC, PercentN (percent total carbon and nitrogen in soil organic horizon)
  - CN (C:N ratio)
  - OrgDepth (depth of the organic horizon in cm)
- Soil moisture and microclimate surrogates
  - SM1 (soil moisture 1-hour average; m3/m3)
  - LWCount1 (Leaf Wetness Count 1-hour average; range 445–1400)
  - Soil1cm1, Soil5cm1 (soil temperatures at 1 cm and 5 cm depth; °C; 1-hour average)
  - AirTemp1 (air temperature 1-hour average; °C)
  - SM24 (soil moisture 24-hour average; m3/m3)
  - LWCount24 (Leaf Wetness Count 24-hour average; range 445–1400)
  - Soil1cm24, Soil5cm24 (soil temperatures at 1 cm and 5 cm depth; 24-hour average; °C)
- Vegetation and ground cover
  - P.Schreberi, V.myrtillus, V.vitis-idaea, V.uliginosum
  - D.flexuosa, Dicranum, P.commune
  - Lichen, Daisy, Equisetum, Galium, Luzula
  - Cladonia, E. angustifolium, Vicia, L.borealis
  - Moss, Shrub
  - Descriptions indicate percentage cover by each species or functional group (total can exceed 100% for some categories like Moss or Shrub)
- Notes
  - All fields are described as header descriptions to aid data discovery, interpretation, and reuse.

# Header Descriptions for Dataset "CH4_N2O_Flux_Data"

- Relationship to CO2 data: Most fields are the same as in the CO2_Flux_Data header descriptions.
- Additional flux measurements
  - Ch4Flux, CO2Flux, N2oFlux
    - Ch4Flux (CH4 flux from the plot; μg CH4-C m^-2 h^-1)
    - Co2Flux (CO2 flux from the plot; μg CO2-C m^-2 h^-1)
    - N2oFlux (N2O flux from the plot; μg N2O-N m^-2 h^-1)
- Purpose of additions
  - These columns extend the flux measurements to include methane and nitrous oxide, alongside the existing CO2 flux data, enabling multi-gas analyses of plot-level gas exchanges.