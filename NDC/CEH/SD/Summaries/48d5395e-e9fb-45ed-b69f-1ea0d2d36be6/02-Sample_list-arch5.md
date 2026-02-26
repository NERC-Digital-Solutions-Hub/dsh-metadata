# Supporting documentation for 02-Sample_List.csv

## Overview
- Provides metadata schema for samples in 02-Sample_List.csv.
- Lists fields to capture: unique sample identifier, sample type, collection location, description, collection date, coordinates, analyses conducted, and notes.

## Key fields and metadata purpose
- Sample_Code
  - Unique sample identifier; ensures traceability and discoverability.
  - Units: n/a; Notes: n/a.
- Sample_Type
  - General description of the sample (e.g., foodstuff group).
  - Units: n/a; Notes: n/a.
- Location
  - Name of the location where the sample was collected; provides spatial context.
  - Units: n/a; Notes: n/a.
- Sample_Description
  - Further description of the sample (e.g., how organisms/foodstuffs were divided and analysed).
  - Units: n/a; Notes: n/a.
- Collection_Date
  - Date of sample collection.
  - Units: dd-mm-yyyy; Notes: n/a.
- Coordinates_of_the_Sample
  - Latitude and longitude of the sampling location.
  - Units: decimal degrees and minutes; Notes: n/a.
- Analysis
  - Analyses carried out (e.g., Gamma = gamma spectrometry; Stable = stable elements by ICP-MS).
  - Units: n/a; Notes: n/a.
- Notes
  - Additional comments, where applicable.
  - Units: n/a; Notes: n/a.

## Data governance and quality considerations for Data Stewards
- Ensure Sample_Code is unique and enforceable as a key identifier.
- Use consistent, defined values for Sample_Type and Analysis to support interoperability.
- Validate Collection_Date format (dd-mm-yyyy) and ensure consistency across records.
- Store Coordinates_of_the_Sample in a standard geospatial format; consider normalization to decimal degrees for mapping.
- Maintain clear provenance by documenting who collected/analysed samples and when; track updates or new analyses.
- Ensure metadata completeness and consistency to improve discoverability in portals and catalogues.
- Be mindful of potential data sharing limitations or embargoes; capture in metadata where relevant (via Notes or governance fields).

## Practical challenges and alignment with aims
- The structure supports discoverability and reuse by recording essential metadata for each sample.
- To meet the Data Steward aim, enforce data standards, metadata accuracy, and timely updates across systems and formats.
- Anticipated challenges (e.g., incomplete user needs, data from multiple legacy systems, large datasets) should be mitigated through data dictionaries, validation rules, and governance processes.

## Recommendations for Data Stewards
- Develop and maintain a data dictionary mapping each field to its definition, allowed values, and formats.
- Implement validation checks to ensure required fields are populated and dates/coordinates follow the specified formats.
- Align with data portals/catalogues by ensuring metadata is published alongside the dataset and kept up to date.
- Document dataset work steps (sampling, division, analyses) to support reproducibility and future updates.
- Plan for handling updates, embargoes, and provenance as part of ongoing data governance.