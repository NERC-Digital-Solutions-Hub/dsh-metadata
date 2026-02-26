# Supporting documentation for 02-Sample_List.csv

## Overview
- A data dictionary describing the schema for the 02-Sample_List.csv, detailing each field with explanations, units, and notes to support consistent data collection and interpretation.

## Key fields and descriptions
- Sample_Code: Unique sample identifier; Units: n/a; Notes: n/a.
- Sample_Type: General description of sample (e.g., foodstuff group); Units: n/a; Notes: n/a.
- Location: Name of the location where the sample was collected; Units: n/a; Notes: n/a.
- Sample_Description: Further description of the sample (e.g., when organism/foodstuff was divided and analysed separately); Units: n/a; Notes: n/a.
- Collection_Date: Date of sample collection; Units: dd-mm-yyyy; Notes: n/a.
- Coordinates_of_the_Sample: Latitude and longitude of sampling location; Units: decimal degrees and minutes; Notes: n/a.
- Analysis: Analyses carried out (Gamma = gamma spectrometry; Stable = stable elements by ICP-MS); Units: n/a; Notes: n/a.
- Notes: Additional comments (where applicable); Units: n/a; Notes: n/a.

## Metadata and data quality
- Each field includes Explanation, with explicit Units and Notes to guide usage.
- Date and coordinate formats are standardized (dd-mm-yyyy and decimal degrees/minutes), aiding validation and interoperability.
- The dataset emphasizes clear documentation of analytical methods (Gamma spectrometry; ICP-MS for stable elements) to support interpretation and reproducibility.

## Governance, discoverability, and reuse
- Clearly defined fields and descriptions support data discoverability and reuse by analysts, policymakers, and cross-team collaborators.
- Metadata facilitates verification of content and format, aiding data quality checks and auditing.

## Relevance to Data Leaders
- Demonstrates how a well-documented data asset is organized, enabling effective data strategy, ownership, and cross-network collaboration.
- Illustrates the importance of metadata completeness (explanations, units, notes) to reduce ambiguity and support user needs.

## Practical recommendations for data leaders
- Ensure complete and consistent metadata across all fields (even when Units are not applicable).
- Enforce standardized date and coordinate formats and validate entries during data entry.
- Consider expanding controlled vocabularies for Sample_Type and Analysis to improve consistency and searchability.
- Document data lineage and ownership for the 02-Sample_List.csv to improve governance and future use.