# Climate suitability for Phytophthora ramorum (Pr) and Phytophthora kernoviae (Pk) infection in UK

## Objectives
- Refine climate suitability models for Phytophthora infection by incorporating updated epidemiological data and literature.
- Develop separate models for Pk and Pr to reflect species-specific temperature and humidity responses.
- Improve spatial resolution to reduce data gaps, especially coastal regions.
- Validate model outputs against field data on onward transmission to assess predictive value and potential spread.

## Approach and modelling framework
- Infection windows: assess climate suitability in 4 km grid squares over 48-hour periods (two days), reflecting infection process timelines.
- Temperature-dependent infection: convert lab time-to-infection data into hourly infection rates by temperature; infection is considered successful in a 48-hour window when summed hourly rates reach one.
- Species-specific rules:
  - Pk: infection between 3°C and 27°C; below 5°C infection is slower and below 2°C prevents completion; at 28–29°C, limited probability of success.
  - Pr: infection between 2°C and 29°C; below 5°C infection occurs regularly; above 29°C prevents completion.
- Humidity: infection requires at least 85% RH for 10 hours or more on both days.
- Outputs: predicted number of suitable infection days per square per year; results are averaged across years and months; reprojected to OS GB National Grid with a 5.5 grid square resolution for risk integration.

## Environmental input data and processing
- Data: hourly temperature and relative humidity from 2007–2011 at 4 km resolution; 360 × 288 grid covering UK (23,246 land squares).
- Source: Met Office data provided for model input.
- Processing: climate layers reprojected to the GB National Grid and used to derive annual average days suitable for infection per square.
- Model code: implemented in R.

## Model outputs and interpretation
- Scotland-specific results:
  - Pr shows much higher suitability than Pk; high suitability areas include Argyll and Bute, Ayrshire, Dumfries and Galloway, with west and southern coasts and parts of the Highlands showing more days suitable for Pr.
  - Pk suitability is low overall in Scotland, with the highest values in Argyll and Bute, Ayrshire, central highlands, Perthshire, and north Highlands, but still much lower than Pr.
- UK-wide results:
  - Pr shows widespread suitability with notable regional variation; predicted annual days suitable for Pr infection can reach 150 days in some years (e.g., 2011) and 70–100 days in other years (2007–2010).
  - Pk shows lower suitability, with annual medians generally in the 15–25 day range across Scotland.
- Seasonal patterns:
  - Pr infection tends to peak November–February.
  - Pk infection tends to peak June–August.
- Year-to-year variability: substantial across years, particularly for Pr in Scotland.

## Validation and predictive value
- Validation datasets (grid cell resolution 5.5 km):
  - (i) England and Wales wild/established plantings: 954 squares; Pk model robust; Pr model less strong in this set; AUC values: 0.72 (Pk) and 0.63 (Pr).
  - (ii) Scottish non-trade premises: 73 squares; presence of Phytophthora (both species) predicted by Pr model; AUC = 0.65.
  - (iii) Larch plantations in Scotland: 1,487 squares; Pr presence predicted well; AUC = 0.81.
- Key interpretation:
  - Across datasets, climate suitability emerged as a significant predictor of infection status.
  - When pathogens’ species were separable (dataset i for Pk), the Pk model better distinguished infection status than the Pr model did for Pr.
  - For datasets where the species was not consistently recorded, the Pr model reasonably predicted the presence of Phytophthora overall.

## Key findings
- Scotland is predicted to have a much higher climate suitability for Pr than for Pk infection.
- Pr infection is predicted to occur year-round with winter emphasis, while Pk is largely restricted to April–October.
- The spatial distribution of Pr suitability is broad and variable across years, with western coastal and southern coastal regions typically more suitable.
- Model validation supports the usefulness of climate suitability as a predictor of onward transmission in several real-world datasets, albeit with variability in predictive strength by dataset and pathogen.

## Implications and limitations
- The models provide a refined, higher-resolution framework to anticipate where climate conditions could permit Phytophthora infection and onward transmission.
- Predictions depend on the accuracy of lab-derived infection rates translated into hourly rates and on the quality/coverage of input climate data.
- Field validation shows generally good discriminatory power, but seasonality and regional differences suggest site-specific validation remains important.
- Extension from Scotland to the UK enhances applicability for risk assessment and management planning.