# Amazon Fertilization Experiment (AFEX)

- Purpose: A full factorial fertilization experiment to study how nutrient additions affect forest dynamics, with a focus on root biomass within the BDFFP KM41 reserve.
- Study area context: Within the Biological Dynamics of Forest Fragments Project (BDFFP) area, KM41 reserve, about 100 km from Manaus; soils are clay-rich Ferrasols; mean annual rainfall 1900–2500 mm with a pronounced dry season (June–October); established forest plots show above-ground biomass ~322 Mg ha-1 and ~280 species (≥10 cm dbh per ha).

## AFEX experiment design

- Treatments and replication:
  - Eight fertilization treatments: Control; nitrogen (N); phosphorus (P); cations; nitrogen + phosphorus; nitrogen + cations; phosphorus + cations; nitrogen + phosphorus + cations.
  - Four replicates per treatment; total of 32 plots.
  - Experimental layout organized into four independent blocks with plots at least 200 m apart.
- Fertilization specifics:
  - Annual fertilization with three applications to mitigate leaching/runoff.
  - Nutrients applied per year: 125 kg ha-1 N (urea), 50 kg ha-1 P (triple superphosphate), 50 kg ha-1 K (KCl), plus 50 kg ha-1 Ca and 20 kg ha-1 Mg as dolomitic limestone.
- Plot characteristics:
  - Each plot: 50 x 50 meters.
  - Plots arranged to be similar in soil, vegetation, and topography.

## AFEX 2.0: Plot delineation

- Mapping context: AFEX blocks and plots located inside the KM41 reserve (location supporting a structured delineation for analysis).
- Plot coding:
  - Blocks: B1, B2, B3, B4.
  - Plots: P1–P8 within each block, each fertilization treatment represented in the block layout.

## Data collection methods

- Root biomass measurement:
  - Method: In-growth core technique using plastic mesh traps (12 cm diameter, 30 cm depth) placed in five central points per 30 x 30 m within each plot.
  - Depths: 0–10 cm and 10–30 cm.
  - Sampling procedure: Five cores per plot, bulked into a composite sample per plot; roots cleaned, dried at 60°C to constant weight, weighed.
  - Temporal schedule: 2017 (August, November); 2018 (February, June, September, December); 2019 (March, June, September, December).
  - Definition: Fine roots defined as <2 mm in diameter; initial installation serves as the stock biomass.
- Data handling:
  - Each sampling event captured as a row in a structured data spreadsheet, with fields detailing plot, block, depth, time interval, sampling time, and dry-weight biomass.

## Data spreadsheet structure (Root biomass)

- Columns and meaning:
  - Census: Sampling number.
  - PlotID: Combination of block and plot codes (e.g., B1P1, B1P2, etc.).
  - Block: Block identifier (B1, B2, B3, B4).
  - Plot: Plot code (P1–P8) within each block.
  - Depth: Soil layer (0–10 cm; 10–30 cm).
  - Time_int: Time interval for sampling within the 60-minute core extraction (0–15, 15–30, 30–45, 45–60 minutes).
  - Time: Sampling time across the four intervals.
  - Time_min: Actual minutes for each sampling (15, 30, 45, 60).
  - tot_weight: Dry weight of the fine root sample in grams.
- Data storage: Deposited in the EIDC system (data repository).

## Data quality and GIS relevance

- Spatial design: 32 plots across 4 blocks, each 50 x 50 m, enabling spatial visualization of treatment effects and depth-specific root biomass.
- Temporal dimension: Repeated measures across 2017–2019 allow time-series mapping of root biomass responses to treatments.
- Data integration: Root biomass data can be joined with plot-level attributes (block, treatment, location) for GIS-based analyses and map-based visualization.
- Considerations for GIS work:
  - Precise georeferencing of plots is needed if coordinates are not provided; plots are conceptually arranged by block and plot within KM41.
  - Potential to layer: plot boundaries, treatment types, depth-specific biomass, and time points to explore spatial-temporal patterns.

## References

- Duque et al., 2017. Insights into regional patterns of Amazonian forest structure and dominance from terra firme forest dynamics plots. Biodiversity and Conservation, 26:669-686.
- De Oliveira & Mori, 1999. A central Amazonia terra firme forest. I. High tree species richness on poor soils. Biodiversity and Conservation, 8:1219-1244.
- Metcalfe et al., 2007. A method for extracting plant roots from soil. New Phytologist, 174:697-703.
- Quesada et al., 2011. Soils of Amazonia (RAINFOUR sites). Biogeosciences, 8:1415-1440.
- Rankin de Merona et al., 1992. Preliminary results of a large-scale inventory of upland rainforest in the Central Amazon. Acta Amazonica, 22:493-534.