# Supporting documentation for Biota_Stable_Element.csv

## Overview
- Defines the metadata and field descriptions for the Biota_Stable_Element.csv dataset.
- Documents sample context, measurement fields, units, and handling notes to support data interpretation and reuse.
- Indicates sample scope includes RAP-based sample types and replicate soil samples, enabling cross-sample comparisons and whole-organism concentration estimation.
- Key units are concentration on a fresh mass basis (mg/kg_fw); certain descriptive fields use complementary units (e.g., Sample_Description in cm).
- Collection dates are formatted as dd-mmm-yyyy; a Notes field captures analysis details and usage in estimation.

## Data Fields and Structure
- Core identifiers and context
  - Sample_Code: Unique sample identifier.
  - RAP: Sample type based on ICRP Reference Animals and Plants (RAPs).
  - Sample_Description: Further explanation of the sample (units in cm for this field).
  - Collection_Date: Date of soil sample collection (dd-mmm-yyyy).
  - Notes: Note on analyses or how samples were used in estimating whole-organism concentration.

- Element concentration fields (primary measurements)
  - For each element (I-127, Li, Be, B, Na, Mg, Al, P, S, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U)
    - [Element]_mg_kg_fw: Concentration on a fresh mass basis (mg/kg_fw).

- Detection limits (metadata accompanying measurements)
  - For many elements, a corresponding Detection_Limit_[Element]_mg_kg_fw field exists.
  - Detection_Limit_[Element]_mg_kg_fw: Detection limit of the element on a fresh mass basis for the given sample (mg/kg_fw).
  - Notes within these descriptions indicate interpretation, e.g., if blank in the concentration field then the concentration was below the detection limit, or if the concentration was detectable.

- Replicates and special sample notes
  - RCN119, RCN120, RCN121 are indicated as replicate soil samples.
  - Notes sections provide guidance on analyses or estimations of whole-organism concentration.

## Measurement, Units and Detection Limits
- Concentration measurements are provided for a broad suite of elements, each on a fresh mass basis with units of mg/kg_fw.
- Detection limits are explicitly captured per sample for many elements, enabling assessment of data quality and the ability to distinguish between non-detects and low concentrations.
- The documentation describes how to interpret blanks in concentration fields and references detection-limit indicators within the detection-limit fields.

## Sample Context and Replication
- RAP-based classification ties samples to ICRP RAP categories, enabling cross-species and cross-context comparisons.
- Replicate soil samples (RCN119, 120, 121) are noted, indicating emphasis on replication for quality assessment and uncertainty estimation.
- Sample_Description may include measurements in centimeters, suggesting related physical description of the sample vicinity or depth.

## Metadata, Notes and Usage
- Notes provide essential context on analyses and how samples were used to estimate whole-organism concentrations.
- The presence of detailed metadata (RAP, replicate indicators, detection limits, and collection dates) supports traceability, reproducibility, and informed data governance.
- The structure is designed to support data discovery, filtering by sample type, date, or detectable concentration, and careful interpretation where detection limits apply.

## Governance and Data Leadership Considerations
- Data richness: Extensive metadata and per-sample detection-limit information enhance data quality assessment and reliable downstream usage (e.g., regulatory reporting, risk assessment, cross-study integration).
- Discoverability and reuse: Clear field definitions, units, and sample context (RAPs, replicates) improve interoperability and ease of integration with other datasets.
- Quality and standards: The dataset combines many elements with corresponding detection limits, facilitating transparent handling of non-detects but requiring consistent interpretation rules across samples.
- Data stewardship implications: Ensure ongoing updates to detection limits and sample metadata are maintained; monitor consistency of units and naming conventions to preserve longitudinal comparability. Consider implementing a data dictionary or schema mapping to support cross-dataset harmonization.