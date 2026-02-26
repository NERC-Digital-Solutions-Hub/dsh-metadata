# Common Birds Census (CBC) Data from the ECN

- Overview
  - Data originate from the UK Environmental Change Network (ECN) and are maintained by the ECN Data Centre (Centre for Ecology and Hydrology).
  - Dataset owners are a consortium of UK government departments and agencies funding site monitoring and network coordination (e.g., DEFRA, Natural England, NERC, Scottish Government, Welsh Government, etc.).
  - ECN requests acknowledgement of data use and a reprint of any publication that cites ECN data.

- Data Collection & Protocol
  - Based on the Common Birds Census (CBC) methodology.
  - CBC involves visits to all parts of a defined plot during the breeding season, recording bird contacts by sight or song on large-scale maps.
  - Outputs include territory counts (CLUST) and, for some species, nest counts (NEST) or both.
  - CBC is designed as a national-scale survey; site-based ECN data provide limited detail on precise population-environment relationships. It is advised to supplement ECN data with data from broader monitoring programs (e.g., BTO).
  - The CBC protocol at ECN sites was largely replaced by the Breeding Bird Survey (BBS) after 1999, with historical CBC data continuing at some sites for comparability.
  - See accompanying bc.pdf for detailed data collection explanations.

- Data Structure & Variables
  - Primary data fields for download:
    - SITECODE: ECN site code
    - SYEAR: Sampling year
    - BI_SPEC: Bird species code
    - CLUST: Number of territories (clusters)
    - NEST: Number of nests (for applicable species)
  - Supporting documentation for quality and issues:
    - ECN_cbc_qtext.csv (SITECODE, SYEAR, BI_SPEC, DESCRIPTION of data issues)

- Site Information (Ranged data per site)
  - Alice Holt: 1994–2007
  - Drayton: 1993–1999
  - Hillsborough: 1993–2001
  - North Wyke: 1993–2002
  - Porton Down: 1994–1998
  - Rothamsted: 1991–1997
  - Wytham: 1971–2003
  - Note: Some sites include pre-ECN or overlapping data; ranges vary by site.

- Explanatory Information: Site Codes
  - Examples of site codes and names, with locations and Broad Tree/BBTO class (e.g., T01 Drayton, farmland; T03 Hillsborough, woodland; T05 North Wyke, woodland; T06 Rothamsted, farmland; T08 Wytham, woodland; T09 Alice Holt, woodland; T10 Porton Down, special).
  - Additional site metadata and a link to further site information:
    - Explanatory Information: Site codes
    - https://catalogue.ceh.ac.uk/id/813712d4-d1624ede-aff8-cf1c337bdc27

- Explanatory Information: Bird Species Codes
  - The dataset uses extensive two-letter and short codes for a wide range of bird species (e.g., AC = Arctic Skua; BC = Blackcap; BH = Black-headed Gull; BT = Blue Tit; etc.).
  - The mapping covers many species with corresponding full names, enabling standardized cross-site analyses.
  - For the full list, see the provided codes in the dataset documentation.

- Quality, Use, & Limitations
  - Use the accompanying quality information to interpret data reliability.
  - The ECN CBC data are best used in conjunction with broader datasets (e.g., BTO) to infer relationships between population levels and environmental change.
  - The dataset provides standardized, site-comparable measures (territories and nests) suitable for temporal monitoring and trend analysis within the ECN framework.

- Availability, Access, & Attribution
  - Data download fields are standardized and structured for easy ingestion (SITECODE, SYEAR, BI_SPEC, CLUST, NEST).
  - Supporting docs and quality notes are available to accompany the data.
  - ECN requests acknowledgment in publications and one reprint of any publication citing the data; these datasets are stored and accessible via ECN portals and the CEH Environmental Information Platform.

- Data Use Guidance for Analysts Monitoring the Environment
  - Aligns with the aim of presenting environmental health over time in a consistent, comparable format.
  - Provides standardized, time-series data across multiple ECN sites with clear site metadata and species coding.
  - Facilitates cross-site comparisons and monitoring of avian community responses to environmental change, while highlighting the need to integrate with broader monitoring programs to overcome site-level limitations.