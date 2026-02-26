# Motion activated camera trap images from cameras located at the ECN Cairngorm long-term monitoring site 2010-2022

## Aim and Rationale
- PIR camera traps deployed to monitor fauna presence and grazing pressure in the ECN Cairngorm Allt a’Mharcaidh catchment.
- Data contribute to the National Biodiversity Network Gateway and are shared with NatureScot to support Invershie and Inshriach National Nature Reserve management.
- Outputs enable phenology insights and ecosystem service assessments; outputs may inform broader species and public-interest data sharing.

## Study Location and Data Collection
- Location: Allt a’Mharcaidh catchment, Cairngorms National Park, within Inverseshie and Inshriach NNR.
- Long-term monitoring by ECN; five camera traps (BR, PA, SN, TL, TR) along main wildlife/people routes.
- Recording period: 2010–2022.
- Camera placements across habitat types: pine plantation, mature Scots Pine woodland, pine regeneration, and riparian zone near a footbridge (highest activity).
- Data include both wildlife and human recreation, enabling ecological and ecosystem service analyses.

## Cameras and Setup
- Camera models used: initially Spypoint IR-B with solar panels; from 2013 onward, Bushnell Trophy Cam family variants.
- Trigger mechanism: passive infrared (PIR); typical trigger speed ~0.2 seconds.
- Field settings: 24/7 operation; single image per trigger with 10-second interval for continuous trigger; 3 pm daily timelapse image for phenology checks.
- Image properties: colour by day, black-and-white at night; maximum reliability with ground-level placement to capture small mammals/birds.
- Data handling: field downloads roughly every 4–6 weeks; clocks checked and synchronized; storage on Sandisk Ultra Class 4 SDHC cards; batteries typically last about a year.
- Data organization: images renamed with camera and timestamp; yearly and camera-based folder structure; 3 pm images stored separately for phenology.

## Data Processing Pipeline

### Initial Steps
- Rename and organize all images; separate 3 pm phenology images; flatten folder structure into a per-year camera-specific directory.

### Object Detection (pre-processing)
- Use Microsoft MegaDetector in Google Colab to identify imagery contents (empty, animal, person, vehicle).
- Outputs a JSON per year with object classifications to guide further processing.

### From Image to Data (Timelapse workflow)
- Load images and MegaDetector JSON into Timelapse (open-access, CC BY-NC-SA 4.0).
- Follow Timelapse Image Recognition Guide with adaptations for efficiency.
- Key stages:
  - Classification: assign images as Empty, People (including dogs), or Wildlife; apply confidence thresholds and manual checks to correct misclassifications.
  - Temporal grouping: segment images into episodes (within 5 minutes) to avoid double-counting individuals; assign unique episode identifiers.
  - Anthropogenic factors: identify and count dogs and bikes within episodes; ensure counts reflect maximums within an episode when multiple images are involved.
  - Object auto counts: generate counts for people and wildlife using >20% model certainty; handle zero counts by setting to 1 where applicable.
  - Optional: manual adjustments to improve accuracy and ensure all images are categorized correctly.

### Wildlife-focused Workflow (5.1.x)
- For wildlife: tag species, add comments, and propagate values across similar images when appropriate.
- For episodes: populate episode-level data for People and Wildlife.
- For accuracy: ensure dog/bike and human counts are captured; use max counts across episodes for robust human counts when counting across multiple cameras is not possible.

## Results

### 3.1 Number and Type of Images
- Total triggered images: 66,005 (2010–2022).
- Distribution: BR (Bridge) and TL (Treeline) cameras accounted for ~81.5% of images.
- Content breakdown: Empty 43.1%; People 44.7%; Wildlife 12.2%.
- Species captured (mammals dominate; notable deer): Roe Deer most frequent (approx. 2,558 images), Red Deer (1,426), Red Squirrel (1,316); other mammals include Badger (966), Pine Marten (1,177), Reindeer (124), Otter (3), Mountain Hare (44). Bird detections present but smaller in counts; total unidentified/uncategorised images included.

### 3.2 Camera Reliability
- Overall reliability: 88.5% across 20,680 recording days.
- Downtime: 2,303 days across five cameras; TR location contributed ~37.6% of downtime with 19 events.
- Downtime patterns: median downtime ~36 days; mainly due to battery issues, occasional user error (e.g., camera not re-activated after service), theft (2 incidents), and occasional camera failures.

### 3.3 Species Present
- Wildlife images (7,697 of 8,050 wildlife images) predominantly mammals (95.6% of wildlife images). Birds and unidentified species each ~2.2%.
- Major mammal groups: Roe Deer, Red Deer, Red Squirrel; other notable detections include Badger, Pine Marten, Deer family, and Otter (rare).
- Species composition varied by camera location (e.g., bridge camera had few deer; SN in regenerating woodland had different assemblages; TL/BR varied with access and exposure).

### 3.4 Image Catalogue File Description
- Image catalogue file includes per-image data: image path, location folder, filename, camera location code, date/time, year/month/day, image contents (empty, people, animals), counts (bikes, dogs, number of animals), auto-count fields for people and animals, species (when identified), comments, and a Group_Code for episode-based grouping.
- Excludes images containing people or empty images from the main wildlife catalogue; retains data extraction for all images.

## Acknowledgements
- Supported by Natural Environment Research Council (NE/R016429/1) as part of UK-SCAPE National Capability.
- Additional support from NatureScot for ECN Cairngorm research.

## Supplementary Material and Timelapse Processing
- Supplementary materials include detailed Timelapse processing guidance (S1) and steps for preparation, initial assignments, wildlife processing, episode-based grouping, and counting routines.
- Timelapse is a free, CC BY-NC-SA 4.0 tool designed to accelerate processing of camera-trap outputs, especially when paired with AI object-detection outputs, enabling processing of a full year’s images in a few hours.