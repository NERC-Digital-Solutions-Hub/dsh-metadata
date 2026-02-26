# Site_Cod

## Overview
- A dataset listing site codes (CCxx) with corresponding site names and their spatial coordinates (Easting and g, likely Northing) for a collection of hydrological features in North Wales, centered around Conwy. 
- Includes a mix of rivers, streams, bridges, lakes, harbours, and multicomponent site records.

## Data structure and content
- Core fields:
  - Site_Cod (e.g., CC51, CC54, CC11)
  - Site name (e.g., Master_Site Aber Las, Afon Cadnant, Conwy Harbour)
  - Easting (numeric)
  - g (likely Northing; numeric)
- Some site codes have multiple parts (e.g., CC66, 1/2/3; CC69, 1/2/3), indicating multiple coordinates or sub-features within a single site.
- Several entries have missing coordinates (e.g., CC16 with no Easting or Northing values), suggesting incomplete data.
- The coordinates fall in ranges typical of the OSGB36 grid (Easting ~ 270k–290k; Northing ~ 340k–380k).
- Notable feature types represented include major sites, rivers/streams (e.g., Afon Ddu, Afon Nug, Afon Oernant), lakes/areas (e.g., Llyn Conwy), bridges/sections (e.g., Tal-y-Cafn bridge, Conwy Harbour), and tributaries.

## Notable patterns and examples
- Examples of entries:
  - CC51, Master_Site Aber Las: Easting 277900, Northing 344500
  - CC54, Afon Cadnant: Easting 286200, Northing 354600
  - CC11, Afon Ddu Lower: Easting 277560, Northing 344880
  - CC15, Conwy Harbour: Easting 278400, Northing 377500
  - CC16, Llyn Conwy: Easting and Northing missing in current data
- Some sites have multiple parts (e.g., CC66 with 1/2/3; CC62/63 for Pont Eidda Stream segments), indicating complex geometries or segmented measurement points.
- A mix of named water features and man-made references (bridges, tribs) within the Conwy catchment.

## Data quality and gaps
- Missing values:
  - Several entries lack Easting and/or Northing (e.g., CC16; some CC66/CC69 parts may be partial).
- Inconsistent formatting:
  - Some lines list multiple attributes in compact form (e.g., “CC66, 1 = Nant Genneth. CC66, 2 = 282100. CC66, 3 = 372600.”)
- Data normalization needed:
  - Normalize field names (e.g., rename g to Northing) and ensure consistent numeric types.
  - Resolve multi-part records into a usable GIS structure (single feature with multi-part geometry or separate point features).

## GIS workflows and deliverables
- Suggested data preparation:
  - Clean and convert to a consistent schema: Site_Cod, Name, Easting, Northing.
  - Address missing coordinates (imputation where appropriate or flag as incomplete).
  - Expand multi-part entries into separate geometry records or multi-part features.
  - Standardize coordinate reference system (likely OSGB36) and project to required CRS for mapping.
- Potential layers:
  - Site_points: point features for each coordinate (or multi-part features per site).
  - Site_parts: separate features for each part of a multi-part site (if keeping granularity).
- Deliverables:
  - Clean CSV/GeoPackage/GeoJSON with metadata.
  - Map visuals showing key hydrological features, with attribution to CC codes and names.
  - Documentation of data gaps and data quality notes.

## Use cases for GIS Specialists
- Build map-based data products to help policy colleagues, clients, and the public explore hydrological features in North Wales.
- Integrate with broader GIS analyses (watershed delineation, stream network mapping, accessibility studies).
- Iterate on data quality through prototype maps and stakeholder feedback to improve usability and accuracy.