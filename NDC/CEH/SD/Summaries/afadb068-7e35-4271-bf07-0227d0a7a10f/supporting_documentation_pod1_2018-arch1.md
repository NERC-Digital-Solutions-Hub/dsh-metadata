# The EMEP-WRF global model, version 4.45

- Global atmospheric chemistry and transport modeling framework
- Based on the official EMEP MSC-W model; EMEP-WRF uses the WRF model (v4.2.2) for hourly 3D meteorology
- Uses ECMWF-IFS data for driving meteorology; GFS-FNL data are used to initialise and nudge every six hours
- Horizontal resolution: 1° x 1° with 21 vertical layers (surface ~40 m to top ~16 km)
- Domain covers the globe
- Emissions are from the IIASA ECLIPSE v6a GAINS model for the year 2015

- Ozone flux calculation framework
- Accumulated ozone uptake (POD) via stomata calculated with the DO3SE model embedded in EMEP
- Inputs required hourly: ozone concentration, temperature, vapour pressure deficit, irradiance, soil moisture
- Vegetation-specific parameterisations (e.g., gmax for stomatal conductance) determine flux
- Outputs POD values as PODyIAM or SPEC (flux above a threshold)
- POD is accumulated over a specified period (e.g., 90 daylight hours)

- Current dataset specifics
- Focus: daily POD1 IAM values summed over the 90-day grassland growing season (mid-April to mid-July) in 2018
- Regions: United Kingdom and United States
- Parameterisation for semi-natural vegetation (as described in Table 1 of the source document) includes inputs such as leaf-level or canopy parameters and time window settings
- Time-period guidance: select the season start/end to maximize flux using local information; the 1 Apr–30 Sep window is used for the 3-month accumulation

- Data characteristics and units
- Data format: shapefile on a 1° x 1° grid
- Attributes: FID (grid cell ID), Lon (center longitude), Lat (center latitude), NAME (USA or UK), POD1 (accumulated POD1 IAM for grassland-growing-season 2018) in mmol m^-2
- Coordinate system: WGS 1984

- Quality assurance and validation
- Underwent QA/QC prior to use; validation against Global Atmosphere Watch (GAW) sites shows the model captures spatial and temporal ozone variations
- Model performance validated through comparison of modelled vs observed daily maximum ozone
- A strong correlation (r^2 = 0.63) between a proxy for growing-season stomatal conductance (POD3 IAM normalized by M7 ozone) and remote-sensed AET/PET supports reliable estimation of stomatal uptake

- How to use the data
- Ozone flux data can be translated into biological impacts (crop yield, tree biomass, flower number) using response functions from the CLRTAP Modelling and Mapping Manual (CLRTAP 2017)
- For grasslands, linear dose–response functions were developed from multiple experiments to relate POD1 IAM to changes in aboveground biomass, total biomass, and flower number (Hayes et al., 2021)
- Ozone flux thresholds (e.g., a 10% reduction) can be used in risk assessment for semi-natural vegetation

- Data structure details
- Shapefile comprises gridded data with five attributes per grid cell (as above)

- Useful background and references
- CLRTAP (2017) Mapping critical levels for vegetation
- Emberson et al. (2000) on modeling stomatal ozone flux across Europe
- Hayes et al. (2021) ozone critical levels for (semi-)natural vegetation dominated by perennial grasslands
- Mills et al. (2018) ozone pollution impact on global wheat production
- Simpson et al. (2012) EMEP MSC-W model technical description
- Vieno et al. (2016) sensitivities of emissions reductions for UK PM2.5
- Related resources: http://www.emep.int/ ; http://icpvegetation.ceh.ac.uk/