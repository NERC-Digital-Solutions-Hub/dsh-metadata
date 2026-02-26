# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from South Basin of Windermere 1945 to 2013.

## Overview
- Long-term monitoring dataset for the South Basin of Windermere, Cumbria, England.
- Coverage: 1945 to 2013 for multiple environmental variables.
- Collected by the Freshwater Biological Association and later by the Centre for Ecology & Hydrology (CEH) and its predecessors.
- Variables include physical, chemical, and biological indicators relevant to lake health and ecosystem dynamics.
- Data have been used in numerous scientific studies, illustrating their value for long-term environmental monitoring and trend analysis.

## Variables and Measurements
- Surface temperature (TEMP; °C)
- Surface oxygen saturation (OXYG; % air-saturation)
- Secchi depth (SECC; m) for water clarity
- Alkalinity (ALKA; µg CaCO3 per L)
- pH (PH)
- Ammonium (NH4N; µg N per L)
- Nitrate (NO3N; µg N per L)
- Soluble reactive phosphate (PO4P; µg P per L)
- Total phosphorus (TOTP; µg P per L)
- Dissolved reactive silicon (SIO2; µg SiO2 per L)
- Phytoplankton chlorophyll a (TOCA; µg per L)

## Sampling Regime and Collection Methods
- Sampling frequency: weekly or fortnightly.
- Time span: some variables collected since 1945.
- Depth-integrated water sampling: from 0 to 5 m (1945–1962), 0 to 10 m (1962–1964), and 0 to 7 m (1964 onward).
- Sampling location: from a boat at a buoy at the deepest part of the lake.
- Data currently provided cover March 1945 to end of 2013.

## Data Structure and Quality Control
- Format: CSV with the following columns:
  - sdate (date of measurement)
  - variable (description of the variable)
  - value (measurement value)
  - sign_if_LT_LOD (indicator if below detection limit, using a < sign)
- Status: raw data that has not yet undergone quality control or calibration (except for some double entries from 2005 onward); visual checks have been performed.
- Metadata context included in the dataset (depth ranges, sampling method, detection-limit flag).

## Data Availability, Metadata, and Documentation
- Data are downloadable as a CSV file with clearly described fields and units.
- Depth integration history and measurement context are documented (sampling depths, deepest-point buoy location).
- Detection-limit indicators are provided to aid interpretation of low measurements.

## Origin, Stewardship, and Data Governance
- Originated with the Freshwater Biological Association (FBA); subsequently managed by CEH and its predecessor institutions.
- Emphasizes transparency of data use and the need for open data sharing; metadata and provenance are maintained to support reuse.
- Current status indicates raw data awaiting full quality assurance and calibration; ongoing governance supports future updates, verification, and public sharing.

## Use in Research and Impact
- Recent publications employing this dataset include:
  - Do early warning indicators consistently predict non-linear change in long-term ecological data? (Journal of Applied Ecology, 2016)
  - Insights into percid population and community biology from a 70-year perch study in Windermere (2015)
  - Pathogens trigger top-down climate forcing on ecosystem dynamics (Oecologia, 2016)
  - Predicting the impact of changing nutrient load and temperature on Windermere phytoplankton (Freshwater Biology, 2012)
  - Spring phytoplankton phenology and drivers of change (Freshwater Biology, 2012)
  - Environmental DNA metabarcoding of lake fish communities reflecting long-term data (Molecular Ecology, 2016)
  - Multiple other studies highlighting climate-themes, carbon and nutrient cycling, and lake ecology (various journals, 2012–2016)

## Implications for Monitoring Frameworks
- Demonstrates the value of long-term, multi-variable datasets for assessing environmental health and policy decisions.
- Highlights common framework considerations:
  - Data gaps and coverage over decadal scales
  - Access to and sharing of datasets with transparent provenance
  - Metadata completeness and clarity (sampling methods, depths, LOD flags)
  - Standardization and transformation needs to enable inter-study comparability
  - Implementing data governance to ensure datasets meet quality and openness standards
  - Communicating complex long-term findings clearly to policymakers and stakeholders

## Key Notes for Practitioners
- The dataset is a rich resource for testing monitoring indicators and trend analyses but requires comprehensive quality assurance and calibration before formal use in decision-making.
- Its structure (CSV with explicit LOD indicators) supports reproducibility and integration with other time-series datasets.
- Ongoing data stewardship and open-data practices will enhance its utility for policy evaluation and future planning.