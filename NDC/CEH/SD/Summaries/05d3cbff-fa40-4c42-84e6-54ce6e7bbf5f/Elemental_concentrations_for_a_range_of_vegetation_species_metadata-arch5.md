# Elemental meta-data

## Overview
- Dataset describes elemental concentrations in plant and soil samples collected by CEH centralised chemistry laboratory.
- Includes identifiers for samples and collection sites, sampling dates, and taxonomic information for plant samples.
- Captures a wide range of elemental measurements with method and unit details, plus non-detect and missing data indicators.

## Data schema and key fields
- Identification and collection
  - Laboratory_ID: CEH centralised chemistry laboratory unique sample identifier.
  - Sample_ID: CEH Radiochemistry laboratory unique sample identifier.
  - Collection_Site: Sampling site.
  - Sampling_date: Date of sampling (format dd/mm/yyyy).
- Biological and site context
  - Species: Latin name of the plant species (n/a if soil sample).
  - Common_name: Common name of the plant species (n/a if no common name or soil sample).
  - Order, Family, Genus: Taxonomic classifications (n/a if soil sample).
- Sample type and status
  - Notes imply plant vs soil context and that some tests reference dry weight vs fresh weight; not all fields are applicable to every sample type.
- Measurements and metadata for elements
  - A large set of elemental concentration fields, including but not limited to Li, Be, Na, Mg, Al, Si, P, S, K, Ca, Ti, Cr, Mn, Fe, Co, Ni, Cu, Zn, Se, Rb, Sr, Y, Zr, Nb, Mo, Cd, Sn, Sb, Cs, Ba, La, Ce, Pr, Nd, Sm, Eu, Gd, Tb, Dy, Ho, Er, Tm, Yb, Lu, W, Hg, Tl, Pb, Th, U.
  - For each element, multiple variants exist:
    - Measured by ICPMS (quantitative or semi-quantitative) or ICPOES (quantitative).
    - Units typically mg per kg (dry weight) or mg per kg (fresh weight) depending on column.
    - Some columns indicate semi-quantitative vs quantitative measurements.
  - Detection and data presence indicators
    - Columns ending with “_<” indicate concentrations below the limit of detection (LOD).
    - Some columns include “n/a - data not available” to denote missing data.
  - Data organization hints
    - Many elements have two-part entries (e.g., “element_mg_kg_quantitative_mg_kg_d ry” and related variants), reflecting different measurement contexts (dry weight vs other conditions) or replicate notes (e.g., 1/2 suffixes).
- Data quality notes
  - Some fields explicitly note non-applicable or not available data.
  - The dataset distinguishes between detected concentrations and non-detect signals, often requiring careful interpretation of LOD flags.

## Data quality, provenance, and governance
- Provenance
  - Originates from a centralized laboratory (CEH) with structured identifiers for samples and sites, enabling traceability.
- Metadata completeness
  - Critical fields include sample identifiers, collection site, sampling date, and species/taxonomy context for plant samples.
  - Comprehensive recording of measurement method (ICPMS, ICPOES) and weight basis (dry weight vs fresh weight) is essential for reuse and comparability.
- Data quality considerations
  - Handling non-detect (<LOD) values consistently across many elements.
  - Managing missing data (n/a) and ensuring clear documentation of why data are missing.
  - Ensuring unit harmonization (mg/kg dry weight vs mg/kg fresh weight) for cross-study interoperability.
- Sharing readiness
  - The dataset aligns with the Data Steward aim to ensure datasets are discoverable, well-governed, and usable by others, with explicit metadata about methods, units, and data quality flags.

## Governance and sharing considerations for Data Stewards
- Standardization
  - Enforce consistent naming, units, and weight basis across all elemental columns.
  - Maintain explicit LOD indicators for non-detects and ensure consistent interpretation rules.
- Metadata completeness
  - Verify presence of Laboratory_ID, Sample_ID, Collection_Site, Sampling_date, Species/Common_name, and taxonomy fields where applicable.
  - Document measurement methods and units for each element to avoid ambiguity.
- Data quality processes
  - Implement validation to catch mismatches between weight basis and reported units.
  - Capture and communicate reasons for missing data (n/a) and how non-detects are encoded.
- Documentation and lineage
  - Document data transformations, QA steps, and any harmonization performed prior to sharing.
  - Provide a data dictionary or data catalog entry mapping each column to its meaning, method, and unit.
- Interoperability and reuse
  - Consider mapping elements to standard chemical ontologies or domain vocabularies where possible.
  - Ensure clear guidance on how to interpret semi-quantitative vs quantitative measurements for downstream analyses.

## Practical guidance for Data Stewards
- Before sharing:
  - Confirm all essential fields are present and correctly formatted (IDs, site, date, species, taxonomy).
  - Validate measurement method and weight basis for all element columns; standardize to a consistent unit where feasible.
  - Ensure non-detects are consistently flagged and documented with corresponding LOD handling rules.
- During curation:
  - Clean obvious inconsistencies (e.g., mismatched units, future-dated samples).
  - Retain original column semantics while providing a harmonized view for end users.
  - Document any data exclusions or imputations.
- In the catalog:
  - Include a data dictionary entry that lists each element column, its measurement method, units, and note about LOD flags.
  - Provide provenance notes about the CEH laboratory and sampling context to aid discoverability and trust.