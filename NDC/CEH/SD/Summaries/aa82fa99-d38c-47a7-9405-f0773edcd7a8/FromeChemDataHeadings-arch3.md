# Column header/Determinand

## Overview
- A dataset-style mapping of environmental water-quality determinands (measurements) with associated sampling details, units, and standardized identifiers.
- Aims to standardize data collection for monitoring, facilitating interoperability and policy evaluation.

## Key determinands and associated metadata
- Physical/flow and basic water properties:
  - Average daily river flow (units: m3/s; example unit annotation: hh:mm m3/s; includes a Units URI)
  - Temperature of water sample (units: deg C; URIs provided)
  - pH (no units; URIs provided)
  - Electrical conductivity (units: µS cm-1; multiple label/URI mappings)
  - Gran alkalinity (units: mEq L-1; URI provided)
- Nutrients and phosphorus species:
  - Dissolved nitrate (unit: mg NO3-N; µg L-1; URIs provided)
  - Dissolved reactive silicon (unit: mg Si L-1; µg L-1)
  - Total Phosphorus (unit: µg L-1)
  - Total dissolved phosphorus (unit: µg L-1)
  - Soluble reactive phosphorus (unit: µg L-1)
- Inorganic anions and cations:
  - Dissolved chloride, dissolved sulphate, dissolved sodium, dissolved potassium, dissolved magnesium, dissolved calcium (units: mg L-1; URIs provided)
  - Dissolved Na, K, Mg, Ca (various determinand labels with corresponding ontologies)
- Other water-quality indicators:
  - Suspended solids (unit references not shown in excerpt)
  - Dissolved ammonium (unit: mg NH4-N L-1; URIs provided)
- Data references and ontologies:
  - Determinand preferred labels and URIs (e.g., CAST URIs)
  - Units preferred labels and URIs
  - Some fields show “No units” or missing URIs, indicating partial standardization in those entries

## Data quality, metadata and governance implications
- The table demonstrates the use of formal ontologies (CAST) and URIs to standardize terminology and units.
- Highlights the importance of:
  - Consistent metadata (units, determinand labels, and URIs)
  - Public sharing of underlying data to support transparency
  - Data governance to ensure datasets are stored, shared, and kept up to date

## Relevance for monitoring-framework authors
- Provides a concrete example of a standardized set of determinants for river-water quality and associated metadata requirements.
- Illustrates common metadata gaps (missing units, missing URIs) that can hinder data integration and policy evaluation.
- Emphasizes the need to:
  - Verify and supplement metadata at the data origin
  - Promote data interoperability through consistent ontologies
  - Plan for data access, sharing, and governance when commissioning new measurements

## Practical takeaways for policy evaluation and decision-making
- Adopt a standardized determinant list with clear units and ontologies to enable comparable indicators across programs.
- Implement rigorous metadata practices and data governance early to avoid barriers to data reuse.
- Use standardized outputs (reports, dashboards) that reflect the same determinants and definitions for clear communication of environmental health findings.