# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) GPS locations of quadrats in saltmarsh and mudflat habitats

## Overview
- GPS locations and elevations for CBESS wave monitoring and sedimentation/erosion instruments ("CBESS_wave_monitoring", "CBESS_sedimentation_erosion").
- Staff: Tom Spencer, Ben Evans.
- Observations located at six UK sites: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands, West Plain).
- Sites chosen to represent contrasting habitats, sediment types, inundation frequency, creek structure, and vegetation.

## Dataset scope and sites
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Habitats: Saltmarsh and Mudflat. Essex saltmarshes on clay soils; Morecambe saltmarshes on sandy soils; mudflats with cohesive clays/sediments in Essex and coarser sediments in Morecambe Bay.
- Each site includes a saltmarsh area and an adjacent mudflat area.

## Sampling design and timing
- Each site comprises 22 quadrats on the unvegetated mudflat and 22 quadrats on the salt marsh (.total per site: 44 quadrats; across six sites, 264 quadrats).
- Quadrat size and orientation: 1 m x 1 m, south-east corner, sides aligned North-South and East-West.
- Spatio-temporal scope: Records collected within two weeks prior to or during the CBESS main campaigns in Winter and Summer 2013.

## Measurements and data handling
- Variables observed: Northing, Easting, Elevation.
- Coordinate system: OSGB1936(2); elevations relative to Ordnance Datum Newlyn.
- Instrumentation: Leica GS08 GNSS system; 3D coordinate quality check threshold of 50 mm (points outside rejected).
- Calibration: Leica RTK corrections applied in real-time where applicable.
- Processing: Data exported as ASCII text; unnecessary/duplicate points removed in MS Excel; no further processing documented.
- Data checks: Quality control procedures listed as NA in the metadata.

## Dataset structure and field descriptions
- Each entry includes: site, habitat (Saltmarsh or Mudflat), quadrat number (1–22), scale (A–D representing spatial context), Easting, Northing, Elevation (relative to OD Newlyn).
- Header/row metadata used to describe data organization; two entries indicated for certain fields (e.g., 1 and 2) with corresponding descriptions.

## Data quality and limitations
- Explicit GPS accuracy threshold (50 mm) applied.
- No subsequent processing beyond ASCII export; minimal quality control metadata (NA for several QC fields).
- Documentation covers site-level context, coordinate system, and sampling timing but lacks detailed QC procedures beyond the 50 mm threshold.

## Relevance for Data Leaders
- Demonstrates end-to-end geospatial data management across multiple sites with consistent field protocols.
- Emphasizes importance of clear metadata: site names, habitat types, coordinate system, elevation reference, and quadrat geometry.
- Highlights potential standardization needs: consistent data quality procedures, complete QC documentation, and unified data dictionaries across CBESS datasets.

## Practical actions and governance implications
- Standardize metadata vocabularies for site, habitat, and quadrat coding across datasets.
- Document and publish complete data quality checks and processing steps, including versioning and update cadence.
- Ensure alignment of coordinate reference systems and elevation references across datasets to improve discoverability and interoperability.
- Consider linking this metadata to a centralized CBESS data catalog to improve data discoverability for policy colleagues and external partners.