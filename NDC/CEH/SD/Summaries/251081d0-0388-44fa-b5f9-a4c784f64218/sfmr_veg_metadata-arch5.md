# Vegetation data from the South Fork McKenzie River in Oregon, USA.

## Overview
- Purpose: Monitoring to assess vegetation response to wildfire in restored and unrestored sites.
- Location: South Fork McKenzie River, Oregon; coordinates lat/long 44.17, -122.30.
- Size: 88.66 KB.
- Collected by: Andrès Holz, Krista Farris, Bobette Jones, Upekala Wijayratne.
- Collected in: June 2021.
- Dataset scope: 20 quadrats across transects with treatments including restored.burned, unrestored.burned, and unrestored.unburned (reference site).
- Taxonomic scope: 69 total taxonomic units; 40 identified to genus/unclear, 29 to species.
- Collection purpose emphasis: Vegetation response to wildfire within different restoration contexts.

## Data content and structure
- The dataset comprises four separate CSV files:
  1) SFMR_Veg_Coordinates
     - Columns: Transect, Quad, Lat, Long.
  2) SFMR_Veg_Species
     - Columns: Transect, Site, Quad, Treatment, Initials, Species.name, Cover.Class, Cover.2, Comments, Category, Family, Duration, Growth_Habit, Native_Status.
     - Notes: Species names; Cover.Class uses Braun-Blanquet scale; Cover.Class.pct converts to percent cover; includes provenance fields (Transect, Site, Quad) and collection initials.
     - Taxa: 69 total; 40 identified to genus/unclear; 29 identified to species.
  3) SFMR_Veg_Ground
     - Columns: Transect, Quad, Type, Cover_Class, Cover_class_pct.
  4) SFMR_Veg_Canopy
     - Columns: Transect, Quad, Measurement, Densiom.
     - Measurement codes: North=1, East=2, South=3, West=4 (decimal values allowed for off-cardinal points).
- Metadata and fields provide: location, treatment, collector initials, taxonomic classification, abundance/cover metrics, ground cover types, and canopy density readings.

## Collection methodology and sampling design
- Standardized field procedures followed; trained fieldworkers collected data.
- Abundance/cover measured using Braun-Blanquet method (converted to percent cover in the dataset).
- Sampling design: 20 quadrats distributed across transects 1 and 2 with various pairings:
  - 8 quadrats in restored.burned treatment.
  - 4 paired quadrats with soil data.
  - 4 quadrats paired with soils sampling locations in unrestored/degraded/burned treatment.
  - 3 quadrats in unburned/non-degraded (reference) treatment.

## Data quality, provenance, and governance
- Quality control: Data digitized from field survey sheets and double-checked prior to upload.
- Provenance: Explicit collection dates, collector initials, and site/treatment designations to support reproducibility and lineage.
- Documentation alignment: Dataset structure and field definitions clearly described to enable interpretation and reuse.
- Intended dissemination: Dataset described for upload to relevant data portals and catalogues, with clear metadata to aid discoverability and governance.

## Governance and stewardship considerations
- Data standards: Metadata and field schemas (coordinates, species data, ground and canopy measures) align with consistent data governance practices for handling multi-file vegetation datasets.
- Metadata richness: Includes taxonomy, growth form, native status, treatment context, and sampling design to support data discovery, filtering, and comparative analyses.
- Availability and updates: Clear record of methodology and structure facilitates future updates or integration with related restoration/wildfire vegetation datasets.
- Documentation needs: Consider adding data rights/licensing, versioning, and data custodians to support long-term stewardship and controlled sharing across portals.