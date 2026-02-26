# ECN_MA

- Purpose and scope
  - The ECN Data Centre provides hourly weather and environmental summaries derived from 5-second measurements collected by Automatic Weather Stations (AWS) across multiple ECN sites.
  - The dataset supports understanding environmental change and is funded by a consortium of UK government departments and agencies; site monitoring and network coordination are managed by this group.

- Data provenance, ownership, and governance
  - Dataset Originator: ECN Data Centre (Centre for Ecology and Hydrology).
  - Dataset Owners: A consortium including Agri-Food and Biosciences Institute, BBSRC, Natural Resources Wales, Dstl, DEFRA, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, NIEA, SEPA, Scottish Government, and SNH.
  - Usage and attribution: Users are requested to acknowledge ECN data in publications and to send one reprint of any publication citing the data.
  - Protocol and standards: ECN employs standard operating procedures to ensure data comparability across sites; a detailed protocol is referenced (ma.pdf).
  - Data sharing and governance: Data may be publicly shared, but this can pose barriers; metadata quality and governance processes are emphasized to ensure datasets meet standards and remain up to date.

- Data structure and content
  - Core data fields for download:
    - SITECODE: Unique code for each ECN site.
    - AWSNO: Individual AWS at a location (multiple AWS can operate concurrently at the same site).
    - SDATE: Sampling date.
    - SHOUR: Sampling hour.
    - FIELDNAME: Variable being measured.
    - VALUE: Measured value.
  - Quality and supplemental information
    - ECN_MA_qtext.csv contains site manager notes explaining circumstances that may affect data quality; associated quality text is viewable in the quality information.
  - Site codes and locations
    - Sites are coded T01 to T12 with names (e.g., Drayton, Glensaugh, Hillsborough, Moor House, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Y Wyddfa/Snowdon, Cairngorms) and coordinates.
    - Many sites have had two AWS units operate concurrently; users must note the AWSNO when using data from such sites.
  - Variables and units (representative examples)
    - Albedo (Wm-2; ground and sky), Dry bulb temperature (°C), Net Radiation (Wm-2), Rainfall (mm, total), Relative Humidity (%), Solar Radiation (Wm-2), Soil temperature (°C at 10 cm and 30 cm), Surface wetness (minutes), Soil moisture (gypsum block and theta probe at various depths), Wind direction (degrees), Wind speed (m/s), and related metrics.
  - Site documentation and data quality
    - Explanatory information provides site-specific notes (e.g., when multiple AWS units exist at a site).
    - The accompanying documentation explains data collection methods and any site-specific considerations (including replacements and cross-checks).

- Usage guidance and considerations
  - When using the data, consult the accompanying quality information to assess data reliability and any caveats.
  - Be aware of concurrent AWS units at sites and use the AWSNO to disambiguate measurements.
  - Acknowledge ECN data usage and consider sharing a reprint of publications citing the data.

- Access, metadata, and documentation
  - Additional information on ECN sites is available at the ECN catalogue (link provided in the documentation).
  - Supporting documentation and variable definitions help interpret the data (e.g., mapping of FIELDNAME to measured variables and units).

- Key challenges for monitoring frameworks (as highlighted by the document)
  - Data gaps and data quality issues (metadata gaps, site-specific quality notes).
  - Access constraints and data-sharing barriers.
  - Silos or fragmentation across organisations and datasets.
  - The need for clear, accessible metadata and data governance to ensure timeliness, comparability, and reuse.

- Summary of the foundational metadata
  - Originator: ECN Data Centre; Field data from hourly summaries of 5-second AWS measurements.
  - Coverage: Multiple ECN sites (T01–T12) with potential concurrent AWS units per site.
  - Primary fields: SITECODE, AWSNO, SDATE, SHOUR, FIELDNAME, VALUE.
  - Quality context: ECN_MA_qtext.csv provides site-specific quality notes; usage should incorporate quality information.