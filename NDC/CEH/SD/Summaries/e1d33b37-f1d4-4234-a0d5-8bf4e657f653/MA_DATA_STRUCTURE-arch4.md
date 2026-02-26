# UK Environmental Change Network (ECN) meteorology data: 1992-2012

- Overview
  - Hourly meteorology summaries derived from 5-second data collected by Automatic Weather Stations (AWS) across ECN sites.
  - Data cover 1992–2012 and are managed by the ECN Data Centre.
  - Intended to support research into environmental change; data use should be acknowledged and users should send a reprint of publications citing the data.

- Data provenance and governance
  - Dataset originator: ECN Data Centre (Centre for Ecology and Hydrology).
  - Dataset owners: UK ECN programme funded by a consortium of government departments and agencies (multiple sponsors listed).
  - Usage attribution: acknowledge data use and provide one reprint of any publication citing the data.
  - Protocol and re-use: Protocol referenced in MA.pdf within the ECN data holdings (EIDC Hub).

- Data content and structure
  - Observation type: hourly summaries derived from approximately 5-second AWS measurements; some sites operated multiple AWS units in parallel to enable cross-checking.
  - Site coverage: 12 ECN sites (Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon, Cairngorms) with site-specific AWS histories.
  - AWS details: most sites used more than one AWS over time; AWS replacements are indicated by AWSNo; cross-checks between concurrent AWS units are common.
  - Data structure and metadata: data tables include fields for site, AWS, sampling date/time, and observations; accompanying quality information is essential for proper use.
  - Variables and units: a comprehensive set of meteorological variables, including but not limited to:
    - Albedo (ground and sky), dry/wet bulb temperatures, net radiation, rainfall, relative humidity, solar radiation, soil temperatures (10 cm, 30 cm), surface wetness, soil moisture (gypsum block, theta probe at 10 cm and 20 cm), volumetric water content, wind direction, wind speed, wind-related temperatures (wet bulb), etc.
  - Data schema highlights: fields and values organized with site codes, AWS identifiers, timestamps (sampling date and hour), and measurement values; field names and units are defined in the provided data dictionaries.

- Data quality, caveats, and usage notes
  - Primary data quality caveat: ensure the accompanying quality information is consulted before analysis.
  - Temporal coverage caveats: AWS replacements and site-specific date ranges may create gaps or discontinuities; cross-check AWSNo when interpreting concurrent measurements.
  - Data provenance notes: detailed site coordinates and time ranges for AWS1 and AWS2 are recorded to aid data integration and cross-site analyses.

- Access, usage guidance for data leaders
  - Access portal: ECN data holdings via the EIDC Hub; protocol document MA.pdf available to assist in re-use.
  - Practical guidance: verify data quality flags, be aware of multiple AWS at a single site, and use site-specific AWS metadata when aggregating across sites.
  - Collaboration and standards: data is structured to support discovery and reuse within a broader data community; documentation and site-level metadata facilitate integration into larger data systems.

- Citation and re-use considerations
  - Acknowledge the ECN data usage in publications.
  - Provide one reprint of any publication citing the dataset to ECN.
  - Reference the dataset originator and dataset owners in any reports or analyses.

- Summary of relevance for data leadership
  - Demonstrates a well-documented, multi-site meteorological data resource with clear governance, provenance, and usage terms.
  - Emphasizes the importance of comprehensive metadata, data quality information, and explicit attribution for data products intended for policy and research collaboration.
  - Illustrates managing data across a network of partners, handling historical data with evolving instrumentation, and maintaining data discoverability for wider regional or national environmental analysis.