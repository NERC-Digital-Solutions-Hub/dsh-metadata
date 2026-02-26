# UK Environmental Change Network (http://www.ecn.ac.uk) Bats (BA)

- Overview
  - A bat-focused dataset within the UK Environmental Change Network (ECN), recording bat species presence/absence and activity along transects using bat detectors.
  - Data collected via transects walked across four periods each year, with links to other widespread monitoring programmes to mitigate limitations in inferring population-environment relationships.
  - Accompanied by quality information to support appropriate data use and interpretation.

- Data Provenance and Access
  - Dataset Originator: ECN Data Centre (Centre for Ecology and Hydrology).
  - Dataset Owners: A consortium of UK government departments/agencies funding site monitoring or network coordination (including Defra, Natural England, Environment Agency, Scottish/Welsh administrations, and related councils/agencies).
  - Acknowledgement: Users are asked to acknowledge data use and to send one reprint of any publication citing the dataset.
  - Protocol Reference: Provided via ECN measurements web page (BAT protocol).

- Data Structure and Content
  - Storage: Observations and related data are held in an Oracle database, structured into 10 site-specific tables for each data group:
    - D1BA_xxx: Observations (e.g., counts by site/date; transect; bat location; bat species or activity codes; counts/values).
    - D2BA_xxx: Survey conduct and equipment details (e.g., bat detector type, protocol flags such as frequency settings and reference usage).
    - D3BA_xxx: Habitats observed along transects (up to three habitat types per sighting).
  - Data organization per site: Tables named D1BA_xxx, D2BA_xxx, D3BA_xxx where xxx is the site code.
  - Core fields (summarised): Site code, sampling date, transect, bat location, field codes for species/habitat, and corresponding values or activity codes.

- Site Codes and Datasets
  - The ECN Bats dataset comprises 10 sites (T01–T11, with T06 not listed in the provided data), each with site-specific metadata and date ranges:
    - T01 Drayton — 52°11'37.95"N 1°45'51.95"W; 29-JUN-1993 to 05-SEP-2006
    - T02 Glensaugh — 56°54'33.36"N 2°33'12.14"W; 07-JUL-1994 to 30-AUG-2012
    - T03 Hillsborough — 54°27'12.24"N 6° 4'41.26"W; 12-AUG-1994 to 05-SEP-2002
    - T04 Moor House - Upper Teesdale — 54°41'42.15"N 2°23'16.26"W; 16-JUN-1993 to 28-AUG-2012
    - T05 North Wyke — 50°46'54.96"N 3°55'4.10"W; 04-JUL-1993 to 30-AUG-2012
    - T07 Sourhope — 55°29'23.47"N 2°12'43.32"W; 12-JUL-1994 to 03-SEP-2012
    - T08 Wytham — 51°46'52.86"N 1°20'9.81"W; 05-JUL-1993 to 21-AUG-2012
    - T09 Alice Holt — 51° 9'16.46"N 0°51'47.58"W; 29-JUN-1994 to 05-SEP-2012
    - T10 Porton Down — 51° 7'37.83"N 1°38'23.46"W; 04-JUL-1994 to 03-SEP-2006
    - T11 Y Wyddfa - Snowdon — 53° 4'28.38"N 4° 2'0.64"W; 16-JUL-1996 to 31-AUG-2011
  - Note: Site T06 is not listed in the provided data.

- Field Naming and Species Codes
  - Fieldname (D1BA_xxx) holds codes for observed bat species; VALUE holds counts. ECN bat codes include:
    - Bb Barbastelle; Es Serotine; M Myotis (Myotid species); Ms Bechstein’s; Mb Brandt’s; Md Daubenton’s; Mm Myotis mysotis; Mw Whiskered; Mn Natterer’s; Nl Leisler’s; Nn Noctule; P Pipistrellus; Ppl Common Pipistrelle; Ppg Soprano Pipistrelle; P Plecotus; Pa Brown long-eared; Pg Grey long-eared; Rf Greater horseshoe; Rh Lesser horseshoe; UU Unidentified bat; XX No bats found.
  - Habitat codes: Up to three habitat types recorded per sighting (HAB1–HAB3) with codes 1–43 describing categories such as Hedgerows, Treelines, Stone walls, Roads, Streams, Ponds, Lakes, Arable land, Grassland types, Woodlands, Built land, and Others.
  - Example habitat descriptions include hedgerows/treelines/walls, various water bodies (ponds, rivers, canals), woodland types, grassland categories (lowland/highland/improved/unimproved), arable land, built-up areas, and other habitats.

- Habitat Coding Details
  - HAB1, HAB2, HAB3 each correspond to a habitat type code and description (three levels of habitat data per observation).
  - Codes map to detailed habitat descriptions (e.g., hedgerows, woodlands, water bodies, grasslands, arable land, built environments, etc.), with a comprehensive listing from 1 to 43 describing each habitat type.

- Data Quality, Usage, and References
  - Use the accompanying quality information when applying the data.
  - Protocol reference and measurement details are available via ECN resources.
  - Researchers are encouraged to acknowledge ECN data use and to share a reprint of publications citing the data.