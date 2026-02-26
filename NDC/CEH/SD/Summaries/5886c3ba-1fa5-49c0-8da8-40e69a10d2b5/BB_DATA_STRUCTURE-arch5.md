# ECN Breeding Bird Survey Dataset Documentation

- Dataset Originator: ECN Data Centre (Centre for Ecology and Hydrology), contact ecn@ceh.ac.uk, http://data.ecn.ac.uk
- Dataset Owners: UK Environmental Change Network (ECN) programme; funded by a consortium of UK government departments and agencies including AFBI, BBSRC, CNW, Dstl, Defra, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, NIEA, SEPA, Scottish Government, and Scottish Natural Heritage
- Purpose and use: Data collected to understand environmental change; users should acknowledge ECN data usage and provide one reprint of any publication citing ECN data

- Protocol and standardization:
  - ECN operates standard operating procedures to ensure data comparability across sites; detailed methodology described in accompanying bb.pdf
  - Protocols enable cross-site comparability and support longitudinal analyses

- Data and metadata governance:
  - Data availability and limitations must be considered (disclosure risks, proprietary issues, embargoes)
  - Users should utilize accompanying quality information and documentation to properly interpret data

- Data collection and structure (Usage Notes overview):
  - Breeding Bird Survey method: birds recorded along a transect within a 1 km square; distance from transect recorded
  - Conducted according to the Breeding Birds Survey methodology (BTO)
  - Transect walked twice per year; national-scale survey with site-level data that may limit precise population-environment relationships
  - Early surveys (BTO Common Bird Census, Moorland Bird Survey) were replaced by the Breeding Bird Survey at ECN sites
  - Data should be used in conjunction with broader datasets (e.g., BTO) for richer analyses
  - Users should apply the accompanying quality information when using data

- Data download fields (core dataset):
  - SITECODE (unique ECN Site code) and LCODE (location ID)
  - VISIT (early or late), SDATE (sampling date)
  - TRANSECT (transect identifier), FIELDNAME (bird species code)
  - VALUE (number of birds observed), DISTANCE (distance category)
  - F (Bird in flight, any distance)

- Supporting documentation (ECN_BB*.csv files):
  - ECN_BB2.csv: survey timing and weather context
    - FROM_HOUR, FROM_MINS, TO_HOUR, TO_MINS
    - CLOUD, RAIN, WIND, VISIBILITY (weather codes)
  - ECN_BB3.csv: habitat context for transects
    - SITECODE, LCODE, VISIT, TRANSECT, FIRSTHL*, SECONDHL* (habitat codes at multiple levels)
  - ECN_BB_qtext.csv: qualitative notes on data quality
    - SITECODE, LCODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING

- Explanatory information: Site codes
  - Example sites T01–T12 (e.g., Drayton, Glensaugh, Hillsborough, Moor House, North Wyke, Rothamsted, Sourhope, Alice Holt, Porton Down, Snowdon, Cairngorms)
  - Each site includes location coordinates and site name
  - Additional information available at the ECN catalogue URL (link provided in document)

- Explanatory information: Bird species codes
  - Comprehensive mapping of two-letter or code identifiers to species names (e.g., AC = Arctic Skua/Arctic Tern; AB etc.)
  - Includes a special code XX for NO BIRDS PRESENT
  - The list provides both species name and code for consistent annotation across datasets

- Explanatory information: Habitat codes
  - The BTO habitat recording system is hierarchical:
    - Level 1: main habitat (A–J)
    - Level 2: main category
    - Level 3 and Level 4: subcategory details
  - Major groups include A: WOODLAND, B: SCRUBLAND, C: Semi-natural Grassland/Marsh, D: HEATHLAND AND BOGS, E: FARMLAND, F: HUMAN SITES, G: WATER BODIES (freshwater), H: COASTAL, I: INLAND ROCK, J: MISCELLANEOUS
  - Each level includes multiple codes to specify detailed habitat characteristics (e.g., Level 2, Level 3, Level 4 codes) such as disturbance from people, presence of dead wood, grazing status, proximity to roads, and vegetation structure

- Site and data quality considerations:
  - Detailed site codes and coordinates enable precise geospatial alignment
  - Quality notes may be attached to sites via ECN_BB_qtext.csv to reflect conditions affecting data quality
  - Data users should reference quality documentation when interpreting results

- Data stewardship implications for Data Stewards:
  - Ensure ongoing governance of standardized codes (sites, species, habitats) and alignment with external datasets (BTO)
  - Maintain and update the supporting documentation to reflect any code changes or site status updates
  - Facilitate data discovery via the ECN data portal and ensure proper attribution and data-use acknowledgments
  - Monitor data availability and embargo considerations and communicate any limitations to users
  - Manage data transfers and updates across multiple formats and large datasets; provide guidance and tools for data creators to meet standards

- Endnotes and access:
  - Additional information available at the ECN data portal and ECN catalogue link
  - Users are encouraged to acknowledge data use and provide reprints for publications citing ECN data