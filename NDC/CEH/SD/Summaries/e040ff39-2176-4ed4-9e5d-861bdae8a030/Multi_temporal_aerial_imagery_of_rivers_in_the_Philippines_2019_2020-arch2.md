# Data overview

- High-resolution aerial imagery (0.2 m spatial resolution) of two riverscapes in the Philippines
- Collected in 2019 and 2020 to identify multitemporal changes; useful for tropical river management applications

- Aerial surveys
  - Two river segments on Luzon: downstream Bislak River and the confluence of Abuan, Bintacan, and Pinacanauan de Ilagan (Ilagan)
  - Sites susceptible to hydrometeorological hazards: river flooding and bank migration
  - Equipment: ALTM Pegasus LiDAR system with D8900 aerial camera on a Cessna T206H (RP-C9122)
  - Flight design: blocks flown at 750–800 m above ground level (AGL) with 20–40% line overlap
  - Survey dates: Bislak 21 March 2019; Bislak 22 January 2020; Ilagan 5 April 2019; Ilagan 14 February 2020
  - Timing intended to coincide with low-flow conditions and minimize cloud shadow/sun-glint

- Aerial image processing
  - Steps: colour corrections, tie-point definition, colour points and selection shapes, rectification
  - Colour corrections performed with Capture One and Adobe Lightroom; outputs TIFF 8-bit
  - Tie-points: 5–10 images per area, at least 5 points per image for alignment
  - Colour points create a triangulated correction model; selection shapes refine corrections
  - Rectification yields a single RGB image with 0.20 m resolution
  - Coordinate system: WGS 84 / UTM Zone 51N

- Nature and units of recorded values
  - Pixel values scaled 0–255 for RGB bands

- Quality control
  - Positional accuracy verified by the third-party responsible for the aerial surveys

- Data structure (files and descriptions)
  - Bislak_2019: Bislak_2019_Orthoimagery_20cm.tif — Orthoimagery for Bislak segment from 21 March 2019
  - Bislak_2020: Bislak_2020_Orthoimagery_20cm.tif — Orthoimagery for Bislak segment from 22 January 2020
  - Ilagan_2019: Ilagan_2019_Orthoimagery_20cm.tif — Orthoimagery for Ilagan segment from 5 April 2019
  - Ilagan_2020: Ilagan_2020_Orthoimagery_20cm.tif — Orthoimagery for Ilagan segment from 14 February 2020

- Relevance for environmental monitoring
  - Provides standardized, multi-temporal spatial data for assessing riverine environmental health and changes over time
  - Datasets can enhance monitoring outputs (maps, charts) and be integrated with other data sources
  - Quality assurance and clear data structure support storage and portal dissemination for broader access