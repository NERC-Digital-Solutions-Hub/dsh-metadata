# Vegetation data from the South Fork McKenzie River in Oregon, USA.

## Overview
- Purpose: Assess vegetation response to wildfire in restored and unrestored sites.
- Location: South Fork McKenzie River, Oregon (Lat/Long 44.17, -122.30).
- Data type and scope: Monitoring data comprising 4 separate CSV files capturing coordinates, species-level data, ground cover, and canopy density.
- Collected and interpreted by: Andrès Holz, Krista Farris, Bobette Jones, Upekala Wijayratne; interpretation by all authors.
- Collection date: June 2021.
- Dataset size: 88.66 KB.
- Access and storage: Data collected to standardized procedures, digitized from field sheets, double-checked prior to upload, and stored/uploaded to appropriate portals.

## Data structure and files
- Four CSV files:
  - SFMR_Veg_Coordinates: Transect, Quad, Lat, Long.
  - SFMR_Veg_Species: Transect, Site, Quad, Treatment, Initials, Species.name, Cover.Class, Cover.2, Comments, Category, Family, Duration, Growth_Habit, Native_Status.
  - SFMR_Veg_Ground: Transect, Quad, Type, Cover_Class, Cover_class_pct.
  - SFMR_Veg_Canopy: Transect, Quad, Measurement, Densiom.
- Dataset identifiers and coding:
  - Treatments: restored.burned, unrestored.burned, unrestored.unburned (reference site at Horse Creek to the East).
  - Cover data: Braun-Blanquet scale (0.1 to 5); converted to percent cover in dedicated columns (Cover.2 and Cover_class_pct).
  - Taxa: Identified to genus/unclear (40 taxa) and to species (29 taxa); total taxonomic units = 69.
  - Canopy: Densiometer readings reflect canopy density as a percentage unoccupied by vegetation.

## Collection methodology
- Survey design: 20 quadrats of 1x1 m.
- Abundance estimation: Braun-Blanquet method (percent cover approximations).
- Quadrat distribution:
  - 8 quadrats along transects 1 and 2 in the restored/burned treatment.
  - 4 paired quadrats with soil data.
  - 4 quadrats paired with soils sampling locations in the unrestored/degraded/burned treatment.
  - 3 quadrats in the unburned/non-degraded (reference) treatment.

## Variables and datasets
- SFMR_Veg_Coordinates: Location data per quadrat (Transect, Quad, Lat, Long).
- SFMR_Veg_Species: Species-level data per quadrat including taxonomy, growth habit, native status, treatment, collector initials, and Braun-Blanquet cover classifications (with a converted percent cover column and contextual notes).
- SFMR_Veg_Ground: Ground cover categories per quadrat (type such as leaf litter, bare ground, moss, log) with Braun-Blanquet cover and percent cover.
- SFMR_Veg_Canopy: Canopy measurements per quadrat per cardinal direction (North/East/South/West) with canopy density readings.

## Quality control and standards
- Field collection followed standardized procedures by trained fieldworkers.
- Data digitized from field sheets and double-checked prior to upload to ensure reliability for comparative analysis and monitoring over time.