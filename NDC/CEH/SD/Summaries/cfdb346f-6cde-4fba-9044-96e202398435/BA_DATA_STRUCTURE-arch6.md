# UK Environmental Change Network (http://www.ecn.ac.uk) Bats (BA)

- Overview
  - ECN Bats dataset (BA) with data captured and organized by the ECN Data Centre; data are owned by the UK Environmental Change Network and sponsored by a consortium of UK government departments and agencies.
  - Sponsors include: Agri-Food and Biosciences Institute, BBSRC, Natural Resources Wales, DSTL, DEFRA, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, Northern Ireland Environment Agency, Scottish Environment Protection Agency, Scottish Government, and Scottish Natural Heritage.

- Acknowledgment and use
  - Users are asked to acknowledge the data source in publications that cite ECN data.
  - Users should send ECN one reprint of any publication that cites the data.

- Survey protocol (bat transect methodology)
  - Bat species are mapped (via bat detector) and behavior recorded along transects.
  - Methodology based on the Bats and Habitats survey used by Prof. S. Harris and colleagues (JNCC).
  - Each transect is walked four times per year in four three-week windows: 15 Jun–6 Jul; 7–27 Jul; 28 Jul–17 Aug; 18 Aug–7 Sep.
  - Surveys are not conducted in heavy rain or strong winds.
  - Limitations exist in relating population levels to environmental change; linking ECN results with other monitoring helps mitigate this.
  - Users should use accompanying quality information when using the data.

- Data structure and storage
  - Data are stored in Oracle in site-specific tables:
    - D1BA_xxx: bat observation data (counts by site/date/ transect and bat species).
    - D2BA_xxx: information about how the survey was conducted (detector type, frequency settings, protocols, etc.).
    - D3BA_xxx: habitat observations along transects.
  - There are 10 site tables for each data type (one per site).

- Site codes and metadata
  - Ten sites with codes and metadata:
    - T01 Drayton (52°11'37.95"N 1°45'51.95"W): 29-JUN-1993 to 05-SEP-2006
    - T02 Glensaugh (56°54'33.36"N 2°33'12.14"W): 07-JUL-1994 to 30-AUG-2012
    - T03 Hillsborough (54°27'12.24"N 6°4'41.26"W): 12-AUG-1994 to 05-SEP-2002
    - T04 Moor House - Upper Teesdale (54°41'42.15"N 2°23'16.26"W): 16-JUN-1993 to 28-AUG-2012
    - T05 North Wyke (50°46'54.96"N 3°55'4.10"W): 04-JUL-1993 to 30-AUG-2012
    - T07 Sourhope (55°29'23.47"N 2°12'43.32"W): 12-JUL-1994 to 03-SEP-2012
    - T08 Wytham (51°46'52.86"N 1°20'9.81"W): 05-JUL-1993 to 21-AUG-2012
    - T09 Alice Holt (51° 9'16.46"N 0°51'47.58"W): 29-JUN-1994 to 05-SEP-2012
    - T10 Porton Down (51° 7'37.83"N 1°38'23.46"W): 04-JUL-1994 to 03-SEP-2006
    - T11 Y Wyddfa - Snowdon (53° 4'28.38"N 4° 2'0.64"W): 16-JUL-1996 to 31-AUG-2011

- Core data fields and data types (D1BA_xxx)
  - Key fields include SITECODE, SDATE (sampling date), TRANSECT, BATLOC_ID, FIELDNAME, VALUE, ACTS/ACTH/ACTF (bat observed/heard/feeding), and related reference tables.
  - Field definitions cover site code, date, transect, location of bat sighting/heard event, field names (species codes), and observed values (counts).

- Survey metadata and measurement details (D2BA_xxx)
  - Contains metadata about the survey setup per site/date, including bat detector type, frequency settings, whether detector settings were kept or adjusted, reference comparisons, and whether sonogram analysis was used.

- Habitat observations (D3BA_xxx)
  - Holds habitat context for bat sightings on each transect.
  - Includes habitat location details (BATLOC_ID), transect information, and up to three habitat types recorded (HAB1–HAB3) with corresponding codes.

- Species codes and taxonomic mapping
  - Fieldname codes in D1BA_xxx correspond to bat species codes; each code maps to Latin and common names (e.g., Bb = Barbastella barbastellus; Pp = Pipistrellus; Ppl = Pipistrellus pipistrellus; XX = No bats found; UU = Unidentified bat, etc.).
  - A description table (M_DESC) provides mappings for these codes, enabling interpretation of counts.

- Habitats and habitat codes
  - Up to three habitat types per sighting are recorded (HAB1, HAB2, HAB3).
  - Codes 1–43 describe habitat types, ranging from hedgerows and treelines to roads, streams, ponds, various woodland and grassland types, arable land, built environments, and other habitats.
  - Each code has a detailed description (e.g., hedgerows, treelines, roads, streams, ponds, arable land, improved grassland, built land, etc.).
  - The habitat coding system provides a structured way to contextualize bat activity with landscape features.

- Usage guidance
  - Full metadata and quality information accompany the data to support appropriate use and interpretation.
  - The dataset is designed to enable data discovery, combination with other datasets, and the creation of data products (e.g., summaries, dashboards) for broader use.

- References and contacts
  - Protocol reference: ECN measurements for terrestrial bats (BA) with a dedicated protocol URL.
  - Users are encouraged to acknowledge ECN and reference the protocol in publications citing the data.