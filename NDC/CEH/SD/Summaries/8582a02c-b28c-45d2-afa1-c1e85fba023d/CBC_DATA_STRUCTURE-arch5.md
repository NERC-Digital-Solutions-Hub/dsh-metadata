# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

- Acknowledgement and governance
  - ECN Data Centre hosts data for the UK Environmental Change Network (ECN) programme.
  - Program funded by a consortium of UK government departments and agencies; sites monitored or network-coordinated by partner organisations.
  - Users are asked to acknowledge ECN data use and to send one reprint of any publication citing ECN data.

- Protocols and data standards
  - ECN applies standard operating procedures to ensure data comparability across sites.
  - Usage methodology is based on the Common Birds Census (CBC) with a mapping-based, visit-based approach during the breeding season; data can include territory counts (CLUST) and nests (NEST).
  - Since 1999 CBC was largely replaced by Breeding Bird Survey (BBS); historical CBC data are available for comparison and some sites have pre-ECN data.
  - Users should consult accompanying quality information when using data.

- Data content and structure
  - Data cover bird populations collected at ECN sites (site-level data with limitations for linking population changes to environmental change at fine scales).
  - Key data fields for download:
    - SITECODE: unique ECN site code (e.g., T01 Drayton, T03 Hillsborough, etc.)
    - SYEAR: sampling year
    - BI_SPEC: bird species code
    - CLUST: number of territories (clusters)
    - NEST: number of nests
  - Supporting documentation (ECN_cbc_qtext.csv) includes SITECODE, SYEAR, BI_SPEC, and issue descriptions affecting data.
  - Explanatory site information provides site names, coordinates, and BTO land-use classifications (e.g., Farmland, Woodland, Special).
  - Explanatory bird species codes map to full species names; a comprehensive, though lengthy, code table is provided to interpret BI_SPEC.

- Site coverage and temporal range
  - Detailed site lists and date ranges vary by location:
    - Alice Holt: 1994–2007
    - Drayton: 1993–1999
    - Hillsborough: 1993–2001
    - North Wyke: 1993–2002
    - Porton Down: 1994–1998
    - Rothamsted: 1991–1997
    - Wytham: 1971–2003
  - The CBC data were standard at lowland ECN sites until 1999, after which BBS data became the standard; historical data exist for context and comparison.

- Data access and usage guidance
  - Data downloadable through site codes and year with species and counts; additional context available in explanatory files.
  - Encouraged to use accompanying quality metadata to understand data limitations and context.
  - Data are suitable for national-scale interpretation and should be cross-compared with broader datasets (e.g., BTO) to mitigate site-scale limitations.

- Practical considerations for data stewards
  - Ensure metadata accuracy and consistency across sites and years.
  - Maintain the mapping between SITECODEs, site descriptions, and coordinates.
  - Preserve and update the CBC/BBS context as protocols evolve, including documenting any transitions or compatibility notes.
  - Manage and communicate data provenance, existing date ranges, and any data quality issues to users.

- Additional context and codes
  - Site codes and their explanatory details (names, coordinates, land-use classification) are provided to support proper interpretation and integration with other datasets.
  - The comprehensive bird species code table supports accurate interpretation of BI_SPEC values across years and sites.