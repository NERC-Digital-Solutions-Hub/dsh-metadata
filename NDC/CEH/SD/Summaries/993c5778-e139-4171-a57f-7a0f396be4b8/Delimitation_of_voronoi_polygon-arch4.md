# DATA HEADER INFORMATION for Delimitation_of_voronoi_polygon.csv

## Overview
- Describes the target tree environment used for delimitation of a Voronoi polygon around trees.
- Supports the ESPA Programme (Project P4GES) with DOI 10.5285/993c5778-e139-4171-a57f-7a0f396be4b8.
- Acknowledgement is required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).
- Includes Zone of Interest (ZOI) types, measurement details, and derived geometric calculations (triangles) used in delimitation.

## Key fields and definitions
- ZOI, Information: Zone of Interest category (categorical). ZOI unit examples: ZOI2: Andasibe, ZOI3: Anjahamana.
- ZOI, Unit: Specific ZOI designation.
- Code, Information: Identifier for the target tree, built from site code + local name initial + size class (L/M/S). Type: Text String.
- N°, Information: Number of neighbouring trees as viewed in a clockwise direction. Type: Numeric; Unit: Unitless.
- Neighbour tree name, Information: Name of each neighbouring tree (relative to target). Type: Text String.
- Distance_from target_tree, Information: Distance from the target tree to each neighbouring tree. Type: Numeric; Unit: Meter.
- % (percentage), Information: Size influence of the neighbouring tree relative to the target, calculated as % = (DBH_T + DBH_N) / DBH_T × 100. Type: Numeric; Unit: Percentage.
- Distance of the picket, Information: Distance from the target tree to the location of a picket used in delimitation. Type: Numeric; Unit: Meter.
- Height neighbour tree, Information: Total height of the neighbouring tree (measured at 1.30 m DBH). Type: Numeric; Unit: Meter.
- N° Picket 1 / N° Picket 2, Information: Identifier numbers for first and second pickets. Type: Numeric.
- Distance between picket, Information: Distance between two neighbouring pickets. Type: Numeric; Unit: Meter.
- Height of each triangle, Information: Height of the triangle formed by the target tree and two neighbouring pickets. Type: Numeric.
- Base of each triangle, Information: Base length of each triangle. Type: Numeric; Unit: Meter.
- Area of each triangle, Information: Area of each triangle (m²). Type: Numeric.
- Forester compass fields: Indicate measurement methods used for certain fields (e.g., orientation).

## Provenance, usage rights, and references
- DOI and project references provided (ESPA, P4GES) to locate and cite data sources.
- Acknowledgement required for derived products, supporting governance and attribution.
- Documentation ties to Manual_2_Belowground_Root_Survey (section 2.3.1) for context and cross-referenced practices.

## Data quality, standards, and metadata notes
- Field-level metadata includes unit, variable type, and measurement context to support discoverability and reuse.
- Some fields explicitly specify units (meters, percentage, meters for areas in m², etc.), while others are text strings or categorical classifications.
- Includes computed metrics (e.g., percentage size relation, triangle areas) that depend on underlying measurements (e.g., DBH, heights), enabling downstream analyses and reproducibility.
- Forester compass and sampling references indicate methodological transparency for data collection.

## Implications for Data Leaders (data strategy, governance, and operations)
- End-to-end data lifecycle: clear provenance, citation requirements, and attribution for derived products, aligning with governance and accountability.
- Metadata richness supports data discovery, interoperability, and cross-partner collaboration in networked data environments.
- Structured field definitions and units reduce ambiguity, facilitating onboarding, data sharing, and scalable analytics across teams.
- Derived calculations (e.g., percentage, triangle metrics) should be captured in reproducible data pipelines with versioned code and documented assumptions.
- Cross-reference with related manuals and projects to ensure consistency in data collection practices and room for updates.
- Potential governance actions: ensure access controls align with project data rights, implement data quality checks for unit consistency and value ranges, and maintain an auditable lineage for any transformations.

## Recommendations for action
- Establish a centralized data dictionary incorporating these fields, units, and methods to support the wider data community and external partners.
- Create and enforce data quality rules (e.g., valid DBH-related calculations, reasonable distance scales, consistent use of forester compass methods).
- Implement a reproducible workflow for deriving triangle areas and related metrics from raw measurements, with version control.
- Ensure proper attribution and acknowledgement workflows are in place for any published or shared derivatives.
- Facilitate cross-site coordination by documenting ZOI definitions and standardizing naming conventions for target and neighbour trees.