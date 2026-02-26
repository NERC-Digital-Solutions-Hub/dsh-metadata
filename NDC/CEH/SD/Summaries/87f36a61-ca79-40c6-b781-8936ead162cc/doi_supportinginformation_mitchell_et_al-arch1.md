# Bird detection data for Seram, Buru, Buton and Sulawesi, Indonesia [NERC Wallacea Project NE/S007067/1] (2021) Mitchell, S.L., Edwards, D.P., Martin, R.W., Deere, N.J., Voigt, M., Kastanya, A., Karja, A., Akbar, P.G., Jordan, K., Tasirin, J., Zakaria, Z., Martin, T., Supriatna, J., Winarni, N., Davies, Z.G., Struebig, M.J.

## Overview of the dataset
- Contains abundance matrices for 426 bird species across 1,350 sites on Borneo (Sabah), Sulawesi (Buton), Seram, Buru, and the islands of Talaud and Sangihe.
- Data are aggregated from four visits for Borneo, Sulawesi, Seram, and Buru; raw abundances from single counts for Talaud and Sangihe.
- Two main CSV files:
  - Mitchell_Wallacea_site_community_data.csv: species-by-site abundance data.
  - Mitchell_Wallacea_site_metadata.csv: site-level metadata and computed indices.

## Experimental design, sampling regime and data collection
- Survey period: 2014–2020.
- Point counts:
  - Borneo (Sabah): 15-minute counts with unlimited radius.
  - Sulawesi (Buton), Seram, Buru: 10-minute counts.
  - Talaud and Sangihe: 20-minute counts.
- Repeats:
  - 4 visits to each site on Borneo, Sulawesi, Seram, and Buru.
  - 1 visit to each site on Talaud and Sangihe.
- Data collection method: experienced observers recorded all species seen or heard during the counting period from a stationary position.
- Personnel: site surveys conducted by various researchers (abbreviated initials in metadata).

## Site metadata and spatial data
- Mitchell_Wallacea_site_metadata.csv includes:
  - Site unique identifier (shared with the community data file).
  - Latitude and Longitude (decimal degrees).
  - RAR: average species range size for all species recorded in the community.
  - RCAR: average individual range size across all individuals recorded in the community.
  - Prop forest 250m: proportion of forest cover within 250 m of the site.
  - Prop forest 1000m: proportion of forest cover within 1 km of the site.
  - Island: island where the site is located.
  - Visits: number of visits per site (used to create aggregated abundance estimates).

## Forest cover estimation and spatial context
- Forest cover estimates derived from 2018 Hansen Global Forest Change data (Hansen et al., 2013).
- Proportions calculated within 250 m and 1 km radii around each site using R packages raster, gtools, and rgdal.
- Island and site identifiers coded to reflect landscape or transect prefixes.

## Relative Average Range (RAR) and Relative Community Average Range (RCAR)
- RAR and RCAR methods follow Newbold et al. (2018) to quantify species’ range sizes within communities.
- RCAR uses log-transformed values of the global species range for each recorded individual.
- Species range estimates sourced from BirdLife International (BirdLife, 2020), combining expert opinion with GBIF-based interpolation (GBIF, 2021).

## Data structure and column definitions
- Mitchell_Wallacea_site_community_data.csv:
  - Site: unique site identifier; prefixes denote landscape or transect (Sangihe/Talaud prefix indicates the whole island).
  - Species columns: English names of the 426 bird species observed.
- Mitchell_Wallacea_site_metadata.csv:
  - Site: unique site identifier (shared with community data file).
  - Latitude, Longitude: geographic coordinates.
  - RAR: average species range size for the community.
  - RCAR: average individual range size for the community.
  - Prop forest 250m: forest cover within 250 m.
  - Prop forest 1000m: forest cover within 1 km.
  - Island: island where the site is located.
  - Visits: number of visits to the site.

## Data sources and references
- Location and sampling details across multiple islands in Indonesia (Borneo/Sabah, Sulawesi/Buton, Seram, Buru, Talaud, Sangihe).
- Forest cover data: Hansen et al. (2013) with 2018 update.
- Range size metrics: Newbold et al. (2018) methodology; species range inputs from BirdLife International (BirdLife, 2020) and GBIF (GBIF, 2021).

## Potential analyses and considerations for analysts
- Cross-island comparisons of species richness and abundance under different sampling regimes.
- Relationships between bird community metrics (RAR, RCAR) and local habitat context (forest cover at 250 m and 1 km).
- Modeling how survey effort (Visits) and count duration influence detected abundance and composition.
- Integration of the two CSV files to explore species-specific patterns in relation to site-level environmental descriptors.
- Data quality and harmonization considerations due to differing count durations and visit numbers across islands.

## Practical notes for use
- Data are organized to support ecological and biogeographic analyses of forest-dependent birds in Wallacea.
- Be mindful of scale effects: 250 m vs 1 km forest cover, and the differences in sampling effort across islands.
- The RCAR index relies on global range estimates and log transformations, which should be considered during interpretation and modeling.