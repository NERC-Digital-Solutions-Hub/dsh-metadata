# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- ECN data describing ground beetles (Carabidae) collected with pitfall traps to monitor predator abundance.
- Fortnightly data collection during May–October, with protocols to ensure comparability across 12 ECN sites.
- Data are used to understand environmental change, support correlations and predictive analyses, and inform decision-making.

## Data scope and collection protocol
- Purpose: monitoring abundance of ground predators (Carabidae) using standardized pitfall-trap protocols.
- Sampling window: fortnightly from May to October.
- Site coverage: 12 ECN sites (Drayton, Glensaugh, Hillsborough, Moor House Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon, Cairngorms) with exact site coordinates provided.
- Protocols: standard operating procedures to ensure cross-site data comparability; detailed collection methods described in accompanying documentation (IG2/IG3 context).

## Data structure and fields
- Primary data download fields:
  - SITECODE: Unique ECN site code
  - LCODE: Location ID within site
  - SDATE: Sampling date
  - TRAP: Trap number
  - FIELDNAME: Variable measured (e.g., quality codes, species information)
  - VALUE: Measured value
  - TYPE: Additional information for specific species (applies to Pterostichus madidus, 6453 2714)
- Species and taxonomy:
  - 6453 series codes correspond to Carabidae genera and species (e.g., Cicindela, Pterostichus madidus, Carabus spp., Nebria spp., etc.), with FIELDNAME and RANK indicating genus or species level.
  - Example: 6453 2714 corresponds to Pterostichus madidus (SPECIES); 6453 2713 to Pterostichus macer, etc.
- Special data notes:
  - For Pterostichus madidus (6453 2714), TYPE may include gender (M/F) and leg colour morphs (e.g., red/black).
- Supporting documentation in the dataset package:
  - ECN_IG2.csv: trap deployment timing (FROMDATE), collection timing (SDATE).
  - ECN_IG3.csv: habitat descriptions (HABDESC).
  - ECN_IG_qtext.csv: qualitative notes from site managers describing data quality issues; linked via quality codes (including 999 for unlisted events).

## Site codes and locations
- Explanatory site codes with names and coordinates:
  - T01 Drayton
  - T02 Glensaugh
  - T03 Hillsborough
  - T04 Moor House - Upper Teesdale
  - T05 North Wyke
  - T06 Rothamsted
  - T07 Sourhope
  - T08 Wytham
  - T09 Alice Holt
  - T10 Porton Down
  - T11 Snowdon (Y Wyddfa)
  - T12 Cairngorms
- Each site entry includes precise latitude/longitude coordinates.

## Variable mapping and quality information
- FIELDNAME categories:
  - Q1–Q8: Quality code fields indicating data quality factors; each Qx has a corresponding Rank indicating species context (GENUS or SPECIES).
  - 6453 taxonomy codes: detailed species/genus descriptions and ranks for ground beetles (e.g., 6453 100 = Cicindela (GENUS); 6453 101 = Cicindela campestris (SPECIES); etc., across numerous genera and species).
- Quality codes:
  - Codes 100–513 cover data quality issues (e.g., no information, sample loss, contamination, equipment issues, etc.).
  - 999: Unusual event described in ECN_qtext file.
  - Additional laboratory/measurement-related codes (e.g., 501–513) describe laboratory handling and processing status.
- Explanatory context:
  - The dataset includes metadata linking quality codes to site-specific notes (ECN_qtext) to aid interpretation of data reliability.

## Usage notes and considerations for analysts
- Acknowledgement and sharing:
  - Users should acknowledge ECN data use and provide a reprint of publications citing ECN data.
- Data quality and interpretation:
  - Use accompanying quality information to assess data reliability; site managers may annotate conditions via ECN_qtext.csv.
- Data access and scale:
  - Challenges may include data at the right scale for local decisions, integration of multiple datasets, and standardization across sites.
- Analytical approach:
  - Data are well-suited for identifying patterns and correlations in ground beetle abundance, testing environmental drivers, and building predictive models.
- Data provenance:
  - Data sources and datasets are trackable; ECN emphasizes metadata and discoverability of datasets via portals with rich metadata.

## Data usage and interpretation challenges (summary)
- Data may be sparse or unevenly distributed at local scales.
- Access pathways can be multi-step, and site/habitat metadata are essential for robust analyses.
- Taxonomic detail (6453 codes) enables fine-grained analyses but requires careful mapping between FIELDNAME and species/rank.
- Data quality varies by site and sampling event; quality codes and text provide crucial context for analyses and interpretation.