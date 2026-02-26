# ECN Butterfly Monitoring Dataset Protocol

- Overview
  - Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology (http://data.ecn.ac.uk; ecn@ceh.ac.uk)
  - Dataset Owners: UK Environmental Change Network (ECN) programme, funded by multiple UK government departments and agencies
  - Purpose: Provide a consistent, monitorable record of environmental change indicators via standardized butterfly monitoring data; aimed at enabling scrutiny of environmental health and policy performance over time

- How the data are produced and standardized
  - ECN uses standard operating procedures to ensure comparability across sites
  - Methodology follows the national Butterfly Monitoring Scheme coordinated by the Biological Records Centre (CEH)
  - Data collection protocol described in accompanying ib.pdf

- Field collection details (butterfly monitoring)
  - Transect divided into up to 15 sections
  - Transect walked weekly from 1 April to 29 September each year
  - Observers record butterflies flying within or passing through a 5 m (width) x 5 m (height) x 5 m (in front) imaginary box
  - Temperature and conditions: recording preferred when 13–17°C with at least 60% sunshine; if temperature >17°C, recording can occur in any conditions except rain; northern upland sites capped at 15°C
  - Use accompanying quality information when utilizing the data

- Data structure and download formats
  - Core data fields (ECN_IB.csv): SITECODE (site), LCODE (location ID within site), SDATE (date), SECTION (transect section), FIELDNAME (species code), VALUE (observation value), BROODED/D (brood information)
  - Supporting documentation (ECN_IB2.csv): adds SHOUR (hour), SMINS (minutes), RECORDER/RECCODE, TEMP, SUNPERC, WSPEEDB, WEEK
  - Quality notes (ECN_IB_qtext.csv): site managers’ qualitative remarks about data quality with FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION
  - Species and site codes are standardized and documented below

- Site codes (ECN sites)
  - T01 Drayton; coordinates 52° 11' 37.95" N, 1° 45' 51.95"W
  - T02 Glensaugh; 56° 54' 33.36" N, 2° 33' 12.14"W
  - T03 Hillsborough; 54° 27' 12.24" N, 6° 4' 41.26"W
  - T04 Moor House - Upper Teesdale; 54° 41' 42.15" N, 2° 23' 16.26"W
  - T05 North Wyke; 50° 46' 54.96" N, 3° 55' 4.10"W
  - T06 Rothamsted; 51° 48' 12.33" N, 0° 22' 21.66"W
  - T07 Sourhope; 55° 29' 23.47" N, 2° 12' 43.32"W
  - T08 Wytham; 51° 46' 52.86" N, 1° 20' 9.81"W
  - T09 Alice Holt; 51° 9' 16.46" N, 0° 51' 47.58"W
  - T10 Porton Down; 51° 7' 37.83" N, 1° 38' 23.46"W
  - T11 Y Wyddfa - Snowdon; 53° 4' 28.38" N, 4° 2' 0.64"W
  - T12 Cairngorms; 57° 6' 58.84" N, 3° 49' 46.98"W
  - Additional site information is available at ECN catalogue page

- Species codes
  - Numeric codes mapped to Latin and common names (e.g., 10 = Black-veined white; 100 = Small white; 102 = Silver-studded blue; 104 = Comma; 106 = Common blue; 108 = Bath white; 110 = Grizzled skipper; 112 = Black hairstreak; 113 = White-letter hairstreak; 115 = Brown hairstreak; 116 = Purple hairstreak; 118 = Lulworth skipper; 119 = Essex skipper; 12 = Dark green fritillary; 120 = Small skipper; 122 = Red admiral; 123 = Painted lady; etc.)
  - Includes extensive list of commonly monitored UK butterflies; some codes (e.g., XX) indicate no butterflies present
  - The full mapping is provided in the dataset documentation

- Usage and acknowledgement
  - ECN requests acknowledgement of data use and one reprint of any publication citing ECN data

- Access and goals for analysts
  - Data are stored and available through ECN data portals
  - Outputs are typically reports, maps, and charts enabling categorization of environmental health against standards
  - Aims to enable broader data value by combining ECN datasets with other relevant data sources

- Key challenges highlighted
  - Increasing the value of datasets by integrating with other data (beyond single-use purposes)
  - Enabling access to the underlying data used to create final outputs for broader scrutiny and reuse