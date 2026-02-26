# Site description

- Long-term alpine research site in Gunnison National Forest, Colorado (38.978725°N, 107.042104°W) on southeast-facing ridgeline at ~3540 m a.s.l. and ~20% slope.
- Substrate transitions from Mancos shale downslope to quartz monzonite porphyry upslope; loose surface gravel, bedrock within 5–10 cm.
- Site is largely barren (0–10% cover by perennial plants) during short summer; snow typically accumulates October and melts June–July; avalanches rare due to ridgeline position; strong westerly winds common.
- Experimental design: fifty 2 × 2 m permanent plots arranged 5 × 10 along the ridge axis (≈40° heading) with 2 × 2 m buffers between plots; overall site footprint 18 × 38 m.

# Census data

- Temporal scope: 2014–2017 (n = 4 censuses), conducted when vegetative growth and flowering were complete (late July–early August).
- Per-individual data: exact coordinates to the nearest centimeter within each plot; permanent aluminium tag anchored in substrate; voucher-based species IDs; one seedling identified as Indet indet.
- Demographic parameters recorded at each census:
  - Size: maximum length and maximum height of vegetative parts (cm).
  - Individual delineation: stems within 3 cm at ground level treated as the same individual unless clearly separate by distance or growth form.
  - Recruitment status: new seedlings or clonal vegetative propagules.
  - Fecundity: number of mature floral structures per individual.
  - Vital status: dormant or dead; annual mortality tracked; deceased tags removed if no aboveground growth for >2 consecutive years.
  - Seedlings germinating and withering within a year recorded as dead.

# Microenvironmental data

- Spatial mapping: measurements at plot corners (2 m resolution) interpolated to a 10 cm grid within each plot using ordinary kriging.
- Substrate surface temperature: iButton data loggers (every 20 minutes, 13 July–10 August 2016); median value used per logger.
- Topography: local slope, elevation, and derived aspect from triangulated measurements.
- Disturbance proxy: distance from a small eastern trail (Euclidean distance transform) to reflect human/animal use.
- Soils:
  - Shallow soil moisture (3.8 cm depth) measured after rain events (July 2015).
  - Deep soil moisture (up to 10 cm) measured after rain events (July 2016).
  - Texture: dry mass fractions for >4 mm, >2 mm, >1 mm, >0.5 mm, and <0.5 mm.
  - Chemistry (subset of 23 samples): Cu, Fe, K, Mn, P, Zn, total nitrates/nitrogen, organic matter, pH, electrical conductivity.
  - Hardness/fracturability: soil penetration energy density (MJ m^-3) via hammering a nail into substrate.
- Output: a rich set of microenvironment rasters describing physiography and disturbance.

# Macroenvironmental data

- Climate context: annual precipitation totals for January–July (dominant snowpack and summer rainfall) from Billy Barr weather station (GTH161), 4.5 km away, for 2013–2017.

# Functional trait data

- Sampling strategy: to minimize plot disturbance, individuals of each species were collected from nearby locations adjacent to plots; 3–5 whole plants per species excavated and roots processed.
- Root traits (belowground): maximum root depth and length, total root volume, root length per mass (specific root length), root tissue density; fine roots (<2 mm) analyzed for length, volume, mass, and specific root length; root morphology quantified via image analysis (SmartRoot in ImageJ); root samples cleared and stained to estimate AMF and DSE fungi using the magnified intercept method.
- Leaf traits (aboveground): five leaves per individual measured for lamina thickness, fresh mass, projected leaf area (via scanning; corrections for small leaves and curling); specific leaf area and leaf dry matter content; biomass fractions of leaves, stems, coarse roots, and fine roots determined; photosynthetic capacity per unit leaf mass measured with LiCor 6400XT under standardized cuvette conditions; leaf carbon and nitrogen concentrations and stable isotopes (δ13C, δ15N) measured.
- Reproductive traits: at end of 2015 season, fruiting from fertile individuals assessed; seeds counted per fruit (n ≈ 29 per sample), relative seed set calculated as fertile seeds/total seeds; mean seed mass computed.
- Data handling: occasional missing observations (68/540) gap-filled using multiple imputation by chained equations.

# Data summarization and analysis procedures

- Microenvironment summaries: kriged grid predictions for all variables; PCA on standardized microenvironment variables; components retained with eigenvalues > 1; predicted scores calculated on the 10 cm grid.
- Realized niches: species presence/absence scored across the 20,000-cell grid by modeling each individual as a circle with a diameter equal to species’ maximum vegetative width; niche centroids derived as the median PCA score across presence cells.
- Vital rates summaries:
  - Recruitment: new establishment events (seedlings or vegetative propagules) in a year.
  - Growth rate: change in vegetative length between successive years.
  - Mortality: death events; occasional dead or dormant individuals censored after thresholds.
  - Fecundity: number of floral structures produced per year.
- Trait data synthesis: species means calculated; small amount of missing data imputed; species-level PCA on standardized traits; component scores retained with eigenvalues > 1; predicted trait scores assigned per species.
- Species neighborhood metrics (trait-based): for pairs of species, compute absolute trait differences and hierarchical differences (0 if Xm < Xn; Xm − Xn otherwise).
- Individual-neighborhood metrics: for focal plant j, crowding coefficient sum over neighboring non-focal individuals k within 50 cm, weighted by s_k e^(-d_jk/δ) with δ = 20 cm; computed separately for intra- and interspecific neighbors.
  - Mean trait difference for focal individual: size-weighted mean neighbor trait minus focal trait.
  - Mean trait hierarchy for focal individual: size-weighted mean neighbor trait value minus focal trait, but set to zero if the neighbor value is not greater than the focal trait.
- Notes on methodology: allometric scaling of trait values with plant size acknowledged but empirical size-trait relationships were generally weak; 50 cm neighborhood radius chosen to capture relevant belowground competitive interactions; authors used species-mean trait values for some neighborhood calculations, acknowledging potential limitations.

# Key GIS-relevant takeaways

- Spatial framework: 18 × 38 m study area with fifty 2 × 2 m plots; high-resolution microenvironment mapping at 10 cm grid interpolated from 2 m plot corners.
- Rich geospatial layers: coordinates and tag-based plant-level data linked to 10 cm microgrid and 20,000-cell realized-niche grid; multiple environmental rasters (temperature, slope, aspect proxy, disturbance, soil moisture/texture/chemistry, hardness) suitable for map-based analyses.
- Temporal dimension: census data (2014–2017) paired with macroclimate (2013–2017) to explore temporally variable drivers of community structure.
- Trait- and neighborhood-focused GIS outputs: rasters and summaries of PCA-derived microenvironment and trait spaces; spatially explicit niche centroids and neighborhood metrics (crowding, mean trait difference, and mean trait hierarchy) for integration into map-based decision tools and policy/communication visuals.