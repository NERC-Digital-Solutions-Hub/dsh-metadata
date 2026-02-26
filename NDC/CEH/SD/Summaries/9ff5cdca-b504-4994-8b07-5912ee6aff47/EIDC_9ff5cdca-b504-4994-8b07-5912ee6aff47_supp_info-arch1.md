# Supporting documentation for R code to reproduce analyses of aboveground carbon stocks and associated plant diversity in fragmented and continuous forest sites in Sabah, Malaysian Borneo (2017)

## Purpose and scope
- Provides the data and R code workflow to reproduce analyses from Fleiss et al. (2020) on aboveground carbon stocks (AGC) and plant diversity in fragmented (conservation set-asides within RSPO-certified oil palm plantations) and continuous forest sites in Sabah, Malaysian Borneo, 2017.
- Data inputs include veg_plot_summary.csv and associated field protocols; analyses are executed in analyses_and_figures.R.

## Data and study design
- Study design:
  - 18 sites: 14 fragmented set-asides and 4 continuous forest sites.
  - Field plots: 49 plots total (2–3 plots per fragmented site; 30 m radius main plots; 20 m radius subplots; additional 5 m radius sapling subplot; eight 1x1 m quadrats for seedlings).
  - Vegetation sampled: trees and palms ≥25 cm dbh in 30 m plots; trees and palms ≥10 cm and <25 cm dbh in 20 m subplots; saplings and seedlings in smaller nested subplots.
  - Additional measurements: lianas, coarse woody debris (CWD), soils (7 parameters), topography, fragmentation metrics (via UAV-derived land cover within buffers), distance to edge, age since fragmentation.
- Land-use contrast: conservation set-asides within RSPO-certified plantations vs continuous primary/logged forest.
- Data structure: plot-level data across 49 plots in 18 sites; fields include coordinates, forest type, AGC components, diameters, wood densities, biomass metrics, and environmental covariates.

## Biomass estimation workflow (carbon_stock_calculations.R)
- Live trees (≥10 cm dbh):
  - Biomass estimated with pantropical allometric equation (Chave et al. 2014) via the BIOMASS R package.
  - Wood density assigned to stems from Global Wood Density Database at the finest taxonomic level available.
  - Height estimation (for stems lacking field height): three methods compared:
    1) Second-order log-log relation between dbh and height from field estimates.
    2) Climatic model incorporating environmental stress (Chave et al. 2014).
    3) Southeast Asia regional model based on dbh (Feldpausch et al. 2012).
  - Eye height estimates validated against clinometer-based tangent method on a subset.
- Palms:
  - Biomass estimated with a mixed-species model using dry mass fraction (0.37), diameter, and stem height (Goodman et al. 2013).
  - Carbon content assumed 47.1%.
- Lianas:
  - Biomass estimated with pantropical allometric equation based on dbh (Schnitzer et al. 2006).
- Coarse Woody Debris (CWD):
  - Biomass estimated as volume × wood density.
  - Volume computed as a frustum of a cone; decay class assigned; density from decay-state-specific values (Pfeifer et al. 2015).
  - Carbon content assumed 47.1%.
- Oil palm AGC:
  - Time-averaged AGC for 0–30 year planting cycle estimated using oil palm growth curves (mean and 95% CI) from Carlson et al. 2013, 2012.
  - 15 datapoints simulated from a Normal distribution using mean/SD from growth curves.
- Conversion to carbon:
  - All biomass converted to carbon using 47.1% carbon content (Thomas & Martin 2012).
- Outputs:
  - plot_carbon dataframe with per-plot AGC metrics under multiple height-estimation methods (20 m and 30 m radii), including:
    - Tree carbon for 10–25 cm dbh and 25–<50 cm dbh classes, by height method.
    - Total tree carbon, palm carbon, liana carbon, CWD carbon, oil palm carbon, and total plot carbon.
    - Palm- and liana-specific components; CWD components by plot and context.
    - Totals combining different components (e.g., total_agc, tree_palm_carbon, etc.).
  - Additional columns for counts, mean dbh by class, wood densities, stem densities, and 7 soil parameters.

## Biodiversity metrics
- Genus-level diversity:
  - Richness per plot for seedlings (<2 cm), saplings (2–10 cm), and trees (≥10 cm).
  - Fisher’s alpha (genus-based) per plot for the same size classes.

## Data outputs and structure
- veg_plot_summary.csv: plot-level summary data used by analyses_and_figures.R; includes:
  - Site_plot_code, Site_code, Forest_type, coordinates, multiple AGC metrics (under different height methods), total AGC, mean diameters by class, mean wood densities by class, stem densities by class, palm counts, liana and CWD metrics, soil parameters, topography (slope, elevation), fragmentation metrics, area/edge buffers, nearest edge distance, years since fragmentation, Fisher’s alpha and richness by size class.
  - Derived variables: ForArea_buffer_Xm_m2 and ForEdge_buffer_Xm_index across buffers (200–2000 m).
- Quality control:
  - Standardized data collection protocols; one observer for height estimates to maintain consistency; data checked for errors.
  - Exclusion of four anomalous data points with extreme Fisher’s alpha values.

## Analytical methods and outputs produced by analyses_and_figures.R
- AGC comparisons:
  - Pearson correlations and scatterplots comparing tree-height estimation methods.
  - Land-use type comparisons of AGC (observed set-asides vs continuous forest vs oil palm proxy data).
  - Bayesian linear mixed-effects models (LMMs) assessing land-use effects on live tree/palm AGC and total AGC (across height methods).
  - Moran’s I to test spatial autocorrelation in LMM residuals.
  - Pseudo-R2 to quantify variance explained by liana and CWD components.
  - Plots of AGC estimates with 95% CIs by land-use type.
- Vegetation structure:
  - Boxplots and Bayesian LMMs for mean wood density, stem density, and mean dbh across four size classes (seedlings, saplings, small trees, medium-large trees).
- Drivers of variation in set-asides:
  - Fragmentation index and soil gradients derived via PCA (fragmentation PC1; soil PCs 1–2) across multiple buffer sizes (0.2–2 km).
  - GAMMs to assess predictors (fragmentation index, soil PCs, elevation, slope) on live tree and palm AGC in set-asides.
- Biodiversity–AGC relationships:
  - Bayesian GLMMs relating AGC to genus richness and Fisher’s alpha by size class.
- Predictive scenarios:
  - Predictions of average AGC for oil palm plantations with varying set-aside coverage (1–100%), plantations without set-asides, and continuous forest; with prediction intervals.

## Validation and quality assurance
- Analyses and code peer-reviewed and accepted for publication (Biological Conservation, Fleiss et al., 2020).
- Biomass workflow aligns with established R package (biomass) and published allometric references; code authors conducted internal checks for errors.

## Reproducibility and data provenance
- Inputs: veg_plot_summary.csv (plot-level summary) and Waddell et al. 2020 vegetation dataset for full vegetation data.
- Outputs: Figures and statistics identical to those reported in Fleiss et al. (2020) Biological Conservation article; all methods and models are documented within the code and accompanying text.
- Documentation links and references to data sources, protocols, and model parameters are provided within the document.