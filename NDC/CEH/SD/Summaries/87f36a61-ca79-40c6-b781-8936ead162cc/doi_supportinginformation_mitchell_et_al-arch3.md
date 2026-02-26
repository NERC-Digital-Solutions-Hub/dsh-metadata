# Bird detection data for Seram, Buru, Buton and Sulawesi, Indonesia [NERC Wallacea Project NE/S007067/1] (2021) Mitchell, S.L., Edwards, D.P., Martin, R.W., Deere, N.J., Voigt, M., Kastanya, A., Karja, A., Akbar, P.G., Jordan, K., Tasirin, J., Zakaria, Z., Martin, T., Supriatna, J., Winarni, N., Davies, Z.G., Struebig, M.J.

## Overview of the dataset
- Contains matrices detailing abundance of 426 bird species across 1350 sites on islands including Borneo (Sabah), Sulawesi (Buton), Seram, Buru, Sangihe, and Talaud.
- Aggregated counts from four visits for Borneo (Sabah), Sulawesi (Buton), Seram, and Buru; raw abundances from single counts on Talaud and Sangihe.
- Primary files:
  - Mitchell_Wallacea_site_community_data.csv: species abundance data per site.
  - Mitchell_Wallacea_site_metadata.csv: site-level metadata and auxiliary variables.

## Experimental design, sampling regime and data collection
- Surveys conducted between 2014 and 2020.
- Point counts:
  - Borneo: 15-minute counts with unlimited radius.
  - Sulawesi (Buton), Seram, Buru: 10-minute counts.
  - Talaud and Sangihe: 20-minute counts.
- Community inventories: four visits per site on Borneo, Sulawesi, Seram, and Buru; single visit on Talaud and Sangihe.
- Observers across islands included SLM, PGA, AK, KJ, RWM.

## Data processing and metadata
- Site coordinates recorded via GPS in Mitchell_Wallacea_site_metadata.csv.
- Forest cover estimated around each point from 2018 Global Forest Change data (Hansen et al., 2013) at radii of 250 m and 1 km.
- Biodiversity indices:
  - Relative Average Range (RAR): average species range size across all species observed in the community.
  - Relative Community Average Range (RCAR): community-weighted mean of individual species ranges, using log-transformed global range sizes per Newbold et al. (2018).
  - Species range data sourced from BirdLife International (BirdLife, 2020), combining expert opinion and GBIF-derived records.
- Community-level calculations use relatively standardized approaches to enable cross-site comparisons.

## Key variables and column structure
- Mitchell_Wallacea_site_community_data.csv:
  - Site: unique site identifier; prefixes denote landscape or transect (Sangihe/Talaud islands use island as prefix).
  - Species columns: names of the 426 observed bird species (in English).
- Mitchell_Wallacea_site_metadata.csv:
  - Site: site identifier matching the community_data file.
  - Latitude, Longitude: geographic coordinates (decimal degrees).
  - RAR: average species range size for the community.
  - RCAR: average individual range size across all individuals observed.
  - Prop forest 250m: proportion of forest cover within 250 m of the site.
  - Prop forest 1000m: proportion of forest cover within 1 km of the site.
  - Island: island where the site is located.
  - Visits: number of visits that contributed to aggregated abundance estimates.

## Potential uses for monitoring frameworks and policy decisions
- Benchmark biodiversity status across multiple islands and habitats, enabling spatial monitoring of avian community structure.
- Track changes over time by leveraging multi-visit sites (where available) and comparing aggregated abundances, RAR, and RCAR indices.
- Assess relationships between habitat quality (forest cover at 250 m and 1 km) and bird community metrics to inform habitat protection and restoration priorities.
- Support cross-site comparability and integration with other environmental health indicators in governance dashboards, reports, and policy reviews.

## Data governance, sharing and limitations
- Emphasizes openness and sharing of underlying data, which may pose barriers in some contexts.
- Metadata completeness and interoperability (e.g., standard units, clear site identifiers) are crucial for reuse.
- Variability in survey duration and number of visits across islands may affect cross-site comparability; Talaud and Sangihe have single counts, while others have four visits.
- Transformation and processing steps (e.g., RAR/RCAR calculations, forest-cover extraction) require careful documentation to ensure reproducibility.
- Encourages dissemination to stakeholders and implementation of data governance processes to maintain data quality and up-to-date datasets.