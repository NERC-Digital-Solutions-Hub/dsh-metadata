# Motion activated camera trap images from cameras located at the ECN Cairngorm long-term monitoring site 2010-2022

## Aim and scope
- Demonstrates environmental condition and policy-relevant activity via standardized monitoring data.
- Monitors fauna presence and grazing pressure at the ECN Cairngorm long-term site; contributes to National Biodiversity Network Gateway and NatureScot management programs; supports phenology and ecosystem service assessments.

## Location and monitoring context
- Site: Allt a’Mharcaidh catchment, Cairngorms National Park; part of Inverseshie and Inshriach National Nature Reserve; ECN long-term monitoring since 1999.
- Cameras: five traps along key wildlife/people paths (BR, TL, PA, SN, TR); locations include bridge, main path, pine plantation, mature woodland, and regeneration area.
- Study period: 2010–2022 (images captured from 08/03/2010 onward).

## Methods: Cameras and setup
- Camera models: varied over time; initial SPPOINT IR-B with solar panels; from 2013 onward, Bushnell Trophy family variants.
- Detection: PIR-based triggers; typical trigger speed ~0.2 seconds; some variation by model.
- Settings: 24/7 operation; one image per trigger, with a 10-second interval for continued triggering; fixed daily timelapse image at 3 pm for phenology checks.
- Storage and power: SD cards (SanDisk Ultra Class 4, up to ~15 MB/s); lithium AA batteries; field downloads approximately every 4–6 weeks.

## Data processing workflow
- Initial steps: images renamed with camera and timestamp; 3 pm images stored separately for phenology.
- Object detection: MegaDetector (Colab) used to classify images (empty, animal, person, vehicle); outputs JSON per image.
- From image to data (Timelapse 2.3.x):
  - Classification: sequential filtering by AI confidence (empty >0.95; people >0.8 then 0.1–0.8; wildlife >0.8 then 0.1–0.8), with manual verification to correct misclassifications.
  - Temporal grouping: images within 5 minutes constitute an episode; assign unique Episode IDs to enable aggregation of counts while acknowledging cross-camera limitations.
  - Anthropogenic factors: count dogs and bikes within episodes; assign counts even when not visible in a single image to improve total group counts.
  - Auto counts: use Timelapse auto-count for people and animals with a 20% certainty threshold; zero counts default to 1 if identified but not counted.
- Supplementary processing: detailed Timelapse workflows provided in supporting materials (S1) to improve efficiency and accuracy.

## Data outputs and content
- Total images: 66,005 triggers (2010–2022); majority from two core cameras along main access routes (BR and TL).
- Image content:
  - Empty: 43.1% of all images.
  - People (including dogs): 44.7%.
  - Wildlife: 12.2%.
- Camera-specific patterns: some cameras yielded higher wildlife or empty rates depending on location (e.g., SN higher wildlife share; BR higher empties due to route and sun exposure).
- Wildlife taxa observed (summary of counts across 2010–2022):
  - Roe Deer: 2,558 images
  - Red Deer: 1,426
  - Red Squirrel: 1,316
  - Pine Marten: 1,177
  - Badger: 966
  - Reindeer: 124
  - Mountain Hare: 44
  - Otter: 3
  - Red Fox: 83
  - Others (birds and unidentified mammals): smaller counts
- Notable species distribution varied by camera location (e.g., deer-dominated signals on some sites; different fauna profiles at bridge vs. path vs. regeneration areas).

## Data quality, reliability, and challenges
- Camera reliability: overall 88.5% across 20680 recording days; downtime events concentrated at a single site (TR); median downtime length ~36 days.
- Downtime drivers: battery issues (often one failing cell), occasional user error after servicing, theft, and occasional device failures.
- Image classification limitations: substantial false positives from vegetation movement, shadows, or bright light; high confidence thresholds used to minimize misclassification, with manual checks at each stage.

## Data management and accessibility
- Image catalogue structure: per-image data include location, timestamp, content classification, counts (bikes, dogs, animals, people), auto-count fields, species identifications, and group/episode codes.
- File organization: year-based folders, then by download date and camera; image entries provide path to wildlife images only (people/empty excluded from the wildlife catalogue).
- Data integration: results compatible with Timelapse (CC BY-NC-SA 4.0) and MegaDetector pipelines; outputs suitable for export to monitoring portals and data portals.

## Timelapse processing and guidance
- Timelapse software used to efficiently process year-long datasets (typical year ~5,000 images); results include categorization (empty/people/animals), species assignment, and counts within minutes.
- Supplementary S1 provides step-by-step instructions for preparation, initial assignments, wildlife-focused processing, and episode-based aggregation.
- Practical notes: quick-paste templates for common fields; episode-based aggregation helps manage repeated sightings and cross-image counts; recommended to include metadata like camera name, software version, and field notes.

## Acknowledgements and governance
- Funded by Natural Environment Research Council (NE/R016429/1) as part of UK-SCAPE National Capability; additional support from NatureScot.
- Contributes to ECN Cairngorm, UKCEH and partner research programs.

## Supplementary material
- S1: Detailed Timelapse processing method, including preparation, initial assignments, wildlife processing steps, episode data population, and guidance on counts for bikes and people.