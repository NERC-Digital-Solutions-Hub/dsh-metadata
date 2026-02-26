# Climate suitability for Phytophthora ramorum (Pr) and Phytophthora kernoviae (Pk) infection in UK April 2013

- Objectives
  - Refine climate suitability models for Phytophthora ramorum (Pr) and Phytophthora kernoviae (Pk) using updated epidemiological data and literature.
  - Develop separate, species-specific models reflecting different temperature and humidity responses.
  - Improve spatial resolution to reduce data gaps (extending from Scotland to the UK) and validate model outputs against field transmission data.

- Approach
  - Examine climate suitability in 4 km grid squares over two-day (48 h) periods to reflect the infection process duration.
  - Invert lab time-to-infection data to derive hourly infection rates for each pathogen at specific temperatures; sum rates over 48 h to determine infection occurrence.
  - Apply species-specific thresholds:
    - Pk: infection between 3–27°C; below 5°C infection proceeds slowly; below 2°C no completion; above 27°C no completion; RH ≥85% for 10 h on both days required.
    - Pr: infection between 2–29°C; below 5°C infection occurs regularly; below 2°C limits; RH ≥85% for 10 h on both days required.
  - Reproduce climate suitability outputs for Scotland and extend to the UK.

- Environmental input data and processing
  - Data: hourly temperature and relative humidity at 4 km grid resolution (2007–2011) across the UK (360 × 288 grid; 23,246 land squares); provided by Met Office.
  - Processing: implement algorithm in R; compute predicted days suitable for infection per square; reproject to OSGB GB National Grid and resample to a 5.5 grid square resolution for overlay with other risk factors.
  - Output metric: average annual number of days suitable for infection per grid square.

- Model outputs and resolution
  - Separate models for Pr and Pk; spatial patterns indicate relative suitability across regions.
  - Seasonal and annual variation documented; 2011 showed higher Pr suitability (median ~150 days) than 2007–2010 (median ~70–100 days); Pk medians ranged ~15–25 days with 2010 highest among years.

- Key findings by region
  - Scotland vs UK
    - Scotland is predicted to be much more suitable for Pr than Pk; all grid cells show many more days suitable for Pr than Pk.
    - Across the UK, Scotland generally exhibits higher suitability than other regions.
  - Pr (Phytophthora ramorum)
    - High-risk areas on average include Argyll and Bute, Ayrshire, Dumfries and Galloway; contiguous high-suitability zones along the west and parts of the south coast and central belt.
    - Some years show large spatial variation in suitability; winter months contribute heavily to predicted infection opportunities.
  - Pk (Phytophthora kernoviae)
    - Higher suitability in Argyll and Bute, Ayrshire, Dumfries and Galloway, central Highlands, Perthshire, and north Highlands (including Skye and Orkney), but overall lower absolute suitability than Pr.
    - All cells have relatively low annual Pk suitability with interannual variability up to ~12 days.

- Seasonal patterns and interpretation
  - Pr infection tends to peak in November–February; capable of year-round occurrence, particularly in winter.
  - Pk infection tends to peak June–August; more constrained to the growing season.
  - The broader geographic reach and seasonality of Pr reflect its faster infection process at low temperatures.

- Model validation
  - Datasets:
    - (i) Wild plantings and established plantings in England and Wales (2002–2009; 240 positives from 954 squares).
    - (ii) Scottish non-trade premises (2007–2012; 93 positives from 73 squares inspected).
    - (iii) Larch fragments across Scotland (FC and commercial; 229 positives from 25,791 fragments).
  - Method: binary logistic regression to assess whether climate suitability predicts infection status; evaluation at a 5.5 km grid resolution.
  - Results:
    - All datasets show climate suitability as a significant predictor of infection status.
    - AUC values indicate reasonable discrimination:
      - (i) England & Wales: Pr AUC 0.63; Pk AUC 0.72.
      - (ii) Scotland: AUC 0.65 (for Pr).
      - (iii) Larch plantations: Pr AUC 0.81.
    - Patterns: infected squares have higher average suitable-days per year than uninfected squares (e.g., +20 days for Pr in (i); ~+7 days for Pk in (i)).
    - In England & Wales, Pk model slightly outperforming Pr model, suggesting easier predictability where Pk has more stringent requirements.

- Data and outputs for risk frameworks
  - Climate suitability layers are designed to feed risk assessments, enabling integration with additional risk factors.
  - Findings support targeting surveillance in regions with higher predicted Pr suitability and seasonal windows with elevated risk, particularly in western Scotland and southern coastal areas.

- Implications for monitoring and policy
  - Provides spatially explicit, temporally resolved risk insights to inform surveillance, early detection, and management of Phytophthora spread.
  - Highlights the value of combining climate suitability with field data to refine monitoring priorities and resource allocation.
  - Demonstrates potential for broader data reuse and sharing of model inputs to enhance environmental monitoring efforts.