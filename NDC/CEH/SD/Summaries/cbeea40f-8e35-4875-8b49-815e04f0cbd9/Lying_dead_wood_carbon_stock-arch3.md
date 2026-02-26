# DATA HEADER information for Lying_dead_wood_carbon_stock.csv

## Overview
- Dataset describes biomass stock in the lying dead wood pool, based on fallen trees sampled along transects per plot.
- Part of ESPA P4GES programme; DOI provided for dataset.
- Acknowledgement required to Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.

## Data structure and variables
- Site_ID: P4GES site code; Type = Text String.
- Category: Wood density classification; Type = Categorical; Values: S (sound), I (intermediate), R (Rotten).
- Density: Numeric; Density values corresponding to wood category; 0 indicates absence of dead wood; Unitless.
- Diameter: Numeric; Diameter of dead wood trunk in the transect crossing area; Unit = Centimeter (cm).
- Volume: Numeric; Estimated volume of lying dead wood; Based on Winrock International 2005; Unit = cubic metres (m3).
- Biomass: Numeric; Biomass stock of lying dead wood; Unit = Mg ha-1 (noted as milligrams per hectare in header, likely Mg ha-1).
- Stock_C: Numeric; Carbon stock of lying dead wood; Unit = Mg ha-1.
- Data recording notes: Some fields may be blank; “Notes” indicate that blank entries mean no data.

## Data provenance and references
- Data source: Field measurements of lying dead wood biomass and carbon stock.
- Volume calculation method: Winrock International 2005 (Logging carbon study reference in Congo).
- Programme: ESPA; Project: P4GES.
- References: Winrock International (2005) Congo field study report; DOI/URL provided in header.

## Data quality, metadata and governance
- Metadata details provided in the header describe units, variable types, and data meanings to support data interpretation and reuse.
- Data governance considerations:
  - Public sharing of underlying data is a governance and transparency requirement.
  - Metadata completeness is essential to verify suitability for use.
  - Data transformation may be needed to harmonize units (e.g., biomass units) across datasets.
- Practical notes for use:
  - The 0 value indicates absence of dead wood; handle missing data accordingly.
  - Ensure consistent use of units (e.g., Mg ha-1 for biomass and carbon stock).
  - Acknowledge data provenance and data-source requirements in any outputs.

## Relevance for monitoring frameworks
- Provides a concrete, field-based indicator of carbon stock in the lying dead wood pool, contributing to forest carbon inventories.
- Supports evaluation of policy measures related to dead wood carbon dynamics and forest health.
- Demonstrates a clear data lineage (field collection, volume estimation method, and reference dataset) essential for monitoring accountability and data governance.
- Highlights the need for robust metadata and data-sharing practices to enable cross-project comparability and avoid data silos.

## Key considerations for implementation
- Maintain dataset provenance and cite Winrock 2005 method for volume estimation.
- Ensure metadata remains up-to-date and publicly accessible where appropriate.
- Clarify and standardize units across datasets to facilitate integration into broader environmental health metrics.
- Monitor data completeness and timeliness to address common barriers such as data gaps and access limitations.