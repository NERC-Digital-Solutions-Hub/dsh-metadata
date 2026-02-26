# Soil nematode communities from peri urban watersheds

## Overview
- Study of soil nematode communities across a watershed in the peri-urban area of Ningbo, China, with sampling in four periods (April 2017, July 2017, October 2017, January 2018).
- Two land uses at each site: farmland and forest.
- 250 g soil collected per site via five random cores; samples stored at 4 °C before shipping to the UK; shipping under Scottish government import license; maintained in quarantine at 8 °C per The James Hutton Institute biosecurity policy.
- Nematode community structure determined through a molecular approach (T-RFLP) following adapted methods.

## Data Collection and Laboratory Methods
- Nematodes extracted from soil using a density centrifugation method adapted from Hallmann and Viaene (2013): 100 g soil in 250 ml bottles, water added, centrifugation, MgSO4 density gradient, centrifugation, sieving, and collection of nematodes; material frozen then freeze-dried.
- DNA extracted from freeze-dried material using PureLink Genomic DNA Mini Kit (ThermoFisher).
- Nematode community structure assessed using directed T-RFLP (adapted from Donn et al. 2012): Nem_SSU_F74 primer and FAM-labeled Nem_18S_R; PCR conditions specified (initial denaturation, cycles with precise temperatures and durations, final extension).
- PCR products digested with:
  - Ple I (Ple I restriction enzyme) with specified buffer, volumes, and digestion conditions (1 hr, 37 °C; denature 65 °C).
  - BtscI with specified buffer, volumes, and digestion conditions (1 hr, 50 °C; denature 80 °C).
- Digests diluted 1:10, mixed with formamide and LIZ 1200 marker, then sequenced on an ABI 3730 capillary sequencer.
- T-RF peaks identified in GeneMapper; baseline fluorescence threshold set to 50 fluorescence units.
- For each sample, relative fluorescence values calculated for peaks; peaks contributing less than 1% of total fluorescence removed; data transformed using the Hellinger transformation.

## Data Structure, Nature, and Units
- Data file: CZOperiurban_watershed_Nematodedata.csv
- Columns:
  - Sample_ID: CZO watershed sample ID; designed to match identifiers from other CZO catchment datasets.
  - Season: season in which samples were collected.
  - Peak_...: the Hellinger-transformed relative fluorescence value for the corresponding T-RF peak (e.g., Peak_54.86 refers to peak 54.86).

## Data Quality, Provenance, and Documentation
- Explicit QA steps include peak filtering (removing peaks <1% of total) and transformation (Hellinger) to standardize abundance data across samples.
- Methods and sequencing/digestion procedures are fully documented, enabling reproducibility and cross-study comparability.
- Data provenance is linked to a consistent Sample_ID system aligning with other CZO datasets, supporting integration and metadata linkage.

## Data Governance, Access, and Sharing Considerations
- Biosecurity, import compliance, and storage conditions are documented, indicating the necessity of maintaining data provenance and chain-of-custody.
- For stewardship:
  - Ensure metadata completeness (collection dates, land-use context, methods, reagents, and software used for peak calling and transformation).
  - Maintain versioning and clear data provenance to support updates and reuse.
  - Facilitate interoperability by preserving the Sample_ID schema and linking to related CZO datasets.
  - Document sharing permissions and any embargoes or use restrictions; provide guidance on re-use and repurposing of the T-RFLP data and transformed outputs.

## References
- Hallmann and Viaene (2013). Nematode extraction. EPPO Bulletin, 43:471-495.
- Donn, S.; Neilson, R.; Griffiths, B.S.; Daniell, T.J. (2012). A novel molecular approach for rapid assessment of soil nematode assemblages—variation, validation and potential applications. Methods in Ecology and Evolution, 3:12-23.