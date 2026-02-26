# TREE_Northumbria_ICPMS_Deer_FM_concentration

## Overview
- Dataset of ICP-MS element concentrations in deer tissues from Northumbria (UK), intended for environmental monitoring and data discovery.
- Captures sample metadata (species names, site, date, UKCEH sample codes/descriptions) and tissue type, plus a Fresh Mass to Dry Mass ratio.
- Contains concentrations for a wide suite of elements (I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U) in mg/kg fresh mass.
- Some values are censored with “<” markers; some samples have missing data (e.g., Roe deer 4 thyroid).

## Dataset structure and fields
- Species identifiers:
  - Latin_Species_Name (explanation: Latin name)
  - Common_Species_Name (explanation: common name)
- Sampling and identifiers:
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes (UKCEH codes)
  - CEH_Sample_Description
- Biological sample details:
  - Tissue
  - Fresh_Mass_Dry_Mass_Ratio
- Concentration data (mg/kg_FM) for: I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U
- Data qualifiers:
  - Some entries marked with less-than signs indicating censored values
  - Notes such as “No data for Roe deer 4 thyroid” indicate sample-specific gaps

## Metadata and data quality considerations
- Units are predominantly mg/kg fresh mass (FM) for metal concentrations; ensure consistent unit interpretation during use.
- Explanations accompany many fields, but the header contains formatting inconsistencies (e.g., “<Be” and repeated “Units = n/a”/explanation segments) that may require cleaning for ingestion into a data catalog.
- Presence of censored values (“<” markers) requires appropriate treatment in analyses (e.g., interval censoring or imputation strategy).
- Several samples lack data for specific tissues or analytes (noted as “No data for Roe deer 4 thyroid”), affecting completeness and comparability across rows.
- Metadata supports linking to UKCEH sample codes and descriptions, aiding traceability and reuse.

## Data governance, sharing and updates
- Data likely intended for upload to portals and catalogues; ensure alignment with repository schemas and controlled vocabularies.
- Governance notes:
  - Maintain data provenance: sample collection metadata, processing (QA/QC), and any transformations.
  - Document handling of censored values and missing data in data dictionaries and pipelines.
  - Respect sharing limitations and any embargoes; capture versioning and change history for updates.
- Operational steps for Data Stewards:
  - Standardize species naming to a controlled vocab and verify alignment with taxonomic references.
  - Validate and harmonize field names, units, and explanations to remove header inconsistencies.
  - Implement data quality checks for censored values and missing records; flag and resolve ambiguities with data creators.

## Challenges and recommendations for Data Stewards
- Incomplete user needs and data acquisition timing:
  - Proactively engage with data creators to secure complete metadata and resolve gaps (e.g., Roe deer thyroid data).
- Heterogeneous systems/formats:
  - Map to a common data model and enforce consistent field naming, units, and typographic conventions.
- Large, complex datasets:
  - Consider modular ingestion (per tissue or per element group) and maintain linkage to sample metadata.
- Outdated or bespoke data frameworks:
  - Prioritize interoperability by adopting open standards for metadata (e.g., clearly specified units, data types, and qualifiers) and documenting any bespoke aspects.