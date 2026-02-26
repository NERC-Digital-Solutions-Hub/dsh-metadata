# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) GPS locations of quadrats in saltmarsh and mudflat habitats

## Overview
- Provides GPS locations and elevations for instruments and features associated with CBESS wave monitoring and sedimentation/erosion monitoring installations.
- Cover six UK sites (Essex and Morecambe Bay) representing saltmarsh and mudflat habitats with contrasting sediment and soil types.
- Data collection aligned with main CBESS campaigns in Winter and Summer 2013.

## Data scope and sites
- Locations: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands, West Plain).
- Site descriptions: Essex and Morecambe Bay saltmarsh chosen to represent contrasting soil types (clay in Essex; sandy in Morecambe Bay) and differing inundation frequency, creek structure, and vegetation. Mudflat sites differ in sediment (Essex: cohesive clays/mud/silt; Morecambe Bay: coarse, mobile sediments).
- Observations include GPS locations and elevations for survey quadrats associated with monitoring installations.

## Sampling design
- Each site comprises 22 quadrats on unvegetated mudflat and 22 quadrats on salt marsh (total 44 per site).
- Quadrats are 1 m by 1 m, located at the south-east corner, oriented North-South and East-West.

## Variables and observations
- Primary coordinates: Northing, Easting, Elevation (relative to Ordnance Datum Newlyn).
- Time reference: Recordings taken within two weeks prior to or during Winter and Summer 2013 campaigns.
- Associated projects: CBESS_wave_monitoring and CBESS_sedimentation_erosion installations.

## Data collection and processing
- Instrumentation: Leica GS08 GNSS system with real-time Leica RTK corrections.
- Coordinate system: OSGB1936(2); elevations relative to OD Newlyn.
- Data handling: Data exported in ASCII text; unnecessary/duplicate points removed in MS Excel; no further processing reported.

## Dataset structure and fields
- Core fields include: Site (Essex or Morecambe with specific site codes CS, WS, WP for Morecambe; AH, FW, TM for Essex), Habitat (Saltmarsh or Mudflat), Quadrat (1–22 per site), Scale (A=1 m; B=1–10 m; C=10–100 m; D=upper limit), Easting, Northing, Elevation, Season (Winter or Summer).
- Header and row metadata described; NA values indicate measurements not performed.
- Dataset records GPS locations for six saltmarsh/mudflat sites, with the per-site quadrat structure noted above.

## Quality, provenance, and access
- Staff: Tom Spencer, Ben Evans.
- Data quality: Coordinate quality check threshold set at 50 mm; points above threshold rejected.
- Data provenance: Unprocessed raw GPS locations with minimal transformation; linked to CBESS wave and sedimentation monitoring datasets.
- Usage notes: Data may be used for spatial analyses of habitat characteristics, site comparisons, and integration with CBESS-related monitoring data.