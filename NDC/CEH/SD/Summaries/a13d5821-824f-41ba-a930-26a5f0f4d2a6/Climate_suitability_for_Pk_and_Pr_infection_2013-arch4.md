# Climate suitability for Phytophthora ramorum (Pr) and Phytophthora kernoviae (Pk) infection in UK

## Objectives
- Refine climate suitability models for Phytophthora ramorum (Pr) and Phytophthora kernoviae (Pk)
- Incorporate updated epidemiological data and recent literature
- Develop species-specific models reflecting distinct temperature and humidity responses
- Improve spatial resolution to reduce data gaps (especially coastal regions)
- Validate model outputs against field datasets to assess alignment with onward transmission

## Modelling approach
- Assess climate suitability in 4 km grid squares over 48-hour periods (two consecutive days)
- Convert lab time-to-infection data into hourly infection rates; infection completion over 48 hours requires rates to sum to 1
- Apply species-specific temperature and humidity rules to determine infection probability within each 48-hour window
- Consider lower/upper temperature thresholds and humidity requirements:
  - Pr: infection 2–29°C; RH ≥85% for ≥10 hours on both days
  - Pk: infection 3–27°C; RH ≥85% for ≥10 hours on both days; additional gap rule below 2°C (see below)
  - Additional rules: if <2°C, no further infection for either pathogen; for Pk, dipping below 2°C for ≥16 hours during a period invalidates it
  - Probabilistic nuance: near upper thresholds (28–29°C for Pr) partial success (1/3 probability)
- Extend models from Scotland to cover the UK

## Environmental input data and processing
- Hourly relative humidity and temperature data (2007–2011) at 4 km resolution; 360 × 288 grid; 23,246 land squares
- Data provided by Met Office; processed in R
- Model outputs resampled/reprojected to Ordnance Survey GB National Grid (5.5 grid square resolution) for integration with risk factors
- Outcome metric: average annual number of days suitable for infection per grid cell (summed over years and months)

## Model rules (infections per 48-hour period)
- Lower thresholds: no completion below 2°C for both pathogens
- Upper thresholds:
  - Pr: no completion above 29°C; 28–29°C yields 1/3 probability of success
  - Pk: no completion above 27°C
- Relative humidity: infection requires RH ≥85% for at least 10 hours on both days

## Outputs and interpretation
- Generated layers indicating the average number of suitable infection days per year per square
- Seasonal peaks:
  - Pr infection peaks mainly November–February
  - Pk infection peaks June–August
- Cross-UK patterns show Scotland generally more suitable for Pr than Pk
- UK-wide patterns reveal higher suitability for Pr relative to Pk, with regional variation

## Scotland-focused findings
- Pr climate suitability far higher than Pk; Pk typically under 30 days/year suitable (median ~17.6; mean ~17.5 ± 4.4)
- Pr shows 50–200 suitable days/year in Scotland (varying by year; median ~117.2; mean ~118.4 ± 33.9)
- High Pr risk areas include Argyll and Bute, Ayrshire, Dumfries and Galloway; Pk suitability is lower overall, with notable but smaller clusters

## UK-wide and regional patterns
- Figures depict annual and regional variation in predicted suitable days across the UK
- Some years (e.g., 2011) exhibit substantially higher Pr suitability (median ~150 days) than earlier years
- Pk suitability remains comparatively low across regions, with western Scotland showing the most notable values

## Model validation
- Validation datasets (infection presence vs. climate suitability) compiled from:
  - (i) Wild and established plantings in England/Wales (detail: 954 squares; Pr and Pk identified)
  - (ii) Scottish non-trade premises (73 squares; both pathogens)
  - (iii) Larch plantations across Scotland (1,487 squares; Pr)
- Binary logistic regression shows climate suitability is a significant predictor of infection status across all datasets
- Discrimination (AUC):
  - Dataset (i): Pk model AUC ≈ 0.72; Pr model AUC ≈ 0.63
  - Dataset (ii): AUC ≈ 0.65
  - Dataset (iii): AUC ≈ 0.81
- Infected squares consistently show higher average annual days of suitability (e.g., +20 days for (ii); +40 days for (iii); larger differences for Pr in larch plantations)

## Data strategy implications for Data Leaders
- Demonstrates value of high-resolution, temporally explicit climate data for ecological risk assessment
- Highlights need for transparent, interoperable data schemas (grid-based, time-stamped environmental data; infection status records)
- Emphasizes cross-sector data integration (field surveys, nurseries, plantations) to validate models
- Identifies data gaps and limitations (regional/coastal coverage, evolving data standards, variability in field reporting)
- Supports iterative, user-informed product development for risk assessment tools within broader plant health and biosecurity networks