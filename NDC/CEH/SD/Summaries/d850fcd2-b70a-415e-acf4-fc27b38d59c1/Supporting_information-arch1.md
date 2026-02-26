# Site description

- Location and environment
  - Long-term alpine research site in Gunnison National Forest, Colorado (38.978725°N, 107.042104°W)
  - Southeast-facing ridgeline at approximately 3540 m above sea level on ~20% slope
  - Substrate: Mancos shale (Upper Cretaceous) downslope; quartz monzonite porphyry (Upper Eocene) upslope
  - Surface layer of loose weathered gravel; bedrock within 5–10 cm
  - Vegetation: primarily barren; 0–10% cover by perennial graminoids, forbs, and woody mats in short summer season
  - Snow typically deposits starting in October; melts June–July
  - Rare avalanches due to ridgeline position; strong west-to-east winds common

- Experimental design
  - Fifty 2 × 2 m permanent plots arranged 5 plots wide × 10 plots long along the main ridge axis (~40° heading)
  - 2 m buffer between plots; overall site area 18 × 38 m
  - Census years: 2014–2017 (n = 4)
  - Individual plants geolocated to nearest cm within plots and tagged
  - Species identification via RMBL Herbarium vouchers; one seedling indeterminate as Indet indet
  - Demographic data per individual: size (max length and max height), recruit status (seedling or clonal propagation), fecundity (mature floral structures per individual)
  - Survival/status: dormancy or death for non-productive years; death of tagged individuals if no aboveground growth for >2 consecutive years; seedlings that germinated and withered in the same year recorded as dead

- Microenvironmental data collection
  - Spatially explicit measurements at each plot corner (2 m resolution) and kriged to 10 cm within plots
  - Substrate surface temperature (°C) via iButton loggers, recorded every 20 minutes, median per logger used
  - Local slope (mm m⁻¹) and elevation to derive aspect
  - Disturbance proxy: Euclidean distance to a small trail on the eastern side (human and animal use)
  - Soil moisture: shallow moisture at 3.8 cm depth measured after rain in July 2015; deep moisture measured to 10 cm depth after rain in July 2016
  - Soil texture: dry mass fractions >4 mm, >2 mm, >1 mm, >0.5 mm, and <0.5 mm
  - Soil chemistry (subset of 23 samples): copper, iron, potassium, manganese, phosphorus, zinc, total nitrates/nitrogen, organic matter, pH, electrical conductivity
  - Soil hardness: hardness energy density (MJ m⁻³) estimated from energy to hammer a 16-penny nail flush into substrate divided by nail volume

- Macroenvironmental data
  - Annual climate data (2013–2017) from Billy Barr weather station (4.5 km away): total precipitation January–July (covering snowpack and summer rains)

- Functional trait data
  - Species-mean trait characterization using undisturbed adjacent plants to plots
  - Root traits: maximum root depth and length, root mass fractions; imaging and analysis of fine roots to derive total root length, volume, and mean cross-sectional area; specific root length; root tissue density
  - Root anatomy: arbuscular mycorrhizal fungi (AMF) prevalence and dark-septate endophyte fungi (DSE) via magnified intercept method
  - Leaf traits: leaf lamina thickness, fresh leaf mass, area, aspect ratio; specific leaf area; leaf dry matter content
  - Biomass partitioning: tissue-level mass fractions for leaves, stems, coarse roots, fine roots; root and stem dry matter contents
  - Photosynthesis: per-mass photosynthetic rate using LI-6400XT under standardized light, CO₂, temperature, and humidity; area corrections for leaf size
  - Chemistry and isotopes: leaf carbon and nitrogen concentrations; leaf δ13C and δ15N
  - Reproductive metrics: fruit set (fertile vs aborted seeds) and mean seed mass (mg)

- Data summarization and analysis framework
  - Microenvironment summary: kriged grid predictions; PCA on standardized microenvironment variables; retained components with eigenvalues > 1; 10 cm resolution scores
  - Realized niche: presence/absence on a 20,000-cell grid; each individual represented as a circle with diameter equal to its maximum vegetative width; niche centroid derived from median PCA scores where the species occurred
  - Vital rates definitions: recruitment (new establishment as seedling or vegetative propagule in a year), growth rate (change in vegetative length year-to-year), mortality (death in a given year), fecundity (number of floral structures produced in a year)
  - Trait data handling: gap-filling for 68 of 540 observations via multiple imputation; species-mean trait PCA with eigenvalue > 1; predicted trait scores for each species
  - Species-level trait neighborhoods: two metrics of pairwise trait differentiation
    - Absolute difference: |Xm − Xn|
    - Hierarchical difference: 0 if Xm < Xn; Xm − Xn otherwise
  - Individual-level trait neighborhoods
    - Crowding coefficient for focal plant j: sum over non-focal neighbors k within 50 cm of focal plant’s equivalent circle, weighted by neighbor size sk and decayed by distance with δ = 20 cm
    - Mean trait difference for focal individual: size-weighted mean neighbor trait value minus focal trait T
    - Mean trait hierarchy for focal individual: size-weighted mean neighbor trait value if greater than focal species’ trait value; 0 otherwise
  - Note: these neighborhood metrics use neighbor sizes and rely on species-mean trait values; size-trait allometric scaling was considered but generally weak in this dataset

- Key scope
  - Comprehensive, multi-scale dataset linking small-scale microhabitat variation, macroclimate, plant demographics, and broad functional traits across the alpine plant community over four years
  - Emphasis on spatially explicit realization of niches, community assembly processes, and trait-mediated interactions through both population-level dynamics and plot-level microenvironment drivers