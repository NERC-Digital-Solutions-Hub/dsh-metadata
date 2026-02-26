# DATA HEADER INFORMATION for Soil_DeltaC13_isotope_value.csv

## Overview
- The dataset records soil organic carbon content obtained with 13C isotope analysis.

## Variables and metadata
- ZOI (Zone of Interest): Categorical; Units indicate categories (ZOI1 Lakato, ZOI2 Andasibe, ZOI3 Anjahamana, ZOI4 Didy).
- Location: Name of the sampling point location; Text string.
- Site: P4GES site code; Text string.
- C%: Carbon content percent; Numeric; unit: %.
- delta13C: Delta 13C per-mille; Numeric; unit: ‰.
- Depth: Depth at which soil sampling was performed; Numeric; unit: cm.

## Context and references
- Related documentation: Manual_1_Classical_Survey.rtf (page 15, section 3.2).
- Project provenance: ESPA Programme; Project P4GES.
- Acknowledgement: Laboratoire des Radio Isotopes, Université d'Antananarivo required for products derived from these data.

## Data quality and accessibility considerations
- Blank cells mean data are not available.
- Data may span multiple sites and ZOIs; standardization across categories is important.
- Metadata supports traceability (site code, location, depth, etc.).

## Potential analyses and use cases
- Analyze relationships between C% and delta13C across different depths and ZOIs.
- Compare soil carbon content between Zone of Interest categories.
- Support data-driven mapping or modeling of soil carbon stocks with accompanying metadata.