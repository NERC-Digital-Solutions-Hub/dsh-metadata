# Field sites and microclimate measurements

- Study area and design
  - Six forest reserve stands in the Northern Boreal zone of Sweden with varying time since last wildfire (47–367 years as of 2014).
  - Similar soil type and vegetation: Scots pine, Norway spruce, dwarf shrubs, and feather moss ground cover.
  - Site coordinates and ages provided; sites labeled NJA, JAR, LAD, GUO, FET, REV.

- Microclimate and weather data collection
  - Weather stations installed at all sites except GUO, measuring air temperature, soil temperature at 1 cm and 5 cm, soil moisture, and surface leaf moisture (Decagon devices).
  - Field data collected June 2012 to July 2014.
  - For GUO, weather data were not available, affecting modeling options.

- Field sampling of plants and soils
  - Post-GHG sampling, gas plots destructively harvested: all plant material clipped, dried at 60°C, and weighed for total biomass.
  - One soil core (5 cm diameter, 10 cm depth) collected at collar centers to assess horizon depths, bulk densities, and total soil C:N.
  - Plant cover estimated by species and aggregated into plant functional types (PFTs: shrub, graminoid, bryophyte); cover summed for each type.
  - June 2012: six soil cores along transects for inorganic N (NO3-, NH4+).
  - September 2013: four additional cores for pH, total phosphorus, loss on ignition (organic matter content), and microbial PLFA content in the soil organic horizon.

- Microbial community analysis (PLFA)
  - Lipids extracted using a modified Bligh and Dyer method; lipids separated into neutral, free fatty acids, and phospholipids; phospholipids methylated to fatty acid methyl esters.
  - PLFA analysis by GC; bacterial PLFAs identified by specific branched and cyclopropyl fatty acids; fungal PLFAs identified as 18:2ω6,9.
  - Total PLFA concentration calculated from identified peaks (nmol PLFA g dry weight).

- Forest floor greenhouse gas (GHG) flux measurements
  - Five permanent PVC collars per site (30 cm diameter, 10 cm height) placed along transects on a moss mat; left for two days before initial measurements.
  - Sampling schedule: June 2012; September 2012; June 2013; July 2014.
  - Ecosystem respiration (ER) and net ecosystem exchange (NEE) measured with a portable infrared gas analyser using opaque or clear chamber lids.
  - PAR measured during NEE assessments to determine photosynthesis contribution.
  - CH4 and N2O measured with a closed static chamber: 10 mL headspace samples collected every 10 minutes over 30 minutes and analyzed by GC with appropriate detectors.
  - Fluxes converted from ppm to mg CH4-C m-2 h-1 and mg N2O-N m-2 h-1; quality control implemented for missing data and contamination.

- Statistical analysis approach
  - Analyses executed in R to address: (a) relationships among time since fire, site properties, and GHG fluxes; (b) inter-site differences in properties and fluxes; (c) predictors of forest floor GHG emissions.
  - Time trends: Linear regressions to assess changes with increasing time since fire; data from cores within collars and transects.
  - Group differences: ANOVA with Tukey’s HSD post-hoc tests; nonparametric Kruskal-Wallis with Dunn’s tests when ANOVA assumptions were violated.
  - Linear mixed effects models (LME) for GHG flux controls:
    - Time since wildfire was initially considered but not significant; replaced by discrete site.
    - Collinearity: correlation matrix used to remove highly collinear predictors (>70% correlation).
    - Random effects included for repeated sampling within plots and to accommodate unequal variances across sites.
    - Fixed effects selected via single-term deletions and likelihood ratio (LR) tests; non-significant terms removed.
    - Interactions dropped if not significant.
  - Two model variants due to GUO weather data gap:
    - All Sites: includes weather data.
    - Including WS Data: excludes GUO data (no weather station at GUO).
  - Fixed-factor lists and handling:
    - Includes site, air temperature proxies, soil moisture, leaf moisture, soil horizon depth (OH), carbon:nitrogen of the horizon, bulk densities, plant biomass, and percent cover of moss, Dicranum, P. commune, total shrub cover, and cover of V. vitis-idaea, V. uliginosum, E. nigrum, D. flexuosa/grass totals.
    - After collinearity checks, Dicranum sp. and P. commune removed due to high correlation with moss and shrub cover, respectively.
    - Plant and soil variables averaged or derived as needed; e.g., AirTemp1 (hourly mean air temperature), environmental variables averaged over one hour prior to sampling.
  - OH denotes soil organic horizon.

- Notes on data interpretation
  - Time since wildfire did not show a significant relation to soil properties or GHG fluxes in the combined dataset; site-level factors were more informative in the final models.
  - Data handling decisions (e.g., exclusion of GUO from certain models) were driven by data availability (weather station) to maximize model reliability.

- References
  - Crossman et al. 2004; de Vries et al. 2012; Ward et al. 2013; Whitaker et al. 2014; Zuur et al. 2009.