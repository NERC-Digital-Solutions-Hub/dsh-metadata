# Data Collection Methods (adapted from methods in Bennett et al (2021) Journal of Animal Ecology )

- Overview
  - An analysis spanning 1664 breeding sites across five sub-colonies.
  - Data collected from 1981 to 2018; sites monitored up to four times daily during the breeding season.
  - Each site in a sub-colony was given a unique ID when first occupied and mapped for consistent year-to-year monitoring.
  - Egg laying and chick fledging data were recorded to derive breeding success.

- Site quality
  - Defined as the average breeding success at sites across all years, excluding the current year (i.e., site quality is a historical average).
  - Breeding success is based on egg laying and chick fledging; a chick is considered fledged if it reaches 15 days old unless there is contrary evidence.

- Monitoring and site characteristics
  - Sub-colonies are geographically close (within 100 m) and cover a full range of habitat types (from high-density to sparsely populated, including exposed platforms and enclosed niches).
  - Habitats vary in physical characteristics (height above sea level, slope, aspect).

- Trend measures
  - Sub-colony size (number of occupied sites) tracked yearly; whole-colony population size also analyzed.
  - Structural-change analysis (R package strucchange) identifies year(s) when population trends shift direction (break points).
  - Each time series is divided into periods with consistent trend direction and labeled as increasing, stable, or decreasing.
  - For each period, the average annual change (sub-colony trend slope) is calculated; this is then categorized as increasing, decreasing, or recovery after decline.
  - The same process is applied to whole-colony data to yield colony-wide trend phases.
  - Across sub-colonies and the colony as a whole, sequences typically show one or more increasing phases, followed by declining phases, then a recovery phase.

- Determination of new vs reoccupied sites
  - Reoccupied sites are those previously occupied in a prior phase, unoccupied in the first year of the current phase, and then reoccupied later in that phase.
  - A five-year burn-in is used to reduce misclassification due to annual skipping by guillemots (average skipping rate ~7.1%).
  - New sites are identified starting from year six of the current increasing phase.
  - Proportions of new vs reoccupied sites are calculated relative to the total sites occupied in each sub-colony per year, allowing comparison across sub-colonies of different sizes.

- References
  - Harris, M. P., et al. 2020. The importance of observer effort on the accuracy of breeding success estimates in the Common Guillemot.
  - Harris, M. P., & Wanless, S. 1988. The breeding biology of Guillemots on the Isle of May.
  - Kokko, H., Harris, M. P., & Wanless, S. 2004. Competition for breeding sites and site-dependent population regulation.
  - Zeileis, A., et al. 2002–2003. strucchange: tools for testing and dating structural changes in data.