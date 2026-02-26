# Hill Visibility Observations by Station

- A geographic dataset capturing which hills are visible from numerous observation stations across Scotland and surrounding areas.
- Each record links a station (KeyName/Place) to its grid coordinates (Easting/Northing) and the hills that can be seen from that location, including azimuth, height, and distance.

## Data Scope and Structure

- Contains multiple station entries (e.g., Achentoul, Aviemore, Fort Augustus, Sligachan, Loch Lomond area, etc.).
- Spatial references use grid coordinates (Easting and Northing) to identify station locations.
- HillsVisible field lists one or more hills visible from the station, with directional bearing (degrees), height (feet), and distance (miles) to each hill.
- The dataset includes a Comments field per row with supplementary notes about the station view, terrain, or data issues.
- Some rows include NA values for certain fields, indicating missing or unavailable information for that station.

## Key Data Fields (structure)

- KeyName / Place: Station identifier and name.
- Easting / Northing: Grid coordinates for the station location.
- HillsVisible: List of visible hills, each with:
  - Hill name
  - Azimuth (degrees)
  - Height (feet)
  - Distance (miles)
- Comments Achentoul / Achentoul (and similarly named columns): Additional descriptive notes about the station’s observations or the hills noted.
- NA fields: Indicate missing data or not applicable for certain stations.
- Miscellaneous notes in comments (e.g., “Records isolated patches as lowest snow level,” “Depth at station units not stated, assumed metric,” historical remarks about data collection cadence or formats).

## Data Quality, Limitations, and Gaps

- Patchy data: Some stations have incomplete or missing HillsVisible details, or NA fields.
- Varied formats: HillsVisible entries combine azimuth, height, and distance in a single string, requiring parsing to standardize.
- Inconsistent units: Height values in feet are given (e.g., 2090', 1956') with some notes indicating metric assumptions for depth or other measures.
- Data provenance notes: Some rows include historical remarks (e.g., references to observations from the 1940s-1950s, occasional notes on snow levels, or reliability of weekly vs. other observation cadences).
- Quality caveats in comments: Patches of records, potential mislogging, and occasional ambiguous references to data collection methods.

## Potential Data Products and Uses for Data Support

- Self-serve dashboards mapping station locations to visible hills:
  - Interactive map showing HillsVisible per station with hover/click details for azimuth, height, and distance.
  - Filters by region, hill height, azimuth range, or distance to support planning and analysis.
- Data transformations to enable easier querying:
  - Parse HillsVisible into structured sub-records (HillName, Azimuth, HeightFt, DistanceMiles).
  - Normalize units and convert grid coordinates to a common geographic coordinate system (e.g., WGS84) for mapping.
- Data quality and reliability views:
  - Flags for stations with missing HillsVisible data or inconsistent formatting.
  - Metadata summaries on data completeness by region and time period.
- Analytical outputs:
  - Visualizations of line-of-sight coverage across regions, identifying gaps where hills are not observed from many stations.
  - Cross-station comparisons to identify agreements/discrepancies in visible features.

## Challenges and Recommendations for Data Support

- Standardize data ingestion:
  - Develop parsers to reliably extract hill name, azimuth, height, and distance from HillsVisible strings.
  - Normalize units and convert coordinates to a consistent CRS.
- Improve data quality controls:
  - Implement validation rules for missing fields and inconsistent entries.
  - Document data provenance and any historical context to guide interpretation.
- Enhance accessibility and reuse:
  - Create an API and a user-friendly dashboard to enable end-users to select stations and view associated hills.
  - Provide export options (CSV/JSON) with flattened, structured hill records per station.
- Proactive data governance:
  - Maintain a data dictionary describing field meanings, units, and accepted value ranges.
  - Establish a data update cadence and QA checks, especially for stations with sporadic or historical data.
- Communication and training:
  - Provide guidance on interpreting HillsVisible entries (e.g., how to read azimuth and distance, handling ambiguous entries).
  - Include notes on limitations due to patchy data or changes in observation practices over time.

## Endnotes

- The dataset serves as a foundational resource for understanding visual access to topographic features from fixed survey stations, suitable for building descriptive maps, self-serve data tools, and region-focused analyses when properly parsed and standardized.