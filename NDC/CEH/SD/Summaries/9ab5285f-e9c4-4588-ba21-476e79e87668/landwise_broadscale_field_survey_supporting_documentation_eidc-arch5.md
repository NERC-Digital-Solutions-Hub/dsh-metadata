# Soil near-surface properties, vegetation observations, land use and land management information for 1800 locations across the Thames catchment, UK, 2018-2021
Landwise Broad-scale Field Survey

- Purpose and scope
  - Documentation of soil near-surface properties, vegetation observations, and land use/management information across the Thames catchment (UK) from 2018 to 2021.
  - Part of the Landwise Broad-scale Field Survey, funded by NERC Natural Flood Management (Grant NE/R004668/1).
  - Aimed at quantifying how different land use/management practices affect soil properties to inform natural flood management.

- Data products and structure
  - Public field contextual data file: LANDWISE_BroadScale_Survey_Field_Contextual_Data_PUBLIC.csv (84 columns, 165 rows).
  - Public point data file: LANDWISE_BroadScale_Survey_Point_Data_PUBLIC.csv (66 columns, 1837 rows).
  - Metadata for field contextual data and point data available in separate CSVs: Field metadata.csv and Point metadata.csv.
  - A unique ID (ID_SiteNo_FieldNo) joins field contextual data with point data.
  - Data have suffixes to distinguish data types: primary data (-Txt, -Obs, -Mea), derived data (-Deriv), and classifications (-Class, -Yr).

- What was measured
  - Field data (contextual)
    - Land owner/manager responses about land use and management (e.g., crops, cover crops, tillage, grazing, drainage, woodland management).
    - Derived classifications from free-text questionnaire responses.
    - General field observations (slope, surface form, water presence, erosion features).
  - Point data (per sampling location)
    - Location coordinates (BNG or LAT/LONG; later converted to BNG and anonymised to 1 km grid).
    - Near-surface soil measurements (0–50 mm bgl): dry bulk density, volumetric water content, organic matter, porosity (and porosity accounting for organic matter).
    - Vegetation: maximum and minimum height.
    - Soil qualitative measurements: hand texture, aggregate stability (slaking/dispersion), calcareous soil test, VESS score for a subset.
    - Observations: soil surface condition and vegetation type.

- Sampling design and coverage
  - 1836 location points sampled across 164 fields/land parcels, covering four land-use/management classes and five soil/geology classes.
  - Targeted sampling across twenty combinations, with pseudo-replicates avoided.
  - Land use/management classes: arable with/without grass in rotation, permanent grassland, broadleaf woodland.
  - Soil/geology classes: combinations including shallow over chalk/limestone, free-draining loamy over chalk/limestone, impeded/drainage loamy/clayey, slowly permeable loamy/clayey, and floodplain/high groundwater loamy/clayey.
  - Field sampling pattern:
    - Arable fields: 15 sampling locations per field (IN1-IN5, UN1-UN5, TR1-TR5 across three area types).
    - Grassland fields: 10 sampling locations (UN1-UN5, TR1-TR5).
    - Woodland parcels: 6 sampling locations; additional woodland samples bulked from 6 sub-samples per grid cell.
  - Fieldwork period: December 2018 – March 2021, with a Covid-19 pause from March–December 2020.
  - Fieldwork method: sampling along a W-walk pattern; location-specific sampling areas adjusted for soil/geology class targeting; VESS tests conducted at designated locations.
  - Woodland specifics: organic surface layer generally shallower than 50 mm; sampling focused on underlying mineral soil.

- Laboratory analyses and instrumentation
  - Soil analyses: dry bulk density, volumetric water content (via oven-drying 105°C, 36 h); particle size distribution via laser diffraction (Malvern Mastersizer 2000) across multiple size bins; orientation to 0.01–2–50–60–63–200–600–2000 µm with expanded 1 µm bins in 2–11 µm range.
  - Additional analyses: texture (hand texturing), aggregate stability (slaking/dispersion), calcareous soil test (HCl), soil organic matter by loss on ignition (400°C, 16 h).
  - Vegetation measurements: height data collected per point.
  - Quality control: instrument calibration checks and QA standards; field and lab data transcription verification; three-stage QA for coordinates to ensure spatial consistency with site boundaries and field maps.

- Derived (secondary) data and classifications
  - Porosity estimates:
    - Standard porosity: based on dry bulk density with assumed mineral density 2.65 g/cm3.
    - Porosity accounting for organic matter: uses weighted average particle density that accounts for organic matter content (2.65 g/cm3 mineral and 1.25 g/cm3 organic fraction) to adjust porosity.
  - Soil texture classifications:
    - Two classifications provided: traditional SSA/Ws (sand, silt, clay) limits, and a revised clay-silt cutoff using laser diffraction data.
    - Revised cutoff uses a 7 µm threshold (with discussions around 5–8 µm alternatives in literature). The dataset provides raw 1 µm bin distributions for 2–11 µm to allow reprocessing as consensus emerges.
    - Texture classifications illustrated with a comparison plot (traditional vs. revised cutoff).
  - Coordinate handling and anonymisation:
    - Primary coordinates captured in field; converted to British National Grid; rounded to 1 m where possible; public release coordinates further anonymised to nearest 1 km grid point.
  - Data processing context:
    - Secondary classifications of free-text responses created by data analysts with independent quality checks.
    - Documentation of data processing steps and assumptions included in accompanying materials.

- Data quality, limitations, and provenance
  - Field teams varied in expertise; a SurveyStaffCode is included to aid cross-team comparisons.
  - Soil organic matter and porosity derived values depend on assumed densities and LOI-based OM estimates; accuracy varies with OM content.
  - Secondary classifications may differ between analysts; QC procedures implemented to mitigate inconsistencies.
  - Anonymisation reduces locational precision; coordinate QC ensures internal consistency at site/field levels.
  - The dataset links to the Landwise Detailed survey dataset (hydraulic and hydrological measurements at higher resolution across seven fields).

- Related information and references
  - Grounded in Landwise project methodology and lab protocols (survey methodology, lab protocol, and supporting documentation referenced in the dataset).
  - Acknowledges field participants and land managers; acknowledges mapping and data processing literature for methods (e.g., VESS, soil texture, particle size standards).
  - Related dataset: Hydraulic and hydrological measurements from the Landwise Detailed survey (Thames catchment, 2021).

- Access, usage notes, and caveats
  - Data are provided with accompanying metadata files describing variable names, units, and descriptions.
  - Users should account for potential field-team biases, derived data uncertainties (porosity, OM, texture), and anonymised coordinates when performing spatial analyses.
  - The dataset supports analyses of soil–land use relationships and informs natural flood management strategies within the Thames catchment.