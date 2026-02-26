# Motion activated camera trap images from cameras located at the ECN Cairngorm long-term monitoring site 2010-2022

- Overview
  - Long-term camera-trap study at ECN Cairngorm Allt a’Mharcaidh (2010–2022) using five traps to monitor fauna and grazing pressure; data linked to National Biodiversity Network Gateway and NatureScot, with potential contributions to other recording schemes; supports phenology studies and ecosystem service assessments.

- Location and hardware
  - Five camera locations along wildlife and public access routes: BR (bridge), TL (treeline), PA (pine woodland), SN (regenerating woodland), TR (track/approach).
  - Habitat types include pine plantation, semi-natural woodland, pine regeneration, and riparian zone; cameras situated to maximize subject presence on paths.
  - Camera models evolved from Spointpoint IR-B with solar panels to Bushnell Trophy Cam derivatives (2010–2022); PIR-triggered with ~0.2 s trigger speed.
  - Settings: 24/7 operation; single image per trigger with 10 s interval if subject remains; daily fixed-time image at 3 pm for phenology; image sizes generally set to 3–8 MP to balance file size; GMT timestamps; storage on Sandisk Ultra Class 4 SD cards; Li-AA batteries with annual lifespan; secured mounts; field of view oriented along paths.

- Data management and processing workflow
  - Field data management: periodic in-field downloads (roughly every 4–6 weeks); clock synchronization across cameras; images renamed to include camera and timestamp; folder structure by year and camera.
  - Object detection: MegaDetector (via Google Colab) applied year-by-year to produce JSON with labels (empty, animal, person, vehicle).
  - Timelapse processing: loaded with Timelapse (CC BY-NC-SA 4.0); adapted workflow for efficiency with AI outputs; steps include:
    - 2.3.3.1 Classification: sequential filtering by content category (empty >95% certainty; people >80% then 10–80%; animals similarly); manual verification after each stage; dogs tagged alongside people where applicable.
    - 2.3.3.2 Temporal grouping: images grouped into episodes within 5 minutes per camera; each episode given a unique Group_Code to enable aggregation and presence timing; cross-camera grouping of people across cameras is not performed.
    - 2.3.3.3 Other disturbances: counting dogs and bikes in images containing people or animals >20% certainty; handling cases where counts span episodes.
    - 2.3.3.4 Object auto counts: auto-counts for people and animals with >20% probability; zero counts adjusted to 1 when needed; auto-counts used with caveats.
  - Metadata and data structures: outputs fed into a structured image catalogue including image paths, camera location, date/time, content category, species, counts, and group identifiers.
  - Supplementary material: detailed Timelapse processing guide in Supplement S1; includes preparation, initial assignments, wildlife workflows, episode-based group info, and handling of counts.

- Data outputs and results
  - Total triggered images: 66,005 (2010–2022); majority from BR (bridge) and TL (treeline) sites.
  - Image content distribution: 43.1% empty; 44.7% contain people; 12.2% contain wildlife; distribution varies by camera location (e.g., BR high human activity; SN higher wildlife presence; TL high empty images due to sun direction and path orientation).
  - Species presence (wildlife images): Roe Deer 2,558; Red Deer 1,426; Red Squirrel 1,316; Pine Marten 1,177; Badger 966; Reindeer 124; Otter 3; assorted birds and unidentifieds; other mammals included Mountain Hare, Red Fox, etc. Species composition varied by camera (e.g., BR low deer, SN higher wildlife proportion).

- Image catalogue and metadata
  - Catalogue fields per image include: Image_Input_Path, Image_Location_Folder_Name, Filename (e.g., BR_20100308_095752.JPG), Camera_Location, DateTime, Year/Month/Date, Image_Contents (Empty/People/Animals), Number_Bikes, Number_Dogs, Auto_Count_People, Species, Number_Animals, Auto_Count_Animals, Comment, Group_Code.
  - Structure supports downstream data discovery, discovery/testing, and cross-year analyses; excludes images containing people from the wildlife catalogue but includes extracted data for analysis.

- Data quality, reliability, and limitations
  - Overall camera reliability: 88.5% across 20,680 recording days; downtime days total 2,303 across five locations.
  - Downtime distribution: TR location experienced most downtime; median downtime length ~36 days; downtime largely due to battery issues, with occasional user error, theft, or camera failures.
  - Image classification limitations: substantial portion of images were empty or false positives (e.g., moving vegetation, shadows, bright light); cross-camera counting of individuals (especially humans) is limited due to episodic grouping and lack of cross-camera linking.

- Supplementary methods and replication notes
  - Timelapse provides efficient processing of large image sets (roughly 2–3 hours per year for typical datasets around 5,000 images/year); supports rapid filtering by content type via AI outputs.
  - Quick-paste templates and year-specific import workflows aid reproducibility; detailed step-by-step instructions available in Supplement S1 and Timelapse guide.

- Data governance, sharing, and provenance
  - Data contributed to and used within national and international biodiversity networks (NBN Gateway, NatureScot); aligns with UK-SCAPE program and ECN Cairngorm long-term monitoring objectives.
  - Acknowledgements: funded by Natural Environment Research Council (NE/R016429/1) as part of UK-SCAPE; additional support from NatureScot; project hosted by CEH.
  - Contact and institutional information provided for further collaboration and access.

- Acknowledgements and supplementary materials
  - Project supported by NERC and NatureScot; supplementary materials include the Timelapse processing guide (S1) and additional methodological details.