# Bird detection data for Seram, Buru, Buton and Sulawesi, Indonesia [NERC Wallacea Project NE/S007067/1] (2021) Mitchell, S.L., Edwards, D.P., Martin, R.W., Deere, N.J., Voigt, M., Kastanya, A., Karja, A., Akbar, P.G., Jordan, K., Tasirin, J., Zakaria, Z., Martin, T., Supriatna, J., Winarni, N., Davies, Z.G., Struebig, M.J.

## Overview of data
- Contains matrices detailing abundance for 426 bird species across 1350 sites on Borneo (Sabah), Sulawesi (Buton), Seram, Buru, Sangihe, and Talaud.
- Aggregated counts from four visits for Borneo/Sulawesi/Seram/Buru; raw abundances from single counts for Talaud and Sangihe.
- Data are organized into two CSV files:
  - Mitchell_Wallacea_site_community_data.csv: species-by-site abundance matrices.
  - Mitchell_Wallacea_site_metadata.csv: site-level metadata and derived indices.

## Experimental design, sampling regime and data collection
- Surveys conducted between 2014 and 2020.
- Visit durations by island:
  - Borneo: 15-minute point counts (unlimited radius).
  - Sulawesi (Buton), Seram, Buru: 10-minute counts.
  - Talaud and Sangihe: 20-minute counts.
- Community inventories involve different numbers of repeated visits:
  - Four visits on Borneo, Sulawesi, Seram, and Buru.
  - One visit on Talaud and Sangihe.
- For each point count, experienced observers recorded all species seen or heard during the survey period at the location.

## Mitchell_Wallacea_site_metadata.csv methods
- GPS coordinates (latitude and longitude) recorded for each site.
- Forest cover around each site estimated using 2018 Hansen Global Forest Change data.
- Forest cover calculated within radii of 250 m and 1 km from each site.
- community range metrics:
  - Relative Average Range (RAR): average species range size for all species in the community.
  - RCAR: community-weighted mean range size across all individuals recorded.
- Species range references:
  - BirdLife International (2020) ranges used as the basis for species ranges.
  - Ranges derived from GBIF (2021) records and expert input.
- Key predictors included in metadata:
  - Site ID (consistent with the community data file)
  - Latitude, Longitude
  - RAR, RCAR
  - Prop forest 250m, Prop forest 1000m
  - Island, Visits (number of visits at the site)

## Column headings - Mitchell_Wallacea_site_community_data.csv
- Site: Unique site identifier (prefix denotes landscape/transect; Talaud/Sangihe prefixes denote the island as a whole).
- Species columns: English names of the 426 bird species observed.

## Column headings - Mitchell_Wallacea_site_metadata.csv
- Site: Site identifier matching Mitchell_Wallacea_site_community_data.csv.
- Latitude: Site latitude in decimal degrees.
- Longitude: Site longitude in decimal degrees.
- RAR: Average species range size for the community.
- RCAR: Average individual range size across individuals in the community.
- Prop forest 250m: Proportion of forest cover within 250 m of the site.
- Prop forest 1000m: Proportion of forest cover within 1 km of the site.
- Island: Island where the site is located.
- Visits: Number of visits conducted for that site (used to create aggregated abundance estimates).