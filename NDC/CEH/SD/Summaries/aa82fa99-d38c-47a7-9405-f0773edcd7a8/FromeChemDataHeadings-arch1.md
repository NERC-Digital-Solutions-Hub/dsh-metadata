# Column header/Determinand

## Overview
- Defines a river water quality dataset structure with a column header set starting with Determinand, followed by sampling and measurement fields.
- For each determinand and unit, the document provides preferred labels and ontology URIs (primarily CAST), supporting semantic interoperability and data discovery.
- Data fields cover sampling metadata (date, time) and a wide range of physico-chemical measurements.

## Key fields and measurements
- Sampling metadata: Sampling Date, Sampling Time
- Hydrology: Average daily river flow (units m3/s or cumecs)
- Physical/chemical properties:
  - Temperature of water sample (deg C)
  - pH (no units)
  - Electrical conductivity (µS cm-1; units labeled as uS/cm @25C)
  - Gran alkalinity (mEq/L)
  - Dissolved nitrate
  - Dissolved reactive silicon
  - Total Phosphorus (Total dissolved phosphorus; units µg/L)
  - Soluble reactive phosphorus
  - Dissolved chloride (Cl)
  - Dissolved sulphate (SO4)
  - Dissolved sodium (Na)
  - Dissolved potassium (K)
  - Dissolved magnesium (Mg)
  - Dissolved calcium (Ca)
  - Suspended solids
  - Dissolved ammonium (NH4)
- For each determinand, the document lists corresponding determinate labels and URIs as well as units labels and URIs (where applicable).

## Data standards and metadata
- Utilizes CAST ontology URIs for both determinands and units (e.g., http://onto.nerc.ac.uk/CAST/xxx).
- Includes explicit unit mappings (e.g., m3/s, deg C, µS cm-1, mEq L-1, mg/L, µg/L) and their human-friendly labels.
- Some entries show "No units" or missing labels/URIs, indicating metadata gaps.

## Data quality and interoperability considerations
- Ontology-backed metadata facilitates data linking, reuse, and reproducibility.
- Metadata gaps (missing determinand labels or unit information) may require manual clarification during data preparation.
- The structure supports harmonisation across datasets by aligning measurements to standard units and CAST URIs.

## Analysts' opportunities and practical use
- Capabilities:
  - Identify correlations between hydrology (flow) and nutrient/ion concentrations.
  - Compare total versus dissolved phosphorus forms and their associations with flow, alkalinity, and conductivity.
  - Develop predictive models of nutrient loading from river flow and water properties.
- Practical considerations:
  - Ensure consistency of units across records, especially where multiple unit representations appear.
  - Map any missing or ambiguous metadata to the CAST URIs or provide clarifications before modelling.
  - Be mindful of potential local-scale limitations and the need to integrate with other data sources for broader analyses.

## Conclusion
- The document presents a comprehensive, ontology-driven schema for river water quality measurements, enabling robust data discovery, interoperability, and analytical modelling. While generally well-structured, some metadata gaps (missing labels/units) should be addressed to maximize analytical reliability.