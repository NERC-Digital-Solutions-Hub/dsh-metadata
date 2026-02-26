# This document is a supplement to the supporting documentation for data series detailed in: 'Turf2Surf_WP2_Supporting_documentation.rtf'

## Overview
- Describes the data structure for soil carbon data in the Conwy catchment, North Wales (2013 and 2014), as detailed in Turf2Surf_Soil_data.csv.
- Part of the Turf2Surf project; data comprises 644 rows with 48 additional measurement columns beyond the first nine shared identifiers.
- Intended for use with related datasets (plant measurements and soil properties) that share the same initial schema.

## Dataset structure and schema
- Shared first 9 columns across related datasets:
  - Site number (unique identifier)
  - Habitat
  - Habitat description
  - Site name
  - Ecosystem component (plant, soil, or roots)
  - If Plant, plant species (otherwise NA)
  - Plot number (1–4)
  - Replicate number
  - Soil depth interval (for soil and roots)
- Missing values are indicated with NA (e.g., restricted depths, limited replicates, or outliers).
- Dataset size: 644 rows, 48 additional columns (labeled J through BE, with NA used where measurements were not performed at a site).

## 48 additional columns and measurements
- Columns J (LOI) through BE (U) describe a comprehensive suite of soil properties, including:
  - Loss on ignition (LOI) and LOI-C (carbon content in LOI fraction)
  - Soil water content and bulk density
  - pH (in water) and electrical conductivity
  - Soil inorganic and organic nitrogen forms (nitrate, ammonium; total dissolved nitrogen)
  - Exchangeable cations (Na, K, Ca) and other soil chemistry metrics
  - Olsen phosphorus and multiple extractable phosphorus fractions (CaCl2, citrate, enzyme, HCl-extractable, etc.)
  - Dissolved organic carbon
  - Bulk and total soil carbon and nitrogen
  - Root biomass and fine root biomass
  - A broad range of elemental concentrations (Al, Si, P, S, Cl, K, Ca, Ti, V, Cr, Mn, Fe, Ni, Cu, Zn, Ga, Rb, Y, Ba, La, Ce, Pr, Nd, Pb, Th, U)
- Each column includes a Unit and Description to aid interpretation (e.g., mg/kg dry soil, mg/L, g/m², % dry weight, etc.).
- Note: The column descriptions for several extractable phosphorus columns are extensive and relate to different extractants and fractions; interpretation requires consistent metadata on method and depth.

## Data provenance and cross-dataset relationships
- 9 initial columns link this soil data to other Turf2Surf datasets that share the same schema (e.g., plant structural measurements, plant biomass, soil physical/chemical/biological measurements, plant physiology).
- This shared schema enables integration and comparative analyses across data types within Conwy catchment sites.

## Data quality, metadata, and governance implications
- Data stewards should ensure comprehensive metadata for:
  - Sampling methods, depth intervals, and plot/replicate design
  - Analytical methods, detection limits, calibration references, and QA/QC procedures
  - Clear handling and documentation of NA values and non-performed measurements
- Important for discoverability and interoperability due to the diverse set of soil properties and the breadth of extractable phosphorus fractions.
- Consider documenting any data transformations (cleaning/normalization) performed before sharing.

## Practical considerations for data management
- Data availability and limitations must be tracked (disclosure risks, potential embargoes, proprietary constraints).
- Systems should support updates and indicate any changes to the dataset over time.
- Upload to appropriate data portals and catalogues; maintain a record of the work performed on datasets.
- Be prepared to address challenges typical to large, multi-system datasets (legacy formats, non-interoperable components) by providing guidance and tooling to users.

## Summary of targeted considerations for Data Stewards
- Ensure alignment with broader Turf2Surf data governance and metadata standards.
- Preserve the linkage between the nine core identifiers and the rich 48-measurement soil chemistry dataset.
- Maintain clear metadata on units, methods, and depth intervals to support reuse and cross-dataset analyses.
- Manage data access, updates, and documentation to facilitate discoverability and responsible sharing.