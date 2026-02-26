# Data overview

- This data resource contains high-resolution aerial imagery (0.2 m spatial resolution) of two riverscapes in the Philippines, collected in 2019 and 2020 to enable multitemporal change detection and support tropical river management applications.

## Study area and scope
- Two river segments on Luzon island, Philippines:
  - Downstream segment of the Bislak River
  - Confluence of the Abuan, Bintacan, and Pinacanauan de Ilagan Rivers (Ilagan)
- Sites are susceptible to hydrometeorological hazards such as river flooding and bank migration.

## Aerial surveys
- Equipment: ALTM Pegasus LIDAR system with a D8900 aerial camera, mounted on a Cessna T206H (RP-C9122).
- Survey design: flight blocks at 750–800 m above ground level (AGL) with 20–40% overlap along flight lines.
- Survey dates:
  - Bislak: 21 March 2019 and 22 January 2020
  - Ilagan: 5 April 2019 and 14 February 2020
- Timing aimed to maximize data quality under low-flow conditions and minimize cloud shadow and sun-glint.

## Aerial image processing
- Processing steps to produce orthoimagery:
  - Colour corrections to improve overall colour quality
  - Tie-point definition (5–10 images, at least 5 points per image)
  - Colour points and selection shapes for correction and rectification
  - Rectification to generate a single RGB image
- Output and format:
  - TIFF images (8-bit) with 0.20 m spatial resolution
  - Coordinate system: WGS 84 / UTM Zone 51N
- Software used: Capture One and Adobe Lightroom for colour corrections; TerraPhoto for tie-points and rectification.

## Nature and units of recorded values
- Imagery values are scaled between 0 and 255 for the red, green, and blue (RGB) bands.

## Quality control
- Positional accuracy of the orthoimagery was checked and verified by the third-party organization responsible for the aerial surveys.

## Data structure and access
- Four orthoimagery files with descriptions:
  - Bislak_2019: Bislak_2019_Orthoimagery_20cm.tif — Orthoimagery for Bislak river segment, 21 March 2019
  - Bislak_2020: Bislak_2020_Orthoimagery_20cm.tif — Orthoimagery for Bislak river segment, 22 January 2020
  - Ilagan_2019: Ilagan_2019_Orthoimagery_20cm.tif — Orthoimagery for Ilagan river segment, 5 April 2019
  - Ilagan_2020: Ilagan_2020_Orthoimagery_20cm.tif — Orthoimagery for Ilagan river segment, 14 February 2020

## Relevance for monitoring frameworks
- Provides high-resolution, multi-temporal spatial data suitable for monitoring river dynamics, flood risk, and bank migration.
- Transparent processing workflow and QA by a third party enhance data reliability for policy evaluation, planning, and decision-making.
- Standardized data products (orthoimagery with explicit metadata such as resolution, coordinate system, and file naming) support reproducibility and integration into monitoring dashboards, reports, or governance datasets.

## Considerations for use in monitoring
- Scope limited to two river segments; may require additional data to generalize across broader basins.
- Metadata includes key technical details (resolution, projection, processing steps), but users may need access provisions or data-sharing arrangements not specified in this summary.