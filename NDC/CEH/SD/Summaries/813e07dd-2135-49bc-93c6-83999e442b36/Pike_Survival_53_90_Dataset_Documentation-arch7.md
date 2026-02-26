# Pike Survival Data 1953-1990

## Overview
- A CSV dataset of binary survival data for Pike (Esox lucius) from Windermere Lake, UK, derived from capture-mark-recapture.
- Used in Vindenes et al. (2013) American Naturalist to study climate-change–related trait dynamics in a top freshwater predator.
- Data origin: Freshwater Biological Association (FBA) and later CEH (Centre for Ecology & Hydrology); rights noted as Database Right/Copyright © NERC - CEH/FBA.
- File: PikeSurvivalData1953_1990.csv (68 kb).

## Data Details
- Format: CSV
- Columns:
  - YEAR: Year of first capture of an individual fish
  - LENGTH: Fork length at capture (cm)
  - SURVIVAL: 1 if the individual was recaptured in the first period after capture, 0 otherwise
- Note on other measurements: Sex, weight, and age were recorded in laboratory processing, but are not included in this dataset.
- Related datasets (metadata and additional measures) available:
  - Pike 1944-2002 metadata
  - Pike - Fecundity Data 1963-2002
  - Pike - Growth Data 1944-1995
  - Windermere Lake Temperature 1944-2002

## Spatial and Temporal Coverage
- Location: Windermere Lake, Cumbria, Great Britain
- Approximate lake centre coordinates (OS Grid): SD393960
- OSGB36 Easting/Northing: 339385, 496080
- WGS84 coordinates: 54.360193, -2.935836
- Time span: Data collected from 1944 onward; the dataset specifically covers survival data for 1953–1990.
- Spatial resolution: Point-level data per capture event within a single lake (Windermere); site-level spatial detail within the lake is not provided in the CSV.

## Sampling Design and Collection Methods
- Sampling period and effort:
  - Standardised methodology from 1982: 64 mm bar mesh multifilament gill nets, 40 m × 3 m per net; 5 nets operated at multiple sites, in both north and south basins.
  - Sampling occurs between mid-October and late December; nets placed at approximately 4–5 m depth.
  - Sites fished for two weeks per season with rotating site selection; 10 sites per basin; annual net-day effort around 348 (1982–1989) and around 240 (since 1990), distributed roughly equally between basins.
- Data collection:
  - Captured pike are killed and processed in the laboratory.
  - Measurements taken: fork length (to 1 mm), wet weight (to 100 g), sex determination, aging via opercular bones.
  - Individually numbered tags used for mark-recapture; sightings by catch-and-release anglers also incorporated.
- Data interpretation:
  - Survival (SURVIVAL) derived from combined tag-recapture data and angler sightings, following methods in Haugen et al. (2007).

## Data Processing and Quality Assurance
- Survival is calculated using standardized procedures described in Haugen et al. (2007).
- Quality control practices include verification of measurements, with checks performed by permutations among three individuals as part of data validation.
- Age dating and birth-date assumption: nominal birth date set to 1 April for aging procedures.

## Provenance and Related Data
- Original data collected by FBA; subsequently maintained by CEH and its predecessors.
- Metadata and context links:
  - Metadata record for Pike 1944-2002
  - Related datasets: Pike fecundity, Pike growth, Windermere lake temperature
- Key references for methods:
  - Le Cren (1959) on aging via opercular bones
  - Frost & Kipling (1959) on age/growth from scales and opercular bones
  - Haugen et al. (2007) on density-dependent dynamics
  - Winfield et al. (2008) on pike population changes in warming lakes

## GIS Considerations and Potential Uses
- Suitable for GIS analyses that explore survival over time within a freshwater system.
- Time-series mapping possibilities:
  - Visualize survival (0/1) by year for individuals, or aggregate by year to show trends.
  - Examine potential spatial patterns within Windermere if site-level locational data can be inferred or joined from additional metadata (not present in this CSV).
- Integration opportunities:
  - Join with the Windermere Temperature dataset and other Pike-related datasets to analyze climate and biological responses spatially and temporally.
  - Combine with age/length data from related datasets for growth-survival analyses.
- Considerations and caveats:
  - Data cover 1953–1990; older and newer data may exist in other datasets.
  - Sampling design changed over time; ensure consistency when comparing across periods.
  - Spatial granularity is lake-wide in this dataset; per-site analyses would require additional site-location data.
  - Survival metric reflects first-interval recapture, which may influence interpretation for long-term survival analyses.

## Access and Citations
- Data rights: Database Right/Copyright © NERC - CEH/FBA
- Document version: 1, 29-8-2013
- Primary data usage reference: Vindenes et al. (2013), American Naturalist
- Additional methodological references listed within the data description (see above).