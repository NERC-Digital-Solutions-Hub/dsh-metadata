# The UK Pollinator Monitoring Scheme

- The PoMS is a UK-wide partnership aiming to establish how insect pollinator populations are changing and to provide evidence for national pollinator strategies.
- Two large-scale surveys drive PoMS:
  - Flower-Insect Timed Count (FIT Count): volunteers count insects visiting target flowers within a 50 cm by 50 cm quadrat for ten minutes; used to generate the primary FIT Count dataset.
  - PoMS 1 km square survey: collects FIT Count data within up to 95 randomly selected 1 km squares, plus pan-trap data (published separately).
- The schemes are run across the UK with volunteer participation, co-located with other national monitoring frameworks (e.g., NPMS), and supported by a network of environmental and conservation organizations.

## Data Access, Licensing and Acknowledgement

- Data are accessible via the Environmental Information Data Centre (EIDC), part of NERC’s Environmental Data Service, hosted by UKCEH.
- Open Government Licence applies; users must cite the dataset in publications describing research that used the data.
- Required acknowledgement: PoMS partnership (UKCEH and JNCC, funded by Defra, Scottish Government, Welsh Government, and DAERA) and the support from NERC, volunteers, and partner institutions.
- Major contributors and funders include UKCEH, JNCC, Defra, Scottish Government, Welsh Government, DAERA, and others; a comprehensive acknowledgment list is provided with the dataset.

## Surveys, Data Collected and Methodology

- FIT Count dataset (2017–2021):
  - Location data resolved to ~1 km, with environmental variables and counts by insect groups visiting target flowers.
  - 2017 was a pilot year; 2020 data have gaps due to COVID; NI data limited (pilot in 2021).
  - Public FIT Counts: counts by volunteers at chosen locations and dates (1 April–30 September), weather thresholds: minimum 13°C (clear sky) or 15°C (cloudy).
  - 1 km square FIT Counts: similar method, conducted in up to 95 randomly allocated 1 km squares; four visits per summer (May–August), some data gaps due to non-visit months or access.
- Habitat and habitat-related data:
  - Sampling squares stratified by land-cover type; habitat categories include agricultural, semi-natural, garden, and urban, derived from UKCEH Land Cover Map (LCM) 2007.
  - 1 km squares co-located with National Plant Monitoring Scheme (NPMS) where applicable.
- Data collection and QA:
  - Data entered via iRecord/Indicia and later consolidated in the Indicia data warehouse (UKCEH).
  - Post-season QA includes photographic verification of target flowers, optional insect photos, and data cleaning with R.
  - Metadata coverage and workflow designed to support data provenance, reproducibility, and governance.

## Data Processing, Quality Assurance, and Corrections

- Data import and cleaning:
  - Raw data retrieved via SQL from Indicia; subsequent cleaning and standardization performed with R.
  - Manual checks include flower identifications, plant family/structure corrections, and harmonization across years.
- Floral corrections and unit corrections:
  - Corrections to target flower identifications based on photographic review; some corrections to floral units (e.g., converting units when miscounted) and documentation of changes.
  - Special handling for non-flowering plants (NA for floral units, grasses standardized in counting).
- Habitat and other metadata:
  - Habitat categorization harmonized across years; manual checks for “Other” habitat entries; development of consistent habitat typologies.
  - Flower-related corrections and family/structure data enhanced through reference datasets; checks to ensure complete floral structure and family information.
- Data integrity checks:
  - Checks for sample ID duplication, correct 1 km square placement, date consistency (single-day counts when required), and daylight-time consistency (to avoid night-time counts passing as day counts).
  - Exports prepared for public (non-1km) and 1 km square datasets, with standardized fields and renamed/derived columns for analytic use.
- Collation and year-to-year consistency:
  - Datasets from 2017–2021 collated; four-year and year-specific edits applied to improve comparability (e.g., floral name standardization, outlier corrections).
  - Final exports include public FIT counts (ukpoms_publicFITCountData_2017-2021.csv) and 1 km FIT counts (ukpoms_1kmFITCountData_2017-2021.csv), plus a combined dataset for cross-year analyses.

## Datasets, Exports and File Attributes

- Public FIT Count data:
  - Contains country, location, date, habitat, target flower, insect counts by group, weather variables, and derived fields (year, etc.).
  - Exported as ukpoms_publicFITCountData_2017-2021.csv.
- 1 km FIT Count data:
  - Similar structure to public FIT Counts, plus location_code and 1 km square-specific fields; additional data on land cover.
  - Exported as ukpoms_1kmFITCountData_2017-2021.csv.
- Dataset attributes (highlights):
  - sample_id: unique sample identifier.
  - country, location_code, location_name: location metadata.
  - x1km_square, sample_projection: spatial references.
  - land_cover, habitat, habitat_other_detail: habitat/land-use metadata.
  - target_flower_corrected, target_other_name, target_flower_family, flower_structure, flower_cover: floral identity and context data.
  - floral_unit_count, floral_unit, flower_context: floral abundance details.
  - count_start_time, cloud_cover, sunshine, wind_speed: weather and timing data.
  - insect counts by group (e.g., bumblebees, honeybees, solitary_bees, wasps, hoverflies, etc.) and all_insects_total.
- Collation across years:
  - Four-year public dataset is prepared; floral corrections and name harmonization applied to ensure cross-year comparability.

## Collaboration, Acknowledgements and References

- PoMS is a multi-organisation partnership with funding from Defra, Scottish Government, Welsh Government, and DAERA; coordinated contributions from UKCEH, JNCC, Bumblebee Conservation Trust, Butterfly Conservation, BTO, Hymettus, Natural History Museum, University of Reading, University of Leeds, University of Plymouth, and others.
- Key references include Defra/BePDefra-project reports on polling monitoring frameworks and PMRP progress (Carvell et al. 2016, 2020; PMRP progress report 2020).
- Website for more information and methodological guidance: https://ukpoms.org.uk/

## Practical Considerations for Monitoring Framework Authors

- Data governance and openness:
  - Open licensing (Open Government Licence) and explicit data citation requirements help ensure data reuse while maintaining transparency.
  - Publicly shareable outputs depend on sharing underlying data with appropriate governance and metadata to enable reuse.
- Data availability and interoperability:
  - Fragmentation across datasets (public FIT Count, 1 km square data, pan-trap data) necessitates careful collation and consistent metadata standards.
  - Metadata gaps or inconsistent provenance can impede reuse; PoMS addresses this via structured QA, official documentation, and a standardized pipeline.
- Data standards and metadata:
  - Column definitions, habitat typologies, and floral identities require careful standardization across years; PoMS undertakes floral corrections, habitat harmonization, and cross-year reconciliations.
- Communication of results:
  - The workflow includes clear export formats and derived fields to support policy relevance, dashboards, and reports for environmental health monitoring.
- Barriers and challenges highlighted:
  - Lack of data at sufficient standards, restricted access, inter-organisational silos, need to publicly share datasets, keeping data up to date, metadata inadequacies, data format transformation efforts, and communicating complex findings clearly.
- Data governance:
  - PoMS maintains data quality through QA processes, data cleaning, metadata enhancements, and a governance approach to ensure datasets meet standards and remain up-to-date.