# Bird detection data for Seram, Buru, Buton and Sulawesi, Indonesia [NERC Wallacea Project NE/S007067/1] (2021) Mitchell, S.L., Edwards, D.P., Martin, R.W., Deere, N.J., Voigt, M., Kastanya, A., Karja, A., Akbar, P.G., Jordan, K., Tasirin, J., Zakaria, Z., Martin, T., Supriatna, J., Winarni, N., Davies, Z.G., Struebig, M.J.

## Overview
- Primary outputs are two CSV data files containing bird abundance data and site metadata.
- Focus on 426 bird species across 1350 sites on multiple Indonesian islands.
- Data structure includes aggregated counts (from multiple visits) and raw counts (from single visits) depending on island.

## Data files
- Mitchell_Wallacea_site_community_data.csv
  - Matrices detailing abundance for 426 bird species across 1350 sites.
  - Aggregated counts from four visits for Borneo (Sabah), Sulawesi (Buton), Seram, Buru.
  - Raw abundances from single counts for Talaud and Sangihe.
  - Columns: Site identifier and one column per species (species names in English).

- Mitchell_Wallacea_site_metadata.csv
  - Site-level metadata with GPS coordinates and derived landscape metrics.
  - Columns: Site, Latitude, Longitude, RAR, RCAR, Prop forest 250m, Prop forest 1000m, Island, Visits.

## Geographic and temporal scope
- Islands: Borneo (Sabah), Sulawesi (Buton), Seram, Buru, Sangihe, Talaud.
- Surveys conducted 2014–2020.
- Point counts:
  - Borneo: 15-minute counts, unlimited radius.
  - Sulawesi (Buton), Seram, Buru: 10-minute counts.
  - Talaud and Sangihe: 20-minute counts.
- Repetition by site: 4 visits on Borneo, Sulawesi, Seram, and Buru; 1 visit on Talaud and Sangihe.

## Methods and data processing
- Community data collection
  - For each point count, observers recorded all species seen or heard during the counting period within unlimited distance.
  - Conducted by multiple teams across islands (e.g., SLM, PGA, AK, KJ, RWM).

- Site metadata and forest context
  - GPS coordinates recorded for each site.
  - Forest cover estimated around each site using 2018 Hansen Global Forest Change data.
  - Forest cover values extracted within 250 m and 1 km radii from each site.

- Derived biodiversity metrics
  - Relative Average Range (RAR): average species range size within the community.
  - Relative Community Average Range (RCAR): average range size across individuals in the community, using log-transformed species range values.
  - Species range estimates sourced from BirdLife International (2020), based on expert opinion and GBIF-informed interpolation.

## Key variables and columns
- Community data (Mitchell_Wallacea_site_community_data.csv)
  - Site: unique site identifier; prefixes denote landscape/transect.
  - Species columns: English names of species observed.

- Metadata (Mitchell_Wallacea_site_metadata.csv)
  - Site: unique site identifier (matches community data).
  - Latitude, Longitude: decimal degrees.
  - RAR: average species range size for the community.
  - RCAR: average individual range size for the community.
  - Prop forest 250m: proportion of forest cover within 250 m.
  - Prop forest 1000m: proportion of forest cover within 1 km.
  - Island: island where site is located.
  - Visits: number of visits conducted at the site (used to create aggregated abundance estimates).

## GIS and analytical implications
- Enables map-based visualization of species abundance and community-range indices across islands.
- Allows contextualization of biodiversity with forest-cover context at local scales (250 m and 1 km radii).
- Supports comparative analyses of aggregated vs. raw counts across islands with differing sampling effort.
- Useful for policy, conservation planning, and public-facing biodiversity communication in the Wallacea region.

## Considerations and caveats
- Sampling effort varies by island (4 visits on some islands vs. 1 on Talaud and Sangihe) affecting comparability of abundance values.
- Derived metrics (RAR/RCAR) rely on external range estimates and log-transformed calculations; interpretation should account for methodological assumptions from Newbold et al. (2018) and BirdLife International 2020 sources.