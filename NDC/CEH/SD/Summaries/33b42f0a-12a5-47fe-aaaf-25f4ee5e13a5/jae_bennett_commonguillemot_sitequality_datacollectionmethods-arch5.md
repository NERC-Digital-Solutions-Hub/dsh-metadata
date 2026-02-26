# Data Collection Methods (adapted from methods in Bennett et al (2021) Journal of Animal Ecology )

## Overview

- Study covers 1664 breeding sites across five sub-colonies, with data collected from 1981–2018.
- Sub-colonies are on the island's west side, within 100 m of each other, and include diverse habitats (e.g., wide ledges, narrow ledges, exposed platforms, enclosed niches).
- Each breeding site is assigned a unique ID from the year it was first occupied and mapped via photographs to ensure consistent multi-year monitoring.
- Monitoring occurs up to four times daily during the breeding season; data include egg laying and chick fledging outcomes.
- Fledging is defined as reaching 15 days of age unless evidence suggests otherwise.
- A key derived metric is site quality: the average breeding success at a site across years, excluding the current year.

## Site Quality Measure

- Site quality is calculated as the average breeding success across all years (excluding the current year) for each site.
- Breeding success combines egg laying and chick fledging outcomes, providing a single metric used to rank site quality.
- Data collected at regular intervals and linked to precise site IDs for longitudinal analyses.

## Trend Measures

- Sub-colony size (number of occupied breeding sites) is tracked yearly to assess population trends.
- Time-series are partitioned into multi-year periods with consistent trend direction using structural-change methods (R package strucchange).
- Breakpoints identify when population trends shift direction; periods are categorized as increasing, stable, or decreasing.
- For each period, the average annual change (sub-colony trend slope) is calculated.
- Trends are analyzed at both sub-colony and whole-colony levels.
- Phases are classified as: increasing, decreasing (decline), and recovery (increase following a decline).

## Determination of New vs Reoccupied Sites

- Reoccupied sites are those that were occupied in a prior phase, unoccupied in the early part of the current phase, and later reoccupied within the same phase.
- A five-year burn-in is used to avoid misclassifying temporary non-breeding as new occupancy, accounting for occasional skipping (average skipping frequency ~7.1% in the population studied).
- New sites are assessed from the sixth year of the phase to ensure comparability with reoccupied sites.
- Proportions of new versus reoccupied sites are calculated per sub-colony per year to account for size differences.

## Data Governance and Quality Considerations for Data Stewards

- Provenance: track site IDs, year, sub-colony, habitat type, and monitoring regime to ensure reproducibility.
- Metadata: capture methodology, definitions (e.g., fledging age, site quality computation), and references to analytical methods (e.g., strucchange).
- Data quality: account for observer effort and potential biases in breeding success estimates; document observer variability and data collection conditions.
- Interoperability: maintain consistent data formats across years and sub-colonies; map site IDs to stable geographic references and photographs.
- Updating and versioning: implement clear procedures for updating site statuses, breakpoints, and trend classifications as new years are added.
- Documentation of processing: preserve scripts (e.g., R packages and functions used for structural-change analysis) and processing steps for auditability.
- Data security and access: manage sensitive or embargoed components if applicable; provide transparent access to aggregated results while protecting raw data integrity.
- Linkages: maintain references to underlying literature (e.g., Harris et al. 2020; Harris & Wanless 1988; Kokko et al. 2004) to support method choices and interpretation.

## References (context for methods)

- Harris, M. P., et al. (2020). The importance of observer effort on the accuracy of breeding success estimates in the Common Guillemot Uria aalge.
- Harris, M. P., & Wanless, S. (1988). The breeding biology of Guillemots Uria aalge on the Isle of May.
- Kokko, H., Harris, M. P., & Wanless, S. (2004). Competition for breeding sites and site-dependent population regulation in a highly colonial seabird.
- Zeileis, A., et al. (2002, 2003). strucchange package and applications for testing and dating structural changes.