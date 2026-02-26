# Amazon Fertilization Experiment (AFEX)

## Overview
- Full factorial fertilization experiment in the BDFFP KM41 reserve (Amazon), started March 2017.
- 8 fertilization treatments, 4 replicates each, total of 32 plots across 4 blocks.
- Aimed at understanding how nutrient additions affect ecosystem carbon fluxes, with measurements of stem CO2 efflux and soil respiration.

## Study area and environmental context
- Location: KM41 reserve, ~100 km from Manaus, Brazil (02 24'S, 59 52'W).
- Soils: clay-rich Ferrasols.
- Climate: annual rainfall 1900–2500 mm with a pronounced dry season (June–October).
- Forest structure context (reference data): aboveground biomass (AGB) ~322 ± 54 Mg ha^-1; mean wood density ~0.67 g cm^-3; species richness ~280 species (≥10 cm DBH) per hectare.

## AFEX design and treatments
- Treatments (8 total): Control; nitrogen (N); phosphorus (P); cations; nitrogen + phosphorus (N+P); nitrogen + cations (N+cations); phosphorus + cations (P+cations); nitrogen + phosphorus + cations (N+P+cations).
- Experimental layout: 4 independent blocks; at least 200 m separation between blocks.
- Plot characteristics: each plot 50 x 50 m; similar soil, vegetation, and topography within blocks.
- Fertilization regime: annually applied in three doses to mitigate leaching and runoff.
  - Nutrients per year: N 125 kg ha^-1; P 50 kg ha^-1; K (as part of cations) 50 kg ha^-1; calcium 50 kg ha^-1; magnesium 20 kg ha^-1 (as dolomitic limestone).

## Plot delineation (AFEX 2.0)
- Detailed delineation of blocks and plots within KM41 to support consistent plot layout and replication.

## Data collection methods
- Stem respiration (CO2 efflux from stems)
  - Sample: 320 trees with DBH > 25 cm; 10 trees per plot.
  - Timing: October 2019.
  - Instrument: infrared gas analyser (EGM-4, PP Systems) with a collar-installed chamber.
  - Protocol: 2-minute measurement per tree to determine CO2 efflux.
- Soil respiration
  - Instrument: Li-COR Li-8100A with a 20 cm survey chamber.
  - Observation: separate collars to partition rhizosphere vs. bulk soil respiration.
  - Collar types and purpose:
    - Short collar (10 cm depth): captures both heterotrophic and rhizosphere respiration.
    - Long collar (25 cm depth) with no windows: excludes roots and mycorrhizae (to estimate heterotrophic respiration).
    - Long collar (25 cm depth) with windows (historical type): excluded both roots and mycorrhizae; evaluation of disturbance effects.
  - Measurement details: autotrophic and heterotrophic components separated by comparing collar types; some collars designed to exclude roots/mycorrhizae began to show root intrusion around mid-2018.
- Temporal coverage
  - 2017: June–July, September, October, November.
  - 2018: monthly through September.
  - 2019: January, February, April, July, October.

## Data management and metadata
- Data spreadsheets and storage
  - Stem CO2 efflux data: stored in an electronic data information system (EIDC).
  - Structure (example fields):
    - A: TAG (tree numerical ID)
    - B: POM (Plot/Inventory marker)
    - C: Block
    - D: Plot
    - E: DBH
    - F: Inicial_CO2 (CO2 efflux at start)
    - G: Final_CO2 (CO2 efflux at end)
    - H: PlotID (block+plot)
    - I: Date of collection
    - J: (date/time or a similar field)
    - K: Obs (replication or observation number)
    - L: Lin Flux (flux value)
  - Soil CO2 efflux data: stored in EIDC with fields such as Census, File.Name, Date, Block, Plot, Group, Type, PlotID, Date_IV, Lin_Flux.
- Data fields and coding
  - Block and Plot: B1–B4; P1–P8 plots within blocks.
  - Collar Group and Type: Group (collar group), Type (T = shallow surface; M = deep 25 cm with windows; S = deep 25 cm with no windows).
  - Date fields: collected date/time recorded by equipment (Date_IV); manual dates for field entries.
- Documentation and provenance
  - Detailed methodologies and field protocols are documented alongside the datasets.
  - References provided for site context and methodological background.

## Governance and data stewardship considerations
- Multidimensional data: longitudinal measurements across multiple treatments, plots, blocks, and collar types (stem and soil respiration) requiring robust metadata and consistent ontologies.
- Data quality and consistency
  - Ensure consistent unit definitions across datasets (e.g., stem CO2 efflux measurements vs. soil CO2 efflux in µmol m^-2 s^-1).
  - Track collar-type changes and root-intrusion issues post-2018 to maintain proper interpretation of respiration components.
  - Address potential data anomalies (e.g., irregular or unclear codes such as “1aR”) in field records.
- Data integration and interoperability
  - Align datasets from different measurement instruments (EGM-4, Li-8100A) with unified metadata to enable cross-dataset analyses.
  - Maintain clear linkages between PlotID, Block, and treatment to support reproducibility and data reuse.
- Access, storage, and updates
  - Data stored in the EIDC system; ongoing data collection should be versioned and updated with clear provenance.
  - Documentation should accompany updates to facilitate discoverability by data users and other stakeholders.
- Usability for data users
  - Provide explicit definitions for all variables, measurement protocols, and equipment models to support data reuse by researchers, managers, and policymakers.
  - Maintain clear mapping between field notes and dataset entries to minimize ambiguity in long-term datasets.

## References
- Duque A, Mulher Landare, HC, Valencia R, Cardenas D, Davies S, de Oliveira A, Perez AJ, Romero Santos H, Vicentini A. 2017. Insights into regional patterns of Amazonian forest structure and dominance from three large terra firme forest dynamics plots. Biodiversity and Conservation 26:669-686.
- De Oliveira A, Mori SA. 1999. A central Amazonia terra firma forest. I. High tree species richness on poor soils. Biodiversity and Conservation 8:1219-1244.
- Quesada, CA et al. 2011. Soils of Amazonia with particular reference to the RAINFOR sites. Biogeosciences 8:1415-1440.
- Rankin de Merona JM et al. 1992. Preliminary results of a large-scale inventory of upland rainforest in the Central Amazon. Acta Amazonica 22:493-534.