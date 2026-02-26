# Methods lifted from Productivity in a dominant herbaceous species is largely unrelated to soil macronutrient stocks, Rowe EC, Toberman H, Adams JL, Lawlor AJ, Thacker SA, Patel M & Tipping E

- Purpose and scope
  - Assess above-ground net primary productivity (NPP) of bracken from a single peak-biomass sample to enable rapid, widespread sampling.
  - Survey conducted July 21 – August 6, 2014 to capture peak bracken biomass.
  - 49 plots chosen to span diverse geological substrates, with roughly equal representation from North Wales (Snowdonia) and the Lake District.
  - Bracken stands required to have 80% cover and no trampling by grazing; bracken is avoided by most livestock and shows strong chemical defenses.

- Study design and site data
  - Plot layout: 1 × 1 m plots demarcated for consistent sampling.
  - Location and environment: sites selected via ground observation and Google Earth; altitude measured in the field; mean annual precipitation from CEH-GEAR; plot-specific nitrogen deposition from APIS.
  - Plant and site measurements: all plant species within plots recorded; environmental trait scores derived from indicator values (Ellenberg N, R, F, L) using UK recalibrations; cover-weighting not applied.

- Biomass and sample collection
  - Bracken fronds cut at ground level within plots; fronds bulk weighed, with a ~500 g subsample dried at 60°C for moisture content and total dry biomass calculation.
  - A 25 g subsample of dry fronds ground for chemical analysis.

- Soil sampling and analysis
  - Soil collected from three positions per plot with a 5 cm diameter auger to 15 cm depth (or excavated holes where stones prevented auger use); bulk density calculated from total soil volume.
  - Fresh soil weighed; moisture content determined after drying; organic carbon measured after ignition at 350°C; pH measured in soil-water slurry.
  - Subsamples dried and ground for chemical analyses; concentrations of total C, N, P, K, Ca, Mg determined using the same methods as plant tissue.
  - Organic P estimated as total P minus inorganic P; inorganic P extracted with 0.5 M sulfuric acid, then measured by molybdate colorimetry using an automated analyzer.
  - Stocks (g m-2) of nutrients calculated using bulk density and total soil depth; total soil N and C stocks used as indicators of nitrogen availability.

- Data processing and statistical analyses
  - Data checked for normality (Shapiro test); transformations applied as needed.
  - Multivariate relationships explored with principal components analysis.
  - Biomass prediction assessed via analysis of variance against a null model.
  - Multiple linear models evaluated with Akaike’s Information Criterion (AIC) to identify best predictor sets from: soil chemistry, plant chemistry, and combined floristic/biophysical variables.
  - Best-performing combinations (up to four predictors) tested across the three categories and in aggregate.
  - Analyses conducted in R, version 3.2.2.

- Dataset characteristics relevant to data governance
  - Data types include: biomass measurements, moisture content, plant tissue nutrient concentrations (C, N, P, K, Ca, Mg), soil chemistry (C, N, P, K, Ca, Mg, pH, organic P), soil bulk density, depth, and nutrient stocks; plot metadata (region, altitude, precipitation, N deposition); species indicator scores (Ellenberg N, R, F, L).
  - Per-plot records integrate biological measurements with environmental context and site metadata, enabling cross-site comparisons and nutrient-stock calculations.
  - Methods reference standard protocols and instrumentation (e.g., EPA digestion method 3051A; Vario EL analyzer; ICP-OES Optima 7300DV), supporting reproducibility and data quality.
  - Data processing steps include explicit calculations of nutrient stocks and environmental indicators, along with transparency about transformations and model selection criteria.

- Data quality, limitations, and considerations for stewardship
  - Potential data gaps: some plots could not reach 15 cm soil depth due to stones; alternative hole measurements recorded, which may introduce depth-related variability.
  - Indicator-value approach uses presence-absence data to mitigate short-term environmental variation, potentially reducing bias from transient changes.
  - Transformations and normality assessments indicate attention to statistical robustness; model selection via AIC helps prevent overfitting.
  - The document describes dataset as part of a broader Macronutrient Cycling programme, but does not specify a public data repository or metadata standard beyond methodological references.

- Acknowledgments and references
  - Funded by UK Natural Environment Research Council (LTLS Macronutrient Cycling Programme) and the University of Liverpool.
  - References include methodological sources for bracken ecology, soil and plant nutrient analyses, Ellenberg indicator values, and R statistical software.