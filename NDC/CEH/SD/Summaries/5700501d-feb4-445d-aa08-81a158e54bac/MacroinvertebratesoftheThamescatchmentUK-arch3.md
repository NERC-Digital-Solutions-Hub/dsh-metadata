# Macroinvertebrates of the Thames catchment

## Overview
- Dataset describing macroinvertebrate communities from wadeable rivers in the Thames catchment, UK.
- Collected over three seasons: Autumn 2009, Spring 2010, Autumn 2010.
- Includes supporting habitat/environmental data.

## Data files and contributors
- Relevant data files:
  - Macroinvertebrates of the Thames catchment - taxon data.csv
  - Macroinvertebrates of the Thames catchment - environmental variables.csv
  - Macroinvertebrates of the Thames catchment - supporting information.csv
- Contributors:
  - Sample collection: Gearóid Webb, Peter Scarlett, Roger Baker, François Edwards
  - Laboratory analysis: Gearóid Webb, François Edwards, Helen Vincent
  - Supporting information: Peter Scarlett, Gearóid Webb, François Edwards
  - Planning and management: François Edwards, Michael Bowes

## Study design and field methods
- 18 sampling sites in the Thames catchment; sampling occurred Autumn 2009, Spring 2010, and Autumn 2010 (not all sites sampled every occasion).
- Field protocol: 1 mm mesh kick net, RIvPACS procedure; additional site variables recorded (depth, width, substrate cover, macrophyte cover).
- Specimens preserved with 4% formaldehyde; in the lab, macroinvertebrates were identified to the lowest taxonomic level possible (usually species).
- Taxon codes and valid names provided in Davies & Edwards (2011) code list.
- Data validation: crosschecking data printouts with laboratory sheets.
- Spatial variables derived: map variables created using Intelligent River Network (IRN) Version 17.
- Key methodological references:
  - RIvPACS protocol (Murray-Bligh et al., 1997)
  - Intelligent River Network (Dawson et al., 2002)

## Data content and structure
- Taxon dataset columns:
  - Site code
  - Sample date
  - Season (Autumn = A, Spring = S)
  - Taxon code (per Davies & Edwards 2011)
  - Taxon name (per Davies & Edwards 2011)
  - Life stage (L = larva/nymph, P = pupa, A = adult, U = not relevant)
  - Abundance in sample
- Supporting information dataset columns:
  - Site code, Site name, Waterbody name, Easting, Northing, OS grid reference
- Environmental variables dataset columns:
  - Site code, Sample date
  - Wetted width (m)
  - Water depth (cm)
  - % cover of rock pavement
  - % cover of boulders/cobbles, pebble/gravel, sand and silt/clay (summing to 100%)
  - % cover by macrophytes

## Quality control and governance
- Taxon names aligned to a standard code list (Davies & Edwards, 2011) to ensure consistency.
- Data entry validated against laboratory records.
- Taxonomic and environmental data linked to site and sampling event identifiers to support traceability.
- Map-derived environmental variables generated using a standardized method (IRN) for consistency across sites.

## Data accessibility and usage notes for monitoring
- Data are organized with clear identifiers (site code, sample date) and accompanying metadata for site context.
- Supporting information provides geographic context (site names, coordinates) and sampling details.
- Metadata and data provenance are documented to facilitate integration into monitoring frameworks and governance processes.
- While not explicitly stated, the dataset is prepared to support monitoring assessments and methodological replication, with emphasis on data quality, openness, and standardized reporting.

## References and mappings
- Taxon coding and nomenclature: Davies, C. and Edwards, F.K. (2011) Code list for recording the macroinvertebrates in freshwater in the British Isles. CEH, Wallingford.
- Habitat/environmental variables mapping: Intelligent River Network (IRN) v17; Dawson, F.H., Hornby, D.D., and Hilton, J. (2002) for automated extraction of environmental variables. Aquatic Conserv: Mar. Freshw. Ecosyst. 12:391-403.
- RIvPACS field protocol: Murray-Bligh et al. (1997).