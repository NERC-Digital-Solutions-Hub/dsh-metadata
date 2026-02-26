# Bird detection data for Seram, Buru, Buton and Sulawesi, Indonesia [NERC Wallacea Project NE/S007067/1] (2021) Mitchell, S.L., Edwards, D.P., Martin, R.W., Deere, N.J., Voigt, M., Kastanya, A., Karja, A., Akbar, P.G., Jordan, K., Tasirin, J., Zakaria, Z., Martin, T., Supriatna, J., Winarni, N., Davies, Z.G., Struebig, M.J.

## Overview
- A dataset of bird detections across 1,350 sites on Borneo (Sabah), Sulawesi (Buton), Seram, Buru, Sangihe, and Talaud.
- Contains 426 bird species abundance matrices and site-level metadata.
- Surveys conducted between 2014–2020 with varying survey durations and visit counts per site.
- Data supports analysis of species presence/abundance, habitat context, and community-level range metrics.

## Data Files and Structure
- Mitchell_Wallacea_site_community_data.csv
  - Matrices detailing abundance of 426 species across 1,350 sites.
  - Aggregated counts from four visits for Borneo (Sabah), Sulawesi (Buton), Seram, Buru; raw counts from single surveys for Talaud and Sangihe.
  - Column headers include Site and species columns (English species names).

- Mitchell_Wallacea_site_metadata.csv
  - Site-level metadata aligned with Mitchell_Wallacea_site_community_data.csv (Site ID shared between files).
  - Latitude and Longitude (decimal degrees).
  - RAR (average species range size across community) and RCAR (average individual range size across individuals in the community).
  - Prop forest 250m and Prop forest 1000m (proportion of forest cover within 250m and 1km radii).
  - Island and Visits (number of visits per site).

## Sampling Design and Data Collection
- Timeframe: surveys conducted 2014–2020.
- Site-specific survey durations:
  - Borneo: 15-minute point counts (unlimited radius).
  - Sulawesi (Buton), Seram, Buru: 10-minute counts.
  - Talaud and Sangihe: 20-minute counts.
- Community inventories involved different numbers of repeated visits:
  - Four visits to Borneo, Sulawesi, Seram, and Buru sites.
  - One visit to Talaud and Sangihe sites.
- Observers conducted point counts from stationary positions, recording all seen or heard species within the survey period and unlimited distance.

## Metadata, Habitat Context, and Derived Metrics
- Site metadata include GPS coordinates and forest cover context around sites.
  - Forest cover estimated using 2018 Hansen Global Forest Change data.
  - Forest proportions calculated within 250 m and 1 km radii around each site.
- Derived biodiversity metrics:
  - RAR (average species range size across the community).
  - RCAR (average individual range size across all individuals in the community).
  - Species range sizes drawn from BirdLife International (based on expert opinion and GBIF records).

## Data Definitions and Column Details
- Mitchell_Wallacea_site_community_data.csv
  - Site: unique site identifier; prefixes indicate landscape/transect; Talaud/Sangihe prefixes denote the whole island.
  - Species columns: English names of species observed.

- Mitchell_Wallacea_site_metadata.csv
  - Site: unique site identifier shared with community data; prefixes indicate landscape/transect.
  - Latitude, Longitude: geographic coordinates of each sampling point.
  - RAR, RCAR: derived community-range metrics.
  - Prop forest 250m, Prop forest 1000m: habitat context around site.
  - Island: island where site is located.
  - Visits: number of visits contributing to aggregated abundance estimates.

## Implications for Data Leadership and Usage
- Cross-island and cross-site comparability with standardized metadata and derived metrics (RAR/RCAR).
- Enables assessment of habitat associations (forest cover context) alongside species abundance.
- Supports coarse- and fine-grained analyses of community structure and species-range-based metrics.
- Important considerations for data governance:
  - Varying survey durations and visit counts across sites require careful handling of aggregated vs. raw counts.
  - Metadata provides provenance and context to facilitate data discovery, quality assessment, and integration with other data sources.