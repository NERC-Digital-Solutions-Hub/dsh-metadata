# ECN Bat Transect Data Documentation

## Overview
- Dataset originate from the ECN Data Centre (Centre for Ecology and Hydrology) and managed by the UK Environmental Change Network (ECN) programme.
- Programme funders and supporters include multiple UK government departments and agencies (e.g., Defra, Environment Agency, Natural England, NERC, etc.).
- Purpose: map-based bat survey data along transects across ECN sites to enable GIS-enabled analysis and monitoring of bat presence, activity, and habitat associations.
- Data are provided with standard protocols to ensure comparability across sites; users are urged to consult accompanying protocols (ba.pdf) and quality notes.
- Acknowledgement and data citation: acknowledge data use and send one reprint of any publication; contact ECN for details (ecn@ceh.ac.uk).

## Data Collection Protocol
- Method: bat species mapping using bat detectors and recording bat activity along transects.
- Survey cadence: transects are walked four times per year, in four three-week windows (mid-June to early September), excluding periods of heavy rain or strong winds.
- Basis: methodology linked to the Bats and Habitats survey led by Prof. S. Harris and colleagues, used by JNCC.
- Limitations: methodology provides limited information on precise population–environment change relationships; linking ECN results with broader monitoring mitigates this.
- Data quality: use accompanying quality information when analyzing data.

## Data Structure and Key Fields
- Core data fields for each observation:
  - SITECODE: unique code for each ECN Site.
  - SDATE: sampling date.
  - TRANSECT: transect identifier.
  - BATLOC_ID: location where bat was seen or heard (unique per survey date).
  - FIELDNAME: variable measured (e.g., species code or habitat code).
  - VALUE: value of the measured variable.
  - ACTS: activity code for bat seen.
  - ACTH: activity code for bat heard.
  - ACTF: activity code for bat feeding buzz heard.
- Supporting documentation files:
  - ECN_BA2.csv: survey conduct details (bat detector type, frequency settings, adjustments, reference comparisons, etc.).
  - ECN_BA3.csv: habitats observed on transect (habitat codes).
  - ECN_BA_qtext.csv: site manager quality notes (text explanations of data quality issues or circumstances).
- Additional reference: accompanying documentation and site/species/habitat code lists are provided to interpret codes.

## Site Codes (Explanatory Information)
- Explanatory information lists ECN sites with code, name, and coordinates (examples include Drayton, Glensaugh, Hillsborough, Moor House – Upper Teesdale, North Wyke, Sourhope, Wytham, Alice Holt, Porton Down, Y Wyddfa – Snowdon, etc.).
- Each site has a precise latitude/longitude location for GIS use.

## Species Codes (Explanatory Information)
- Codes map to bat species (Latin and common names), including:
  - Bb = Barbastella barbastellus (Barbastelle)
  - Es = Eptesicus serotinus (Serotine)
  - M = Myotis (Myotis spp.)
  - Ms = Myotis bechsteinii (Bechstein's)
  - Mb = Myotis brandtii (Brandt's)
  - Md = Myotis daubentonii (Daubenton's)
  - Mm = Myotis myotis (M. myotis)
  - Mw = Myotis mystacinus (Whiskered)
  - Nn = Nyctalus noctula (Noctule)
  - Pp = Pipistrellus (Pipistrelle)
  - Ppl = Pipistrellus pipistrellus (Common pipistrelle)
  - Ppg = Pipistrellus pygmaeus (Soprano pipistrelle)
  - P = Plecotus (Long-eared)
  - Pa = Plecotus auritus (Brown long-eared)
  - Pg = Plecotus austriacus (Grey long-eared)
  - Rf = Rhinolophus ferrumequinum (Greater horseshoe)
  - Rh = Rhinolophus hipposideros (Lesser horseshoe)
  - UU = Unidentified bat
  - XX = No bats found
- Detailed species list links codes to both Latin and common names for GIS labeling and analysis.

## Habitat Codes (Explanatory Information)
- HAB1, HAB2, HAB3: first, second, and third habitat type codes recorded near each bat sighting. Units: n/a.
- A broad set of habitat type codes is provided to describe the surrounding environment at sighting locations.

## Habitat Types (Explanatory Information)
- A comprehensive catalog of 43 habitat types with descriptive definitions, covering:
  - Hedgerows, treelines, stone walls, footpaths, tracks/bridleways, roads, ditches, streams, rivers (fast/slow), canals.
  - Woodenlands (semi-natural and plantations), broadleaved and coniferous forests (semi-natural and plantations), mixed and young plantations, recently felled woodland, parkland.
  - Grasslands (upland/lowland unimproved and semi-improved/improved), arable, amenity grassland.
  - Rocks, quarries, bare soil, built land, and an "Others" category for unspecified habitats.
- Each habitat type is assigned a numeric code (1–43) for inclusion in field data and GIS workflows.

## Data Usage and GIS Readiness
- Data are designed for map-based presentation and analysis of bat detections in relation to site location, transect geography, and habitat context.
- Availability of site coordinates and rich habitat/species coding supports spatial joins, habitat suitability mapping, and trend analyses when combined with broader ECN datasets.
- Users should consult quality notes (ECN_BA_qtext.csv) to understand data quality implications for GIS analyses.

## Access, Acknowledgements, and Contact
- Data usage requires acknowledgement of ECN data and site, with a request to provide one reprint of any publication using the data.
- Primary contact for data is ecn@ceh.ac.uk; additional site codes and habitat/species details are available through ECN documentation.