# Motion activated camera trap images from cameras located at the ECN Cairngorm long-term monitoring site 2010-2022

## Aim and Rationale
- Monitor fauna presence and grazing pressure at ECN Cairngorm Allt a’Mharcaidh catchment.
- Data support national and regional biodiversity initiatives (NBN Gateway, NatureScot NNR management) and phenology studies; includes potential for ecosystem service assessments.

## Location and Scope
- Allt a’Mharcaidh catchment, Cairngorms National Park; part of Inverseshie and Inshriach National Nature Reserve.
- Five camera traps deployed along wildlife/people trails: BR, PA, SN, TL, TR.
- Study period: 2010–2022; data linked to long-term ecological monitoring by ECN.

## Cameras and Setup
- Camera models varied: Spypoint IR-B (with solar panels) used early; from 2013 onward mainly Bushnell Trophy Cam family.
- Triggering: passive infrared; ~0.2 s detection; 24/7 operation; initial image plus up to 1 more image after 10 s if subject remains.
- Recording settings: 3–8 MP images, high flash, 10 s interval, auto sensitivity; fixed daily 3 pm image for phenology checks.
- Storage and power: SD cards (SanDisk Ultra Class 4, 15 MB/s); lithium AA batteries; field downloads ~every 4–6 weeks; cameras secured to trees/posts; field clock synchronization to minimize drift.

## Data Processing and Workflow
- Image renaming and organization: images renamed to include camera name and timestamp; 3 pm phenology images moved to a separate folder; yearly folder structure created per camera.
- Object detection: Microsoft MegaDetector (via Google Colab) applied year-by-year to generate per-image JSON outputs (empty, animal, person, vehicle).
- Timelapse processing: loaded with a custom table in Timelapse (CC BY-NC-SA 4.0) to classify and count contents; workflow adapted for efficiency.
- Classification steps (image to data):
  - First filter for empty images ( MegaDetector >95% certainty).
  - Then identify people ( >80%, then 10–80%; manual checks after each stage).
  - Then identify wildlife ( >80%, then 10–80%; manual checks).
  - Animals tagged to species; dogs and bikes counted; occasional notes for other anthropogenic factors.
- Temporal grouping: images assigned to episodes (within 5 minutes) to avoid over-counting individuals; episodes receive unique identifiers.
- Corporeal counts:
  - Auto-counts used for people and wildlife with >20% confidence; ranges adjusted to maximize accuracy while acknowledging limitations.
  - For bikes/dogs, counts may exceed single-image visibility; the maximum across an episode is captured for later extraction.
- Additional wildlife accounting: steps to assign species, counts, and notes; procedures to ensure no missed images.

## Image Catalogue and Metadata
- Dataset size: 66,005 triggered images (2010–2022); majority from BR and TL cameras.
- Image content breakdown: roughly 43.1% empty; 44.7% containing people (including dogs); 12.2% wildlife.
- Wildlife assemblage: mainly Roe Deer, Red Deer, Red Squirrel; other mammals include Badger, Pine Marten, Otter, Mountain Hare, Red Fox, etc.; various bird species recorded.
- Metadata schema (image catalogue file):
  - Image_Input_Path, Image_Location_Folder_Name, Filename, Camera_Location (BR, PA, SN, TL, TR), DateTime, Year, Month, Date, Image_Contents (Empty/People/Animals), Number_Bikes, Number_Dogs, Auto_Count_People, Species, Number_Animals, Auto_Count_Animals, Comment, Group_Code.
  - Wildlife images include: path to image, species name, counts; images with people/empty are not included in the wildlife catalogue but data remains extractable.
- Data layout supports traceability from raw image to processed data, including the root folder, per-year organization, and per-camera views.

## Data Quality and Reliability
- Overall camera reliability: 88.5% across 20680 recording days; downtime on 2303 days across five cameras.
- Most downtime linked to camera location TR; downtime events were 57 across 13 years; median downtime about 36 days.
- Primary downtime causes: battery issues, occasional user error, camera theft (2), and occasional failures or misconfigurations.
- Data quality caveats: substantial portion of empty images likely due to false triggers; variability across camera locations and lighting conditions (e.g., sun angle causing higher false positives).

## Results Highlights
- Image distribution by camera reflects site usage: BR and TL contributed the majority of wildlife and people images; SN camera more oriented to wildlife on a quieter trail; other cameras showed variable empty image rates depending on location.
- Species presence varied by location; some cameras recorded few deer (e.g., BR) while others captured higher wildlife diversity (e.g., SN).

## Sharing, Documentation, and Access
- Data contribute to national biodiversity initiatives; linked to NBN Gateway and NatureScot for NNR management.
- Timelapse and processing tools are open access with CC BY-NC-SA 4.0 license; supplementary material (S1) provides detailed step-by-step processing guidance.
- Documentation includes extensive supplementary sections (e.g., S1 Timelapse processing) and a structured image catalogue file, enabling reuse and re-analysis by data stewards and researchers.

## Supplementary Materials and Acknowledgements
- Supplementary material S1 provides detailed Timelapse processing steps and instructions.
- Acknowledgements: funded by Natural Environment Research Council (NE/R016429/1) as part of UK-SCAPE, with support from NatureScot.

## Implications for Data Stewardship
- Demonstrates end-to-end data lifecycle: hardware, data collection, metadata-rich cataloging, automated object detection, manual validation, and episode-based aggregation.
- Emphasizes data governance needs: standardized metadata, provenance, clear processing pipelines, data quality checks, and licensing/open-access tooling.
- Highlights practical challenges for data sharing: long-running fieldwork, multi-year datasets, heterogeneous hardware, and evolving processing methods, all of which require robust documentation and update mechanisms.