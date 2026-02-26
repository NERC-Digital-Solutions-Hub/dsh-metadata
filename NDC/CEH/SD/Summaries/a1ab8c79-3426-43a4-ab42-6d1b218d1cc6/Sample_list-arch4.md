# Supporting documentation for Sample_list.csv

## Overview
- Defines the metadata fields for the Sample_list.csv dataset.
- Each sample row includes identifiers, attribution, description, collection details, physical measurements, location, site associations, and additional comments.
- Emphasizes structured metadata to support discovery, interoperability, and data governance.

## Key fields and purpose
- Sample_Code: Unique sample identifier. Units: n/a. Notes: (empty).
- RAP: ICRP Reference Animals and Plant (RAP) attribution for the sampled species. Units: n/a. Notes: (empty).
- Sample_Description: Part of the organism analysed (e.g., which body/organ portion). Units: n/a. Notes: (empty).
- Collection_Date: Date of sample collection. Units: dd-mmm-yy. Notes: (empty).
- Dry/Fresh_Ratio: Dry to fresh weight ratio. Units: unitless. Notes: (empty).
- Coordinates_of_the_Sample: Grid reference of sampling location. Units: decimal degrees and minutes. Notes: (empty).
- Sample_Association: Unique sample identifier of soil sampled at the same site. Units: n/a. Notes: (empty).
- Notes: Additional comments (where applicable). Units: n/a. Notes: (empty).

## Metadata, standards, and discoverability implications
- RAP field links samples to standardized organism/taxa attribution (ICRP RAP), enabling cross-study comparisons.
- Collection_Date uses a clear date format to support temporal analyses and versioning.
- Coordinates_of_the_Sample provides geospatial context in a defined format (decimal degrees and minutes) for mapping and spatial analyses.
- Sample_Description clarifies which portion of the organism was analysed, aiding reproducibility and data interpretation.
- Sample_Association enables grouping of related samples from the same site (facilitating site-level analyses and data integrity).
- Explicit Units and Explanation per field support data quality, validation, and interoperability across systems.

## Practical considerations for Data Leaders
- Ensure RAP attributions are consistently applied to avoid taxonomy mismatches.
- Enforce date and coordinate formats across the data pipeline to maintain consistency.
- Maintain robust metadata for each field (Explanation, Units, Notes) to support discoverability and user understanding.
- Leverage Sample_Association to manage related samples and prevent duplication of effort.
- Use the Notes field to capture any data provenance or contextual information that could affect analysis or interpretation.