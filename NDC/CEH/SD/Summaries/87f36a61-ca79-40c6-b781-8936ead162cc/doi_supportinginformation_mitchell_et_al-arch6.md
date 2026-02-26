# Bird detection data for Seram, Buru, Buton and Sulawesi, Indonesia [NERC Wallacea Project NE/S007067/1] (2021) Mitchell, S.L., Edwards, D.P., Martin, R.W., Deere, N.J., Voigt, M., Kastanya, A., Karja, A., Akbar, P.G., Jordan, K., Tasirin, J., Zakaria, Z., Martin, T., Supriatna, J., Winarni, N., Davies, Z.G., Struebig, M.J.

## Overview of the data
- Two CSV files:
  - Mitchell_Wallacea_site_community_data.csv: abundance matrices for 426 bird species across 1350 sites; aggregated counts for Borneo (Sabah), Sulawesi (Buton), Seram, Buru; raw counts for Talaud and Sangihe.
  - Mitchell_Wallacea_site_metadata.csv: site coordinates and ecological metrics.
- Study scope:
  - Surveys conducted 2014–2020 across multiple islands: Borneo (Sabah), Sulawesi (Buton), Seram, Buru, Talaud, Sangihe.
  - 426 species and 1350 sites in total.
- Data units:
  - Abundance data include aggregated multi-visit counts on some islands and single-count data on Talaud/Sangihe.
- Purpose:
  - Facilitate cross-island comparisons of bird communities and support data-driven exploration and self-service analyses.

## Experimental design, sampling regime, and data collection
- Point-count surveys:
  - Borneo: 15-minute counts with unlimited radius.
  - Sulawesi (Buton), Seram, Buru: 10-minute counts.
  - Talaud and Sangihe: 20-minute counts.
- Repetition:
  - Borneo, Sulawesi, Seram, Buru: 4 visits per site.
  - Talaud and Sangihe: 1 visit per site (raw counts).
- Observers:
  - Island-specific observers (e.g., SLM, PGA, AK, KJ, RWM) led data collection.

## Mitchell_Wallacea_site_data and Mitchell_Wallacea_site_metadata.csv methods
- Mitchell_Wallacea_site_data.csv:
  - For each site: a unique Site identifier (prefixes denote landscape/transect).
  - Species columns: English names of the 426 species.
  - Abundance: aggregated counts per site (where applicable) or raw counts for Talaud/Sangihe.
- Mitchell_Wallacea_site_metadata.csv:
  - Site identifiers aligned with the data file.
  - Latitude and Longitude: decimal degrees of sampling points.
  - RAR: average species range size for the community.
  - RCAR: average range size across all individuals in the community.
  - Prop forest 250m: proportion of forest cover within 250 m of the site.
  - Prop forest 1000m: proportion of forest cover within 1 km of the site.
  - Island: island hosting the site.
  - Visits: number of visits used to compute aggregated abundances.

## Spatial and ecological calculations
- Forest cover estimation:
  - Based on 2018 Global Forest Change data (Hansen et al., 2013) at 250 m and 1 km radii around each site.
- Relative range metrics:
  - RAR (relative average range): log-transformed average range size across species in the community.
  - RCAR (relative community average range): log-transformed average range size across all individuals, using BirdLife International species ranges (BirdLife, 2020) with GBIF (2021) data for interpolation.
- Species range references:
  - BirdLife International (2020) for species range estimates.
  - GBIF (2021) data used in calculations and interpolation.

## Data structure and field details
- Site identifiers:
  - Prefixes indicate landscape or transect; for Sangihe and Talaud, prefixes denote the whole island.
- Metadata fields:
  - Latitude, Longitude, RAR, RCAR, Prop forest 250m, Prop forest 1000m, Island, Visits.
- Data alignment:
  - Site IDs in Mitchell_Wallacea_site_data.csv correspond to Mitchell_Wallacea_site_metadata.csv.

## Notes on use and interpretation
- Sampling variation:
  - Different count durations and visit numbers across islands affect comparability; use RCAR/RAR and forest-proportion metrics to contextualize community differences.
- Data application:
  - Suitable for cross-site and cross-island analyses of bird communities, integration with forest cover data, and exploration of species-range implications on community structure.
- Data provenance:
  - Mitchell et al. (2021); environmental and range references from Hansen et al. (2013), BirdLife International (2020), GBIF (2021).