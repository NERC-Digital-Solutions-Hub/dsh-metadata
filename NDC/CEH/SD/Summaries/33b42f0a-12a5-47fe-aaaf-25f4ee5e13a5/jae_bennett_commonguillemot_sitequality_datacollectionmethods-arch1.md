# Data Collection Methods (adapted from methods in Bennett et al (2021) Journal of Animal Ecology )

## Data scope and monitoring
- 1664 breeding sites across five sub-colonies were included.
- Breeding data span from 1981 to 2018; monitoring occurred up to four times daily during the breeding season.
- Sub-colonies are on the west side of the island, within 100 meters of each other, selected to cover the full range of breeding habitats (e.g., wide ledges, narrow ledges, exposed platforms, enclosed niches; varying heights and aspects).
- Each site, identified in the first year of occupation, was mapped and assigned a unique ID to enable consistent year-to-year monitoring.
- At each site, egg laying and chick fledging were recorded; a chick was considered to have fledged if reaching 15 days of age unless there was evidence to the contrary.

## Site quality measurement
- Site quality is estimated as the average breeding success at sites across all years, following Kokko et al. (2004).
- Breeding success at each site is calculated from data excluding the current year (i.e., using past years’ performance).
- This approach yields a site-quality metric that reflects historical productivity rather than the present-year outcome.

## Trend measures
- Trends are derived from sub-colony size time series (number of occupied breeding sites per year) and, separately, whole-colony population size.
- Breakpoints are identified using the R package strucchange to detect significant changes in trend direction.
- Each time series is partitioned into periods with consistent trend direction and labeled as increasing, stable, or decreasing.
- For each period, the average annual change (sub-colony trend slope) is calculated.
- Phases are categorized as increasing (positive slope), decreasing (decline), or recovery (increasing after a decline).
- The colony-level analysis mirrors the sub-colony approach; both levels show sequences of one or more increasing phases, followed by one or more declining phases, and then a recovery phase.

## New vs reoccupied sites
- Reoccupied sites are defined as sites that had been occupied in a previous phase, were unoccupied in the first year of the current phase, and were occupied again later in the current phase.
- A burn-in period of the first five years is used when estimating reoccupation rates to account for occasional skipping of breeding.
  - Average annual skipping frequency is 7.1% (n=696/9741 individuals).
- To ensure comparability with new sites, only occupy data from the sixth year onward are considered for new site identification.
- The proportion of sites that are new or reoccupied is calculated for each sub-colony and year, accounting for sub-colony size differences.

## References
- Harris, M. P., Heubeck, M., Bogdanova, M. I., Newell, M. A., Wanless, S., & Daunt, F. (2020). The importance of observer effort on the accuracy of breeding success estimates in the Common Guillemot Uria aalge. Bird Study, 67(1), 93-103.
- Harris, M. P., & Wanless, S. (1988). The breeding biology of Guillemots Uria aalge on the Isle of May over a six year period. Ibis, 130(2), 172-192.
- Kokko, H., Harris, M. P., & Wanless, S. (2004). Competition for breeding sites and site-dependent population regulation in a highly colonial seabird, the common guillemot Uria aalge. Journal of Animal Ecology, 73(2), 367-376.
- Zeileis, A., Kleiber, C., Kraemer, W., & Hornik, K. (2003). Testing and Dating of Structural Changes in Practice. Computational Statistics & Data Analysis, 44, 109-123.
- Zeileis, A., Leisch, F., Hornik, K., & Kleiber, D. (2002). strucchange: An R Package for Testing for Structural Change in Linear Regression Models. Journal of Statistical Software, 7(2), 1-38.