# ECN Butterfly Monitoring Data Description

- Overview
  - Dataset originator: ECN Data Centre (http://data.ecn.ac.uk; ecn@ceh.ac.uk), Centre for Ecology and Hydrology.
  - Data providers: UK government departments and agencies involved in environmental change monitoring (list includes DEFRA, Natural England, Environment Agency, Scottish Government, Welsh Government, and others).
  - Purpose and usage: Butterfly monitoring data collected under the national Butterfly Monitoring Scheme; acknowledges data usage and requests a reprint of publications citing the data.
  - Protocol reference: butterflyProtocol.pdf accompanying the document.

- Protocol Summary
  - Sampling design: Butterflys recorded on transects divided into up to 15 sections.
  - Protocol: National Butterfly Monitoring Scheme methodology (Biological Records Centre, CEH).
  - Field method: Transect walked weekly from 1 April to 29 September; observers record butterflies flying within or passing through a 5m x 5m x 5m imaginary box.
  - Environmental conditions: Temperature 13–17°C and sunshine at least 60%.
  - Quality: Use accompanying quality information when using the data.

- Data Structure
  - Core fields: SITECODE (site code), LCODE (location ID), SDATE (date of data recording), SECTION (transect section ID), FIELDNAME (species code), VALUE (measured value).

- Site Codes
  - 12 ECN sites (T01–T12) with site names, coordinates, and dataset date ranges. Examples:
    - T01 Drayton; coordinates 52°11'38" N, 1°45'52" W; 14-Apr-1993 to 19-Dec-2012.
    - T12 Cairngorms; coordinates 57°6'59" N, 3°49'47" W; 06-Oct-1999 to 26-Dec-2012.
  - Each site includes a specific date range within the dataset.

- Species List
  - Extensive coded butterfly list with numeric codes, Latin names, and common names (e.g., 2: Aglais urticae – Small tortoiseshell; 10: Aporia crataegi – Black-veined white; 29: Coenonympha pamphilus – Small heath; 90: Papilio machaon – Swallowtail; 122: Vanessa atalanta – Red admiral; 123: Cynthia cardui – Painted lady; etc.).
  - Complete mapping provided in the document.

- Additional Information
  - ECN_IB2.csv contains supplementary data: SITECODE, LCODE, SDATE, SHOUR, SMINS, RECORDER, RECCODE, TEMP, SUNPERC, WSPEEDB, WEEK.

- Quality Information
  - ECN_IB_qtext.csv provides quality metadata: LCODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, SITECODE, DESCRIPTION.
  - Details accompany quality notes for data reliability and applicability.

- GIS and Data Integration Considerations
  - Spatial joining: Use SITECODE and LCODE to link site information with geographic coordinates.
  - Temporal analysis: Use SDATE and WEEK for time-series analyses.
  - Data quality: Leverage ECN_IB_qtext.csv to filter or flag data quality issues before GIS visualization.
  - Data packaging: Data may be spread across multiple providers and files (ECN_IB2.csv and ECN_IB_qtext.csv) requiring consolidation.

- Usage Guidance
  - Acknowledge ECN data usage in outputs; share reprints of publications citing the data.
  - Reference accompanying butterflyProtocol.pdf for methodological context and data collection specifics.

- Challenges and Considerations for GIS Specialists
  - Data fragmentation across multiple sources and formats.
  - Potential data gaps and resolution variability between sites.
  - Need for data cleaning and standardization prior to integration into GIS workflows.
  - Ensuring consistent interpretation of quality metadata when filtering spatial-temporal analyses.