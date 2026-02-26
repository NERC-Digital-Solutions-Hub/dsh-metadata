# Primary data is a table of observed interactions between Drosophila species (vinegar fly) and hymenopteran parasitoids across two elevation transects.

## Overview
- Presents observed interactions between Drosophila pupae and parasitoids across two elevation transects in the Australian Wet Tropics.
- Identification of host and parasitoid species achieved for a subset via DNA metabarcoding; broader screening via PCR.
- Data used to construct quantitative host–parasitoid networks with a hierarchical sampling design.

## Study design and sampling
- Hierarchical sampling approach used to build and enrich interaction networks.
- Core network: random selection of 182 pupae per site with full host/parasitoid identification.
  - Across core: 722 hosts identified (86–138 samples per site).
  - 179 hosts parasitized; parasitoids identified in 147 cases.
- Enrichment: additional samples (2659 total; 339–564 per site) screened for parasitoid DNA via PCR; parasitized samples sequenced to identify hosts/parasitoids.
- Final analysis combines core and enriching data into an enriched quantitative network using:
  - Relative host frequencies
  - Host-specific parasitism rates from the core network
  - Interaction frequencies derived from core and enriching sets

## Study sites and environmental context
- Location: Australian Wet Tropics World Heritage area (450 km rainforest corridor along northeast Queensland).
- Two elevation transects:
  - Paluma Range (Paluma Range National Park)
  - Kirrama Range (Girramay National Park)
- Elevation range: 59–916 m above sea level.
- 7 sites per transect (total of 14 sites) chosen to span elevation.
- Site identifiers include transect, site code, latitude/longitude, and elevation (e.g., K070 at 70 m, P090 at 90 m).

## Field methods and sampling design
- Trap type: bottle traps baited with fermented banana.
  - Construction: 1.5 L bottles with side windows for ingress; rain-shielded lids; ant-repellent coating.
  - Setup: traps hung 1.5 m above ground; minimum 5 m between traps; 5 m from road edges.
- Bait: 50 g mashed Cavendish bananas with baker’s yeast; cardboard strips to facilitate pupation.
- Exposure durations: short (11–12 days), medium (14–15 days), long (24 days).
- Sampling period: 11 March – 12 April 2016 (mid-late wet season).
- Collection: 15 traps per site sampled (5 per exposure length); placement exclusions applied for raiding, dryness, or flooding.
- Pupae handling: collected pupae stored individually in 96-well plates with ethanol and frozen if needed; later identified or left as NA if not run.

## Data structure and core datasets
- PupaeIdentification.csv
  - Each row represents a single pupae.
  - Key columns:
    - SampleID, Transect, Site (elevation), ExposureLength, TrapID
    - Host (Drosophila species; NA if unknown)
    - Parasitoid (pseudo-species; NA if none)
    - Parasitised (true/false from PCR)
    - Group (Screen Only, Core, Enriching)
- Environmental data
  - DataLoggerRecords.csv
  - Hourly readings for temperature and relative humidity.
  - Columns include DateTime, Temp, Humidity, SerialNumber, Site, Trap, Transect.
  - Data from multiple loggers; some sites had limited usable data.
- Sequences
  - SequencesTable.csv
  - Details of sequences used to identify Drosophila species.
  - Columns include Species, Location, Sample Code, Locus, Year, GenBank accession, Seq.

## Data processing and analytical approach
- DNA-based identifications:
  - Core network identifications for host and parasitoid via DNA metabarcoding.
  - Additional samples screened with PCR to identify parasitoid presence; dependent sequencing provided host/parasitoid IDs.
- Network construction:
  - Core network provides baseline interaction frequencies and parasitism rates.
  - Enriching set increases sampling of interactions; integrates with core to form the enriched network.
- Data provenance:
  - Sample collection by Chris Jeffs (grant to Owen Lewis, University of Oxford).
  - Sequencing conducted by Jan Hrček (Institute of Entomology, Czech Academy).
  - Data curation and analysis by Chris Terry (University of Oxford / QMUL).

## Permits and provenance
- Permit WITK16977516 from Queensland Department of Environment and Heritage Protection (to Chris Jeffs).

## Notes for analysts
- The dataset enables correlations between host species presence, parasitoid incidence, and environmental variables (temperature/humidity) across elevations.
- Hierarchical sampling allows robust estimation of core interaction frequencies and targeted enrichment of rare interactions.
- Data structure supports replication, subsetting by transect/site/exposure length, and integration with environmental covariates for predictive modeling.