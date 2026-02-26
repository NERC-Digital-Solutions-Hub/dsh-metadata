# Supporting documentation for Sample_list.csv

## Overview
- Documents the metadata fields and explanations used to describe samples in Sample_list.csv.
- Each field specifies the type of information captured (identifier, taxonomic attribution, description of analyzed material, collection date, sample mass relation, location, site-level associations, and comments).
- Indicates standard units and notes conventions for each field, with many notes left empty in this version.

## Field definitions

- Sample_Code
  - Explanation: Unique sample identifier.
  - Units: n/a
  - Notes: (empty)

- RAP
  - Explanation: International Commission on Radiological Protection (ICRP) Reference Animals and Plant (RAP) into which the sampled species can be attributed.
  - Units: n/a
  - Notes: (empty)

- Sample_Description
  - Explanation: Part of the organism analysed (e.g., whole organism vs. a specific part).
  - Units: n/a
  - Notes: (empty)

- Collection_Date
  - Explanation: Date of sample collection.
  - Units: dd-mmm-yy
  - Notes: (empty)

- Dry/Fresh_Ratio
  - Explanation: Dry to fresh weight ratio.
  - Units: unitless
  - Notes: (empty)

- Coordinates_of_the_Sample
  - Explanation: Grid reference of sampling location.
  - Units: decimal degrees and minutes
  - Notes: (empty)

- Sample_Association
  - Explanation: Unique sample identifier of soil sampled at the same site.
  - Units: n/a
  - Notes: (empty)

- Notes
  - Explanation: Additional comments (where applicable).
  - Units: n/a
  - Notes: (empty)

## Data quality and governance implications

- Metadata completeness: Several Notes fields are empty, highlighting opportunities to enrich context and provenance.
- Standardization: Explicit units and date formats are defined (e.g., dd-mmm-yy, decimal degrees), enabling consistent data integration.
- Data provenance: RAP field links samples to standardized radiological reference groups, aiding cross-study comparability.
- Data sharing considerations: Clear metadata structure supports reproducibility, though the absence of detailed Notes may impede interpretability without further documentation.

## Practical considerations for monitoring frameworks

- Define essential metadata fields for environmental monitoring datasets, ensuring consistent use of identifiers, attribution, temporal, spatial, and sample-context information.
- Ensure data quality processes capture and verify:
  - Unique Sample_Code generation and consistency across datasets.
  - Accurate RAP/classification alignment for taxonomic attribution.
  - Clear description of sample portions analyzed (Sample_Description).
  - Standardized collection date formats and proper handling of date time data.
  - Correct units and calculation methods for Dry/Fresh_Ratio.
  - Standardized geospatial references (Coordinates_of_the_Sample) and coordinate system.
  - Explicit linking of related samples at the same site (Sample_Association).
- Implement governance around Notes to capture study-specific context, methodology, or caveats that affect interpretation.

## Recommendations for improvement

- Populate Notes with dataset-specific qualifiers, limitations, or data provenance details.
- Consider adopting controlled vocabularies for RAP and Sample_Description to improve interoperability.
- Prefer ISO 8601 for dates and a single, canonical coordinate reference system to facilitate data sharing and GIS integration.
- Ensure positive metadata that documents data quality checks, derivative calculations (e.g., how Dry/Fresh_Ratio was determined), and any transformations applied.