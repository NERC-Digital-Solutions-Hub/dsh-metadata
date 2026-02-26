# Landscape area data 1978 [Countryside Survey], Great Britain Version: 1: 15-1-2016 Countryside Survey data © NERC - Centre for Ecology & Hydrology

## Overview
- Dataset of Broad and Priority Habitat areas in 1km squares across Great Britain from the 1978 Countryside Survey.
- Covers 256 1km sampling squares.

## Data file and structure
- File: LANDSCAPE_AREA_FEATURE_HAB_1978.csv
- Columns and meaning:
  - SQUARE: 1km square sampling site code (text)
  - YEAR: Year of survey (numeric)
  - ID: Landscape area polygon identifier (unique within a year)
  - BROAD_HABITAT: Broad habitat code (numeric)
  - BROAD_HABITAT_NAME: Broad or Priority Habitat name (text)
  - AREA: Area of habitat within the 1km polygon (square metres)
  - LAND_CLASS90: ITE Land Classification 1990 code (numeric)
  - COUNTRY: Country containing the square (ENG, SCO, WAL)
  - COUNTY: County or equivalent (Eng & Wal) or Council (Sco)
  - EZ_DESC_07: Countryside Survey Environmental Zone description (text)

## Interpretation notes
- AREA represents habitat area within the specified 1km square.
- BROAD_HABITAT_NAME provides human-readable habitat names corresponding to BROAD_HABITAT codes.
- LAND_CLASS90 references the ITE Land Classification framework used in GB datasets.

## Usage and attribution
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement example: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
- Data are © NERC CEH; all rights reserved.

## Access and references
- Countryside Survey website: http://www.countrysidesurvey.org.uk/
- 1978 Data Rescue Final Report (Wood et al., 2012): CS1978_final_report_PDF.pdf
- Technical reports and related publications (e.g., Scott 2007) detailing national estimates and methodologies.
- Related datasets and classifications:
  - ITE Merlewood Land Classification (1990 and earlier iterations)
  - Biodiversity Broad Habitat Classification guidance (Jackson, 2000)

## Practical considerations for analysts
- Temporal scope: data from 1978; suitable for historical habitat analysis and change detection when combined with later surveys.
- Spatial scale: 1km squares; align with other GB-wide datasets at compatible scales.
- Data integration: may require unifying with ITE Land Classification (1990) and Broad Habitat classifications; verify code mappings.
- Data access: ensure proper permissions and metadata availability; plan for potential administrative steps to obtain datasets.

## Data quality and caveats
- Coverage limited to 256 1km squares for 1978; may not represent the entire GB.
- Data may require cross-walking between classifications (e.g., LAND_CLASS90 to current schemes).
- Ensure consistent interpretation of COUNTRY/COUNTY boundaries and environmental zone descriptions.

## References and metadata sources
- Countryside Survey project overview and methodologies (CS website)
- 2012 Countryside Survey: Measuring Habitat Change Over 30 Years (CS1978 Data Rescue Final Report)
- Statistical and technical reports on UK national estimates from Countryside Survey
- Supporting classifications and habitat guidelines (ITE Land Classification; JNCC Broad Habitat guidance)