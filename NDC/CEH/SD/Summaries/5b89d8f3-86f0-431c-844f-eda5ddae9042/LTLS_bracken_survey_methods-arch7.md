Methods lifted from Productivity in a dominant herbaceous species is largely unrelated to soil macronutrient stocks, Rowe EC, Toberman H, Adams JL, Lawlor AJ, Thacker SA, Patel M & Tipping E

## Aim
- Develop rapid, map-ready data outputs for bracken NPP by using a single peak-biomass sample, enabling broad spatial comparison across sites.

## Study design and site selection
- Survey window: 21 July 2014 – 6 August 2014.
- Regions: northern Snowdonia (North Wales) and the Lake District.
- Site identification: ground observations and Google Earth imagery to locate bracken stands.
- Plot criteria: stands with ≥80% bracken cover, undisturbed by grazing; 49 plots in total.
- Substrates: aimed to cover a range of geological substrates; sites chosen to be free-draining soils where bracken thrives.

## Spatial and environmental data inputs
- Plot coordinates and altitude collected in the field with GPS.
- Mean annual precipitation per location from the CEH-GEAR dataset.
- Site-specific nitrogen deposition estimates from APIS.
- Visualization and planning assistance via Google Earth for locating stands.

## Field measurements and sample collection
- Plot layout: 1 × 1 m plots; all plant species recorded within each plot.
- Bracken biomass: fronds cut at ground level, bulk weighed; subsample (~500 g) dried to determine moisture content and total dry biomass.
- Vegetation: all other vegetation clipped at plot boundaries and dried for whole-plot analyses.
- Soil sampling: three 5 cm diameter auger cores per plot to 15 cm depth (or excavations where stones prevented auger use).
- Soil measurements: fresh weight; subsample moisture after drying; organic C by ignition; bulk density from total volume; pH in soil-water slurry; soils air-dried and milled for chemical analyses.
- Laboratory analyses for plant tissue and soil: C, N by oxidative combustion; P, K, Ca, Mg by ICP-OES; inorganic P via molybdate colorimetry after acidic extraction; organic P derived by difference.
- Stocks: soil total N, C, and macro-nutrient stocks calculated for top 15 cm using bulk density; nutrient stocks used as indicators of availability (organic P and total stocks for K, Ca, Mg).

## Data processing and trait integration
- Indicator scores: environmental trait scores calculated from species occurrences using Ellenberg framework (N, R, F, L); plot means computed from present species (UK-adapted scores); no cover-weighting to avoid bracken dominance.

## Data analysis and software
- Software: R, version 3.2.2.
- Data checks: normality assessed with Shapiro tests; transformations applied as needed.
- Exploratory analysis: PCA to investigate relationships among biomass and explanatory variables.
- Inferential modelling: ANOVA to test deviations from null models; multiple linear models evaluated with AIC to select best predictors.
- Predictor categories: (1) soil chemistry, (2) plant chemistry, (3) floristic trait means and biophysical variables; best four predictors considered across categories.

## GIS and data-product implications
- Georeferenced plot data enable spatial mapping of:
  - Above-ground bracken biomass (NPP proxy).
  - Topsoil nutrient stocks (C, N, P, K, Ca, Mg) and organic/inorganic P distinctions.
  - pH, bulk density, moisture status, and C:N ratios.
  - Ellenberg-based environmental trait scores across plots.
- Potential map layers:
  - Biomass distribution maps at plot-level resolution.
  - Soil nutrient stock and availability maps for top 15 cm.
  - Overlay with geology, elevation, and precipitation layers (CEH-GEAR, APIS) for habitat and management planning.
- Data provenance considerations:
  - Data drawn from multiple sources (CEH-GEAR, APIS, Google Earth, Ellenberg trait values); maintain metadata linking plot locations to source datasets and methods.
  - GPS-derived elevations and site coordinates essential for accurate spatial analyses and reproducible mapping.

## Data sources and metadata references
- CEH-GEAR precipitation dataset.
- APIS nitrogen deposition data.
- Google Earth for site identification.
- Ellenberg indicator values (UK-adapted).
- Analytical methods aligned with EPA 3051A digestion and ICP/OES/oxidative combustion protocols.

## Acknowledgements
- Notable funders and collaborators: NERC Macronutrient Cycling LTLS project and University of Liverpool; statistical method advice and site access acknowledged.