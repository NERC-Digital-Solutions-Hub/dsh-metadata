# WildCrickets06L_EarlyDominanceVsSenescence

- Overview
  - Dataset describes singing activity for each cricket sample and each male individual.
  - Includes early-life dominance classification: high dominance (H) or low dominance (L) relative to the population median.
  - Aims to relate early dominance to senescence-related singing patterns.

- Key variables
  - EarlyDominance: H or L (dominance early in life)
  - Year: year when the cricket was alive
  - ID: individual identification
  - Temp: ambient temperature at sampling (°C)
  - Age: age at sampling (days)
  - Sings: whether the cricket sang at sampling (1 = yes, 0 = no)

- Observations and structure
  - Observations are per sample and per individual male.
  - Sings is a binary outcome; EarlyDominance is a categorical grouping (H/L).

- Potential uses
  - Investigate associations between early-life dominance and later singing behavior/senescence.
  - Examine effects of age and temperature on singing activity.
  - Explore cohort or individual-level patterns across years.

- Data quality considerations
  - EarlyDominance is a categorical label (H/L) based on population median—clarify calculation method if reusing.
  - Sings and EarlyDominance are binary/categorical; ensure consistent encoding (H/L, 1/0).
  - Temperature units are degrees Celsius; confirm measurement conditions.
  - Year is described as “year when the cricket was alive”—determine whether this refers to calendar year or a life-year count for longitudinal interpretation.
  - Metadata completeness (sampling design, location, methods) would enhance usability and discoverability.