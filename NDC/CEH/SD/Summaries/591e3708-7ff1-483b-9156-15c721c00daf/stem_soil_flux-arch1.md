# Amazon Fertilization Experiment (AFEX)

## 1. Study area
- Located in the BDFFP area, KM41 reserve, ~100 km from Manaus (02°24'S, 59°52'W).
- Soils: clay-rich Ferrasols (~30% of the Amazon Basin).
- Climate: annual rainfall 1900–2500 mm with a pronounced dry season (June–October).
- Forest characteristics (for context): above-ground biomass (AGB) ~322 ± 54 Mg ha^-1 (≥10 cm DBH); mean wood density ~0.67 g cm^-3; ~280 species (≥10 cm DBH) per hectare.

## 2. AFEX experimental design and plot delineation
- AFEX: full factorial fertilization experiment with eight treatments and four replicates per treatment (32 plots total).
- Treatments: Control; nitrogen (N); phosphorus (P); cations; N+P; N+cations; P+cations; N+P+cations.
- Plot layout: 50 × 50 m plots, minimum 50 m apart; four independent blocks (B1–B4) at least 200 m apart.
- Fertilization: annual applications (three applications per year) to reduce leaching/runoff.
  - Rates per year: N 125 kg ha^-1 (as urea), P 50 kg ha^-1 (as triple superphosphate), cations 50 kg ha^-1 (as KCl), Ca 50 kg ha^-1, Mg 20 kg ha^-1 (as dolomitic limestone).
- AFEX 2.0: updated plot delineation within KM41 to locate all fertilized blocks and plots.

## 3. Collection methods and measurements
- Stem respiration (CO2 efflux)
  - 320 trees total (≥25 cm DBH), 10 trees per plot.
  - Measurement instrument: infrared gas analyser (EGM-4, PP systems) with a collar attached to the tree.
  - Protocol: CO2 efflux measured over 2 minutes.
- Soil respiration (autotrophic and heterotrophic)
  - Instrument: Li-Cor Li-8100A with 20 cm survey chamber.
  - Two collar types per plot to partition respiration sources:
    - Short collar (10 cm depth): captures all soil respiration components.
    - Long collar (25 cm depth): with/without windows to exclude roots and mycorrhizae (windows exclude roots; the no-window version excludes both roots and mycorrhizae).
  - Difference between 25 cm and surface collars used to estimate rhizosphere respiration.
  - Collar types used: T (shallow, no roots cut), M (deep with window, allows mycorrhizae ingrowth; used until mid-2018), S (deep with no windows, excludes roots and mycorrhizae).
- Sampling timeline
  - 2017: June–July, September, October, November.
  - 2018: monthly through September.
  - 2019: January, February, April, July, October.
- Data organization and measurement metadata
  - Stem CO2 data and soil CO2 data are stored in spreadsheets deposited in the EIDC system.
  - Stem data fields include: TAG (tree ID), POM Block, Plot, DBH, Inicial_CO2, Final_CO2, Date, PlotID.
  - Soil data fields include: Census/File.Name, Date, Block, Plot, Group (collar group), Type (collar type), PlotID, Date_IV, Obs (replicate), Lin_Flux (soil CO2 efflux in µmol m^-2 s^-1).

## 4. Data spreadsheets and variables
- Stem CO2 efflux spreadsheet
  - Key columns: TAG, POM, Block, Plot, DBH (D), Inicial_CO2 (F), Final_CO2 (G), Date (H), PlotID (I).
- Soil CO2 efflux spreadsheet
  - Key columns: Census/File.Name, Date, Block, Plot, Group, Type, PlotID, Date_IV, Obs, Lin_Flux.
- Column-level descriptions
  - Block: B1, B2, B3, B4.
  - Plot: P1–P8 within each block.
  - Group: collars installed on the ground (types).
  - Type: T (shallow), M (deep with window), S (deep without window).
  - PlotID: Block + Plot combination.
  - Lin_Flux: CO2 flux in µmol m^-2 s^-1.

## 5. Data quality, management, and accessibility
- Data are organized for cross-dataset analysis (stem vs soil respiration) and tied to plot, block, and tree-level metadata.
- Data deposited with metadata in the EIDC system to support discoverability and reuse.
- Notable data issues:
  - Root intrusion into deep-with-window collars began affecting measurements after mid-2018, prompting changes in collar approach.
  - Scale and resolution: measurements cover plots within KM41, which may limit broad-scale extrapolation but are suitable for within-plot and within-block analyses.

## 6. References (context for methods and site characteristics)
- Duque et al. 2017. Insights into regional patterns of Amazonian forest structure.
- De Oliveira & Mori 1999. High tree species richness in central Amazonia terra firme forest.
- Quesada et al. 2011. Soils of Amazonia, rainforest site references.
- Rankin de Merona et al. 1992. Large-scale upland rainforest inventory (Central Amazon).