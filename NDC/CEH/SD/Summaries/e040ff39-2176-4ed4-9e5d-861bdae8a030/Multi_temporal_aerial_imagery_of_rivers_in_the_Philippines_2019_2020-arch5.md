# Data overview

- The resource provides high-resolution aerial imagery (0.20 m spatial resolution) of two riverscapes in the Philippines, collected in 2019 and 2020 to enable multitemporal change detection and support tropical river management applications.

## Location and scope

- Sites are on Luzon island:
  - Bislak River downstream segment
  - Confluence of Abuan, Bintacan, and Pinacanauan de Ilagan Rivers (Ilagan)
- Both segments are prone to hydrometeorological hazards such as river flooding and bank migration.

## Data collection

- Platform and sensors: ALTM Pegasus LIDAR system with a D8900 aerial camera, mounted on a Cessna T206H RP-C9122.
- Flight plan: sites divided into blocks; flown at 750–800 m above ground level (AGL) with 20–40% overlap along flight lines.
- Temporal coverage: surveys conducted on specific dates to capture low-flow conditions and minimize cloud shadow/sun-glint.
  - Bislak: 21 March 2019 and 22 January 2020
  - Ilagan: 5 April 2019 and 14 February 2020

## Image processing and standardization

- Processing goals: produce spatially corrected orthoimagery.
- Key steps:
  - Color corrections using Capture One and Adobe Lightroom (RGB balance, intensity, saturation, contrast).
  - Output TIFFs (8-bit).
  - Tie-point definition (5–10 images per set, at least 5 points per image) to recompute alignment.
  - Color points and selection shapes to improve rectification; triangulated color-point correction model; correction polygons for selection shapes.
  - Rectification yields a single RGB image with 0.20 m resolution, using WGS 84/UTM Zone 51N.
- Recorded value scale: RGB bands use 0–255.

## Data structure and availability

- Orthomosaic files:
  - Bislak_2019_Orthoimagery_20cm.tif — Orthoimagery for Bislak river segment, 21 March 2019
  - Bislak_2020_Orthoimagery_20cm.tif — Orthoimagery for Bislak river segment, 22 January 2020
  - Ilagan_2019_Orthoimagery_20cm.tif — Orthoimagery for Ilagan river segment, 5 April 2019
  - Ilagan_2020_Orthoimagery_20cm.tif — Orthoimagery for Ilagan river segment, 14 February 2020

## Quality and provenance

- Positional accuracy validated by a third-party survey provider.
- Metadata includes file names and descriptions for dataset provenance and traceability.

## Usage considerations for data stewards

- The dataset supports multitemporal analysis for river management decisions; ensure users understand the low-flow-condition context of the imagery.
- Formats are TIFF/orthomosaic with consistent 0.20 m resolution and standard coordinate system (WGS 84 / UTM Zone 51N).
- Processing involved multiple software tools; consider providing or linking a reproducible processing workflow for future updates or extensions.
- Large file sizes may require robust data transfer and storage solutions; plan for updates if new imagery is collected.