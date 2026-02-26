# Amazon Fertilization Experiment (AFEX)

- Study location and context:
  - Conducted within the Biological Dynamics of Forest Fragments Project (BDFFP) area, KM41 reserve, ~100 km from Manaus, Amazonia.
  - Site features: Ferralsol soils (~30% of the Amazon Basin), annual rainfall 1900–2500 mm with a pronounced dry season (June–October).
  - Forest baseline: above-ground biomass (AGB) ~322 ± 54 Mg ha^-1; mean wood density ~0.67 g cm^-3; ~280 species (≥10 cm DBH) per hectare.
  - AFEX started March 2017 as a full factorial fertilization experiment.

- Experimental design (AFEX 1.0):
  - Fully factorial with eight treatments and four replicates per treatment (32 plots total) arranged in four independent blocks at least 200 m apart.
  - Plot size: 50 x 50 m; treatments distributed across plots with consistent soil, vegetation, and topography.
  - Fertilization regime (annual, split into three applications to reduce leaching/runoff):
    - 125 kg ha^-1 year^-1 N as urea
    - 50 kg ha^-1 year^-1 P as triple superphosphate
    - 50 kg ha^-1 year^-1 cations (KCl, Ca, Mg as dolomitic limestone)
  - Treatments:
    - Control
    - Nitrogen (N)
    - Phosphorus (P)
    - Cations
    - N + P
    - N + Cations
    - P + Cations
    - N + P + Cations

- AFEX 2.0: plot delineation and ongoing management
  - Location maps indicate all fertilized AFEX blocks/plots within KM41.
  - Fertilization conducted annually by hand along a systematic walk within plots.

- Data collection methods (CO2 flux measurements):
  - Stem respiration (CO2 efflux):
    - 320 trees (DBH > 25 cm), 10 trees per plot, measured October 2019.
    - Instrument: infrared gas analyser (EGM-4, PP Systems) with a sealed collar and 2-minute measurement.
  - Soil respiration (autotrophic and heterotrophic components):
    - Li-Cor Li-8100A system with 20 cm survey chamber.
    - Two collar types at two randomly chosen points per plot:
      - Short collar (surface) measuring all flux components (rhizosphere included).
      - Long collar (25 cm depth) with windows to exclude roots and mycorrhizae.
      - A third type (25 cm depth, no window) excluded roots and mycorrhizae; used for comparison with the windowed collar.
    - Rhizosphere respiration estimated as the difference between 25 cm and surface measurements.
  - Sampling timeline:
    - 2017: June–July, Sept, Oct, Nov
    - 2018: monthly through September
    - 2019: January, February, April, July, October

- Data management and datasets:
  - Stem CO2 efflux dataset (deposited in EIDC system) structure:
    - Key columns include: TAG (tree ID), POM (measurement location), Block, Plot, DBH, Inicial_CO2 (start flux), Final_CO2 (end flux), Date, PlotID, and a plotting of measurement data.
  - Soil CO2 efflux dataset (deposited in EIDC system) structure:
    - Key fields include: Census (campaign), File.Name (project name), Date, Block, Plot, Group (collar set), Type (collar type), PlotID, Date_IV (timestamp), Obs (repeat), Lin_Flux (flux in µmol m^-2 s^-1).
  - Collar type definitions:
    - T = shallow surface collars (all soil components)
    - M = deep collars with a window (excluded roots; allowed mycorrhizae; later discontinued due to root ingress)
    - S = deep collars with no window (exclude roots and mycorrhizae)
  - Data column notes summarize experimental blocks, plots, measurement dates, and flux calculations.

- References and context:
  - Foundational studies on Amazon forest structure, species richness, and soils (Duque et al., De Oliveira & Mori, Quesada et al., Rankin de Merona et al.) to contextualize the AFEX experiment within regional forest dynamics and soil characteristics.