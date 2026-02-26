# A long-term alpine research site in the Gunnison National Forest, Colorado

## Overview
- Long-term, standardized ecological monitoring to demonstrate environmental condition and policy-relevant health over time.
- Combines census data, micro- and macroenvironmental measurements, and functional trait analyses to understand community dynamics and environmental drivers.
- Emphasizes data verification, quality assurance, transformation, and presentation in clear formats (maps, charts, reports), with datasets stored and shared via appropriate portals.

## Site and Sampling Design
- Location: Gunnison National Forest, Colorado; 38.978725°N, 107.042104°W, ~3540 m a.s.l. on a southeast-facing ridgeline with ~20% slope.
- Substrate: Mancos shale downslope; quartz monzonite porphyry upslope; surface layer of loose weathered gravel; bedrock within 5–10 cm.
- Vegetation: Primarily barren; 0–10% cover by perennial plants during the short summer season.
- Climate context: Snow typically accumulates October; melts June–July; strong westerly winds common; avalanches rare.
- Plot design: Fifty 2 × 2 m permanent plots arranged in a 5 × 10 grid along the ridge, with 2 m buffers, spanning an ~18 × 38 m area.

## Census Data Collection (2014–2017)
- Annual censuses conducted when growth and flowering were complete (late July–early August).
- Individual tracking: each plant tagged and located to the nearest centimeter; species verified with RMBL herbarium vouchers.
- Demographics recorded per individual: size (max length/height), recruitment status (seedling or clonal), fecundity (number of mature floral structures), dormancy/death status, and annual survival.
- Delineation rules: distinct individuals separated by >3 cm; special rules for grasses/sedges and connected plants.

## Microenvironmental Data
- Spatial mapping: measurements at plot corners (2 m resolution); interpolated to 10 cm resolution within plots via ordinary kriging.
- Substrate surface temperature: measured with iButton data loggers (every 20 minutes; 2016 data used as medians).
- Topography: local slope, elevation, aspect derived from clinometer data.
- Disturbance proxy: distance from a historic eastern trail serving human/animal activity.
- Soil moisture: shallow (3.8 cm) moisture in July 2015; deep moisture (up to 10 cm) in July 2016.
- Soil texture and chemistry: particle-size fractions; a subset (n=23) analyzed for Cu, Fe, K, Mn, P, Zn, total N, organic matter, pH, electrical conductivity.
- Soil hardness: soil penetration energy density (MJ m^-3) measured in July 2015.

## Macroenvironmental Data
- Climate data (2013–2017) from the Billy Barr weather station (4.5 km away).
- Yearly variable: total precipitation January–July (snowpack and early season rainfall).

## Functional Trait Data
- Species-level trait measurements taken adjacent to permanent plots to minimize disturbance.
- Root traits: 3–5 individuals per species excavated for root depth, length, volume, root cross-sectional area, and specific root length; fine roots analyzed for AMF and DSE colonization via magnified intercept method.
- Leaf traits: five leaves per individual measured for lamina thickness, fresh mass, area, aspect ratio; dried for leaf mass per area (LMA) and leaf dry matter content (LDMC).
- Biomass partitioning: tissue mass fractions (leaves, stems, coarse and fine roots) and root/stem dry matter content.
- Photosynthesis: per-mass leaf photosynthetic rate measured with LiCor 6400XT under standardized conditions; leaf area corrections applied for small or curled leaves.
- Chemical traits: leaf carbon and nitrogen concentrations; carbon/nitrogen isotopes (δ13C, δ15N).
- Reproductive traits: mature fruits collected to estimate seed set, mean seed mass, and fertility (fertile vs aborted seeds).

## Data Summarization and Analysis
- Microenvironment summarization: kriged grid values for all variables; PCA on standardized predictors; retained PCs with eigenvalues > 1; generated 10 cm grid scores.
- Realized niches: presence/absence per 10 cm grid cell; niche centroids defined by median PC scores of occupied cells.
- Vital rates: recruitment (new establishment), growth rate (size change year-to-year), mortality, and fecundity (floral structures per year).
- Trait data: species means calculated; missing data gap-filled with multiple imputation; trait PCA with PCs > 1; predicted trait scores per species.
- Neighborhood analyses:
  - Species-level: two metrics of trait differentiation between species (absolute difference and hierarchical difference based on trait PCA).
  - Individual-level: crowding coefficient within 50 cm, weighting neighbors by size and distance (decay with distance); computed for intra- and interspecific neighbors.
  - Mean trait difference: size-weighted local mean trait difference from focal individual’s trait value.
  - Mean trait hierarchy: size-weighted local mean trait value relative to focal species; nonzero only when local mean exceeded focal value.
- Considerations: acknowledges potential limitations of size-trait allometry; size-trait relationships generally weak and thus not heavily relied upon for individual-level estimates.

## Data Management and Access
- Emphasizes storage and upload of datasets to appropriate portals to enable broad access and reuse.
- Standardized formats and clear documentation to support reproducibility and policy-relevant monitoring.

## Relevance for Environmental Monitoring
- Provides a comprehensive, multi-scale framework linking micro- and macro-environmental drivers to population dynamics and functional strategies.
- Generates standardized outputs (maps, niche centroids, trait-neighborhood metrics, vital rates) suitable for tracking environmental health and informing management decisions over time.
- Demonstrates approaches to augment dataset value through integrated analyses and transparent data sharing.