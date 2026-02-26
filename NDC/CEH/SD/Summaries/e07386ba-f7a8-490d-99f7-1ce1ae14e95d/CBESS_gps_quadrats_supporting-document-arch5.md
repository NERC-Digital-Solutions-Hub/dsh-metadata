# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) global positioning system (GPS) locations of quadrats in saltmarsh and mudflat habitats

## Overview
- GPS locations and elevations for instruments and features associated with CBESS wave monitoring and sedimentation/erosion monitoring installations.
- Staff responsible: Tom Spencer, Ben Evans.
- Dataset comprises survey quadrat locations across six UK sites (three in Essex, three in Morecambe Bay) representing saltmarsh and adjacent mudflat habitats.

## Spatial and site details
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Habitat types: Saltmarsh and Mudflat.
- Soil/habitat contrasts:
  - Essex: clay soils (saltmarsh) with differing inundation, creek structure, and vegetation.
  - Morecambe Bay: sandy soils (saltmarsh).
  - Mudflat contrasts: cohesive clays/mud/silt in Essex vs coarse, mobile sediments in Morecambe Bay.

## Data collection and timing
- Observations collected within two weeks prior to or during CBESS main sampling campaigns in Winter and Summer 2013.
- Each site comprises 22 quadrats on the unvegetated mudflat and 22 quadrats on the salt marsh (total per site: 44 quadrats; 6 sites across two habitats).

## Variables and measurements
- Primary variables: Northing, Easting, Elevation (relative to Ordnance Datum Newlyn).
- Quadrats: 1 m square, oriented north-south and east-west; southeast corner coordinates recorded.

## Methods and data handling
- GPS equipment: Leica GS08 GNSS system with real-time Leica RTK corrections (calibration in real time).
- Coordinate system: OSGB1936(2) for Northings/Eastings; elevation relative to OD Newlyn.
- Data recording: GPS locations and elevations; two-site documentation categories with field descriptions.
- Data processing: Data exported in ASCII text; unnecessary/duplicate points removed in MS Excel; no additional data transformations performed.
- Quality checks: 50 mm 3D coordinate quality threshold applied (points outside this threshold rejected).

## Data structure and metadata
- Dataset fields include: Season (Winter/W), Site (Morecambe or Essex; specific site codes), Habitat (Mudflat or Saltmarsh), Quadrat number (1–22), Scale (A-D for location granularity: A=1m, B=1–10m, C=10–100m, D=upper limit), Easting, Northing, Elevation, and related header/row formatting guidance.
- NA values indicate measurements or steps that were not performed (e.g., certain data checks or processing steps).

## Access, updates, and stewardship notes
- Data are location-based observations tied to specific CBESS monitoring installations; no explicit update schedule or embargo details provided.
- Documentation includes standard metadata for data stewards: provenance (staff, sites, instruments), measurement procedures, data formats (ASCII), and quality thresholds to support discovery, reuse, and interoperability.

## Key considerations for data governance
- Ensure consistent use of OSGB1936(2) coordinates and elevation reference across all sites.
- Maintain the documented 50 mm quality filter and Leica RTK calibration approach for reproducibility.
- Preserve the original unprocessed state where noted (no post-processing beyond basic cleanup in Excel) to support traceability.
- Retain site and habitat context (Essex vs Morecambe Bay; saltmarsh vs mudflat) to enable comparative analyses.
- Capture metadata on any future updates or reprocessing to sustain data discoverability and usability.