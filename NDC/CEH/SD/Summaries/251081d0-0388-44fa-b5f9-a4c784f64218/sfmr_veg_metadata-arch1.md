# Vegetation data from the South Fork McKenzie River in Oregon, USA.

## Overview
- Data type: Monitoring data collected June 2021; size 88.66 KB.
- Location: Latitude 44.17, Longitude -122.30.
- Purpose: Assess vegetation response to wildfire in restored and unrestored sites.
- Collection and interpretation: Collected by Andrès Holz, Krista Farris, Bobette Jones, Upekala Wijayratne; interpreted by all authors.
- Data structure: Four CSV files providing coordinates, species-level data, ground cover, and canopy measurements.

## Data structure and contents
- SFMR_Veg_Coordinates: Transect, Quad, Lat, Long.
- SFMR_Veg_Species: Transect, Site, Quad, Treatment, Initials, Species.name, Cover.Class, Cover.2, Comments, Category, Family, Duration, Growth_Habit, Native_Status; includes Cover.Class.pct (percent cover) and taxonomy details; total taxonomic units = 69 (40 genus/unclear, 29 species).
- SFMR_Veg_Ground: Transect, Quad, Type, Cover_Class, Cover_class_pct (ground vegetation cover categories and percent).
- SFMR_Veg_Canopy: Transect, Quad, Measurement (North=1, East=2, South=3, West=4; decimals indicate off-cardinal points), Densiom (canopy density reading as percent unoccupied by vegetation).

## Measurements and scales
- Abundance/cover: Braun-Blanquet scale (0.1 to 5) converted to percent cover (Cover.Class.pct).
- Canopy: Densiometer readings indicating canopy unoccupied by vegetation (%).

## Collection methodology and sampling design
- Sampling design: 20 (1x1) quadrats total.
- Distribution: 8 quadrats along transects 1 and 2 in restored/burned treatment; 4 paired quadrats with soil data; 4 quadrats paired with soils sampling locations in unrestored/degraded/burned treatment; 3 quadrats in unburned/non-degraded treatment.
- Sampling period: June 2021.
- Coordinates and quadrat mapping: Each site/quadrat identified by Transect, Site, Quad; coordinates in SFMR_Veg_Coordinates.

## Treatments and site context
- Treatments represented in data: restored.burned, unrestored.burned, unrestored.unburned.
- Study context: Vegetation response to wildfire across restored vs unrestored sites, with reference site at Horse Creek to the East.

## Data quality and provenance
- Data collection followed standardized procedures by trained fieldworkers.
- Data digitized from field survey sheets and double-checked prior to upload.

## Potential analyses and use cases
- Compare vegetation composition, functional traits (Growth_Habit, Native_Status), and taxonomic diversity across treatments.
- Analyze relationships between species-level cover (Braun-Blanquet to percent) and canopy cover (Densiom) to infer light-availability effects post-fire.
- Integrate with soil data (paired quadrats) for habitat and wildfire impact analyses.
- Use coordinates and transect structure to map spatial patterns or reuse in broader regional vegetation assessments.