# Data description, Measures of peatland carbon cycling from peat mesocosm incubation experiments.

- Overview of the dataset
  - Two laboratory-based studies from Black Law Wind Farm, Lanarkshire, Scotland, investigating abiotic (temperature, water table) and biotic (plant functional type legacy) controls on peatland carbon cycling.
  - Study 1: effects on CO2 and CH4 fluxes from peat mesocosms over 322 days with a fully factorial design (temperature, water table, plant functional type legacy).
  - Study 2: effects on peat and litter decomposition and associated CO2 fluxes using litter bags over 363 days with a fully factorial design (temperature, peat PFT, litter treatments).
  - Data types span gas flux time series, litter decomposition, and comprehensive peat/peat-litter biochemical and microbial properties, enabling linkage of physical/biotic drivers to GHG flux and decomposition outcomes.

- What data are included
  - Gas flux data
    - CO2 and CH4 fluxes measured in peat mesocosms; six measurement points per experiment.
    - Methods of calculation from chamber concentrations, temperature, chamber volume, and surface area.
  - Experimental treatments and structure
    - Study 1: three temperatures (12, 14, 16°C), three water table levels (low 25 cm, intermediate 15 cm, high 5 cm), three plant functional types (shrubs Calluna vulgaris, graminoids Eriophorum vaginatum, bryophytes Sphagnum capillifolium); 108 cores across treatments; four replicates per combination.
    - Study 2: three temperatures (12, 14, 16°C), three peat PFTs, eight litter bag treatments (no litter, single-species litter for each PFT, and 1:1:1 mixture); 288 cores; four replicates per temperature × PFT × litter-treatment combination.
  - Decomposition and respiration data (Study 2)
    - Litter mass remaining (% of initial mass) after 363 days.
    - CO2 emissions measured at six time points; respiration rates derived from IRGA measurements during enclosure.
  - Peat and litter biochemical/physical properties
    - Peat: bulk density, pH, total C, total N, C:N, C stock, N stock; PLFA-based microbial community data (biotic indicators).
    - Litter: total C, total N, C:N; initial microbial community data for peat and litter.
  - Microbial and biochemical analyses (both studies)
    - PLFAs quantified by GC to infer microbial groups (bacteria vs fungi; gram-positive vs gram-negative bacteria) and overall microbial biomass.
    - Ratios: fungal-to-bacterial PLFAs (F:B); gram-positive-to-gram-negative bacterial PLFAs.
  - Sampling details and site context
    - Peat cores collected May 2011 (Study 1) and October 2012 (Study 2) from a blanket bog at Black Law Wind Farm.
    - Supplementary peat samples collected for microbial and chemical analyses; standardized sample processing and storage.

- Experimental design and replication
  - Study 1
    - Fully factorial: 3 temperatures × 3 water table levels × 3 plant functional types.
    - 12 cores per PFT per temperature-water table combination; total of 108 cores across three temperature rooms.
    - Incubation duration: 322 days with six gas measurements.
  - Study 2
    - Fully factorial: 3 temperatures × 3 peat PFTs × 8 litter treatments.
    - 4 replicates per combination; total of 288 cores.
    - Incubation duration: 363 days; six CO2 measurements and immediate respiration measurements at intervals.

- Measurements and instruments
  - Gas measurement
    - CO2 and CH4 fluxes measured with opaque chambers; headspace gas samples analyzed by Perkins Elmer AutosystemXL GC with FID and methaniser.
    - Calibration against certified standards (CO2: 500 and 4000 ppm; CH4: 1 and 10 ppm).
  - Chemical and physical analyses
    - Total C and N: LECO Truspec CN Analyser.
    - pH: Hanna pH meter.
    - Bulk density: standard soil methods.
  - Microbial analyses
    - Phospholipid fatty acids (PLFAs) extracted and quantified by GC; microbial groups identified by characteristic PLFAs.
    - Internal and external standards used for quantification and quality checks.
  - Decomposition and respiration
    - Litter bags prepared with 0.50 g air-dried litter; 1 mm mesh to balance decomposer access and loss.
    - Litter mass remaining calculated from pre- and post-incubation weights (oven-dried basis).
    - Respiration measured with portable IRGA (EGM-4) in a sealed chamber for standardized intervals.

- Data quality, handling, and provenance
  - Standardized collection and handling to minimize variability (controlled use of deionised water to regulate nutrient inputs; consistent moisture maintenance).
  - Replication across temperature rooms and treatment combinations to support robust inference.
  - Calibration and method references indicate adherence to established protocols (e.g., Holland et al., 1999; Frostegård et al.; Carter, 1993; IPCC context; related methodological literature).

- How the data can be used (Data Support perspective)
  - Time-series analyses of CO2 and CH4 flux responses to temperature, water table, and plant functional type legacy.
  - Linking GHG flux patterns to peat chemical properties, microbial community structure, and nutrient status.
  - Assessing decomposition dynamics under varying abiotic and biotic conditions, with connections to C and N cycling in peatlands.
  - Cross-study integration to explore interactions between temperature, substrate type (peat vs litter), and microbial composition on carbon cycling processes.
  - Development of data products such as dashboards or dashboards-ready datasets that enable end users to explore fluxes, decomposition rates, and microbial indicators across treatment combinations.

- References and methodological foundations
  - Methods and analytical protocols referenced across the studies (e.g., PLFA analysis, gas flux calculations, standard soil and litter analyses, and laboratory instrumentation), including Carter (1993), Holland et al. (1999), Frostegård et al. (1991, 1993), Frostegård (1993), Hogg (1993), IPCC context, and related methodological sources.