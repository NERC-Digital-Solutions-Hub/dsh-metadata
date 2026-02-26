Bird detection data for Seram, Buru, Buton and Sulawesi, Indonesia [NERC Wallacea Project NE/S007067/1] (2021) Mitchell, S.L., Edwards, D.P., Martin, R.W., Deere, N.J., Voigt, M., Kastanya, A., Karja, A., Akbar, P.G., Jordan, K., Tasirin, J., Zakaria, Z., Martin, T., Supriatna, J., Winarni, N., Davies, Z.G., Struebig, M.J.

## Overview
- Data comprises two CSV files:
  - Mitchell_Wallacea_site_community_data.csv: abundance matrices for 426 bird species across 1350 sites.
  - Mitchell_Wallacea_site_metadata.csv: site-level attributes and calculated indices.
- Geographic scope: islands of Borneo (Sabah), Sulawesi (Buton), Seram, Buru, Sangihe and Talaud.
- Survey period: 2014–2020.
- Observation method and effort:
  - Borneo: 15-minute point counts with unlimited radius.
  - Sulawesi (Buton), Seram, Buru: 10-minute counts.
  - Talaud and Sangihe: 20-minute counts.
- Repetition:
  - Four visits per site on Borneo, Sulawesi, Seram, and Buru.
  - One visit per site on Talaud and Sangihe.
- Data content:
  - For each site, an experienced observer recorded all species seen or heard during the survey period within unlimited distance.
  - Abundance is aggregated across four visits for some islands; raw abundances are provided for Talaud and Sangihe.

## Experimental design, sampling regime and data collection
- Site selection and surveying teams:
  - Surveys conducted by multiple observers (e.g., SLM, PGA, AK, KJ, RWM) across islands.
- Spatial data:
  - Site GPS coordinates (latitude and longitude) recorded for each site.
- Habitat context:
  - Forest cover around each site estimated using 2018 Global Forest Change data (Hansen et al., 2013).
  - Forest cover values extracted at radii of 250 m and 1 km from each point.
- Community metrics:
  - Relative Average Range (RAR): mean species range size across the community (based on BirdLife International range estimates; BirdLife 2020).
  - Relative Community Average Range (RCAR): average range size across all individuals in the community (log-transformed values).
  - Species range estimates derived from GBIF records, anchored to BirdLife International distributions.
  - RCAR uses community-weighted mean range size; RAR uses species-level average ranges.
  
## Data files and key columns
- Mitchell_Wallacea_site_community_data.csv
  - Site: unique site identifier; prefix denotes landscape/transect (Sangihe/Talaud islands use island-wide prefixes).
  - Species columns: English names of the 426 bird species; abundance counts per site (aggregated across visits where applicable).
- Mitchell_Wallacea_site_metadata.csv
  - Siteunique identifier: links to Mitchell_Wallacea_site_community_data.csv.
  - Latitude, Longitude: precise sampling coordinates.
  - RAR: average species range size for the community.
  - RCAR: average individual range size across the community.
  - Prop forest 250m: proportion of forest cover within 250 m of the site.
  - Prop forest 1000m: proportion of forest cover within 1 km of the site.
  - Island: island on which the site is located.
  - Visits: number of visits used to create aggregated abundance estimates.

## Data processing and methodological notes
- Habitat and range metrics:
  - Forest cover estimates derived from Hansen et al. (2013) with 2018 data products.
  - RAR and RCAR calculated per Newbold et al. (2018) methodology, using BirdLife International species ranges (BirdLife, 2020) and GBIF records.
  - RCAR involves log-transformed range sizes; RAR uses species-average ranges.
- Data aggregation:
  - Abundances are aggregated across four visits for Borneo, Sulawesi, Seram, and Buru; Talaud and Sangihe rely on raw abundances from single counts.
- Quality and provenance:
  - Observers recorded all species detected within the specified survey duration and radius.
  - Data structured to support standard analyses and cross-site comparisons, with explicit site identifiers and harmonized metadata.

## Implications for analysts monitoring the environment
- Standardized, multi-site bird community data across multiple islands enables temporal and spatial comparisons of avian diversity and habitat associations.
- Availability of RAR and RCAR offers a consistent framework to assess species’ range-related biodiversity aspects at the community level.
- Habitat context (forest cover at 250 m and 1 km) supports analyses of habitat influence on community composition and range-size metrics.
- Data standardization and transparent metadata facilitate integration with other datasets and reusability for policy performance monitoring.

## Considerations and opportunities
- Dataset value can be enhanced by linking with additional environmental or anthropogenic data (e.g., climate variables, land-use change).
- Underlying data accessibility and documentation should be preserved to enable reuse, replication, and broader scrutiny.
- Differences in sampling effort (number of visits) and counts (aggregated vs. raw) should be accounted for in comparative analyses.