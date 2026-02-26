# UK Pollinator Monitoring Scheme metadata: Flower-insect timed count data from the UK Pollinator Monitoring Scheme, 2017-2020 version 2

- Purpose and scope
  - Metadata for the Flower-insect timed count (FIT Count) data from the UK Pollinator Monitoring Scheme (PoMS), 2017–2020, version 2 (deduplicated from the previous version).
  - PoMS is part of a wider Pollinator Monitoring and Research Partnership (PMRP) to track UK pollinator populations and inform national pollinator strategies.
  - Data support engagement of volunteers and provide evidence for policy and management decisions.

- Data access, citation, and acknowledgement
  - Data accessible via DOI: https://doi.org/10.5285/13aed7ac-334f-4bb7-b476-4f1c3da45a13
  - Licensed under the Open Government Licence; dataset must be cited in publications describing research using the data.
  - Acknowledgement required for funding and contributions:
    - PoMS funded by Defra (England), Welsh Government, DAERA (NI), JNCC, UKCEH; UKCEH funding via NERC award NE/R016429/1 (UK-SCAPE).
    - Contributions from volunteers and numerous partner organisations.
  - Authors and institutions include UKCEH, universities, and conservation charities (e.g., Bumblebee Conservation Trust, Butterfly Conservation, etc.).

- Dataset and outputs
  - PoMS comprises two surveys: the Flower-Insect Timed Count (FIT Count) and the 1 km square survey; the dataset here includes FIT Count data (2017–2020) and related environmental data.
  - FIT Count aims to quantify insects visiting flowers in 50 cm × 50 cm patches over ten minutes, at locations and dates chosen by participants, to monitor pollinator change across cropped and non-cropped landscapes.
  - The 1 km square survey yields additional FIT Count data and pan-trap data (published separately); co-located with National Plant Monitoring Scheme squares in GB.

- Methodology and data collection
  - Public FIT Counts
    - Conducted 1 April–30 September each year; weather thresholds determine suitability:
      - If sky clear: minimum temperature 13°C
      - If sky cloudy: minimum temperature 15°C
    - Participants select a location with a target flower from a provided list (or another suitable flower) and count visiting insects for ten minutes in a 50 cm × 50 cm quadrat.
  - 1 km square FIT Counts
    - Follow the same methodology as public counts but conducted in up to 75 randomly allocated 1 km squares; four visits per summer (May–August), aiming for one visit per month.
    - Squares co-located with PoMS pan-trap surveys; data linked to habitat and land-cover information.
  - Habitat and stratification
    - Squares classified by habitat cover using CEH Land Cover Map 2007 into broad categories (agricultural vs semi-natural) and further stratified by predominant habitat, to compare cropped and non-cropped landscapes.
    - England, Scotland, and Wales have defined 1 km square sampling areas; Northern Ireland data is included in the public FIT Count dataset.
  - Target flowers and taxonomic corrections
    - Target flowers are coded (with corrections possible after photo review). Corrected identifications are applied when photos are reviewed post-count.
  - Data quality controls
    - Online data entry via iRecord/Indicia; season-end QA checks include:
      - Flower identification checks against photos; corrections applied as needed.
      - Floral unit counts checked against the target flower; plant family names added via lookup tables.
      - For 1 km square data, grid references verified to be within linked squares; misallocated data corrected.
      - Counts outside the recording period or with missing geolocations excluded.

- Data files and structure
  - ukpoms_1kmFITCountData_2017-2020.csv
    - Contains FIT Count results from the 1 km square surveys.
    - Key fields include: sample_id, country (England, Scotland, Wales), location_code/name, X1km_square, sample_projection (OSGB), land_cover (agricultural or semi-natural), date/year, habitat, target_flower (and corrected versions), target_flower_family, flower_cover, floral_unit_count, floral_unit, flower_context, count_start_time, cloud_cover, sunshine, wind_speed, habitat_type, flower_structure, and counts for insect groups (bumblebees, honeybees, solitary_bees, wasps, hoverflies, other_flies, butterflies_moths, beetles, insects_small, insects_other) plus all_insects_total. Additional metadata on data entry and recorder type is included.
  - ukpoms_publicFITCountData_2017-2020.csv
    - Contains FIT Count results from the public counts.
    - Key fields mirror the 1 km dataset with some differences:
      - Country includes England, Isle of Man, Northern Ireland, Scotland, Wales.
      - Date/year, X1km_square, sample_projection (OSGB or OSNI), digitised_by, recorder_type, habitat, target_flower (with NI-specific entries like NA), target_flower_corrected, target_other_name/target_other_name_corrected, target_flower_family, flower_cover, floral_unit_count, floral_unit, flower_context, count_start_time, cloud_cover, sunshine, wind_speed, habitat_type, flower_structure, insect group counts (bumblebees, honeybees, solitary_bees, wasps, hoverflies, other_flies, butterflies_moths, beetles, insects_small, insects_other) and all_insects_total, plus additional fields for enjoyment and difficulty in NI data.
  - The 2017 data in version 1 had duplicates; version 2 has deduplicated data and updated metadata.

- Data governance, quality, and documentation
  - Quality assurance steps include photo-based verification, standardised data formats, and alignment of flower and insect categories across years.
  - Metadata and documentation reference methodological guidance on the PoMS website and integration with broader PMRP frameworks.
  - References include design and testing of national pollinator monitoring (Carvell et al. 2016), PMRP establishment (Carvell et al. 2020), and PMRP progress (2020).

- Usage notes and references
  - See the PoMS methodological guidance for field techniques, target flowers, and insect group definitions.
  - Cited works provide context for the design, evaluation, and governance of UK pollinator monitoring frameworks.