# The purpose of the data is to compare the amount of a key pheromone between two sibling species of Drosophila

## Overview
- Objective: quantify and compare the cuticular hydrocarbon 7,11-heptacosadiene (7,11-HD) between two Drosophila species.
- Species and lines: D. simulans (strain a2a2b, derived from Tsimbazaza) and D. sechellia (derived from Cousin Island, Seychelles).
- Sample set: 15 females per species, isolated as virgins and kept with other females for five days before extraction.

## Experimental design and data collection
- Extraction protocol:
  - Females anaesthetised on ice, transferred to hexane, vortexed, and hexane evaporated under nitrogen.
  - Vials stored at -20°C until shipping.
  - Hydrophobic extracts re-suspended in 50 μL of a standard solution (10 ng/mL C18 and 10 ng/mL C26 in hexane).
- GC analysis:
  - Instrument: Agilent 7890 GC with flame ionization detector; DB-1 column.
  - Injector: splitless, 250 °C; carrier gas: helium.
  - Temperature program: 50 °C (1.5 min) → 150 °C; then to 280 °C with two ramps, hold.
  - Data handling: ChemStation; peak areas normalized to internal standard C26 to derive relative quantities.
- Identification:
  - 7,11-HD identified by retention time relative to C26 standard.
  - Relative quantity expressed as ng based on peak area comparison to C26.
- Documentation:
  - Datasets named 711HDsech.csv (D. sechellia) and 711HDsim.csv (D. simulans).
  - Some samples failed to produce detectable traces and were excluded.

## Datasets and data structure
- Data format: CSV files with two columns (sample, ng); column 1 is sample identifier, column 2 is ng amount.
- Content organization: measurements of 7,11-HD per sample, relative to internal standard C26.
- Identification: retention time relative to C26 standard used to confirm 7,11-HD presence.

## Data processing and quality control
- Processing: peak integration conducted using ChemStation, with normalization to the C26 internal standard.
- Quality notes:
  - Some samples yielded no traces and were excluded from analyses.
  - Documentation does not specify uncertainty estimates or replication beyond the 15 samples per species.

## Provenance and collaboration
- Rearing and extractions: Stephen Goodwin's lab, University of Oxford; Deniz Erezyilmaz.
- Gas chromatography analysis: University of Groningen; J. C. Billeter's lab; Nicolas Dubovetsky.
- Data lineage: samples originated from two species/lines as described; analyses performed with standard GC methods and internal standard normalization.

## GIS-related notes and potential reuse
- The data are non-spatial, per-sample chemical measurements.
- Potential GIS use if linked with metadata (species, strain origins, collection sites) to explore geographic or lineage-based patterns or to annotate map-based visualizations of pheromone levels when spatial metadata becomes available.