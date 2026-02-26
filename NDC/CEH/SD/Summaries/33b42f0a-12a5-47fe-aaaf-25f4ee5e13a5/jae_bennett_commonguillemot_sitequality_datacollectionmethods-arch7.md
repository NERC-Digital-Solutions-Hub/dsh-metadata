# Data Collection Methods (adapted from methods in Bennett et al (2021) Journal of Animal Ecology)

- Overview
  - Studied 1664 breeding sites across multiple sub-colonies on the Isle of May, monitored from 1981 to 2018.
  - Sub-colonies were located on the west side of the island within 100 meters of each other and included diverse habitats (e.g., wide/narrow ledges, exposed platforms, enclosed niches).
  - Each breeding site was assigned a unique ID in the first year of occupation and mapped on photographs to ensure consistent year-to-year monitoring.
  - Data collected at each site included egg laying and chick fledging; a chick was considered fledged if it survived to 15 days unless evidence suggested otherwise.
  - Monitoring occurred up to four times daily during the breeding season, with an average of about 171 sites per sub-colony (range 37–323).

- Site quality
  - Site quality is defined as the average breeding success at a site across all years, following Kokko et al. (2004).
  - For each site, breeding success was calculated excluding the current year to produce a stable quality metric.

- Monitoring and data structure
  - Sub-colony size (number of occupied breeding sites) was recorded annually to derive population trends.
  - Monitoring began at different times across sub-colonies (1981–1984), with ongoing recording of occupancy and success.
  - A consistent spatial framework was maintained by mapping sites and using unique identifiers across years.

- Trend measures
  - Trends were derived from multi-year sub-colony size time series.
  - The time series were partitioned into periods of consistent trend direction using structural-change analysis (R package strucchange) to identify breakpoints.
  - For each identified period, the average annual change in sub-colony size (sub-colony trend slope) was calculated.
  - Periods were categorized as increasing, stable, or decreasing; within these, phases were labeled as increase, decline, or recovery (increase after a decline).
  - The same segmentation and labeling approach was applied to whole-colony population size in addition to sub-colony analyses.

- New vs reoccupied sites
  - Reoccupied sites were defined as sites occupied in a previous phase, unoccupied in the first year of the current phase, and then occupied again later in the same phase.
  - A five-year burn-in was used to minimize misclassification due to skipping breeding in early years (average skipping frequency ~7.1%).
  - Only sites that became new from the sixth year of a phase were considered “new” for comparability with reoccupied sites.
  - Proportions of new and reoccupied sites were calculated relative to the total number of sites occupied in each sub-colony each year, to account for size differences.

- Key methods and tools
  - Structural-change analysis to detect breakpoints in trends (strucchange R package).
  - Consistent year-to-year site mapping via photographic schematics and unique site IDs.
  - Data integration across years and sub-colonies to assess spatial and temporal dynamics of breeding success and occupancy.

- References for methodology
  - Harris et al. (2020) on observer effort and breeding success estimates.
  - Harris & Wanless (1988) on breeding biology of Guillemots.
  - Kokko, Harris, & Wanless (2004) on competition for breeding sites and population regulation.
  - Zeileis et al. (2002, 2003) on the strucchange package and structural-change testing.