# Otter Carcass Data Variables and Definitions

- A data dictionary detailing identifiers, geographic information, temporal data, biological attributes, body condition metrics, spatial coordinates, and tissue chemistry measurements for otter carcasses.
- Data are used by the Predatory Bird Monitoring Scheme and the Cardiff Otter Project, with unique identifiers from both CEH and UWC systems.

## Key data categories

- Identifiers
  - CEH Ref: Unique numeric identifier assigned by the Predatory Bird Monitoring Scheme.
  - UWC Ref: Unique numeric identifier assigned by the Cardiff University Otter Project.

- Temporal data
  - Month Found: Month in which the otter body was found.
  - year Found: Year in which the otter body was found.

- Geographic location
  - County: County in England or Wales where the otter body was found.
  - X-coordinate: X spatial coordinate (no unit specified).
  - Y-coordinate: Y spatial coordinate (no unit specified).

- Biological attributes
  - Sex: Sex of the otter (Female or Male).
  - AgeClass: Age class (Juvenile, Sub-adult, or Adult).

- Body condition
  - Condition coefficient (K): Body condition coefficient as defined by Kruuk & Conroy (1991).

- Measurements and tissue chemistry (liver tissue)
  - % Dry matter: Percentage of dry mass from liver sample (drying 0.5 g sample at 70°C for 48 hours).
  - Al, Mn, Fe, Co, Ni, Cu, Zn, Se, Sr, Mo, Cd, Sb, Pb, Hg, Cr, As, V, Ag: Dry weight concentration of respective elements in liver tissue.
  - Units for all elements: mg/kg.
  - Classes for each chemical: ND (Non detected) or NA (Not analysed) when applicable.

## Data quality and standards considerations

- Data originate from multiple sources; potential inconsistencies in formats and coding.
- Missing data and varying data resolutions are common (e.g., complementing location with precise X/Y vs. county-level info).
- ND/NA classifications require consistent handling during GIS processing and analysis.
- No explicit spatial reference system is stated for X/Y coordinates; coordinate system Standardization may be needed for mapping.

## GIS and mapping implications

- X and Y coordinates enable point-based geospatial mapping of otter findings.
- County and coordinate data allow both coarse (county-level) and precise (point-level) spatial analyses.
- Liver tissue chemistry variables can be linked to spatial features to explore spatial patterns of contaminant exposure.
- The dataset supports map-based visualizations (e.g., distribution of finds by month/year, sex/age class breakdowns, and chemical concentrations by location).

## End-use and workflow recommendations for data products

- Data preparation
  - Harmonize coding for Sex (e.g., consistently use Female/Male) and AgeClass (Juvenile/Sub-adult/Adult).
  - Standardize handling of ND/NA values across all chemical measurements.
  - Document provenance and data sources for CEH Ref and UWC Ref.
- Data quality
  - Implement validation checks for temporal and spatial fields (valid months, years, and plausible coordinates).
  - Validate chemical concentration units and confirm drying method details for % Dry matter.
- GIS implementation
  - Ensure a defined coordinate reference system for X/Y (e.g., WGS84 or a local projection) and document it in metadata.
  - Create attribute domains and coded values where appropriate (e.g., Sex, AgeClass, ND/NA flags).
  - Develop data-to-map workflows that can handle missing values and variable data resolutions.
- Data products
  - Generate interactive maps showing carcass locations, filtered by time, county, sex, or age class.
  - Create choropleth layers for aggregate chemical concentrations by area and time, with appropriate handling of ND/NA values.
  - Provide metadata and lineage to support reproducibility and future updates.