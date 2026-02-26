# Data Collection Methods (adapted from methods in Bennett et al (2021) Journal of Animal Ecology )

## Purpose and scope
- Describes methods for estimating site quality and population trends across 1,664 breeding sites of guillemots from 1981–2018.
- Data collected from five sub-colonies with intensive monitoring (up to four checks daily during the breeding season).
- Sites chosen to cover the full range of breeding habitats and site types; unique IDs assigned per year of occupation and sites mapped for consistent cross-year monitoring.
- Focus on egg laying and chick fledging success as primary outcomes; a chick is considered to have fledged if it reaches 15 days old unless evidence suggests otherwise.

## Site quality measurement
- Site quality is defined as the average breeding success at a site across all years except the current year (per site and per sub-colony).
- Breeding success metrics are derived from annual observations of egg laying and chick fledging outcomes.
- Data handling includes assigning unique site IDs, spatial mapping, and consistent monitoring across years.
- The monitoring design includes coverage of a wide range of habitat types and site characteristics, enabling robust site-quality comparisons.

## Trend measures
- Population trends derived from sub-colony size data (number of occupied breeding sites per year) and whole-colony population size.
- Trend direction and change points identified using structural-change analysis (R package strucchange) to detect significant breakpoints in time series.
- Each time series divided into phases (increasing, stable, decreasing); annual change within each phase computed as sub-colony trend slope.
- Phases categorized as increasing, decreasing (decline), or recovery (increase after decline); applied to both sub-colony and colony-wide data.
- Expected pattern across sites: sequences of increasing phases, followed by declines, then recoveries.

## New vs reoccupied sites
- Definitions:
  - Reoccupied sites: previously occupied in an earlier phase, unoccupied in the first year of the current phase, and occupied again later in the same phase.
  - New sites: sites not occupied in the first six years (burn-in) and occupied from year six onward in the increasing phase.
- Burn-in period: first five years used to minimize misclassification due to annual skipping of breeding (average skipping frequency ~7.1%).
- Proportions of new vs. reoccupied sites are calculated relative to total sites occupied in each sub-colony each year to account for size differences.

## Data collection details and approach
- Sub-colonies located on the western side of the island, within 100 meters of each other, selected to span the full range of breeding habitats and site types.
- Monitoring cadence and photographic mapping ensure consistent site identification across years.
- Data collection emphasizes reliable classification of breeding outcomes, site-status changes, and donor-specific effort to improve accuracy.

## Tools, methods, and references
- Statistical approach for detecting structural change uses the R package strucchange (Zeileis et al., 2002; 2003).
- Sited quality and long-term breeding success reference foundational studies (Harris & Wanless; Harris et al., 2020) and related methods for site-dependent population regulation (Kokko, Harris, Wanless, 2004).
- Key methodological sources supporting measurement definitions, burn-in concept, and interpretation of trend changes.