# PRIMARY Dyfnant Forest draining in to Llyn Vyrnwy

## Overview
- A set of hydrological and environmental observations from the Dyfnant Forest area around Vyrnwy, covering rainfall, streams, and boreholes.
- Datasets include geographic coordinates, altitude, descriptions of site conditions, soil/vegetation types, land management history, and temporal coverage from the mid-1990s to 2001.
- Reference to a primary hydrochemistry study: Neal et al. 2004, The hydrochemistry of plantation spruce forest catchments with brown earth soils, Vyrnwy in mid Wales.

## Datasets Included
- Vyrnwy Rainfall
  - Location: Vyrnwy Rainfall, AA
  - Coordinates: LAT 52.7593, LON -3.4833; Easting 300000, Northing 319000
  - Altitude: 350 m
  - Description: Continuously open rain collector located in open moorland above forest
  - Main soil/vegetation: Podzol, Acid grassland
  - Land management: Rough grazing
  - Timing: Start 5-Dec-1994 to End 16-Feb-2001
  - Reference: 10
- Vyrnwy1 Stream
  - Location: W
  - Coordinates: LAT 52.7860, LON -3.4309; Easting 303600, Northing 321900
  - Altitude: 320 m
  - Description: Ephemeral stream draining in to Afon Hirnant
  - Main soil/vegetation: Brown Earth; Plantation Sitka spruce forest
  - Land management: 100% clearfelled April 1997
  - Timing: Start 7-Oct-1994 to End 16-Feb-2001
  - Reference: 10
- Vyrnwy2 Stream
  - Location: X
  - Coordinates: LAT 52.7796, LON -3.5107; Easting 298200, Northing 321300
  - Altitude: 258 m
  - Description: Ephemeral stream draining in to Llyn Vyrnwy
  - Main soil/vegetation: Brown Earth; Plantation Sitka spruce forest
  - Land management: Standing crop (control for Vyrnwy1 stream)
  - Timing: Start 7-Oct-1994 to End 16-Feb-2001
  - Reference: 10
- Vyrnwy1 Borehole
  - Location: Y
  - Coordinates: LAT 52.7860, LON -3.4309; Easting 303600, Northing 321900
  - Altitude: 320 m
  - Description: By ephemeral stream in Dyfnant Forest draining in to Afon Hirnant
  - Main soil/vegetation: Brown Earth; Plantation Sitka spruce forest
  - Land management: Clearfelled April 1997
  - Timing: Start 7-Oct-1994 to End 16-Feb-2001
  - Reference: 10
- Vyrnwy2 Borehole
  - Location: Z
  - Coordinates: LAT 52.7796, LON -3.5107; Easting 298200, Northing 321300
  - Altitude: 258 m
  - Description: At roadside by ephemeral stream in
  - Main soil/vegetation: Brown Earth; Plantation Sitka spruce forest
  - Land management: Standing crop (control for Vyrnwy1 borehole)
  - Timing: Start 7-Oct-1994 to End 16-Feb-2001
  - Reference: 10

## Geographic and Temporal Coverage
- Spatial: Dyfnant Forest area near Vyrnwy with multiple measurement sites (rainfall, streams, boreholes) at specific coordinates and elevations ranging roughly 258–350 m.
- Temporal: Data collected from 7-Oct-1994 through 16-Feb-2001 for streams and boreholes; rainfall data from 5-Dec-1994 through 16-Feb-2001.

## Data Attributes and Metadata
- Consistent schema across datasets:
  - Location code, precise coordinates (easting/northing and lat/long), altitude
  - Descriptions of site conditions and hydrological role
  - Soil types and vegetation (noting plantation Sitka spruce and brown earth soils)
  - Land management history (e.g., clearfelling in 1997; standing crop controls)
  - Mining status (None)
  - Start and end dates for data collection
  - Reference number (10) linking to primary study/metadata
- Metadata supports understanding of site conditions (forestry practices, land management) and potential hydrological responses.

## Data Quality, Processing, and Transformation
- Datasets are described with standardized fields enabling cross-dataset QA and harmonization.
- Sites reflect changes in land use (e.g., 1997 clearfelling) that may affect hydrological signals; stewardship should note these when merging time series.
- Temporal alignment across rainfall, streams, and boreholes facilitates integrated hydrological analysis.

## Provenance and References
- Primary reference: Vyrnwy: streams, groundwater and rainfall, Neal C., Reynolds B., Neal M., and Williams B. 2004. Hydrology and Earth System Sciences (Hydrol Earth Syst Sci) 8, 460-484.
- Reference number for all entries: 10, indicating a single provenance record linked to the primary study.

## Access, Sharing, and Governance Considerations
- Explicit sharing terms and access restrictions are not stated in the provided text.
- Governance actions for Data Stewards:
  - Confirm data access terms and any embargoes with the primary project or data owners.
  - Verify data licensing and rights for redistribution or reuse in new analyses.
  - Document metadata completeness and any quality flags or processing steps performed.
  - Ensure time-series data are synchronized across rainfall, streams, and boreholes if used together.
  - Capture provenance notes about land-management events (e.g., 1997 clearfelling) that influence interpretation.

## Challenges and Considerations for Data Stewards
- Incomplete user needs and priorities may arise; align dataset documentation with potential user questions (hydrochemistry context, land-use effects).
- Data from multiple systems and formats (rainfall, streams, boreholes) require careful harmonization.
- Handling of period with major land-use change (clearfelling) to ensure correct interpretation of hydrological responses.
- Potential interoperability with other Vyrnwy datasets or regional studies, such as the referenced hydrochemistry study.

## Key Takeaways for Data Stewards
- The primary Dyfnant Forest dataset collection provides a cohesive, time-binned set of hydrological measurements tied to forest land-use history, with detailed geographic metadata and consistent reference linkage to a foundational study.
- For effective reuse, ensure complete metadata capture, clarify access terms, and document any site changes that could affect analyses across rainfall, stream, and borehole records.