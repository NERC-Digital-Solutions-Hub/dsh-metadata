# Site description

## Overview
- Long-term alpine research site in Gunnison National Forest, Colorado (approximately 3540 m above sea level).
- Location: southeast-facing ridgeline on a ~20% slope; contact between Mancos shale downslope and quartz monzonite porphyry upslope.
- Surface: loose weathered gravel; bedrock within 5–10 cm depth.
- Vegetation: primarily barren; 0–10% cover by perennial plants during the short summer season.
- Experimental setup: fifty 2 × 2 m permanent plots arranged 5 × 10 along the ridge axis (≈ 40° heading) with 2 m plot-to-plot buffers; overall site area ~18 × 38 m.

## Experimental design and data collection
- Census period: 2014–2017 (4 years).
- Within every plot: all individuals located to the nearest centimeter, tagged with aluminium tags.
- Species identification: via RMBL herbarium vouchers; one seedling labeled “Indet indet” when unidentified.
- Demographic data per individual: size (max length and height), recruitment status (seedling or clonal propagule), fecundity (number of mature structures per individual), dormancy/death rules, and annual mortality/removal criteria.

## Microenvironmental data
- Spatial mapping: measurements at each plot corner (2 m resolution) with 10 cm kriging-based interpolation within plots.
- Substrate surface temperature: iButton data loggers recorded 20-min intervals (13 July–10 August 2016); median per logger used.
- Topography: local slope, elevation, and derived aspect.
- Disturbance proxy: distance from a trail (Euclidean distance) as a proxy for human/animal disturbance.
- Soil moisture: shallow (3.8 cm) measured July 2015; deep soil moisture up to 10 cm depth measured July 2016.
- Soil texture: fractions (>4 mm, >2 mm, >1 mm, >0.5 mm, <0.5 mm).
- Soil chemistry: subset of 23 samples analyzed for Cu, Fe, K, Mn, P, Zn, total nitrates/N, organic matter content, pH, and conductivity.
- Soil physical property: soil penetration energy density (MJ m^-3) measured July 2015.

## Macroenvironmental data
- Climate context: annual data 2013–2017 from nearby Billy Barr weather station (~4.5 km away).
- Variable summarized: total precipitation from January through July each year (capturing snowpack and early/rainy-season influences).

## Functional trait data
- Sampling around plots: individuals from nearby locations (3–5 per species) to minimize disturbance to plots.
- Root traits: max depth/length/volume, root cross-sectional area, specific root length (mm g^-1), root tissue density; fine-root morphology and biomass fractions; AMF and DSE colonization estimated via magnified intercept method.
- Leaf traits: leaf lamina thickness, fresh mass, leaf area, aspect ratio, specific leaf area, leaf dry matter content.
- Plant tissues: biomass fractions of leaves, stems, coarse roots, fine roots; root and stem dry matter content.
- Photosynthesis: per-mass rate measured with LiCor 6400XT under standardized conditions; area-adjusted for leaf size.
- Leaf chemistry and isotopes: carbon concentration, nitrogen concentration, δ13C, δ15N.
- Reproductive traits: 10 mature fruits per species sampled in 2015; seeds counted per fruit, fertile vs aborted seeds; mean seed mass.
- Data collection ethics: adjacent plants used to avoid plot disturbance.

## Data summarization and analysis
- Microenvironment summarization: kriged grid predictions; PCA on z-transformed variables; components with eigenvalues > 1 retained; 10 cm resolution scores derived.
- Realized niches: presence/absence per 10 cm grid cell; individuals modeled as circles with diameter equal to maximum vegetative width; realized niche centroid derived as the median of microenvironment PCA scores at presence points.
- Vital rates: recruitment (new established individuals), growth rate (change in vegetative length year-to-year), mortality (death in a given year), fecundity (floral structures per year).
- Trait data: species means; missing data imputed using multiple imputation by chained equations (MICE); PCA on z-transformed traits; components with eigenvalues > 1 retained; species-level trait scores computed.
- Trait neighborhood analyses:
  - Between-species: absolute difference |Xm − Xn| and hierarchical difference (0 if Xm < Xn; Xm − Xn otherwise) based on trait PCA scores.
  - Individual-level crowding: crowding coefficient within 50 cm, weighting neighbor size and distance with decay, for intra- and interspecific neighbors.
  - Mean trait difference: size-weighted mean neighbor trait around each focal individual minus focal trait.
  - Mean trait hierarchy: size-weighted neighbor trait value exceeding the focal trait (0 if not).
- Notes: trait data largely relies on species-mean values for neighborhood metrics; limited allometric scaling due to weak size-trait relationships.

## Data quality, gaps, and considerations
- Small amount of missing trait data (68 of 540 observations) gap-filled via multiple imputation.
- Spatially explicit, multi-scale data integration (2 m plot grid to 10 cm kriging grids; 20,000 grid cells for realized niches).

## Data products and reuse potential
- High-resolution microenvironment maps (10 cm grids) linked to species distributions and niches.
- Realized niche centroids for each species across the study area.
- Demographic rates (recruitment, growth, mortality, fecundity) per individual/year.
- Comprehensive trait dataset with PCA-based trait axes and neighborhood metrics (intra- and interspecific).
- Individual-level spatial-context metrics (crowding, mean trait difference, and trait hierarchy) enabling analyses of trait-mediated interactions.
- Supports cross-scale analyses of how microhabitat, macroclimate, and functional traits drive species distributions and population dynamics.

## Relevance for data support
- Demonstrates end-to-end data lifecycle: field collection, precise geo-referencing, multi-faceted micro- and macroenvironmental measurement, extensive trait phenotyping, robust data summarization (PCA, niche analysis), and advanced statistical handling (imputation, neighborhood metrics).
- Provides clearly defined data products and transformation steps that enable self-serve exploration and comparative reuse in ecological data support workflows.