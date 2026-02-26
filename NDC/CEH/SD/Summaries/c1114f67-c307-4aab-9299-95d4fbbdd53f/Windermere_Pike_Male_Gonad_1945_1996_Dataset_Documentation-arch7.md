# Windermere Pike Male Gonad Weight Data (1945 to 1996)

- Overview
  - Dataset of estimated gonad weight and related data for male pike (Esox lucius) from net sampling.
  - Data collection: 1945–1996. Initially by the Freshwater Biological Association (FBA); since 1989 by CEH and its predecessor IFE.
  - File: Windermere_Pike_Male_Gonad_Data_1945_to_1996.csv (CSV, ~225 KB).

- Spatial and Temporal Coverage
  - Location: Windermere Lake, Cumbria, Great Britain.
  - Spatial references: approximate grid reference SD393960; OSGB36 Easting/Northing 339385,496080; coordinates provided in WGS84 (54.360193, -2.935836).
  - Time span: 1945–1996.
  - Environmental variable: annual average water surface temperature (Temp, °C).

- Data Columns and Measurements
  - Individual: unique identifier for each fish.
  - Weight: body weight (g).
  - Length: length at capture (cm).
  - Age: age at capture (years).
  - Year: year of capture (calendar year).
  - Temp: annual average water surface temperature (°C).
  - GSI: gonadosomatic index (dimensionless).
  - Gonad: estimated gonad weight (g).
  - Units are specified in parentheses above.

- Experimental Design and Sampling Regime
  - Species monitored: Pike (Esox lucius) in the north and south basins.
  - Sampling method: gill netting with 64 mm bar mesh since 1982; nets are 40 m x 3 m, set on the lake bottom, Oct–Dec.
  - Sampling sites: 10 sites per basin; five nets in water at a time; sites rotated to cover the lake; each site fished for ~2 weeks per season.
  - Effort: 1982–1989 ~348 net days annually; 1990 onward ~240 net days annually, distributed between basins.
  - Birth date reference for aging: 1 April; left opercular bone used for aging (Frost & Kipling method).

- Analytical Methods
  - Measurements: fork length to 1 mm; wet weight to 100 g; pike dissected to determine sex.
  - Gonad weight estimation: linear function; gonad weight of the lightest individual ~2% of body weight; heaviest ~4% of body weight (Craig 1996).

- Data Quality and Quality Control
  - Quality checks: measurements validated by permutations across three individuals.
  - Methodological notes: pre-1982 data reflect non-standardized methods; standardization implemented from 1982 onward (N.B. references include Le Cren 2001; Winfield et al. 2008; Frost & Kipling 1959; Craig 1996).

- GIS and Data Integration Considerations
  - Suitable for map-based analyses of gonad weight, GSI, and body size across space (Windermere basin sites) and time (1945–1996).
  - Combines biological measurements with environmental context (temperature) and spatial metadata (grid references, OSGB36/WGS84).
  - Considerations for GIS use: historical methodology variation prior to 1982; consistent post-1982 sampling protocol; need for data harmonization if integrating with other datasets or resolutions.