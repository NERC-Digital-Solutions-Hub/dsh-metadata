# Macroinvertebrates of the Conwy catchment

- An archive of macroinvertebrate community data from the Conwy catchment in Wales, UK, sampled over 2008–2010, with accompanying habitat and geographical metadata.
- Data are organized into three CSV files: taxon data, environmental variables, and supporting information.
- Version-controlled dataset (Version 1.0, 28/06/2016) with contributions from multiple team members for sample collection, laboratory analysis, and metadata documentation.

## Data files and structure

- taxon data.csv
  - Columns: Site code, Year, Sample date, Taxon code (per Davies & Edwards 2011), Taxon name, Life stage (L, P, A, U), Abundance.
- environmental variables.csv
  - Columns: Site code, Year, Wetted width (m), Water depth (cm), Velocity (m/s), % cover of rock pavement, % cover of boulders/cobble, % cover of sand, % cover of silt/clay, % cover by macrophytes.
- supporting information.csv
  - Columns: Site code, Site name, Easting, Northing, OS grid reference, Distance from source (km), Altitude (m), Slope (m/km), Stream Strahler order, Upstream catchment area.
- The accompanying information file provides a site-key and detailed site-level attributes.

## Methods and quality assurance

- Field sampling
  - Study sites are tributaries of the Conwy, sampled in November 2008, 2009, and 2010.
  - Macroinvertebrates collected with a 1 mm kick net following the RIvPACS protocol; accompanying site variables (depth, width, velocity, substrate and macrophyte cover) recorded.
  - Samples preserved in 4% formaldehyde in the field, then returned to the lab.
- Laboratory processing
  - In the lab, samples were washed through a 500 μm sieve; macroinvertebrates identified to the lowest feasible taxonomic level (usually species).
  - Valid taxon names and unique taxon identification codes provided in Davies & Edwards (2011).
  - Data entry validated by cross-checking printouts with laboratory sheets.
- Data handling and derivation
  - Map/auxiliary variables derived for sites using Intelligent River Network (Version 17), following methods described by Dawson et al. (2002).
  - Sample identifiers defined by a unique combination of site code and year; a site-code key is provided in the supporting information.
- Data integrity
  - Clear documentation of variable definitions and units within the metadata files.
  - Version control and contributor records maintained.

## Metadata and supporting information

- Site-level metadata includes coordinates (Easting/Northing, grid references), distance from source, altitude, slope, stream order, and catchment area.
- The supporting information file contains a wide set of site records (e.g., AFON CADNANT, AFON DDU UPPER, AFON LLEWESIG, etc.) with detailed geospatial and catchment context to support spatial analyses and reproducibility.

## Provenance, contributors, and governance

- Contributors by role:
  - Sample collection: Gearóid Webb, Peter Scarlett, John Davy-Bowker
  - Laboratory analysis: Gearóid Webb, Helen Vincent, François Edwards
  - Supporting information: Peter Scarlett, Gearóid Webb, François Edwards
  - Planning and management: François Edwards, David Cooper
- Purpose and governance
  - Data management aligned with good data governance practices for large datasets: documentation, provenance, and updateability.
  - Plan to upload datasets to relevant portals and catalogue data holdings; documentation supports discoverability and reuse.
- Versioning and authenticity
  - Version 1.0 documented; revision control implied for future updates to ensure traceability.

## Data stewardship considerations and reuse

- Relevance for data stewards
  - Provides a well-documented, species-level macroinvertebrate dataset with associated habitat data suitable for bioassessment, ecological modeling, and river health monitoring.
  - Clear taxon coding system (Davies & Edwards 2011) and QA steps support interoperability and re-use.
- Governance and standards
  - Metadata clearly defines structure, units, and data derivation methods; enables data discovery and integration with other aquatic datasets.
  - Potential challenges noted in typical data stewardship contexts: coordinating timely data transfer, aligning metadata across different systems, and ensuring interoperability of legacy formats.
- Access, licensing, and updates
  - While licensing is not specified in the document, the data stewardship approach emphasizes publishing datasets to portals with appropriate licensing and embargo controls as needed, along with ongoing updates and versioning.