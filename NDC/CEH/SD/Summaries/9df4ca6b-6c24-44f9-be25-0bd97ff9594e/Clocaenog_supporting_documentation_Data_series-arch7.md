# Climoor field site in Clocaenog forest Supporting documentation for data

- A climate change manipulation experiment using automated roof technology to create drought and warming treatments for upland moorland in Clocaenog Forest, North East Wales.
- Established in 1998; powered by solar and wind; replicated drought and warming treatments with three replicate plots for each treatment and three control plots (total 9 plots).
- Location coordinates: grid SJ019519; latitude 53.055°N, longitude -3.465°W. The site is dominated by Calluna vulgaris (heather) with additional species; soil type is humo-ferric podzol.

## Spatial layout and context for GIS

- Site layout and plot configuration described in Appendix 3; plots are 4 m x 5 m arranged in blocks with controls shading treatment plots.
- Plot-level and landscape-scale data collection enable map-based visualization of treatments, microclimate, and ecological responses.
- Appendix 1–3 provide detailed plot layout, quadrat locations, and a Clocaenog site layout map.

## Climate treatments and experimental design

- Treatments:
  - Warming (W): retractable aluminium mesh curtains over plots; reduces night-time heat loss; curtains retract during rain to limit rainfall exclusion.
  - Drought (D): retractable polyethylene roof over plots to exclude rainfall; approximately 20% reduction in annual rainfall and up to ~80% of growing-season rainfall excluded in earlier periods; operation timing has varied (May–Sept, later Apr–Oct).
  - Controls (C): scaffolding to mirror shading from roofs without applying drought or warming.
- Replication and blocking:
  - 3 warming plots, 3 drought plots, 3 control plots (n=9), arranged across 4 blocks with specific associations between treatment and block.
- Operation details:
  - Drought roofs trigger based on tipping-bucket rainfall sensors; wind limits (>10 m/s) prevent curtain operation to avoid damage.
  - Warming curtains operate to reduce heat loss at night; rain-triggered retraction can affect rainfall inputs.

## Datasets and data types (described and organized by data type)

- AWS meteorological data (daily): relative humidity, air temperature, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction.
- Micro-meteorological plot data (daily): plot-level soil and air temperature, soil moisture (various methods over time).
- Rainfall data (site level) and rainfall chemistry (biweekly): storage rain gauge for rainfall totals; rain chemistry including pH, nitrate, chloride, sulfate, DOC, ammonium.
- Throughfall data (plot-level rainfall) (fortnightly): rainfall per plot to derive treatment-level rainfall changes; data may be excluded if measurements are compromised.
- Water table depth (biweekly to current): permeable tubes down to bedrock; maximum detectable depths per plot.
- Soil respiration (fortnightly to weekly; 1998–present): with various instrumentation over time (CIRAS, LICOR, automated LI-COR 8100); flux expressed as mg CO2-C m^-2 h^-1; collar-based measurements.
- Trace gases CH4 and N2O (sampling with static chambers): sampled at 0, 15, 30 minutes; analyzed by gas chromatography.
- Net ecosystem CO2 exchange (NEE) (periodic): measurements in 2002–2004 and 2011 using CIRAS-2 and later LICOR systems; includes adjustments for biomass.
- Photosynthesis (ambient and response curves): measurements using CIRAS-2; data include leaf-level photosynthesis, stomatal conductance, internal CO2 concentration; occasional species-specific curves.
- Vegetation survey data (plant biomass) – Pin point method (1998–2012): three quadrats per plot with 300 pins per plot; conversion of pin hits to biomass using species-specific calibration factors.
- Canopy reflectance (NDVI and PRI): ground-based spectrometer measurements (2001–2004); indices NDVI680, NDVI570, PRI.
- Vegetation phenology, annual growth, and pathogens: shoot elongation, budburst, leaf counts, and pathogen signs (2000, 2002, 2004; ongoing growth monitoring in later years).
- Vegetation chemistry: leaf chemistry and litter chemistry (C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates).
- Litterfall: monthly collection (1999–2002), later less frequent; biomass conversion and carbon/nitrogen analysis.
- Root biomass: soil cores (various years: 2003, 2004, 2008, 2011); identification of organic/inorganic horizons and root extraction.
- Soil microbial biomass: chloroform fumigation method (2000, 2001, 2012); microbial biomass carbon expressed per g soil organic matter.
- Nitrogen mineralisation: incubation cores with initial and final measurements to derive net mineralisation rates.
- SOM, SOC and bulk density: soil core analyses, separate organic/inorganic horizons, dry weight, and conversions to g m^-2.
- Soil solution and leachate chemistry: lysimeters and tensioned samplers; pH, NO3, Cl, SO4, DOC; analyzed using ion chromatography and TOC.

## Data processing, quality, and accessibility

- Data processing notes highlight legacy methodologies and conversions between raw instrument units (e.g., g CO2 m^-2 h^-1 and µmol m^-2 s^-1) to standard units (mg CO2-C m^-2 h^-1) using established conversion factors.
- Quality control performed via basic visual checks; some datasets (legacy) may not have complete documentation of processing steps; not all data are stored in the on-site EIDC (post-2015 data not always present).
- Data availability:
  - Primary data stored with CEH Bangor and, where applicable, in the EIDC; contact researchers for access to specific datasets and current storage locations.
  - Not all smaller or post-2015 data are guaranteed in the EIDC; cross-verification with authors recommended for GIS mapping and data integration.

## How this supports GIS and map-based data products

- Richly geospatial multi-year dataset available at plot level, enabling:
  - Visualization of treatment allocation (W, D, C) over time on maps.
  - Spatial linkage of meteorological and ecological responses to plot locations.
  - Time series mapping of rainfall exclusion, canopy indices, soil respiration, NEE, and litter/biomass changes.
  - Integration of plot-level climate manipulation data with soil and vegetation layers (soil chemistry, canopy reflectance, biomass, litterfall, root biomass, and phenology).
- Data are suitable for creating GIS layers such as:
  - Treatment type per plot by year.
  - Rainfall reduction percentages per plot/year (throughfall vs site rainfall, with adjustments).
  - Sensor locations and measurement strategies (AWS towers, micro-mete plots, lysimeters, collars).
  - Spatially explicit datasets for model validation and visualization (NEE, soil respiration, CH4/N2O fluxes, litterfall, canopy indices).

## Key considerations and contacts

- Primary contact for data details: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor.
- Documentation version: update to version 6 - 04/11/2016.
- Note: Data collection methodologies evolved over time; for GIS usage, verify year-specific data sources, plot assignments, and any missing years or plots when building time-enabled maps.

- Overall, Climoor provides a comprehensive, long-term, plot-level geospatial dataset for drought and warming experiments with diverse environmental and ecological measurements, suitable for map-based analysis and data products in GIS applications.