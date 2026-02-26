# DRAINAGE AREAS AND STREAM FLOW CONVERSION

- Purpose of the document
  - A dataset catalog detailing hydrological and hydrochemical measurements across multiple catchments in mid-Wales (e.g., Hafren, Hore, Tanllwyth, Vyrnwy) to study river hydrochemistry, forestry impacts, and related processes.
  - Data are intended to support data exploration, combination, analysis, and the creation of accessible data products (dashboards, reports) for end users.

- Key datasets and data types
  - River and watershed measurements:
    - Discharge/stream flow at various sites (e.g., Tanllwyth flume, Hafren streams, Tanllwyth). Includes both permanent gauges and experimental sites.
  - Meteorological and chemical measurements:
    - Rainfall and daily chloride data (Lower Hafren daily chloride; Daily rainfall chloride; Tanllwyth daily chloride).
    - Throughfall and stemflow samples (throughfall & stemflow at Hafren region; associated boreholes).
    - Total dissolved nitrogen (Carreg Wen total dissolved nitrogen; rainfall-related measurements).
  - Groundwater and borehole data:
    - Exploratory boreholes across Hafren (upper, lower slopes, valley bottom), with associated soils, vegetation, and land management metadata.
  - Site-specific descriptors:
    - Location codes, coordinates (E/N, latitude/longitude in WGS84), altitude, descriptions of catchment features, soil types, vegetation, land management, and mining history.
  - Time coverage and structure:
    - Start dates around 1983–1994 for many sites, with ongoing or end dates noted; some time series include borehole-related adjustments (noted around 7 March 1995).

- Spatial and temporal scope
  - Catchments and sites include: Lower Hore (A), Upper Hore (D), Tanllwyth (K), Lower Hafren (B), Upper Hafren (G), Rainfall (C), Vyrnwy rainfall/streams (AA–Z), and multiple boreholes and slope sites (LS1–LS4, US1–US3, VB1, etc.).
  - Each site provides precise easting/northing and latitude/longitude coordinates (WGS84), with site-specific descriptions of drainage area, soils, and vegetation.
  - Catchment areas (for flow conversion) include: Lower Hore 3.172 sq km, Upper Hore 1.62 sq km, Tanllwyth 0.916 sq km, Lower Hafren 3.58 sq km, Upper Hafren 1.22 sq km.

- Data structure, metadata, and references
  - Consistent metadata fields per site: location code, coordinates, altitude, description, main soil types, vegetation, land management, mining, start/end dates, and primary reference numbers.
  - References (REF. NUMBER 1–10) correspond to published hydrology/hydrochemistry studies detailing the dataset’s context and findings.
  - Documentation includes notes on data provenance, potential data quality issues (e.g., borehole effects on Tanllwyth time series after 7-Mar-1995), and data usage guidance.

- Data quality and challenges
  - Time spent understanding the “ask” due to data being distributed across teams and formats.
  - Patchy data availability and data in diverse formats across multiple systems.
  - Communication of complex hydrochemical and hydrological information in accessible terms.
  - Ensuring outputs are widely shared and reused; promoting outputs for broader data use.

- Data conversion and units
  - Flow conversions:
    - From cumecs to mm/15min: mm/15min = cumecs × 0.9 / catchment_area_km2
    - From mm/15min to cumecs: cumecs = mm/15min × catchment_area_km2 / 0.9

- Usage and outputs for data support
  - Create self-serve data products (dashboards, pivot tables, charts) enabling end users to explore hydrochemistry, rainfall, and discharge data.
  - Combine and compare datasets (e.g., discharge vs. rainfall vs. chloride) to assess impacts of land management changes (e.g., forestry harvesting, thinning, clearfell events).
  - Provide guidance on tool usage and promote outputs; incorporate feedback to refine products.
  - Support policy and planning tasks in organizations with broader, non-specialist remits (e.g., local councils, private companies).