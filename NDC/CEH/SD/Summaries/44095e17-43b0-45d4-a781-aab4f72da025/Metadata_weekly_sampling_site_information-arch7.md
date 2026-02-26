# DRAINAGE AREAS AND STREAM FLOW CONVERSION

## Overview
- A comprehensive dataset of hydrochemical and hydrological observations for Hafren and Plynlimon catchments in mid-Wales.
- Contains per-site attributes: location, coordinates, altitude, description, soils, vegetation, land management, mining, sampling period, and bibliographic references.
- Includes multiple data types: stream channels, boreholes, ephemeral/conduit features, rainfall and chloride measurements, and groundwater-related data.
- References (bibliography) linked by primary reference numbers accompanying site records.

## Data structure
- For each site, attributes include:
  - Site name and location code
  - Spatial coordinates: Easting, Northing; Latitude/Longitude (WGS84)
  - Altitude (metres)
  - Description of the site (e.g., main stream channel, borehole, rainfall site)
  - MAIN SOIL TYPES and VEGETATION
  - LAND MANAGEMENT and MINING status
  - START DATE and END DATE (sampling/recording period)
  - PRIMARY REFERENCE NUMBER and COMMENTS
- Categories of sites include Lower Hore, Lower Hafren, Tanllwyth, Rainfall, Upper Hore, Stemflow, Throughfall, Cloud, Vyrnwy-related sites, boreholes, and various Tanllwyth/valley-bottom references.
- Bibliographic references (REF. NUMBER 1–10) provide the hydrochemistry and hydrology literature supporting the data (e.g., rainfall, throughfall, groundwater, and forestry impact studies).

## Key site examples (selected)
- Lower Hore (Code A): Main Hore stream channel above lower flume; Podzol/Gley soils; 77% Sitka spruce plantation; felled 1985–1988; start 10-May-1983; reference 2.
- Lower Hafren (Code B): Main Hafren channel; Podzol/Gley; 50% Sitka spruce; phased felling/thinning since 1985; start 10-May-1983; reference 4.
- Rainfall (Code C): Near Carreg Wen meteorological site; peat soil; acid moorland; rough sheep grazing; start 10-May-1983; reference 1.
- Tanllwyth (Code K) and Tanllwyth Bridge (AD): Main Tanllwyth channel near borehole; mixed Podzol/Gley soils; plantation forestry; sampling 1991–2006; reference 7.
- Vyrnwy-related data (Codes AA, Y, Z, etc.): Rainfall/streams/boreholes in Dyfnant Forest; Brown Earth soils; plantation Sitka spruce; sampling 1994–2001; reference 10.
- Ephemeral streams and stands of different catchment areas (e.g., South East 1, South East 3, Valley Bottom 1) with associated boreholes and chloride measurements; details include land management practices and start/end dates.

## References
- Reference set (REF. NUMBER 1–10) documents key hydrochemical and hydrological studies, including:
  - Rainfall, cloud water, and throughfall studies
  - Impacts of conifer harvesting on stream water quality
  - Hydrology and water quality of headwaters and plantation forestry interactions
  - Groundwater occurrence and geology
  - Nitrogen, chloride, and total dissolved nitrogen analyses in rainfall, streamwater, and groundwater
- Notable sources: Wilkinson et al. 1997; Neal et al. 1997, 2003, 2004, 2010; Kirchner & Neal 2000; Neal et al. 2004; Neal et al. 2004 (Tanllwyth); Neal et al. 2004 (Tanllwyth); Neal et al. 2004 (Vyrnwy); and related works.

## Drainage areas and stream flow conversion
- Reported catchment areas (sq. km):
  - Lower Hore (A): 3.172
  - Upper Hore (D): 1.62
  - Tanllwyth (K): 0.916
  - Lower Hafren (B): 3.58
  - Upper Hafren (G): 1.22
  - Note: Upper Hafren drainage area is 122 ha to flow gauging structure and 117 ha to chemistry sampling point
- Flow conversion formulas:
  - Convert Cumecs to mm/15 min: mm/15min = Cumecs × 0.9 ÷ catchment_area_km2
  - Convert mm/15 min to Cumecs: Cumecs = mm/15min × catchment_area_km2 ÷ 0.9

## GIS usage implications
- Use site codes to join per-site attributes to spatial features (points/lines) on a map.
- Ensure coordinate systems are consistent (Lat/Lon WGS84 and local grid) when integrating easting/northing with lat/long.
- Apply the catchment-area-based flow conversions for hydrological modelling and time-series analyses.
- Leverage start/end dates to build time-enabled GIS layers capturing land management actions (e.g., clearfell, thinning) and sampling periods.
- Link to bibliographic references to contextualize hydrochemistry and hydrology findings for each site.