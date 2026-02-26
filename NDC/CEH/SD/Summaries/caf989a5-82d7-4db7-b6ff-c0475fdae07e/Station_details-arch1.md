# KeyName|Place|Easting|Northing|HillsVisible|Comments

- Scope of the dataset
  - A comprehensive gazetteer of observation stations, primarily across Scotland (with some entries outside continental UK), listing station name, geographic coordinates (Easting/Northing), and the hills visible from each site.
  - HillsVisible fields describe visible hills with bearing, height, and distance from the station.

- Data structure and fields
  - Key fields include:
    - KeyName: identifier for the station
    - Place: location name
    - Easting / Northing: grid coordinates (likely OS National Grid)
    - HillsVisible: list of hills with bearing (degrees), height (feet), and distance (miles)
    - Comments: additional notes per station (sometimes linked to the same line as HillsVisible)
  - HillsVisible entry format examples:
    - Ben Graim More: 209°, 1956', 3 miles
    - Meall A Bhealach: 003°, 1105', 3 miles
    - Ben More: 3843', 20 miles wsw of station
    - Aviemore entry: 100° to 360° 1466' (447 m) to 4293' (1309 m) 2800 m to 18 km at regular intervals of height and distance
  - Some rows include NA for comments or HillsVisible, and several entries show variability in formatting.
  - Elevations are listed in feet (with apostrophe notation), distances in miles, and bearings in degrees.

- Observed patterns and coverage
  - Wide geographic spread across Scotland, including notable highland and island sites (e.g., Achentoul, Aviemore, Kinlochewe, Sligachan, Ben Nevis area references, Islay, Orkney entries like Lerwick, NATO FSS sites, and various power stations and lodges).
  - Frequent references to major hills and ranges (e.g., Ben Nevis, Ben More, Ben Lomond, Meall Mor, Suilven, Glencoe/Ben Vorlich, Cairn Gorm areas, Beinn a’ Bhàthaich, etc.).
  - Some entries provide extensive lists of visible peaks with multiple bearing-distant pairs, indicating long horizon lines from certain vantage points.

- Data quality and caveats
  - Units and formatting are not fully standardized across all rows (feet for elevation, miles for distance, degrees for bearing).
  - Several entries contain NA values in HillsVisible or Comments, indicating missing data.
  - Some rows include embedded notes in Comments (e.g., unit conventions, data provenance, or observational caveats such as “Depth at station units not stated, assumed metric”).
  - Occasional inconsistencies or truncation in the text (e.g., long lines with mixed data) which may require normalization for automated use.
  - The dataset appears to merge diverse site types (stations, lodges, power stations, NATO FSS sites, universities, airports), which may affect context and metadata needs.

- Potential analytical uses
  - Build horizon visibility maps by mapping station coordinates to visible peaks and distances.
  - Cross-validate with digital elevation models to assess line-of-sight reach and horizon extents.
  - Compare bearing/distance tallies across sites to identify areas with broad vs. limited visibility.
  - Combine with temporal data (if available) to study how visibility observations vary with conditions or seasons.

- Limitations and recommendations for improvement
  - Standardize field formats: separate fields for hill name, bearing, height, and distance; ensure consistent units.
  - Include metadata: observation date, observer, measurement method, and data source.
  - Explicitly separate NA cases and provide a data dictionary to clarify ambiguous entries.
  - Normalize place names and coordinates to a common reference (e.g., OSGB36) to ease GIS integration.
  - Clarify whether HillsVisible elevations are peak heights or line-of-sight horizon heights, and confirm units for all numeric fields.
  - Consider tagging entries by site type (station, power station, lodge, NATO site, university, etc.) to support targeted analyses.