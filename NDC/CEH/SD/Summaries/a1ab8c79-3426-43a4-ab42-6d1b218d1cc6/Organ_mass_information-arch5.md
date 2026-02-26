# Biota

## Overview
- A dataset schema for recording biota with basic identification and body mass measurements across multiple anatomical components.
- Key fields include English and Latin names, collection date, a unique ID, and body mass measurements in grams for several parts (whole body, gut, thyroid-related tissues, liver, kidney, and carcass).

## Key Fields and Definitions
- Biota
  - Explanation: English name of biota
  - Units: n/a
- Latin_name
  - Explanation: Latin name of species
  - Units: n/a
- Collection_Date
  - Explanation: Date sample was collected where known
  - Units: dd month yyyy
- ID
  - Explanation: Identifier in the data (where applicable)
  - Units: n/a
- Whole_body_g
  - Explanation: Mass of whole body
  - Units: grams
- Gut_g
  - Explanation: Mass of gut
  - Units: grams
- Tissue_with_thyroid_g
  - Explanation: Mass of sample containing the thyroid; the thyroid was too small to easily separate, so an area around it was analyzed as a whole
  - Units: grams
- Thyroid_g
  - Explanation: Mass of the actual thyroid (single gland)
  - Units: grams
- Liver_g
  - Explanation: Mass of liver
  - Units: grams
- Kidney_g
  - Explanation: Mass of kidney
  - Units: grams
- Carcass_g
  - Explanation: Mass of carcass
  - Units: grams

## Metadata and Standards
- Each field includes a clear Explanation and Units to ensure consistency across datasets.
- Emphasis on distinguishing related tissue masses (e.g., Tissue_with_thyroid_g vs Thyroid_g) to support precise recording and downstream analyses.
- Preference for standardized date formats and unique identifiers to aid discoverability and provenance.

## Data Quality, Transformation, and Sharing
- Data Stewards should:
  - Quality assure, clean, and potentially transform datasets before sharing.
  - Ensure that sharing limitations (embargoes, access constraints) are respected.
  - Upload datasets to relevant portals and catalogue data holdings.
  - Document data processing steps and any transformations performed.

## Data Governance and User Needs
- Work with data creators to ensure standards are met (accuracy, metadata, and format) and to capture relevant user needs (discoverability, usability).
- Maintain visibility into data availability and any limitations (e.g., disclosure risks, proprietary issues).

## Challenges for Data Stewards
- An incomplete picture of user needs and priorities.
- Timely acquisition of data from contributors.
- Getting data creators to meet standards, including metadata.
- Interoperability across many systems and formats, including difficult ones.
- Handling large datasets that are hard to transfer.
- Dealing with outdated databases requiring bespoke, non-interoperable solutions.