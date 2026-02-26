# Motion activated camera trap images from cameras located at the ECN Cairngorm long-term monitoring site 2010-2022

## Overview
- A long-term camera-trap study (2010–2022) at the ECN Cairngorm Allt a’Mharcaidh catchment in the Cairngorms National Park, contributing to National Biodiversity Network data and NatureScot management.
- Five camera locations along key wildlife and recreation routes; multiple camera models used over time.
- Data processing combines AI object detection (MegaDetector) with the Timelapse software to classify images, count objects (people, bikes, dogs, wildlife), and generate episode-level groupings for accurate presence/counts.
- Outputs include an image catalogue with rich metadata suitable for GIS mapping, spatial summaries, and time-based analyses.

## Location and context
- Site: Allt a’Mharcaidh catchment, Cairngorms National Park; part of Inverseshie and Inshriach National Nature Reserve.
- Cameras positioned along active wildlife and human use paths; five traps deployed at varying habitats (pine plantation, mature woodland, regeneration zone, riparian zone).
- Data integrated with ongoing monitoring (ECN) and shared with national recording schemes; supports ecosystem service and management assessments.

## Cameras and setup
- Camera history: initial Spointpoint IR-B with solar panels; from 2013 onward mostly Bushnell Trophy Camera HD lineage.
- Triggering: passive infrared (PIR); ~0.2 s trigger speed; typical 24/7 operation.
- Field setup: aimed along paths to maximize subject visibility; mounted on trees/posts with security fittings.
- Imaging: one image per trigger with 10-second gaps for continued triggers; daily fixed-time image at 3 pm for phenology checks.
- Storage and workflow: SD cards with ~15 MB/s speed; field downloads every ~4–6 weeks; clock synchronization across devices.

## Data processing pipeline
- Image handling:
  - Yearly data imported into Timelapse (open-source; CC BY-NC-SA 4.0) and linked to AI-detection outputs (MegaDetector JSON).
  - Pre-processing includes renaming and organizing by camera and year.
- Object detection:
  - MegaDetector identifies empty, animal, person, vehicle; processed in batches per year (one Colab run per year with GPU).
- From image to data (Timelapse workflow):
  - Cataloguing and classification: images labeled as Empty, People (incl. dogs), or Animals; species tagged where possible.
  - Temporal grouping: images grouped into episodes (events) if within 5 minutes at a given camera; episodes assigned unique identifiers (Group_Code) to support aggregation.
  - Anthropogenic factors: dogs and bikes counted; 20% certainty threshold used for auto-counts; manual checks to adjust misclassifications.
  - Group info: EpisodePeople and EpisodeWildlife fields populated after initial classifications.
  - Counting caveats: counting people across cameras is challenging; where possible, maximum counts across an episode are used to avoid double-counting.
- Special considerations:
  - Proxy filtering to minimize false positives (e.g., vegetation movement, shadows).
  - Guidance notes provided in supplementary material (S1) for Timelapse processing.

## Image catalogue and metadata
- Catalogue structure: each row corresponds to a single image with fields including:
  - Image_Input_Path, Image_Location_Folder_Name, Filename, Camera_Location, DateTime, Year/Month/Date, Image_Contents (Empty/People/Animals), Number_Bikes, Number_Dogs, Auto_Count_People, Species, Number_Animals, Auto_Count_Animals, Comment, Group_Code.
  - Wildlife images contain the location path to the image; images with people or empty are not included in the wildlife catalogue but data are present for completeness.
- Example metadata elements:
  - Location codes: BR (Bridge), TL (Treeline), SN (Regeneration), PA (Partial/Primary woodland), TR (Trail/Track).
  - Image timestamps are GMT and reconciled with camera clocks as needed.

## Results and key findings
- Total images: 66,005 triggered images across 2010–2022.
- Activity distribution:
  - Majority from two core cameras along bridge and main access path (high-traffic areas).
  - A substantial portion of images are Empty (43.1%), with remaining images containing People (44.7%) and Wildlife (12.2%).
- Species present (wildlife images):
  - Mammals dominate (95.6% of wildlife images); common species include Roe Deer (Capreolus capreolus), Red Deer (Cervus elaphus), Red Squirrel (Sciurus vulgaris), Pine Marten (Martes martes), Red Fox, and others.
  - Deer-dominated signals vary by camera location (e.g., bridge camera shows few deer; other locations show more wildlife).
- Camera reliability:
  - Overall reliability ~88.5% across 20680 recording days; downtime distributed across cameras with TR showing higher downtime.
  - Downtime periods often 36 days median, frequently due to battery issues or post-servicing downtime; occasional theft or misconfigurations noted.
- Data quality considerations:
  - High rate of false positives from environmental triggers; 6–7 figures of images require manual verification.
  - Some time drift corrections required; multiple camera models introduced over the period may affect consistency.

## GIS-relevant outputs and applications
- Spatial summaries by camera location enable mapping of wildlife presence, human activity, and species hotspots.
- Episode-based counts support temporal analyses of species activity and visitor presence within defined time windows.
- Image catalogue provides rich metadata for layer creation (e.g., species presence per location, activity levels, phenology signals from fixed 3 pm images).
- Suitable for integrating with policy or management datasets (NNR management, ecosystem services, citizen science data).

## Access, reproducibility, and materials
- Timelapse processing method (S1) documents step-by-step workflows; Timelapse tool is open access and designed to work with MegaDetector outputs.
- Supplementary materials (Section 5) provide detailed processing steps, assignments, and quality control guidance.
- Acknowledgements note NERC UK-SCAPE funding and NatureScot support.

## Endnotes and credits
- Funded by Natural Environment Research Council (NE/R016429/1) as part of UK-SCAPE; ECN Cairngorm data collaboration with NatureScot.