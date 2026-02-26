# AFEX Experiment

- Site and climate
  - Location: AFEX project area, Biological Dynamics of Forest Fragments Project (BDFFP/INPA), ~80 km north of Manaus, Amazonas, Brazil.
  - Climate: mean air temp ~26°C; mean annual precipitation ~2,400 mm; relative humidity 75–92% (August–April).

- Experimental design
  - Full factorial nutrient addition experiment with eight treatments: Control; N; P; cations (Ca, Mg, K); N+P; N+cations; N+P+cations.
  - 4 replicate plots per treatment; 4 independent blocks (each at least 250 m apart).
  - Plot layout: each plot 50 m x 50 m; central measurement area 30 m x 30 m.
  - Nutrient application: dry granules applied three times per year.
    - Rates: N 125 kg ha-1 year-1 (as urea); P 50 kg ha-1 year-1 (as triple superphosphate); Ca 50 kg ha-1 year-1; Mg 20 kg ha-1 year-1 (as dolomitic limestone); K 50 kg ha-1 year-1 (as potassium chloride).

- Root sampling and data collection
  - Ingrowth cores: five 12 cm-diameter, 30 cm-deep root-free cores per plot, installed August 2017 in central 30 x 30 m area.
  - Sampling schedule: every three months; cores collected and homogenised by plot and soil depth (0–10 cm; 10–30 cm).
  - Focus period: fine roots produced between November 2017 and February 2018 (middle of wet season).
  - Processing: roots washed; 60-minute sampling intervals used to estimate total root biomass; Michaelis-Menten asymptotic curve employed to extrapolate to 180 minutes.

- Mycorrhizal colonisation data
  - Depth for AM assessment: 0–10 cm soil depth.
  - Subsampling: fine root tips (<1 mm) analyzed for mycorrhizal colonisation.
  - Preparation: roots cleared, stained, and mounted for microscopy (Trypan Blue staining; standard tropical protocols adapted).
  - Quantification: percentage of root length colonised by mycorrhizal structures; categories include hyphae, arbuscules, vesicles, and composite indicators (e.g., hyphae_arbuscule, hyphae_ves, hyphae_arb_ves).
  - Method details: steps include KOH clearing, autoclaving, H2O2 bleaching, 2% HCl acidifying, staining, and slide preparation evaluated at 40x.

- Data structure and spreadsheet metadata
  - Key fields include:
    - Block: 1–4 (indicating plot installation block)
    - Plot: 1–8 (per block)
    - TRT: treatment description (control, P, N, cations, N+P, N+cations, N+P+cations)
    - no_am: percentage of root length not colonised by AM
    - hyphae: percentage colonised by AM hyphae
    - hyphae_arbuscule: percentage with hyphae and arbuscules
    - hyphae_vesicle: percentage with hyphae and vesicles
    - hyphae_arb_ves: percentage with hyphae, arbuscules, and vesicles
    - total_col: total percentage of root length colonised by mycorrhizal structures
  - Descriptive labels provide context for plotting and treatment details.

- Outputs and potential data products
  - Data-ready formats for analysis of root biomass and mycorrhizal colonisation across treatments, depths, and timepoints.
  - Enables exploration of nutrient addition effects on root dynamics and AM associations.
  - Supports up-scaling to understand below-ground contributions to nutrient acquisition and forest floor processes.

- References and protocols
  - Protocols and methods cited for root sampling, mycorrhizal assessment, and chemical analyses, including:
    - AM colonisation staining and assessment methods (McGonigle et al. 1990)
    - Root sampling and processing methods (Metcalfe et al. 2007)
    - Mycorrhizal response literature (Brundrett et al. 1984; Wurzburger & Wright 2015; McCormack et al. 2015)
  - Contextual environmental data and previous measurements referenced (Araújo 2002; related ecological studies).