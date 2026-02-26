# Data Collection Methods (adapted from methods in Bennett et al (2021) Journal of Animal Ecology )

## Context and Scope
- Studied 1664 breeding sites across five sub-colonies on the island, covering diverse breeding habitats.
- Monitoring: up to four visits per day during the breeding season; sites mapped with unique IDs for year-to-year consistency.
- Habitats ranged from wide ledges with many pairs to narrow, exposed or enclosed niches; monitoring began in 1981–1984.
- At each site, eggs laid and chicks fledged were recorded; a chick fledged if it reached 15 days of age unless otherwise indicated.
- Site quality is defined as the average breeding success at a site across all years, excluding the current year.

## Site Quality
- Data span: breeding success recorded 1981–2018 across the five sub-colonies.
- For each site, calculate the mean breeding success with the current year excluded; this serves as the site quality metric.
- Spatially explicit site-level data allows comparison across habitat types and years.

## Trend Measures
- Derived from sub-colony size time series (number of occupied breeding sites per year).
- Structural-change detection:
  - Use the R package strucchange to identify breakpoints where population trends shift direction.
  - Classify periods on each side of breakpoints as increasing, stable, or decreasing.
  - Compute the average annual change within each period (sub-colony trend slope).
- Aggregation:
  - Apply the same procedure to whole-colony population size.
  - Label phases as increasing, decreasing (decline), or recovery (increasing after decline).
- Result: sequences of increasing, declining, and recovery phases for both sub-colony and colony-wide trends.

## Determination of New vs Reoccupied Sites
- Definitions:
  - Reoccupied: sites that had been occupied in a previous phase, unoccupied in the first year of the current phase, but occupied later in the current phase.
  - New sites: first appear from the sixth year of the current phase.
- Burn-in period:
  - First five years of the initial increasing phase are treated as burn-in to minimize misclassification due to occasional skips in breeding (average skipping ~7.1% of individuals).
- Measures:
  - A site is considered reoccupied if occupied at least once in the burn-in, unoccupied in year six, and then occupied later in the phase.
  - Proportions of new and reoccupied sites are calculated relative to total sites occupied in each sub-colony in each year, ensuring comparability across sub-colonies of different sizes.

## References
- Harris, M. P., et al. (2020). The importance of observer effort on the accuracy of breeding success estimates in the Common Guillemot Uria aalge. Bird Study.
- Harris, M. P., & Wanless, S. (1988). The breeding biology of Guillemots Uria aalge on the Isle of May over a six-year period. Ibis.
- Kokko, H., Harris, M. P., & Wanless, S. (2004). Competition for breeding sites and site-dependent population regulation in a highly colonial seabird, the common guillemot Uria aalge. Journal of Animal Ecology.
- Zeileis, A., et al. (2002, 2003). strucchange: An R package for testing and dating structural changes. Journal of Statistical Software / Computational Statistics & Data Analysis.