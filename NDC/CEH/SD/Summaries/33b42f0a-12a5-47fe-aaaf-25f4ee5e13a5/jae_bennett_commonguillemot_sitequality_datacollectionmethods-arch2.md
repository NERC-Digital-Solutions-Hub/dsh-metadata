# Data Collection Methods (adapted from methods in Bennett et al (2021) Journal of Animal Ecology )

## Overview
- Standardized methods to assess environmental health indicators via breeding site data from common guillemots.
- Two core outputs: site quality (habitat/siting quality) and population trend measures (sub-colony and colony-level).
- Includes distinction between new and reoccupied breeding sites to understand habitat turnover and use.
- Data span: 1981–2018 across five sub-colonies; 1664 breeding sites in total.

## Data collection design
- Sub-colonies located on the west side of the island, within 100 meters of each other, covering diverse habitat types (wide/flat ledges, narrow/sloped ledges, exposed platforms, enclosed niches; varying heights and aspects).
- Each breeding site assigned a unique ID in the year it was first occupied; monitored across years.
- Monitoring schedule: up to four checks per day during the breeding season.
- Data recorded at each site: egg laying and chick fledging success.
- Fledging criterion: chick reaches 15 days old unless evidence suggests otherwise.
- Visual mapping from photographs used to maintain consistency across years.

## Site quality metric
- Site quality estimated as the average breeding success at each site across all years, excluding the current year (per site).
- This follows the approach of Kokko et al. (2004) and provides a standardized measure of habitat/site quality.

## Trend analysis (sub-colony and colony levels)
- Derived from time-series of sub-colony size (number of occupied breeding sites each year).
- Trend direction changes identified with the R package strucchange to locate breakpoints where trends shift significantly.
- For each period between breakpoints:
  - Calculate the average annual change in sub-colony size (sub-colony trend slope).
  - Classify periods as increasing, stable, or decreasing.
- Repeated similarly for whole-colony population size.
- Phase classification:
  - Increasing (positive trend), Decreasing (negative trend), and Recovery (increasing after a decline).
  - Sequences consist of one or more increasing phases, followed by declines, then recoveries.

## New vs reoccupied sites
- Definitions:
  - Reoccupied sites: previously occupied in an earlier phase, unoccupied in the first year of the current phase, then occupied again later in the same phase.
  - New sites: first occupied from the sixth year of an increasing phase onward.
- Burn-in period: first five years of the increasing phase treated as burn-in to account for occasional skipping of breeding (average skipping ~7.1%).
- Assessment:
  - A site is considered reoccupied if it was occupied during the burn-in, unoccupied in year 6, and occupied again later in the increasing phase.
  - Only sites occupied from year 6 onward are considered as potential new sites.
  - Proportions calculated as the number of new and reoccupied sites divided by the total number of sites occupied in each sub-colony per year, to account for sub-colony size differences.

## Data management and quality
- Unique site identifications and photographic mapping enable consistent cross-year monitoring.
- Standardized data collection and analysis procedures facilitate comparability across sub-colonies and years.
- Outputs include clear formats (site quality measures, trend phases, and new vs reoccupied site metrics) suitable for reporting environmental health and policy performance over time.

## Outputs and interpretation
- Site quality scores per site (excluding current year) as a baseline for habitat suitability.
- Trend phase timelines for sub-colonies and the overall colony to assess population health and dynamics.
- Metrics on habitat turnover via the proportion of new vs reoccupied sites, indicating colonization dynamics and habitat use.
- All outputs support consistent reporting, visualization (maps and charts), and data portal storage for reuse and scrutiny.

## References
- Harris, M. P., Heubeck, M., Bogdanova, M. I., Newell, M. A., Wanless, S., & Daunt, F. (2020). The importance of observer effort on the accuracy of breeding success estimates in the Common Guillemot Uria aalge. Bird Study, 67(1), 93-103.
- Harris, M. P., & Wanless, S. (1988). The breeding biology of Guillemots Uria aalge on the Isle of May over a six year period. Ibis, 130(2), 172-192.
- Kokko, H., Harris, M. P., & Wanless, S. (2004). Competition for breeding sites and site-dependent population regulation in a highly colonial seabird, the common guillemot Uria aalge. Journal of Animal Ecology, 73(2), 367-376.
- Zeileis, A., Kleiber, C., Kraemer, W., & Hornik, K. (2003). Testing and Dating of Structural Changes in Practice. Computational Statistics & Data Analysis, 44, 109-123.
- Zeileis, A., Leisch, F., Hornik, K., & Kleiber, W. (2002). strucchange: An R Package for Testing for Structural Change in Linear Regression Models. Journal of Statistical Software, 7(2), 1-38.