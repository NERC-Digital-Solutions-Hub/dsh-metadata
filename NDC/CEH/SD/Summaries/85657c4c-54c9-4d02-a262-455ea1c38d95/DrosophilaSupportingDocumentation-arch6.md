# Primary data is a table of observed interactions between Drosophila species (vinegar fly) and hymenopteran parasitoids across two elevation transects.

## Overview
- Captures observed interactions between Drosophila hosts and parasitoids across two elevation transects in the Australian Wet Tropics World Heritage area.
- Elevation range per transect: 59–916 m above sea level; 7 sites per transect (14 sites total).
- Data include host and parasitoid identifications (where possible), along with environmental context and sequencing information.

## Data collection and sampling design
- Trapping method: bottle traps baited with fermented banana, using 1.5 L bottles with entry windows, rain-shield, and ant deterrents.
- Trap placement: 1.5 m above ground, minimum 5 m apart, at least 5 m from roads to reduce sun exposure effects.
- Bait and setup: 50 g banana bait with baker’s yeast; cardboard strips to aid pupation.
- Exposure periods: long (24 days), medium (14–15 days), short (11–12 days); short exposure data unavailable for P070 due to weather.
- Sample selection: 15 randomly chosen traps per site (5 per exposure) used for pupae extraction; traps raided, excessively dry, or flooded were excluded.
- Storage: pupae stored individually in 96-well plates with ethanol and kept at -15°C.

## Hierarchical network construction
- Core network: 182 pupae per site randomly selected; 722 hosts identified (86–138 per site); 179 parasitized; 147 parasitoids identified.
- Enriching network: 2,659 additional samples screened by PCR for parasitoid DNA; parasitized samples sequenced to identify host and parasitoid.
- Data integration: core and enriching datasets combined into an overall enriched quantitative network using relative host frequencies and host-specific parasitism rates from the core network; interaction frequencies inferred from both core and enriching sets.

## Data structure and contents
- PupaeIdentification.csv
  - SampleID: unique sample identifier
  - Transect, Site: transect and site identifiers
  - Elevation: site elevation (m above sea level)
  - ExposureLength: Short, Medium, or Long
  - TrapID: trap identifier within site
  - Host: host species (or NA if unknown)
  - Parasitoid: parasitoid (pseudo-species)
  - Parasitised: whether parasitoid DNA detected (TRUE/FALSE)
  - Group: testing category (Screen Only, Core, Enriching)
- Environmental Data: DataLoggerRecords.csv
  - Date: timestamp (YYYY-MM-DD HH:MM:SS)
  - Temp, Humidity: environmental readings
  - SerialNumber: data logger identifier
  - Site, Trap, Transect: context identifiers linking readings to location
  - Hourly readings captured during sampling period
- SequencesTable.csv
  - Details of sequences used for Drosophila species identification
  - Columns include Species, Location, Sample Code, Locus, Year, GenBank accession, Sequence

## Molecular methods and validation
- DNA metabarcoding performed on a subset to identify host and parasitoid species (hierarchical sampling scheme).
- PCR screening used on the broader set to detect parasitoid DNA; positive samples sequenced for precise identification.
- See Jeffs et al. 2020 (preprint) for full molecular methods.

## Study logistics and provenance
- Sample collection by Chris Jeffs; funding under grant held by Owen Lewis (University of Oxford).
- Sequencing conducted at the Hrček lab (Institute of Entomology, Czech Academy of Sciences).
- Data curation and manuscript preparation by Chris Terry (University of Oxford / QMUL).

## Permits and study sites
- Permit: WITK16977516 (Queensland Department of Environment and Heritage Protection).
- Sites: Paluma Range Road (Paluma Range National Park) and Kirrama Range Road (Girramay National Park) within the Australian Wet Tropics.
- Geographic scope: 14 sites total across two elevation transects (K070, K150, K230, K310, K390, K570, K670, K730 for Kirrama; P070, P090, P250, P350, P505, P590, P650, P780, P880 for Paluma).

## Supplementary data and notes
- Temperature and humidity records accompany the main dataset (data loggers).
- Genome sequence table provides reference material used for host/parasitoid identification.

## Data quality, reuse, and limitations
- Quality controls include exclusion of traps with ant predation, dryness, or flooding; variability in data logger usability across sites.
- Core vs. enriching data approach supports robust estimation of interaction frequencies while expanding the dataset through targeted sequencing.
- Clear metadata and data provenance facilitate reuse for network analyses, host–parasitoid interaction studies, and environmental context integration.