# Amazon Fertilization Experiment (AFEX)

- Study area and context
  - Located in the KM41 reserve of the Biological Dynamics of Forest Fragments Project (BDFFP), ~100 km from Manaus, Brazil.
  - Soils: clay-rich Ferrasols (about 30% of the Amazon Basin region); mean annual rainfall 1900–2500 mm with a pronounced dry season (June–October).
  - Forest characteristics in the area include above-ground biomass around 322 Mg ha-1 and tree species richness ~280 species per hectare (≥10 cm DBH).

- Experimental design (AFEX 2.0: Plot delineation)
  - Full factorial fertilization experiment with eight treatments across 32 plots, arranged in four independent blocks at least 200 m apart.
  - Plots are 50 x 50 m, with a minimum 50 m separation between plots.
  - Treatments: Control; nitrogen (N); phosphorus (P); cations; N + P; N + cations; P + cations; N + P + cations.
  - Fertilization schedule: annually, split into three applications to reduce leaching/runoff.
  - Fertilizer composition per year: approximately 125 kg ha-1 N (urea), 50 kg ha-1 P (Ca(H2PO4)2), 50 kg ha-1 K (KCl), and 50 kg ha-1 Ca plus 20 kg ha-1 Mg (dolomitic limestone).
  - Plot delineation materials and figures indicate all plots are located within KM41 reserve boundaries.

- Data collection methods
  - Stem respiration (CO2 efflux) measurements
    - Sampled from 320 trees with DBH > 25 cm (10 trees per plot).
    - CO2 efflux measured using an infrared gas analyser (EGM-4) with a collar attached to the tree; measurements recorded over 2 minutes.
  - Soil respiration measurements
    - Autosotrophic and heterotrophic soil respiration assessed with Li-Cor 8100A system using a 20 cm chamber.
    - Two collar configurations per plot to partition respiration components:
      - Short collar (10 cm depth) permitting access to roots and rhizosphere.
      - Long collar (25 cm depth) with windows to exclude roots and mycorrhizae (no windows variant excluded roots/mycorrhizae; some collars with windows were removed after 2018 due to root ingress).
    - Difference between measurements with 25 cm depth and surface collars used to estimate rhizosphere respiration.
  - Temporal scope
    - Field campaigns conducted across 2017 (June–November), 2018 (monthly through September), and 2019 (January, February, April, July, October).

- Data structure and data management
  - Stem CO2 efflux dataset (example structure)
    - Columns include: TAG (tree ID), POM (plot/location marker), Block, Plot, DBH, Inicial_CO2 (start), Final_CO2 (end), Date, PlotID.
    - Each row corresponds to a single measurement event per tree.
  - Soil CO2 efflux dataset (example structure)
    - Columns include: Census (campaign number), File.Name (project name), Date, Block, Plot, Group (collar group), Type (collar type), PlotID, Date_IV, Obs (measurement repetition), Lin_Flux (CO2 efflux in µmol m-2 s-1).
    - Collar types encoded as:
      - T: shallow surface collars (no root cutting; includes all soil respiration components).
      - M: deep collars (25 cm) with a 41 µm mesh window (excluded roots; developed root ingrowth by mid-2018 led to changes).
      - S: deep collars (25 cm) with no windows (exclude roots and mycorrhizae).
  - Data management notes
    - Data are deposited in the EIDC system.
    - Descriptions of fields include plot identifiers (Block, Plot), reference to measurement collars, and timing stamps for each observation.
    - Figures referenced in the document illustrate the study area, plot delineation, and measurement equipment.
  - Data interpretation context for GIS
    - Spatial layout comprises 32 plots across 4 blocks, with explicit block/plot identifiers enabling spatial joins to a GIS map.
    - Measurements link to individual trees within plots (stem respiration) and to soil respiration collars distributed within plots (spatially explicit but not necessarily provided as precise coordinates in the text).
    - Fertilization treatment as an attribute per plot enables thematic mapping of treatment effects over space and time.
  - Limitations and notes
    - 2018 collar design adjustments due to root ingress affected the continuity of certain collar types.
    - Data spans multiple years with potential variability in measurement dates and sampling intensity.

- References
  - Duque et al. 2017; De Oliveira & Mori 1999; Quesada et al. 2011; Rankin de Merona et al. 1992 (sources detailing regional forest structure, species richness, and soil properties relevant to the study area).