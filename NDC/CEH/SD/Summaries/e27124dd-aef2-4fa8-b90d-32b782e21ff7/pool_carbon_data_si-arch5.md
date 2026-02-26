# Carbon concentrations in natural and restoration pools in blanket peatlands in Scotland, 2013-2015

## Overview
- Dataset describing carbon concentrations in natural and restoration pools across blanket peatlands in Scotland, collected 2013–2015.
- Data collection and generation methods are outlined in the related Hydrological Processes manuscript (2022); data have undergone quality control (e.g., values below detection limits addressed).
- Available as six CSV files, spanning both combined and site-specific datasets, with detailed variable metadata.

## Data files and structure
- Pool_Carbon_Quarterly
  - Sites: CL, LL, MU
  - Description: All quarterly data from LL, CL, MU pooled into one table.
- Pool_Carbon_Routine
  - Sites: CL only
  - Description: Routine, more frequently sampled data for CL.
- Pool_Carbon_Routine_DOC
  - Sites: CL only
  - Description: Piezo soil water DOC data at different depths.
- Pool_Carbon_Routine_Colour
  - Sites: CL only
  - Description: Piezo soil water colour data at different depths.
- Pool_Carbon_Routine_Depth
  - Sites: CL only
  - Description: Pool depth on sampling day (from continuous loggers).
- Pool_Carbon_Routine_Soil
  - Sites: CL only
  - Description: Bulked soil solution from piezometers (all depths bulked into one sample).

## Variables and measurements (highlights)
- Pool and sampling metadata
  - Pool, Treat (NAT = natural; ART = artificial/restoration), Year, Date, Time/Week, Quarter
  - Site codes: CL, LL, MU
  - Pool area (m^2), Pool depth (cm), Pool volume (m^3)
- Hydrological and chemical parameters
  - pH; EC (µS/cm); DO (mg/L); Water Temp (°C)
  - Water quality indices: abs254 (abs/m), SUVA (l/mg/m), E4E6 ratio (465/665)
  - Dissolved organic carbon: DOC (mg/L); POC (mg/L)
  - Gases: CH4 (µg/L), CO2 (mg/L)
  - Water column properties: DOC at various positions (BASE, INFLOW, OUTFLOW, SURFACE, OLF), WTD (cm)
- Depth- or position-specific measurements
  - Depth below peat (cm) for samples; Depth of sample collection (from piezometers)
- Data organization
  - Distinctions between routine (frequent CL data) and quarterly datasets
  - Details on measurement depths and sample types captured in accompanying variable descriptors

## Data quality, provenance and documentation
- Data are quality controlled; notes indicate addressing values below detection limits.
- Data collection methods referenced in the primary manuscript (Hydrological Processes, 2022).
- Each file includes explicit units and descriptions for all variables, supporting robust metadata and reuse.
- Metadata conventions cover Year, Date, Week/Quarter, Pool, Treat, Site, and depth-related context, enabling traceability.

## Data governance considerations for Data Stewards
- Harmonization across files:
  - Ensure consistent use of pool identifiers, site codes, and treatment categories (NAT/ART) across quarterly and routine datasets.
  - Map variables with similar meaning across files (e.g., DOC measurements at different depths) to a common data model.
- Metadata and documentation:
  - Preserve the provided units and descriptions; consider additional metadata fields for data lineage, collection methods, QC procedures, and versioning.
  - Document any data transformations, amalgamations (e.g., Pool_Carbon_Quarterly), and filtering steps.
- Data availability and updates:
  - Tracking of data availability, embargoes, and potential updates to routine vs. quarterly datasets.
  - Establish a protocol for: new measurements, corrections (e.g., QC adjustments), and version control.
- Interoperability and discoverability:
  - Use standardized field names and controlled vocabularies where possible to facilitate discovery and cross-study comparisons.
  - Prepare a data dictionary and a readme that mirrors the level of detail in the six CSV files.

## Access, reuse, and limitations
- Suitable for cross-site peatland carbon dynamics analyses, time-series comparisons, and methodological studies of pool chemistry.
- Users should reference the primary manuscript for data collection methods and QC steps.
- Potential caveats:
  - CL site is the focus for Routine data; quarterly data are more broadly distributed across CL, LL, MU.
  - Differences in sampling cadence and depths between Routine and Quarterly datasets.
  - Some variables have multiple related measurements (e.g., DOC, Abs254, SUVA, E4E6) that require careful alignment when aggregating.

## Recommendations for cataloguing and use
- Include detailed data provenance notes and a data dictionary aligned with the six CSV files.
- Create a unified view or join key (Pool, Site, Year, Date/Week) to enable straightforward time-series analyses.
- Tag data by site and dataset type (Quarterly vs Routine) to support targeted queries.
- Reference the Hydrological Processes 2022 manuscript for comprehensive methods and QC context.