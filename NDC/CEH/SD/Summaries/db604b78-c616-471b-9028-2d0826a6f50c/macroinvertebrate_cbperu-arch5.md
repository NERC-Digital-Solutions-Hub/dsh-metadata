# Macroinvertebrate community data:

## Overview
- Dataset of taxonomic and abundance data for benthic macroinvertebrates from 10 rivers in glacial valleys of the Cordillera Blanca, Ancash, Peru.
- Collected to analyze biodiversity responses to glacial retreat; data linked to the article "Declining glacier cover drives changes in the biodiversity of aquatic macroinvertebrates in the Cordillera Blanca, Peru."
- Seasonal data available in two separate files: Wet (Macro_CBPeru_Wet.csv) and Dry (Macro_CBPeru_Dry.csv).

## Data Content and Structure
- Files and scope:
  - Macro_CBPeru_Wet.csv (wet season)
  - Macro_CBPeru_Dry.csv (dry season)
- Data arrangement:
  - Rows represent sampling sites; columns represent taxa (41 taxa identified overall; 38 taxa in dry season, 39 taxa in wet season).
  - First column = Site; first row = Taxon descriptions.
  - Second column contains the replication number (RN) indicating 6 subsamples per river (1–6). P01 in the dry season has only 5 subsamples due to conditions.
- Taxonomic detail:
  - Abundance counts for macroinvertebrates; identifications mainly to genus level for many taxa (e.g., Trichoptera, Ephemeroptera, Plecoptera). Some Chironomidae identifications are at subfamily level or morphotype-based.
  - A 41-item taxonomy map (Sp1–Sp41) includes families/subfamilies, orders, and genus-level descriptions in the accompanying table.
- Temporal coverage:
  - Sampling seasons: October 2019 (dry season) and October 2020 (wet season).

## Sampling and Methods
- Study sites and rivers:
  - 10 rivers in Parón, Huaytapallana, and Llanganuco basins.
- Field method:
  - Substrate sampling with a Surber net (250 μm mesh) over a defined 15-meter section.
  - At each site, 6 subsamples collected from riffle, pool, and bank habitats; composite sample prepared from 5 subsamples per site.
  - Samples preserved in 96% ethanol in the field.
- Laboratory processing:
  - In the lab, samples washed through a 250 μm sieve; macroinvertebrates sorted and identified to the lowest possible taxonomic level (genus-level for many groups).
  - Taxonomic references used: Domínguez & Fernández (2009) and Prat et al. (2011) for Chironomidae larval morphotypes.
  - Counts include larvae, nymphs, and pupae; adult stages included for Coleoptera.

## Geographic and Site Metadata
- Site coding:
  - Sites labeled P01–P10, representing enumeration of the 10 glacial rivers studied.
- Geographic attributes captured (per site):
  - Coordinates (UTM 18S)
  - Valley name, basin area (km²), glacier area (km²), glacier coverage (GCC %)
  - Distance from glacier (km), slope (%), altitude (m above sea level)
- Notable data notes:
  - GCC varies across sites (e.g., P08 GCC = 0.00% with missing distance from glacier), and some entries show negative or incomplete values (e.g., P08 distance from glacier listed as "-").
  - P09 and P10 field entries appear misformatted in the provided table, indicating potential data quality review needs.

## Data Quality and Provenance
- Quality control:
  - The same person collected substrate samples at all sites.
  - Processing completed within 48 hours of collection.
  - Taxonomic identifications corroborated by a professional expert.
  - Separation and counting performed for the entire site sample; records independently verified by two professionals.
- Versioning and authorship:
  - Version 1.0; description indicates dataset creation by Palacios, E. (author) with contributions from Medina, K.; Loarte, E.; Gamboa, M.; Brown, L.; Pellicciotti, F.; Castañeda, A.; Polo, R.; Tapia, P.
  - Related to macroinvertebrate biodiversity study in the Cordillera Blanca.

## Data Governance, Access, and Documentation
- Data format and structure are explicitly documented (two CSV files with site-by-taxa layout and replication dimension).
- Metadata and taxon mapping provided (Table 2) to interpret species/taxon codes and descriptions.
- References for taxonomic identification guidance are provided (Domínguez & Fernández, 2009; Prat et al., 2011).

## Contributors and Roles
- Sample collection: Palacios, E.; Medina, K.; Loarte, E.
- Laboratory analysis: Palacios, E.; Gamboa, M.; Brown, L.
- Supporting information: Castañeda, A.; Polo, R.; Tapia, P.
- Planning and management: Medina, K.; Loarte, E.; Brown, L.; Pellicciotti, F.

## Limitations and Considerations for Data Stewards
- Seasonal and site data gaps:
  - Dry season vs. wet season data presence; some taxa counts differ between seasons (38 vs. 39 taxa).
- Data integrity considerations:
  - Some site data entries (P09, P10) appear misformatted; require data cleaning and validation before integration.
  - Geographic variables for certain sites show zero or missing GCC values and inconsistent distance measurements.
- Taxonomic resolution:
  - Genus-level identifications are not uniform across all taxa; some groups resolved only to subfamily or morphotype level, which may affect cross-study comparability.
- Use and reuse:
  - Data are tied to a specific publication; appropriate citation to the referenced article and taxonomic guides is recommended.
  - Ensure consistent handling of replication numbers when aggregating or comparing site-level abundances across seasons.