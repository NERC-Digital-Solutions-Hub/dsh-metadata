# Methods lifted from Productivity in a dominant herbaceous species is largely unrelated to soil macronutrient stocks, Rowe EC, Toberman H, Adams JL, Lawlor AJ, Thacker SA, Patel M & Tipping E

## Aim and study design
- Assess above-ground net primary productivity (NPP) of bracken from a single peak biomass sample to enable rapid sampling across multiple sites.
- Survey conducted July 21 to August 6, 2014, targeting peak bracken biomass.
- 49 plots selected to span different geological substrates, with roughly equal representation in North Wales (Snowdonia) and the Lake District.
- Plots required at least 80% bracken cover and no grazing trampling.
- Bracken and associated vegetation analyzed to relate biomass to soil chemistry, plant chemistry, and floristic/biophysical variables; environmental conditions inferred from species indicator scores.

## Field methods and sampling design
- Sites identified via ground observations and Google Earth to locate bracken stands visible in summer and winter senescence.
- Plot size: 1 × 1 m quadrats; altitude recorded in the field; mean annual precipitation per site obtained from CEH-GEAR dataset.
- Bracken fronds cut at ground level within the plot; bulk weighed, with a ~500 g subsample dried at 60°C to determine moisture content and total dry biomass.
- All other vegetation within and at plot boundaries cut and dried to constant weight.
- A 25 g subsample of dry fronds ground for chemical analysis.
  
## Soil sampling and laboratory analyses
- Soil sampled at three locations per plot using a 5 cm diameter auger to 15 cm depth; stones prevented sampling in some plots, resulting in holes instead with recorded dimensions.
- Fresh soil weighed; subsample dried to determine moisture; bulk density calculated from total soil volume.
- Organic carbon concentration determined by ignition at 350°C for three days; total soil C and N, and P, K, Ca, Mg determined using digestion and ICP-OES methods.
- Inorganic P extracted from a 0.5 g sub-sample using 0.5 M sulfuric acid, then analyzed by molybdate colorimetry.
- pH measured in a 10 g soil to 25 mL water slurry.
- Nutrient stocks (g m^-2) calculated for top 15 cm using bulk density; organic P and total K, Ca, Mg stocks used as indicators of availability.
- Plant and soil element stocks preferred over mere concentrations in dense soils to reflect availability.

## Environmental and floristic indicators
- Species occurrence used to derive environmental trait scores based on Ellenberg values: fertility (N), alkalinity (R), moisture (F), and light (L).
- Plot-specific indicator means calculated from the present species using recalibrated UK values; no cover-weighting applied to avoid bracken dominance and to dampen short-term variation.

## Data analysis and statistics
- Analyses performed in R (version 3.2.2).
- Normality assessed with Shapiro tests; variables transformed to achieve normality where needed.
- Explore relationships with principal components analysis (PCA) after transformation/normalization.
- Biomass assessed against potential predictors using analysis of variance (ANOVA) against the null model.
- Model selection via Akaike’s information criterion (AIC) to identify best predictor combinations from three predictor categories: soil chemistry, plant chemistry, and floristic trait/biophysical variables.
- Evaluated combinations included the best four predictors across categories based on single-factor AIC; additional cross-category comparisons were also assessed.

## Data management and reproducibility
- Data sources tracked; datasets created may be made discoverable with metadata; standard protocols and references (e.g., EPA digestion method, Ellenberg indicators) underpin methods and analyses.

## Acknowledgements and funding
- Funded by the UK Natural Environment Research Council (Macronutrient Cycling LTLS project; Grant NE/J011533/1) and the University of Liverpool (Grant NE/J011630/1).
- Acknowledgements to David Cooper for statistical guidance and to site owners/managers for access.

## References (selected guidance)
- Seasonal variation and sampling considerations for bracken.
- Databases and indicators used: CEH-GEAR precipitation, APIS deposition data, Ellenberg indicator values, and standard digestion/analytical methods.