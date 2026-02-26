# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Dataset Owners
- The UK Environmental Change Network (ECN) programme is sponsored by a consortium of UK government departments and agencies with an interest in understanding environmental change.
- Contributing organisations include: Agri-Food and Biosciences Institute; Biotechnology and Biological Sciences Research Council; Cyfoeth Naturiol Cymru - Natural Resources Wales; Defence Science & Technology Laboratory; Department for Environment, Food and Rural Affairs; Environment Agency; Forestry Commission; Llywodraeth Cymru - Welsh Government; Natural England; Natural Environment Research Council; Northern Ireland Environment Agency; Scottish Environment Protection Agency; Scottish Government; Scottish Natural Heritage.
- ECN requests acknowledgement of data use and asks for one reprint of any publication citing ECN data.

## Protocol
- ECN employs standard operating procedures to ensure data comparability across sites.
- See accompanying bb.pdf for details on data collection processes.

## Usage Notes
- Bird species are recorded on a transect within a 1 km square, including distance from transect.
- Methodology follows the Breeding Birds Survey (BBS) by the British Trust for Ornithology (BTO).
- Each transect is walked twice per year.
- Site-based ECN data are national-scale and have limited detail on population-environment relationships; users are advised to combine ECN data with data from broader monitoring programmes (e.g., BTO) to mitigate limitations.
- Initially, ECN used BTO Common Bird Census (lowland) and Moorland Bird Survey (upland); the Breeding Bird Survey replaced these at ECN sites.
- Include accompanying quality information when using the data.

## Data Download
- SITECODE: Unique code for each ECN Site.
- LCODE: Location ID (unique with site).
- VISIT: Visit timing (E = early, L = late).
- SDATE: Sampling date.
- TRANSECT: Transect identifier.
- FIELDNAME: Bird species code.
- VALUE: Number of birds observed.
- DISTANCE: Distance category (1 = within 25 m, 2 = 25–100 m, 3 = >100 m), F = bird in flight.
- Supporting Documentation – ECN_BB2.csv: Includes start/end times (FROM_HOUR, FROM_MINS, TO_HOUR, TO_MINS) and weather codes (CLOUD, RAIN, WIND, VISIBILITY).
- Supporting Documentation – ECN_BB3.csv: Habitat information for transects, including annual transect, habitat level 1–4 codes (FIRSTHL and SECONDHL fields).
- Supporting Documentation – ECN_BB_qtext.csv: Quality notes attached by site managers; fields indicate affected field, date ranges, and ongoing status.

## Explanatory Information: Site Codes
- Site and location mappings for: T01 Drayton; T02 Glensaugh; T03 Hillsborough; T04 Moor House - Upper Teesdale; T05 North Wyke; T06 Rothamsted; T07 Sourhope; T09 Alice Holt; T10 Porton Down; T11 Y Wyddfa - Snowdon; T12 Cairngorms.
- Coordinates are provided for each site. Note: T08 is not listed in the provided mapping.
- Additional site information available at the CEH Catalogue: https://catalogue.ceh.ac.uk/id/813712d4-d162-4ede-aff8-cf1c337bdc27

## Explanatory Information: Bird Species Codes
- Extensive list of species codes and names (e.g., AC = Arctic Skua, AF = Spotted Crake, AV = Avocet, BB = Blackbird, etc.).
- Codes are used in FIELDNAME to identify observed species; the list covers a wide range of common and rare birds.

## Explanatory Information: Habitat Codes
- BTO habitat recording system with Level 1 codes (A–J) representing main habitat types, plus Level 2, Level 3, and Level 4 codes for finer classification.
- Examples by top level:
  - A - WOODLAND: Level 2 broad categories (e.g., Broadleaved, Coniferous), plus Level 3/4 descriptors (disturbance, shrub density, dead wood, etc.).
  - B - SCRUBLAND (or young woodland <5 m): Levels 2–4 codes for composition, disturbance, and boundaries.
  - C - Semi-natural Grassland/Marsh: Levels 2–4 codes for hedgerows, boundaries, and management.
  - D - HEATHLAND AND BOGS; E - FARMLAND; F - HUMAN SITES; G - WATER BODIES (freshwater); H - COASTAL; I - INLAND ROCK; J - MISCELLANEOUS.
- Each level adds detail about habitat type and environmental context (e.g., presence of hedges, grazing, proximity to roads, management practices, etc.).