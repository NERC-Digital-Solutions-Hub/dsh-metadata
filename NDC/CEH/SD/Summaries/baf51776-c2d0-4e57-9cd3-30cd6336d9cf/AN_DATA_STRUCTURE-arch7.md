# ECN Data Centre NO2 Passive Diffusion Tube Dataset

- Origin and purpose
  - Dataset originated from the ECN Data Centre (Centre for Ecology and Hydrology).
  - Part of the UK Environmental Change Network (ECN) program; monitors environmental change across multiple sites.
  - Focuses on measuring Nitrogen Dioxide (NO2) using passive diffusion tubes deployed for two-week periods.

- Dataset owners and access
  - Dataset owners: The UK Environmental Change Network (ECN) programme, funded by a consortium of UK government departments and agencies.
  - Acknowledgement requested for data use; request a reprint of any publication citing the data.

- Data content and structure
  - Primary download fields:
    - SITECODE: Unique ECN site code.
    - SDATE: Sampling date.
    - TUBEID: Tube identifier (experimental or blank).
    - FIELDNAME: Variable measured (e.g., NO2, WEIGHTNO2, NO2PPB, TDIFF, Q1–Q8).
    - VALUE: Measured value.
  - NO2 measurement details
    - WEIGHTNO2: Weight of NO2 on the mesh (micrograms).
    - NO2: NO2 concentration (micrograms per cubic meter).
    - NO2PPB: NO2 concentration (parts per billion).
    - TDIFF: Exposure time (minutes).
    - Q1–Q8: Quality codes (integers).
  - Supporting data
    - ECN_AN2.csv: Site deployment metadata
      - SITECODE, TUBEID, DEPDATE, DEPHOUR, DEPMINS, SDATE, SHOUR, SMINS.
    - ECN_AN_qtext.csv: Quality text explanations
      - SITECODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION.
  - Quality codes
    - Comprehensive list of codes (e.g., 100, 101–187, 200–239, 501–513, 999) with descriptions for data loss, sampling issues, field and laboratory problems, and unusual events.
    - 999 indicates an unusual event; see accompanying quality text for details.

- Site and spatial context
  - Explanatory information lists 12 ECN sites (T01–T12) with site names and coordinates, enabling geospatial mapping:
    - Examples: Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon (Y Wyddfa), Cairngorms.
  - Additional site information and location details available via the CEH catalogue link provided in the documentation.

- Protocol and data quality
  - Standard operating procedures to ensure comparability across sites.
  - Passive diffusion tubes deployed for two-week periods, with blank tubes included as quality checks.
  - Quality information accompanies data to aid in interpretation and filtering.

- Usage notes and documentation
  - Use accompanying quality information when analyzing data.
  - Quality text for non-standard issues is embedded in ECN_AN_qtext.csv (linked via SITECODE and FIELDNAME with date ranges and descriptions).
  - Site-specific and measurement-specific context is available in ECN_AN2.csv and ECN_AN_qtext.csv.
  - Further site metadata and information: https://catalogue.ceh.ac.uk/id/813712d4-d1624ede-aff8-cf1c337bdc27

- Practical GIS considerations
  - Data are suitable for map-based visualization of NO2 concentration across ECN sites over time.
  - Integrate SITECODE with site coordinates for spatial mapping; join by DEPDATE/SDATE for temporal visualization.
  - Pay close attention to Q1–Q8 quality codes and 999 unusual-event entries to filter or annotate datasets.
  - Ensure alignment of field names and units when aggregating (micrograms/m3 or ppb) and when calculating derived metrics.
  - Handle missing values and quality flags to maintain map reliability.

- Processing tips
  - Merge NO2 VALUE with SITECODE and spatial coordinates to create site-time NO2 maps.
  - Use ECN_AN2.csv to enrich the dataset with deployment timing (DEPDATE/DEPHOUR/DEPMINS) and sampling times (SDATE/SHOUR/SMINS).
  - Use ECN_AN_qtext.csv to attach quality context to measurements flagged with quality codes (Q1–Q8) and 999 events.
  - Confirm site coordinates against the CEH catalogue for accurate georeferencing before mapping.