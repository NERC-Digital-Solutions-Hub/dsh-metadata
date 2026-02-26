# WildCrickets06J_EarlyEmergenceVsSenescence Description of content

- Purpose: Describes singing activity per cricket sample and per individual male, with classification of early or late emergence relative to the population median in the season.

- Core target variable:
  - Emergence: E (emerged earlier) or L (emerged later)

- Temporal context:
  - Year: the year when the cricket was alive

- Identity and sampling context:
  - ID: unique individual identifier

- Environmental and biological context:
  - Temp: ambient temperature at sampling (in °C)
  - Age: age of the cricket at sampling (in days)

- Behavioral outcome:
  - Sings: 1 if singing was observed at sampling, 0 otherwise

- Data structure implications for data systems:
  - Rows correspond to samples (and associated individuals) with both demographic (year, ID, age) and context (temperature) data plus a binary behavioral outcome (Sings) and a categorical emergence label (E/L)

- Metadata considerations for data quality and reuse:
  - Clear definitions for Emergence (E vs L) tied to population median per season
  - Consistent measurement units (°C for Temp, days for Age)
  - Need for documentation on sampling method, timing, and any missing data patterns

- Potential analyses and data products:
  - Model probability of singing as a function of age, temperature, and emergence class
  - Explore how emergence timing relates to singing activity across years
  - Use ID to track individual trajectories if longitudinal data exist

- Data governance implications:
  - Ensure consistent coding of Emergence and Sings across datasets
  - Maintain provenance: year, sampling conditions, and measurement methods
  - Assess data completeness and potential biases due to missing temperature or age information