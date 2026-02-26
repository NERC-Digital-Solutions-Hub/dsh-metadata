# Data overview:

- This data resource provides high-resolution aerial imagery (0.2 m spatial resolution) of two riverscapes in the Philippines, captured in 2019 and 2020 to enable multitemporal change identification and support tropical river management applications.

## Scope and purpose
- Multi-temporal orthoimagery for two river segments to identify changes over time and support river management decisions.

## Survey areas and timing
- Locations on Luzon island:
  - Bislak River downstream segment
  - Confluence of Abuan, Bintacan, and Pinacanauan de Ilagan (referred to as Ilagan)
- Segments are prone to hydrometeorological hazards like flooding and bank migration.
- Aerial surveys coordinated to capture low-flow conditions and minimize cloud shadow/sun-glint.

## Data collection and instrumentation
- Sensor suite: ALTM Pegasus LIDAR system with a D8900 aerial camera.
- Platform: Cessna T206H RP-C9122.
- Flight planning: survey blocks flown at 750–800 m above ground level (AGL) with 20–40% line overlap.
- Survey dates:
  - Bislak: 21 March 2019 and 22 January 2020
  - Ilagan: 5 April 2019 and 14 February 2020

## Aerial image processing workflow
- Colour corrections to improve overall quality (Capture One and Adobe Lightroom): RGB balance, intensity, saturation, contrast; outputs TIFF 8-bit.
- Rectification workflow (TerraPhoto) involving:
  - Tie-point definition: 5–10 images per scene, at least 5 points per image.
  - Colour points and selection shapes to refine alignment and rectification.
  - Triangulated correction model using colour points; correction polygons via selection shapes.
- Output: a single RGB orthomosaic with 0.20 m spatial resolution (WGS 84/UTM Zone 51N).

## Data characteristics
- Pixel values for RGB bands are scaled from 0 to 255.

## Data structure and files
- Bislak_2019: Bislak_2019_Orthoimagery_20cm.tif — Bislak river segment, 21 March 2019
- Bislak_2020: Bislak_2020_Orthoimagery_20cm.tif — Bislak river segment, 22 January 2020
- Ilagan_2019: Ilagan_2019_Orthoimagery_20cm.tif — Ilagan river segment, 5 April 2019
- Ilagan_2020: Ilagan_2020_Orthoimagery_20cm.tif — Ilagan river segment, 14 February 2020

## Quality control
- Positional accuracy and other quality checks performed by a third party responsible for the aerial surveys.

## Potential applications and uses
- Multitemporal change detection and monitoring of river dynamics.
- Support for tropical river management, planning, hazard assessment, and related analyses.
- Provision of self-serve data products for researchers and practitioners working with riverine environments.