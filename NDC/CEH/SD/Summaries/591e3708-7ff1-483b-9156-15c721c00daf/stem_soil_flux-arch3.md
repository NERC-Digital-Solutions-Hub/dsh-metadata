# Amazon Fertilization Experiment (AFEX)

## Study area and context
- Conducted within the Biological Dynamics of Forest Fragments Project (BDFFP) area, KM41 reserve, ~100 km from Manaus.
- Local soils: clay-rich Ferrasols; annual rainfall 1900–2500 mm with a pronounced dry season (Jun–Oct).
- Forest characteristics in the area include above-ground biomass ~322 ± 54 Mg ha-1 (≥10 cm DBH) and mean wood density ~0.67 g cm-3; species richness ~280 species per hectare (≥10 cm DBH).

## Experimental design
- AFEX is a full factorial fertilization experiment with eight treatments and four replicates per treatment (32 plots total), organized into four independent blocks at least 200 meters apart.
- Fertilization schedule: annually 125 kg ha-1 N (urea), 50 kg ha-1 P (triple superphosphate), 50 kg ha-1 K (KCl), plus 50 kg ha-1 Ca and 20 kg ha-1 Mg as dolomitic limestone; treatments include controls and combinations of N, P, and cations.
- Plots are 50 × 50 meters, with at least 50 meters between plots, established in similar soil, vegetation, and topography.

## Data collection and measurement methods
- Stem respiration (CO2 efflux) measured on 320 trees (10 per plot) in October 2019 using an infrared gas analyser (EGM-4). A collar was installed at the tree and sealed for 2 minutes to determine CO2 efflux.
- Soil respiration measured with Li-Cor Li-8100A system using a 20 cm chamber; two collar types used to partition respiration sources:
  - Short collar (10 cm depth) capturing total soil respiration including rhizosphere.
  - Deep collar (25 cm depth) with a window to exclude roots and mycorrhizae (S-type excludes roots/mycorrhizae; M-type excludes roots but allows mycorrhizae; later limited as roots entered the collar in 2018).
- Collar deployment included two groups per plot, with depth and window configurations to separate autotrophic and heterotrophic components.
- Sampling timeline:
  - 2017: June–July, September, October, November
  - 2018: monthly through September
  - 2019: January, February, April, July, October

## Data management and metadata
- Data spreadsheets deposited in the EIDC system, with detailed field definitions:
  - Stem CO2 efflux dataset fields include: TAG (tree ID), POM (plot inventory point), Block, Plot, DBH, Inicial_CO2, Final_CO2, Date, PlotID.
  - Soil CO2 efflux dataset fields include: Census, File.Name, Date, Block, Plot, Group, Type (collar type: T = shallow; M = deep with window; S = deep without window), PlotID, Date_IV, Obs, Lin_Flux (µmol m-2 s-1).
- Tables describe data structure and column meanings (e.g., PlotID as block+plot combination; collar types T/M/S with their implications for root/mycorrhizae exclusion).
- Data collection and management emphasize openness, traceability, and reproducibility of measurements and metadata.

## Key considerations for monitoring frameworks
- The AFEX design demonstrates rigorous replication, full-factorial treatment structure, and standardized measurement protocols essential for robust environmental monitoring.
- Detailed metadata and data organization facilitate transparency and reuse across studies and policy-relevant assessments.
- Use of publicly accessible data repositories (EIDC) aligns with governance and data-sharing requirements commonly faced by monitoring framework authors.
- Methodological notes (e.g., collar depth and root ingress over time) illustrate the need to adapt measurement approaches while documenting changes for interpretability.