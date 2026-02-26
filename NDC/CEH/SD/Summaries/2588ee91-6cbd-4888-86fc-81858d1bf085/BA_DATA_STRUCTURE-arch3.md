# ECN Bat Monitoring Dataset

- Dataset Originator: ECN Data Centre (http://data.ecn.ac.uk), Centre for Ecology and Hydrology; contact ecn@ceh.ac.uk
- Dataset Owners: UK government departments and agencies sponsoring ECN (e.g., AFBI, BBSRC, NRW, DSTL, Defra, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, NIEA, SEPA, Scottish Government, SNH)
- Acknowledgement: ECN requests acknowledgement of data use and one reprint of any publication citing ECN data

- Protocol
  - ECN uses standard operating procedures to ensure site comparability
  - A  accompanying PDF explains data collection methods and quality information

- Usage Notes
  - Bat activity recorded along transects using bat detectors; species identified via detector output
  - Transect walks occur four times yearly in specific date windows; surveys not conducted in heavy rain or strong winds
  - Methodology provides broad insight; limitations in resolving precise relationships between bat populations and environmental change, mitigated by linking with broader monitoring programs
  - Use accompanying quality information when analyzing data

- Data Download (key fields)
  - SITECODE: Unique ECN site code
  - SDATE: Sampling date
  - TRANSECT: Transect identifier
  - BATLOC_ID: Location where bat seen/heard (unique per survey date)
  - FIELDNAME: Variable measured (species codes)
  - VALUE: Value of the measurement
  - ACTS: Activity code – bat seen
  - ACTH: Activity code – bat heard
  - ACTF: Activity code – bat feeding buzz heard

- Supporting Documentation
  - ECN_BA2.csv: Survey conduct information (bat detector type, frequency settings, comparisons, audio analysis)
  - ECN_BA3.csv: Habitat observations along transect (habitat codes)
  - ECN_BA_qtext.csv: Textual notes on data quality and circumstances affecting data quality

- Explanatory Information
  - Site Codes: List of ECN sites (e.g., T01 Drayton, T02 Glensaugh, T03 Hillsborough, etc.) with geographic coordinates
  - Species Codes: Codes for bat species and common names (e.g., Bb Barbastella barbastellus, Pp Pipistrellus, Nl Nyctalus leisleri, etc.)
  - Habitat Codes: Codes for habitat context near sighting (HAB1, HAB2, HAB3) with descriptions and units

- Explanatory Information – Habitat Types
  - A comprehensive set of habitat type categories (1–43) including hedgerows, treelines, stone walls, various water features (ditches, streams, rivers, canals), woodlands (semi-natural and plantations), scrub, beaches, wetlands, ponds, lakes, different grasslands (upland/lowland unimproved/improved/semi-improved), arable, amenity grassland, rock surfaces, quarries, bare soil, built land, and an “Others” category

- Additional Information
  - Further details about ECN sites available at the ECN site catalogue
  - The data come with quality metadata to support proper interpretation and comparability

- Endnote
  - The document emphasizes data provenance, standardization, and governance to support transparent reuse and informed environmental monitoring decisions