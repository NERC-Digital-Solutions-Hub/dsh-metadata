# Climate suitability for Phytophthora ramorum (Pr) and Phytophthora kernoviae (Pk) infection in UK

- Objective of modelling
  - Refine climate suitability models for Phytophthora infections by incorporating updated epidemiological data and literature.
  - Develop separate, pathogen-specific models for Pr and Pk to reflect distinct temperature and humidity responses.
  - Improve spatial resolution to reduce data gaps, extend UK coverage (originally Scotland, now UK), and validate model outputs against field transmission data.

- Data and inputs
  - Environmental data: hourly temperature and relative humidity at 4 km grid resolution, 2007–2011, across the UK (360 x 288 lat-long grid; 23,246 land squares). Data supplied by Met Office (via Laura Burgin).
  - Data preprocessing: reprojected climate layers to Ordnance Survey GB National Grid and resampled to a 5.5 grid square resolution for integration with risk factors.
  - Reference epidemiology: laboratory-derived infection time distributions by temperature (inverted to hourly infection completion rates) used to drive the model (Kyle Jennings, FERA data).

- Modelling approach
  - Spatial-temporal framework: evaluate climate suitability within 4 km grid squares over 48-hour (two-day) windows, reflecting the time needed for the infection process.
  - Infection criteria: infection on a focal day if cumulative hourly infection rates sum to one over the 48-hour period, with species-specific temperature and humidity rules.
  - Pathogen-specific rules:
    - Pr (Phytophthora ramorum): infection between 2°C and 29°C; upper threshold at 29°C with 1/3 success probability for 28–29°C; regular infections below 5°C.
    - Pk (Phytophthora kernoviae): infection between 3°C and 27°C; upper threshold at 27°C; slower and rarer below 5°C.
  - Lower humidity rule: infection succeeds only if RH ≥ 85% for at least 10 hours on both of the two days.
  - Outputs: layers representing the number of days suitable for infection per square per year; annual averages across 2007–2011; results oriented for integration into risk frameworks rather than absolute probabilities.
  - Geographic scope: initially Scotland-focused; extended to cover the UK.

- Outputs and products
  - Spatial layers of climate suitability (days per year) for Pr and Pk, aligned to UK grid for overlay with additional risk factors.
  - Summary and visualization:
    - Maps of annual average suitable days per square; standard deviation across years to show year-to-year variability.
    - Seasonal and annual patterns of predicted infection: Pr tends to peak in November–February; Pk peaks June–August.
  - Relative suitability: results presented as relative measures across grid cells, not absolute risk, enabling comparative assessments.

- Model validation and data use
  - Validation datasets (summarized to model grid resolution):
    - (i) Wild and established plantings in England & Wales (2002–2009): 954 squares inspected; 31 positive for Pk, 74 positive for Pr.
    - (ii) Scottish non-trade premises (2007–2012): 73 squares inspected; 34 positive (both pathogens combined).
    - (iii) Larch plantations in Scotland (FC and commercial): 1,487 squares inspected; 39 positive for Pr.
  - Analytical approach: binary logistic regression to test whether square infection status is predicted by model-derived climate suitability; assessed with AUC.
  - Key validation results:
    - All datasets show climate suitability as a significant predictor of infection status.
    - AUC values indicate reasonable discriminative ability: Pr in EW (0.63), Pr in Scottish non-trade premises (0.65), Pr in larch plantations (0.81); Pk in EW (0.72) when modeled separately.
    - Quantitative associations: infected squares tend to have ~20 more suitable days/year (Pr) or ~40 more days (Pr in larch; dataset iii); Pk in EW shows ~7 more days on average.
  - Interpretation: climate suitability models discriminate well between infected and uninfected sites, with pathogen-specific models performing differently across datasets. Pk predictions showed strong performance in some datasets, while Pr predictions were more robust across Scotland-wide validation.

- Key findings and patterns
  - Scotland is predicted to be much more climatically suitable for Pr than for Pk; across Scotland, Pr-days are typically many tens to a couple hundred per year, whereas Pk-days are generally far fewer (median around 17–18 days, with variability).
  - Spatial patterns: high Pr suitability along west and south coasts and central belt; Pk suitability clustered in Argyll & Bute, Ayrshire, Dumfries and Galloway, central highlands, Perthshire, and parts of the north highlands (including Orkney), but still lower than Pr.
  - Temporal patterns: Pr suitability is widespread year-round with stronger winter signal; Pk suitability largely restricted to April–October, reflecting its narrower temperature/humidity envelope.
  - Year-to-year variability is substantial, especially for Pr in some regions; annual medians for Pr ranged notably (e.g., 70–100 days in 2007–2010, rising to ~150 days in 2011).

- Implications for data use and decision support
  - Outputs can be combined with other risk factors to identify priority areas for monitoring, early detection, and management actions.
  - The modelling framework supports scenario analyses and can be extended as more epidemiological data become available.
  - Encourages data sharing and integration across systems to improve model inputs, reduce patchiness, and enhance web-accessible data products for end users.

- Limitations and considerations
  - Validation notes: field data are limited and uneven across datasets; seasonality predictions require further field validation.
  - Outputs are relative measures of suitability rather than absolute infection risk; depend on the quality and resolution of input climate data and laboratory-derived infection times.
  - Differences in data collection and pathogen recording across sites can affect model alignment with observed infections.