# Motion activated camera trap images from cameras located at the ECN Cairngorm long-term monitoring site 2010-2022

- Aim and purpose
  - Use camera traps to monitor fauna in the ECN Cairngorms Allt a’Mharcaidh catchment (2010–2022).
  - Quantify grazing pressure and contribute data to the National Biodiversity Network Gateway; share with NatureScot for NNR management; support phenology studies and ecosystem-service assessments.
  - Data also capture recreational use to inform broader ecosystem analyses.

- Study site and camera deployment
  - Location: Allt a’Mharcaidh catchment, Cairngorms National Park; part of Inverseshie and Inshriach National Nature Reserve (NNR).
  - Five active camera traps (2010–2022) positioned along routes used by wildlife and people: BR (bridge), TL (treeline), PA (pine woodland), SN (regen woodland), TR (track access).
  - Camera placement along main access routes to maximize subject presence; one camera near a footbridge sees the most activity.
  - Long-term ecological monitoring since 1999 as part of ECN.

- Cameras and technical setup
  - Models varied over time: initial Spypoint IR-B with solar panels; from 2013 onward, Bushnell Trophy Cam series and derivatives.
  - Trigger mechanism: passive infrared (PIR); typical detection ~0.2 s; 24-hour operation; one image per trigger, with up to 10 seconds between subsequent frames if subject remains in view.
  - Image capture: color by day, black-and-white at night; typical field-of-view oriented along paths to keep subjects in frame longer.
  - Data storage: SD cards (SanDisk Ultra Class 4, 15 MB/s); batteries (lithium AA); field-downloading every ~6 weeks to monitor function and reduce downtime; clocks synchronized to GMT.
  - Annual/seasonal variation: different camera models used across years; some cameras upgraded or replaced at various times.
  - Daily 3 pm timelapse image to monitor camera operation and phenology.

- Data processing workflow
  - Image handling and initial preparation
    - Images renamed to include camera name and timestamp; 3 pm images placed in a separate folder; tree-downloaded into yearly camera folders.
  - Object detection and initial filtering
    - MegaDetector (via Google Colab) classifies each image as empty, person, animal, or vehicle; outputs JSON per image.
  - From image to data (Timelapse workflow)
    - Timelapse (CC BY-NC-SA 4.0) used to classify and count content, following Timelapse Image Recognition Guide with project-specific adaptations.
    - Classification workflow:
      - Empty images filtered with >95% MegaDetector certainty.
      - People filtered with >80% certainty, then 10–80% with manual checks.
      - Wildlife filtered first at >80%, then 10–80%, with manual checks at each stage; species identified where possible; dogs counted as dogs.
      - Remaining unassigned images likewise filtered and categorized.
  - Temporal grouping and aggregation
    - Images grouped into episodes (events) if captured within 5 minutes at the same camera; episodes assigned unique IDs to support aggregation of counts within an event.
    - People, wildlife and other disturbance factors (dogs, bikes) recorded; counts derived where possible.
  - Auto counts and manual checks
    - Auto_count_People and Auto_count_Animals generated with a >20% probability threshold; zero counts adjusted to at least 1 when applicable.
    - Group-level counts (e.g., maximum number of individuals in an episode) used for later extraction.
  - Optional advanced counting (not fully implemented for all years)
    - Accurate counting across cameras is possible but time-consuming; describes approach to assign unique IDs per episode and aggregate counts across multiple images/cameras.

- Outputs and data coverage
  - Images and period
    - Total triggered images: 66,005 from 2010–2022.
    - Most images from two core cameras along major routes: BR (bridge) and TL (treeline) together account for ~81.5% of all images.
  - Content breakdown
    - Empty: 43.1% of all images.
    - People: 44.7% of images containing people (including dogs).
    - Wildlife: 12.2% of images containing wildlife.
  - Camera-specific results
    - BR and TL dominate image counts; BR 46.3%, TL 35.2% of all images.
    - SN (regen woodland) shows higher wildlife representation; BR shows more human activity (due to location on main access route).
    - TL has the highest proportion of empty images due to south-facing exposure and winter sun effects.
  - Species presence (mammals most common)
    - Roe Deer: 2,558 images (most frequent mammal).
    - Red Deer: 1,426 images.
    - Red Squirrel: 1,316 images.
    - Badger: 966 images.
    - Pine Marten: 1,177 images.
    - Other notable species: Mountain Hare, Otter, Red Fox, various birds; many images unidentified or non-target.
  - Taxonomic detail
    - Among wildlife images, mammals dominate (95.6% of wildlife images are mammals); birds and other unidentified categories ~2.2% each.
  - Image catalogue
    - Each row corresponds to a single image with fields including:
      - Image path, camera location, date/time, contents category (empty/people/animal), counts (bikes, dogs, animals, auto counts), species, group/episode IDs, and free-text comments.
    - Excludes images that contain people or are classified as empty from the final catalogue; dataset contains extracted metadata for all images.

- Data quality, reliability and limitations
  - Overall camera reliability: 88.5% across 20680 recording days.
  - Downtime: 2303 days across all cameras; TR location most affected (approx. 37.6% of downtime).
  - Downtime episodes: 57 across 13 years; median downtime length ~36 days.
  - Common downtime causes: battery failures (often a single faulty battery), occasional user error (e.g., failure to restart after servicing), theft and other occasional camera failures.
  - Spatial and inference limitations
    - Content classification relies on AI (MegaDetector) with manual validation; false positives and false negatives are possible (e.g., vegetation movement, shadows, sun glare causing false triggers).
    - Episode-based counting improves reliability within a camera’s episodes but prevents cross-camera aggregation of individuals; cross-camera individuality and movement across cameras are not fully captured for precise counts.
  - Data granularity and scale
    - Local-scale data (site-specific) suitable for site-management decisions and long-term trend analysis; potential extrapolation needed to compare across sites or scales.

- Image catalogue and supplementary materials
  - Image catalogue file structure and field descriptions provided; supports downstream analysis and reproducibility.
  - Supplementary materials and Timelapse processing guide (S1) detail year-by-year processing steps and workflow.
  - Timelapse method highlights processing speed (roughly 2–3 hours per year for full processing of ~5,000 images) and the importance of correct initial tagging to enable efficient downstream filtering.

- Acknowledgements
  - Funded by Natural Environment Research Council (award NE/R016429/1) under UK-SCAPE; additional support from NatureScot.