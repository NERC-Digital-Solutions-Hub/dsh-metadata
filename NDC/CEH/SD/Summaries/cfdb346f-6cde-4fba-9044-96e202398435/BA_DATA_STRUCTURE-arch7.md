# UK Environmental Change Network (http://www.ecn.ac.uk) Bats (BA)

- Overview
  - ECN bat dataset documenting bat detections along transects using bat detectors, with four surveys per site-year.
  - Methodology adapted from Bats and Habitats survey; surveys not conducted in heavy rain or strong winds.
  - Acknowledgement and data-use requests: acknowledge data in publications and send one reprint.
  - Noted limitations: limited ability to resolve precise population-environment change relationships; linking to broader monitoring mitigates this.

- Data structure and storage
  - Core data (D1BA_xxx): 10 tables (one per site) storing counts and related survey data
    - Key fields: SITECODE, SDATE (date), TRANSECT, BATLOC_ID (bat sighting/hearing location), FIELDNAME (bat species code), VALUE (count), ACTS/ACTH/ACTF (bat activity codes)
  - Survey methodology and equipment (D2BA_xxx): 10 tables
    - Fields include BATDETECTORTYPE, KEPTPROTOCOLFREQUENCY, ADJUSTFREQUENCY, USEREFERENCECD, USESONOGRAMANALYSIS
  - Habitat observations (D3BA_xxx): 10 tables
    - Fields include HAB1/HAB2/HAB3 (habitat types recorded near sighting), BATLOC_ID, FIELDNAME, VALUE (habitat code)
  - Core metadata: described in accompanying metadata documentation (structure referenced by standard ECN metadata tables)

- Field and code mappings
  - Species codes (FIELDNAME / VALUE):
    - Bb = Barbastella barbastellus; Es = Eptesicus serotinus; M = Myotis; Ms = Myotis bechsteinii; Mb = Myotis brandtii; Md = Myotis daubentonii; Mm = Myotis myotis; Mw = Myotis mystacinus; Mn = Myotis nattereri; XX = No bats found; Nl = Nyctalus leisleri; Nn = Nyctalus noctula; Pp = Pipistrellus; Ppl = Pipistrellus pipistrellus; Ppg = Pipistrellus pygmaeus; P = Plecotus; Pa = Plecotus auritus; Pg = Plecotus austriacus; Rf = Rhinolophus ferrumequinum; Rh = Rhinolophus hipposideros; UU = Unidentified bat
    - Habitat codes: 1–43 with descriptions (e.g., hedgerows, treelines, stone walls, roads, streams, various woodlands, grasslands, arable, built land, others), including detailed sub-descriptions for several categories
  - Habitat fields: HAB1, HAB2, HAB3 indicate up to three habitat types per sighting

- Site codes and locations
  - T01 Drayton: 52°11'37.95"N 1°45'51.95"W; date range 29-JUN-1993 to 05-SEP-2006
  - T02 Glensaugh: 56°54'33.36"N 2°33'12.14"W; 07-JUL-1994 to 30-AUG-2012
  - T03 Hillsborough: 54°27'12.24"N 6°4'41.26"W; 12-AUG-1994 to 05-SEP-2002
  - T04 Moor House - Upper Teesdale: 54°41'42.15"N 2°23'16.26"W; 16-JUN-1993 to 28-AUG-2012
  - T05 North Wyke: 50°46'54.96"N 3°55'4.10"W; 04-JUL-1993 to 30-AUG-2012
  - T07 Sourhope: 55°29'23.47"N 2°12'43.32"W; 12-JUL-1994 to 03-SEP-2012
  - T08 Wytham: 51°46'52.86"N 1°20'9.81"W; 05-JUL-1993 to 21-AUG-2012
  - T09 Alice Holt: 51° 9'16.46"N 0°51'47.58"W; 29-JUN-1994 to 05-SEP-2012
  - T10 Porton Down: 51° 7'37.83"N 1°38'23.46"W; 04-JUL-1994 to 03-SEP-2006
  - T11 Y Wyddfa - Snowdon: 53° 4'28.38"N 4° 2'0.64"W; 16-JUL-1996 to 31-AUG-2011

- Data access and usage notes
  - Data resides in an Oracle database with site-specific tables (D1BA_xxx, D2BA_xxx, D3BA_xxx)
  - Protocol reference and quality information are provided by ECN
  - Data authorship and sponsor acknowledgments are requested in user communications

- GIS considerations for use
  - Site coordinates and date ranges enable spatiotemporal mapping of bat detections and habitats
  - Species and habitat codes map to detailed attribute tables for map-based visualization
  - Multiple tables per site allow layered GIS analyses (counts by species, detector settings, and habitat associations)
  - Data quality notes should be applied when interpreting relationships between bat activity and environmental change

- Protocol and contact
  - Protocol reference: http://www.ecn.ac.uk/measurements/terrestrial/b/ba
  - Dataset originator: ECN Data Centre; ECN sponsorship by multiple UK government and environmental bodies
  - Acknowledgement and publication request: acknowledge data use and send one reprint if cited