# Supporting documentation for UK Environmental Change Network (ECN) bird data: 1995-2012 (Rennie, S. et al (2015) http://doi.org/10.5285/c616149a-fb19-4d6b-a9e5-84363538ed7e)

- The ECN bird data (1995-2012) are managed by the ECN Data Centre (data.ecn.ac.uk) and CEH, funded by a consortium of UK government departments/agencies.
- Users must acknowledge ECN data use and send one reprint of any publication citing ECN data.

Overview and governance
- ECN operates under a consortium of sponsoring organisations (e.g., Defra, Natural England, NERC, Scottish Government, etc.) funding site monitoring and network coordination.
- Data use requires acknowledgment and submission of a reprint, enabling impact tracking and demonstration of data value for environmental-change research.
- The dataset is designed to be used in conjunction with broader monitoring programs (notably the Breeding Bird Survey by BTO), due to national-scale data limitations for linking population trends to environmental change.
- The Breeding Bird Survey replaced earlier ECN protocols (Common Bird Census at lowland sites and Moorland Bird Survey at upland sites); accompanying quality information should be used when analyzing data.

Data scope and methodology
- Bird species are recorded on transects within 1 km squares; distance from transect is captured.
- Methodology follows the Breeding Birds Survey (BTO); transects are walked twice per year.
- Data are national-scale transect data with limited site-based environmental linkage; integration with broader datasets is advised to interpret drivers of change.
- Early ECN protocols (before 1995) were replaced by the Breeding Bird Survey at ECN sites.

Data structure and content
- Core data fields (tabular structure):
  - SITECODE, Description: Site code
  - SITECODE, Data type
  - LCODE, Description: Location code
  - LCODE, Data type
  - VISIT, Description: Visit (E=early, L=late)
  - VISIT, Data type
  - SDATE, Description: Sampling date
  - SDATE, Data type
  - FROM_HOUR / FROM_MINS, TO_HOUR / TO_MINS (metadata for survey timing)
  - TRANSECT, Description: Transect
  - FIRSTHL1/SECONDHL1, etc.: Habitat codes (Levels 1–4)
  - FIELDNAME, Description: Bird species code
  - VALUE, Description: Count value
  - DISTANCE, Description: Distance category (within 25 m, 25–100 m, >100 m, or in flight)
- Site codes:
  - Example sites (T01 Drayton to T12 Cairngorms) with coordinates and date ranges (1995–2010/2012 ranges)
- Bird species codes:
  - Extensive mapping of two-letter and short codes to Latin/common names (e.g., AC = Arctic Skua, BT = Blue Tit, BI = Black-headed Gull, etc.)
  - Includes a wide range of common, rarer, and seasonal species; establishes a controlled vocabulary for species observations.
- Habitat and metadata (ECN_BB2.csv and ECN_BB3.csv):
  - ECN_BB2.csv: Survey observed on the transect; fields for weather and survey timing:
    - FROM_HOUR/MINS, TO_HOUR/MINS
    - CLOUD, RAIN, WIND, VISIBILITY (weather codes per BTO)
  - ECN_BB3.csv: Habitats observed on the transect; fields for habitat codes:
    - FIRSTHL1/SECONDHL1, FIRSTHL2/SECONDHL2, FIRSTHL3A/SECONDHL3A, FIRSTHL3B/SECONDHL3B, FIRSTHL4A/SECONDHL4A, FIRSTHL4B/SECONDHL4B
    - Year, TRANSECT, Habitat Level 1–4 codes
- Habitat coding system (Levels 1–4):
  - Level 1 code groups (A–J) and Level 2–4 codes per habitat type (Woodland, Scrubland, Semi-natural Grassland/Marsh, Heathland/Bogs, Farmland, Human Sites, Water Bodies, Coastal, Inland Rock, Miscellaneous)
  - Each habitat type includes detailed Level 2–4 codes describing subcategories (e.g., A: Woodland; Level 2: Broadleaved/Coniferous/Mixed; Level 3/4: disturbance, shrub density, dead wood, management, etc.)
  - Examples provided for each habitat type, including near-road disturbance, grazing, boundary features, and vegetation structure

Data integrity, interoperability, and usage notes
- The dataset uses a rich, hierarchical habitat coding scheme and a comprehensive species code list, which supports detailed habitat-management and species-habitat analyses but requires careful metadata alignment for interoperability with other datasets.
- The accompanying metadata tables (ECN_BB2.csv and ECN_BB3.csv) are essential for proper interpretation of survey conditions and habitat context; ensure these are accessible with the dataset when enabling reuse.
- Researchers are advised to use ECN data in combination with broader monitoring programs (e.g., BTO data) to contextualize population-environment relationships.
- Data stewardship considerations include maintaining consistency of codes across time, ensuring updates to habitat and weather metadata accompany observed data, and clearly documenting any data quality flags or exclusions.

Practical considerations for data stewards
- Ensure proper data governance: track data provenance, acknowledge sponsors, and manage data sharing with clear usage guidance and citation requirements.
- Maintain metadata quality: keep ECN_BB2.csv and ECN_BB3.csv up to date and ensure alignment with the primary observation dataset (SITECODE, LCODE, VISIT, SDATE, TRANSECT, FIELDNAME, VALUE, DISTANCE).
- Support interoperability: document and preserve the structure of Site codes, Location codes, Visit designations, and the hierarchical habitat codes; provide mappings or crosswalks if integrating with other datasets.
- Communicate limitations: clearly denote that site-based data provide limited detail on population-environment links and that supplementary datasets are recommended for deeper analyses.
- Facilitate reuse: provide guidance on how to cite ECN data, offer access through the ECN Data Centre, and encourage submission of resulting reprints to ECN for impact tracking.

End notes
- The document emphasizes (a) data governance and sponsor attribution, (b) methodological context (Breeding Bird Survey, transects, distance codes), (c) detailed data schema for observational data, and (d) rich metadata on weather, habitat, and site characteristics to support robust data interpretation and reuse.