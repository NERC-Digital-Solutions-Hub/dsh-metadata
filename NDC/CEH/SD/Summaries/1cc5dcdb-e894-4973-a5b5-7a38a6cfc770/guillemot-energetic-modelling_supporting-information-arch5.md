# Activity, energy expenditure and mass data from common guillemots from the Isle of May during the 2016-2017 annual cycle

## Overview
- Biologging dataset for common guillemots (Uria aalge) from the Isle of May National Nature Reserve, Scotland, covering the 2016-2017 annual cycle.
- Derived daily metrics include foraging time, sea surface temperature (SST), energy expenditure, location, and daylight hours.
- Data delivered as a single CSV file: IoM_Guillemot_SST_F_DEE_Loc_Mass.csv, with ten columns.

## Data collection and provenance
- Study site: Isle of May, coordinates 56°11′N, 02°33′W.
- Instrumentation: GLS devices (MK3006, Biotrack, UK) attached to Darvic leg-rings.
- Handling: birds weighed to the nearest gram before deployment and at retrieval using a Pesola spring balance; processing time per capture < 5 minutes.
- Processes:
  - Data collected from light, temperature, and conductivity measurements.
  - Derived daily data include guillemot activity (hours foraging), SST, energy expenditure, location fixes, and daylight hours.
- Access and contributors:
  - Scottish Natural Heritage granted access to the Isle of May.
  - Planning/collection/management contributions by Sarah Wanless, Mike Harris, Francis Daunt, Mark Newell, and Maria Bogdanova.
  - Data processing by Ruth Dunn.

## Dataset composition and file format
- File name: IoM_Guillemot_SST_F_DEE_Loc_Mass.csv
- Columns (10 total):
  1) logger.id: unique ID for each individual
  2) Adult.E: daily adult energy expenditure (kJ)
  3) sst: sea surface temperature (°C)
  4) Foraging: daily time spent foraging (hours)
  5) day.length: daily daylight hours (hours)
  6) lon: longitude
  7) lat: latitude
  8) distance.coast.km: distance to nearest coastline (km)
  9) start.mass: mass at deployment (g)
  10) end.mass: mass at retrieval (g)

## Data quality, standards and stewardship considerations
- Clear, machine-readable structure with explicit units (kJ, °C, hours, grams, kilometers).
- Provenance documented: contributors and processing steps retained.
- Dataset suitable for discovery and reuse, enabling analyses of activity, energetics, and spatial ecology during the 2016-2017 cycle.
- Documentation supports data governance through metadata and consistent formatting, facilitating sharing across portals and with data users.

## Access, sharing and limitations
- Single CSV dataset; no embargo details provided.
- Temporal and geographic scope clearly defined (Isle of May, 2016-2017); derived metrics accompany raw measurements.