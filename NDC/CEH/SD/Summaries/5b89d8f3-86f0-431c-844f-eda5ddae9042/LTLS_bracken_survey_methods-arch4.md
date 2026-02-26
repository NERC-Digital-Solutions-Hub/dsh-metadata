# Methods lifted from Productivity in a dominant herbaceous species is largely unrelated to soil macronutrient stocks

## Study aim and scope
- Assess above-ground net primary production (NPP) of bracken via a single peak biomass sample to enable rapid survey across multiple sites.
- Conducted a short, intensive field survey during peak bracken biomass (21 July – 6 August 2014).
- Cover two comparable UK regions: northern Snowdonia (North Wales) and the Lake District; plots selected across different geological substrates.

## Sampling design and plots
- 49 plots sampled, each 1 × 1 m, with bracken stands of at least 80% cover and not grazed/trampled.
- Sites identified using ground observations and Google Earth imagery to locate bracken stands visible in summer and winter.
- Plot locations chosen to span a range of substrates and environmental conditions; sampling window synchronized with peak above-ground biomass.

## Measurements and laboratory analyses (bracken)
- Bracken fronds within each plot clipped at ground level, bulked, weighed, and a ~500 g subsample dried at 60°C to determine moisture content and total dry biomass.
- A 25 g subsample of dry bracken ground for chemical analysis.
- Plant tissue analyses included carbon (C) and nitrogen (N) contents by oxidative combustion with thermal conductivity detection (Vario EL).
- Phosphorus (P), potassium (K), calcium (Ca), and magnesium (Mg) concentrations measured by Inductively Coupled Plasma Optical Emission Spectrometry (ICP-OES).

## Soil sampling and analyses
- Soil sampled from three locations per plot using a 5 cm diameter auger to 15 cm depth; if stones impeded sampling, holes were excavated with dimensions recorded.
- Fresh soil weighed; subsamples dried to determine moisture content; organic C measured by ignition at 350°C for three days; bulk density calculated from sample volume.
- pH measured in a soil-water slurry (10 g soil, 25 mL water).
- Soil samples air-dried, ground; total C, N, P, K, Ca, Mg measured using the same methods as plant tissue analyses; organic P estimated as total P minus inorganic P.
- Inorganic P extracted from 0.5 g soil milled sample using 0.5 M sulfuric acid with subsequent molybdate colorimetry (AQ2 analyser).
- Stocks (g m^-2) calculated for top 15 cm using bulk density; organic P stock and total element stocks (K, Ca, Mg) used as indicators of availability.

## Environmental and trait data
- Mean annual precipitation per site from CEH-GEAR (interpolated meteorological data).
- Site altitude determined in the field with GPS.
- Plot-specific nitrogen deposition estimates obtained from APIS (Air Pollution Information System).
- Environmental conditions inferred via Ellenberg indicator values (N, R, F, L) calculated as mean values across species present (UK recalibrations); presence-absence weighting used to minimize short-term variation and to avoid bracken domination in indicator means.

## Data processing and statistical analysis
- Analyses performed in R (version 3.2.2).
- Variable distributions assessed with Shapiro–Wilk tests; necessary transformations applied to normalize distributions.
- Relationships between biomass and predictors explored using principal components analysis (PCA) after standardization.
- Predictive relationships tested with analysis of variance (ANOVA) against a null model.
- Model selection conducted with Akaike’s Information Criterion (AIC) across three predictor categories: soil chemistry, plant chemistry, and floristic/biophysical variables.
- Combined best predictors from all categories (top four by AIC for single-factor models) were also evaluated.

## Data quality, governance, and limitations
- Data collected from field plots with careful measurement of bulk density and moisture; some plots could not be sampled to full depth due to stones, requiring excavation with recorded dimensions.
- Indicator-value scores based on species present, using standardized Ellenberg framework, recalibrated for UK species; cover-weighting avoided to prevent bracken dominance from skewing results.
- Sampling design integrated external data sources (CEH-GEAR for precipitation, APIS for N deposition) to contextualize site conditions.
- Emphasis on reproducibility through documented laboratory methods (EPA digestion protocol, Vario EL analysis, ICP-OES) and transparent statistical approach (R, PCA, ANOVA, AIC).