# Dataset Originator E CN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

- Overview
  - UK Environmental Change Network (ECN) butterfly monitoring dataset, part of the national Butterfly Monitoring Scheme.
  - Data collected from 12 ECN sites across the UK, with transects conducted weekly during the butterfly season.
  - Protocol emphasizes standardized transect methodology, environmental context (temperature, sunshine), and quality information to accompany data usage.

- Data provenance and providers
  - Data originator: ECN Data Centre, Centre for Ecology and Hydrology.
  - Data providers: consortium of UK government departments and agencies funding site monitoring and network coordination (e.g., DEFRA, Natural England, Environment Agency, Scottish and Welsh agencies, NERC, etc.).
  - Use acknowledgement required: credit the datasets and send one reprint of publications citing the data.

- Protocol and collection methodology
  - butterfly observations recorded along a transect divided into up to 15 sections.
  - Weekly walks from April 1 to September 29 each year.
  - Observers record the number of butterflies within a defined 5m x 5m x 5m box in front of the observer.
  - Conditions: temperature between 13-17°C and at least 60% sunshine.
  - Use accompanying quality information when analyzing the data.

- Data structure and schema
  - Core fields:
    - SITECODE: Unique ECN site code
    - LCODE: Location ID
    - SDATE: Date of data recording
    - SECTION: Transect section ID
    - FIELDNAME: Species code
    - VALUE: Count or measurement value
  - Structure supports site-level, transect-level, and species-level data integration.

- Site codes and metadata
  - 12 sites (e.g., Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Y Wyddfa/Snowdon, Cairngorms).
  - Each site entry includes location coordinates and the dataset date range (varies by site, e.g., 1992–2012 for several sites; some earlier or later ranges noted).
  - Site-specific dates indicate when data are available within the ECN dataset.

- Species list and coding
  - Species are encoded by numeric codes with Latin and common names provided (e.g., 2 = Aglais urticae - Small tortoiseshell, 10 = Aporia crataegi - Black-veined white, etc.).
  - Large, multi-entry list covers a wide range of UK butterfly species observed in the network.

- Additional information and quality data
  - ECN_IB2.csv provides supplementary information (e.g., SITECODE, LCODE, SDATE, SHOUR, SMINS, RECORDER, RECCODE, TEMP, SUNPERC, WSPEEDB, WEEK).
  - ECN_IB_qtext.csv contains quality information for locations and variables, with date ranges and descriptive notes.
  - Quality data support assessment of data reliability and temporal coverage.

- Usage notes and governance
  - Data use requires acknowledgement to ECN and related providers.
  - Researchers should reference accompanying quality information and protocol documents (e.g., butterflyProtocol.pdf) when interpreting results.
  - Data are designed for long-term environmental change research and cross-site comparability, with standardized collection and metadata to facilitate reuse.