# Lower Hore, LOCATION CODE = A.

## Overview
- A metadata dataset describing multiple hydrology, meteorology, and water-quality sites in the Hafren/Hore catchments, with detailed site-level attributes and cross-site references.
- For each site, records include precise coordinates (Easting/Northing, Latitude/Longitude in WGS84), altitude, physical description, soils, vegetation, land management, mining history, time span (start date to end date, with some ongoing indicated as Cont..), and a primary reference number linking to published sources.
- Data types covered include stream channel measurements, rainfall and rainfall-related analyses, throughfall, stemflow, groundwater, chlorides, total dissolved nitrogen, and borehole data; some sites have borehole effects noted.
- A set of drainage-area definitions and flow-conversion formulas is provided for converting between cumecs and rainfall-derived flow measurements, tied to specific site catchment areas.

## Dataset structure and metadata fields
- Site-level fields present for each entry:
  - Location code, Easting, Northing
  - Latitude/Longitude (WGS84), Altitude (m)
  - Description of site (e.g., main stream channel above/below flumes, met site)
  - Main soil types, Vegetation, Land management
  - Mining history
  - Start date, End date (End date may be Cont..)
  - Primary reference number, Comments
- Multiple site categories are included (Lower Hore, Lower Hafren, Rainfall, Upper Hore, Stemflow, Throughfall, Tanllwyth, Vyrnwy-related sites, etc.), each with consistent metadata fields.
- Bibliographic linkage via Primary Reference Numbers (1–10) to published works listed under “REF. NUMBER” with full citations.

## Data content types
- Hydrological measurements and stream-related data, including discharge readings from flumes and boreholes.
- Meteorological and chemical data: rainfall, cloud water, daily chloride, total dissolved nitrogen.
- Ephemeral streams, boreholes across Hafren, and plots with standing crop or clearfelled land management notes.
- Groundwater studies and long-term time series notes, with caveats about borehole effects on certain records.

## Provenance and references
- Each site’s data is associated with a Primary Reference Number that maps to a bibliographic entry (numbers 1–10), covering studies on rainfall, cloud water, throughfall, stemflow, nutrient and chloride analyses, and hydrochemistry of the Severn headwaters.
- Detailed site notes include methodological and interpretive caveats (e.g., Tanllwyth borehole effects on samples, discharge readings at Tanllwyth flume).

## Spatial and temporal coverage
- Spatial: Coordinates provided in multiple formats (E,N; Latitude/Longitude in WGS84); sites reference major catchments (Lower Hore, Upper Hore, Tanllwyth, Lower Hafren, Upper Hafren).
- Temporal: Start dates around 1983–1994 for many components; end dates commonly 1999–2001 or ongoing; some datasets labeled Cont.. indicating continuing collection.
- Drainage areas and site-specific catchment areas are quantified for flow-conversion calculations.

## Drainage areas and flow conversion
- A dedicated section lists catchment areas (sq. km) for key sites:
  - Lower Hore (A) – 3.172
  - Upper Hore (D) – 1.62
  - Tanllwyth (K) – 0.916
  - Lower Hafren (B) – 3.58
  - Upper Hafren (G) – 1.22
- Upper Hafren drainage area note: 122 ha to flow gauging structure, 117 ha to chemistry sampling point.
- Flow unit conversions:
  - mm/15min to cumecs: cumecs = mm/15min × 0.9 / catchment_area_km2
  - cumecs to mm/15min: mm/15min = cumecs × catchment_area_km2 / 0.9

## Data quality and governance notes
- Site-specific quality concerns are documented where applicable (e.g., Tanllwyth samples after 7-Mar-1995 affected by borehole; guidance to use Tanllwyth data only up to that date for long-term series).
- Acknowledgement that datasets span different systems and formats and may require harmonization for integration.
- Some end dates are open-ended or marked Cont.., indicating ongoing data collection; metadata should reflect current status during publishing.

## Access, sharing, and maintenance recommendations
- The dataset is organized with clear site codes and primary references, facilitating discoverability and proper citation in data portals.
- Encourage embedding complete metadata per site, including exact coordinates, description, soils, vegetation, land management, borehole caveats, and data provenance notes.
- Maintain linkage between site entries and bibliographic references; preserve borehole notes and any site-specific data quality caveats in shared metadata.
- Include explicit data-update timelines and versioning when publishing to portals; document any data transformations (e.g., QA steps, cleaning, and transformations) applied prior to sharing.

## Data stewardship implications and actions
- Ensure metadata completeness and consistency across all sites, including coordinates, units, and tissue of metadata fields (soil types, vegetation, management, mining).
- Harmonize data formats and coordinate systems, preserving original values and adding standardized fields for interoperability.
- Capture and communicate data quality indicators and site-specific caveats (e.g., borehole effects, 1995 changes in Tanllwyth data).
- Maintain accurate provenance by preserving Primary Reference Numbers and corresponding citations; automate reference lookups where possible.
- Define clear data access policies and embargo handling if applicable; establish procedures for updating end dates and continuing records.
- Align with Data Stewards aims by adopting a publishing mindset to ensure datasets are discoverable, usable, and up to date, with appropriate governance and documentation.