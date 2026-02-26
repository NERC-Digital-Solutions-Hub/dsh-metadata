# Field sites and microclimate measurements

- Study setting: six forest reserve stands in the Northern Boreal zone of Sweden, with soil and vegetation types similar across sites (Scots pine, Norway spruce, dwarf shrubs, and feather mosses).
- Sites and fire history: coordinates and time since last wildfire (as of 2014) are NJA (47 years), JAR (53), LAD (136), GUO (183), FET (232), REV (367).
- Microclimate data collection: weather stations measuring air temperature, soil temperature at 1 cm and 5 cm, soil moisture, and surface leaf moisture; installed at all sites except GUO; data collected from June 2012 to July 2014.

- Field sampling and analyses overview:
  - Plant and soil sampling conducted after final GHG sampling.
  - Biomass: plant material within gas-chamber collars dried and weighed for total dry weight.
  - Soils: one 5 cm diameter, 10 cm depth core per collar to assess horizon depths, bulk densities, and total soil C:N.
  - Vegetation cover: estimated by species (and grouped into plant functional types) with cover sums potentially exceeding 100%.
  - 2012 soil cores: six cores along transects for inorganic N (NO3-, NH4+).
  - 2013 soil cores: four cores for pH, total phosphorus, loss on ignition (organic matter content), and microbial PLFA content in the soil organic horizon.

- Microbial community analyses (PLFA):
  - Lipids extracted from soil, separated into neutral, free fatty acids, and phospholipids; phospholipids converted to fatty acid methyl esters.
  - PLFA analysis by GC; bacterial PLFAs identified by specific branched/cyclopropyl fatty acids; fungal PLFAs identified as 18:2ω6,9.
  - Total PLFAs calculated from identified peaks; expressed as nmol PLFA per gram dry weight.

- Forest floor greenhouse gas (GHG) flux measurements:
  - Setup: five permanent PVC collars per site (30 cm diameter, 10 cm height) along transects on a moss mat.
  - Sampling schedule: initial setup with two-day acclimation; measurements in June 2012, September 2012, June 2013, and July 2014.
  - GHGs: ecosystem respiration (ER) and net ecosystem exchange (NEE) measured with a portable infrared gas analyser; PAR measured for NEE.
  - NEE interpretation: negative indicates net CO2 sequestration (GPP > ER); positive indicates net CO2 release.
  - Additional gases: CH4 and N2O measured with closed static chambers; 10 mL headspace samples taken every 10 minutes for 30 minutes and analyzed by GC (CH4 with FID; N2O with ECD).
  - Data processing: gas concentrations converted to fluxes (mg CH4-C or mg N2O-N m-2 h-1); quality control to identify missing data and atmospheric contamination.

- Statistical analyses and modeling:
  - Goals: assess relationships between time since fire, site properties, and GHG fluxes; compare inter-site differences; identify predictors of forest floor GHG emissions.
  - Software: analyses performed in R.
  - Core methods:
    - Linear regression to examine trends in site properties and GHG fluxes with time since fire (data drawn from both within collars and transects).
    - ANOVA with Tukey's HSD for discrete site differences (e.g., vegetation cover); nonparametric alternatives (Kruskal-Wallis with Dunn’s test) when ANOVA assumptions were not met.
  - Linear mixed effects models (LME) for drivers of forest floor GHG fluxes:
    - Time since wildfire removed as a predictor after finding no significant relationship with soil properties or GHGs; site treated as discrete factor.
    - Collinearity assessment to remove highly correlated predictors (>|70%|).
    - Random effects to account for repeated sampling per plot and unequal variances among sites.
    - Fixed effects selected via stepwise deletions and likelihood ratio tests; non-significant terms removed.
    - Likelihood ratio tests used to quantify effect sizes and significance in final models.
  - Model variants due to missing weather data at GUO:
    - All Sites model set (including GUO) with weather-related data considered.
    - Including WS Data model set (weather-station data included) excluding GUO data due to lack of weather station.
    - After addressing collinearity, key fixed factors considered included: Site, Temperature (AirTemp1), Sampling Period, PAR, Soil Moisture, Leaf Moisture, Depth of organic horizon, C:N of organic horizon, Bulk Density of organic horizon, Final Plant Biomass, percent moss, percent of Dicranum sp., percent P. commune, percent total shrub, and percent cover of V. vitis-idaea, V. uliginosum, E. nigrum, D. flexuosa/Total Grass.
    - In practice, only terms meeting collinearity and significance criteria remained in the final models.
  - Notes on data usage:
    - The GUO site lacked a weather station, leading to two modeling approaches to maximize data usage: one including all sites (All Sites) and one using weather-station data (Including WS Data) but excluding GUO.
    - Some plant species were excluded from model selection if highly correlated with broader plant functional types (e.g., P. schreberi and V. myrtillus removed due to correlations with total moss and shrub cover, respectively).

- Reference framework:
  - Methods and analyses reference established protocols for PLFA-based microbial biomass, soil property measurements, and GHG flux calculations, with citations to Crossman et al. (2004), de Vries et al. (2012), Ward et al. (2013), Whitaker et al. (2014), and Zuur et al. (2009).