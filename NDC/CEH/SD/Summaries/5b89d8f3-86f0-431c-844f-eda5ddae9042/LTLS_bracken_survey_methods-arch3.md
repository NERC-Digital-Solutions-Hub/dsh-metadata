# Methods lifted from Productivity in a dominant herbaceous species is largely unrelated to soil macronutrient stocks

## Overview
- Describes a short-term field survey assessing above-ground bracken productivity (NPP) and associated soil/plant nutrient status across multiple sites to evaluate relationships with environmental variables.
- Sampling aimed to occur at peak above-ground biomass to enable rapid, across-site comparisons.

## Study design and site selection
- Timeframe: 21 July 2014 to 6 August 2014.
- Locations: 49 plots in two regions – northern Snowdonia (North Wales) and the Lake District.
- Plot criteria: stands with ≥80% bracken cover, not grazed/trampled; sites chosen to span a range of geological substrates; sites selected based on ground observations and Google Earth searches.
- Site context data: mean annual precipitation from CEH-GEAR; altitude measured in the field via GPS; plot-specific nitrogen deposition estimates from APIS.

## Measurements and sampling protocol
- Bracken biomass: 1 × 1 m plots; fronds cut at ground level, bulked and weighed; a ~500 g subsample dried at 60°C to determine moisture and calculate total dry biomass.
- Plant chemistry: a 25 g subsample of dry bracken fronds ground for analysis of carbon and nitrogen contents (oxidative combustion with thermal conductivity detection).
- Other vegetation: all species within the plot recorded (presence-absence).
- Soil sampling: three sub-samples per plot using a 5 cm diameter auger to 15 cm depth (adjusted where stones prevented sampling); fresh soil weighed, subsamples dried for moisture and organic C determination; bulk density calculated from sample volume and dry weight.
- Soil chemistry: concentrations of total C, N, P, K, Ca, Mg measured via the same methods as plant tissue analysis; organic P estimated as total minus inorganic P.
- Inorganic phosphorus: 0.5 M sulfuric acid extraction, followed by molybdate colorimetry using a discrete analyzer.
- pH: measured in a 10 g soil to 25 mL deionised water slurry.
- Special notes: where stones impeded soil sampling to 15 cm, holes were excavated and dimensions recorded.

## Nutrient stocks and indicators
- Soil nutrient stocks: calculated for the top 15 cm using measured bulk density (g m^-2) for elements (including organic P and total stocks of K, Ca, Mg).
- Availability indicators: soil total N/C ratio used as an indicator of N availability; nutrient stocks used to reflect availability in dense mineral soils or organic soils, as appropriate.
- Floristic environmental indicators: Ellenberg indicator values (N, R, F, L) calculated from species present; mean plot values derived from UK-validated indicator scores; presence-absence data used (no cover-weighting) to reduce bracken dominance effects and to dampen short-term variation.

## Data analysis and modeling
- Software: R (version 3.2.2).
- Preliminary checks: Shapiro tests for normality; transformations applied as needed to achieve normal/near-normal distributions.
- Exploratory analyses: principal components analysis to assess relationships between biomass and potential predictors.
- Model assessment: analysis of variance (ANOVA) to test differences from the null model for biomass; multiple linear models evaluated with Akaike’s information criterion (AIC) to identify best predictor combinations within three categories: soil chemistry, plant chemistry, and floristic/biophysical variables.
- Model selection: considered the best four predictors across all categories based on single-factor AIC, and also evaluated combinations using a four-predictor rule.
- Data handling approach: emphasis on standardized comparisons across sites with transformations and normalization.

## Special considerations and limitations
- A few plots could not be sampled to full depth due to stones; this was documented as a limitation.
- Bracken and its own abundance could dominate indicator scores; presence-absence-based indicators were used to mitigate this influence.

## Acknowledgements and references
- Funding: UK Natural Environment Research Council (LTLS Macronutrient Cycling Research Programme) and University of Liverpool.
- Acknowledgements: thanks to site owners/managers and individuals providing statistical guidance.
- References: includes methodological sources for Ellenberg indicators, nutrient analyses, and related ecological measurement techniques (e.g., EPA digestion method, ICP-OES, and sequence of data sources like CEH-GEAR and APIS).