# Motion activated camera trap images from cameras located at the ECN Cairngorm long-term monitoring site 2010-2022

## Overview
- Long-term camera-trap monitoring (2010–2022) at Allt a’Mharcaidh catchment, Cairngorms National Park, within the Inverseshie and Inshriach National Nature Reserve (NNR).
- Aim: quantify fauna presence and grazing pressure to inform management and ecosystem assessments; data linked to citizen science and scoping for phenology studies and ecosystem services.
- Data shared with NatureScot and other schemes; supports ongoing monitoring and potential public data sharing.

## Location and study design
- Site: ECN Cairngorm long-term monitoring site in the Allt a’Mharcaidh catchment.
- Camera layout: five traps positioned along wildlife and human use paths (BR, PA, SN, TL, TR) including a footbridge access bottleneck.
- Habitat contexts: pine plantation, semi-natural woodland, pine regeneration, riparian zone.
- Monitoring duration: 2010–2022, with long-run ecological data context since 1999.

## Cameras and setup
- Camera models: initial Spypoint IR-B with solar panels; from 2013 onward, Bushnell Trophy Camera derivatives until 2022; 2022 onward used Bushnell Core Trail Cam.
- Trigger mechanism: passive infrared (PIR); typical detection speed ~0.2 seconds.
- Image settings: 24-hour operation; single image per trigger, plus up to 10-second burst if subject remains in view.
- Daily verification image: fixed-time 3 pm image for phenology/monitoring checks.
- Data capture and storage: SD cards (SanDisk Ultra Class 4, 15 MB/s); batteries generally last a year; secured with straps and locks.
- Field practices: cameras angled to maximize subject in frame; field downloads every ~6 weeks to minimize downtime; clock checks to reduce drift.

## Data processing workflow
- Initial image handling: rename images with camera name and timestamp; separate 3 pm phenology images.
- Object detection: MegaDetector (Google Colab) used year-by-year to classify images as empty, animal, person, or vehicle.
- From image to data: Timelapse (open software, CC BY-NC-SA 4.0) used to process detected images; custom adaptations for efficiency.
- Classification workflow:
  - Empty vs. content images: apply high-certainty filters first (empty >95%; people >80%; then 10–80%), followed by manual checks.
  - Wildlife images: similarly filtered and species identified where possible; dogs counted; bikes counted when associated with people.
  - Temporal grouping: episodes created for images within 5 minutes at a given camera; provides start/end times and max counts per episode.
  - Auto counts: auto-counts produced for people and wildlife with >20% model certainty; zero counts adjusted to at least 1 when present.
- Metadata and grouping enhancements:
  - Episode-based grouping used to prevent double counting across images and cameras.
  - Group IDs and episode data attached to images; plans described for unique yearly IDs (YYYY_000) to aid longitudinal counting.
- Wildlife vs. human disturbance factors: explicit steps to count bikes and dogs within episodes; procedures described to maximize accuracy given real-world camera limitations.

## Image catalogue and metadata
- Image dataset: 66,005 triggered images across 2010–2022.
- Classification breakdown (overall):
  - Empty: 28,457 images (43.1% of all images).
  - People (including dogs): 29,498 images.
  - Wildlife: 8,050 images.
- Camera contribution: majority from two core cameras along main routes (BR and TL) driving 81.5% of images.
- Species highlights (mammals): Roe Deer (33%), Red Deer (18.5%), Red Squirrel (17.1%), Badger (966 images), Pine Marten (1,177), Reindeer (124); other species present in smaller numbers.
- Birds and other groups: diverse bird species recorded; many images unidentified to species; overall wildlife composition varied by camera location.
- Data catalogue structure: rows correspond to single images; includes image path, location code, date/time, content category, counts (bikes, dogs, animals), auto-count fields, species identifications, and episode/group identifiers.

## Camera reliability and data quality
- Overall camera reliability: 88.5% across the study period.
- Downtime: 2,303 downtime days across 20,680 recording days (37.6% of downtime associated with camera TR).
- Downtime events: 57 downtime periods across 13 years; median downtime length ~36 days.
- Common causes: battery failures (often due to a single weak battery), occasional user error after servicing, theft, and occasional camera failures.
- Variability across locations: downtime events per camera ranged from nine to ten over the period, with the TR location contributing the most downtime.

## Key findings and outputs
- Data indicate substantial use of cameras at core access routes, yielding a large portion of detections for humans and wildlife.
- Species presence reveals dominant large herbivores (Roe Deer, Red Deer) with notable small mammal detections (Red Squirrel, Badger, Pine Marten) and a wide array of bird taxa.
- The 3 pm daily image sequence supports phenology observations and site condition monitoring.
- The processing workflow demonstrates a scalable approach to handling long-term camera-trap data, balancing automated detection with manual validation.

## Data sharing, governance, and accessibility
- Outputs disseminated via reports and visual materials; underlying data are structured for sharing and reuse.
- Open-source tools used (Megadetector, Timelapse) with openly described workflows.
- Data and metadata practices emphasize transparency, traceability, and reproducibility, aligning with governance needs in monitoring frameworks.
- Acknowledgements indicate support from major funding bodies and agencies (NERC, NatureScot) and data-sharing ambitions with national and regional schemes.

## Supplementary material and methodology details
- Supplementary material (S1) provides extended step-by-step Timelapse processing guidance.
- Timelapse processing approach details (S1) cover preparation, initial assignments, wildlife classification, episode assignment, and group-level calculations.
- Detailed procedural steps (5.1.x) outline practical guidance for reproducibility, including:
  - Preparation, quick-paste templates, and year-specific data import.
  - Initial image assignments (camera naming, empty/people/animals tagging).
  - Wildlife tagging, species assignment, counts, and auto-count fields.
  - Episode population and group-level data extraction strategies.
  - Special considerations for calculating numbers of bikes and people across episodes and cameras.

## Acknowledgements
- Funded by the Natural Environment Research Council (NE/R016429/1) as part of the UK-SCAPE National Capability.
- Additional support from NatureScot for ECN Cairngorm research.