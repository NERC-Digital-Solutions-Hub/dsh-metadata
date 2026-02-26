# Declining glacier cover drives changes in the biodiversity of aquatic macroinvertebrates in the Cordillera Blanca, Peru.

## Overview
- A dataset of taxonomic and abundance data for benthic macroinvertebrates from 10 rivers in the glacial valleys of Parón, Huaytapallana, and Llanganuco in the Cordillera Blanca, Ancash, Peru.
- Connected to the article investigating how aquatic biodiversity responds to glacial retreat.
- Data files: Macro_CBPeru_Wet.csv (wet season) and Macro_CBPeru_Dry.csv (dry season).

## Study Area and Sampling Design
- Study area features rivers whose waters originate on the western flank of glaciers Huandoy and Huascarán.
- Sampling dates: October 2019 and October 2020.
- At each site: a defined 15-meter reach with six subsamples (five subsamples at P01 during the dry season due to weather).
- Subsampling method: 250 μm mesh net; six subsamples composited per site.
- Field preservation: substrate stored in airtight bags with 96% ethanol.
- Laboratory processing: samples washed through a 250 μm sieve; macroinvertebrates identified to lowest possible taxonomic level; genus-level for Trichoptera, Ephemeroptera, Plecoptera; Chironomidae subfamilies identified; counts include larvae, nymphs, and pupae; Coleoptera counts include adults.
- Site codes: P01–P10; Table 1 provides geographic context and glacier cover metrics.

## Data and Taxa
- Abundance data are organized with sites in the first column and taxa in the first row.
- 41 taxa identified in total; 38 taxa in the dry season and 39 taxa in the wet season.
- Taxon descriptions include genus-level identifications where possible (italics in the original table indicate genus-level identifications).
- The dataset includes a mapping of site, family/subfamily, and order for each recorded taxon (see Table 2 in the dataset).

## Geographic and Environmental Metadata
- Site-level geographic details include:
  - Coordinates (UTM 18S) for each site (P01–P10)
  - Valley name, basin area (km²), glacier area (km²), glacier cover (% GCC)
  - Distance from glacier (km), slope (%), altitude (m above sea level)
- Glacier cover (GCC) values range across sites, with a notable 0.00% GCC at P08 (and some missing distance data for that site).
- The data describe streams sourced from the western slopes of Huandoy and Huascarán glaciers.

## Quality Control and Provenance
- Consistent field collection: the same person collected substrate at all sites.
- Processing completed within 48 hours of collection.
- Taxonomic identifications corroborated by a professional expert; counts verified by two professionals.
- Documented contributor roles: sampling, laboratory analysis, supporting information, and planning/management.

## Data Structure and Access
- Two CSV files reflect seasonal abundances: Macro_CBPeru_Wet.csv and Macro_CBPeru_Dry.csv.
- Structure: rows represent sites; columns represent taxa; a separate column (RN) indicates replicate number (1–6). P01 in the dry season has 5 subsamples.
- Taxonomic scope includes 41 taxa overall, with a detailed taxonomy mapping (family/subfamily and order) provided for each taxon.
- Taxonomic references used for identification include:
  - Domínguez & Fernández (2009) for benthic South American macroinvertebrates
  - Prat et al. (2011) for Chironomidae larval morphotypes in high Andean rivers

## Potential Uses and Considerations for Analysts
- Use the GCC gradient and seasonal data to model how glacier retreat influences macroinvertebrate biodiversity and community composition.
- Potential analyses: correlations between taxon richness/abundance and GCC, beta diversity across sites, seasonal differences in assemblages, and trait- or lineage-specific responses.
- Consider data limitations:
  - Some sites have missing GCC or distance data (e.g., P08).
  - Taxa identifications vary in resolution (some only to genus or subfamily level).
  - Slight replication differences (P01 has fewer subsamples in dry season).
  - Spatial scale and local site conditions may affect generalisability beyond the study area.