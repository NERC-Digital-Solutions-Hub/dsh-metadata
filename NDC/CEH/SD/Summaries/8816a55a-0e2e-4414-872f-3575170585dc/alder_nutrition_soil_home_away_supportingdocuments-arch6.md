# Plant biomass, nutrition, ecosystem carbon fluxes and soil nutrients in common alder growing on home and away soil from Aberdeenshire, Scotland. 2018

## Aim and scope
- Investigates how conspecific (home) vs heterospecific (family/away) soils and their associated symbionts influence alder seedling growth, nutrition, and carbon allocation.
- Uses 13C pulse-labelling to trace recent photosynthate allocation to fine roots and symbiotic partners (Frankia nodules and ectomycorrhizal fungi).
- Tests relationships between leaf nutrient status (N, P) and belowground carbon/nutrient allocation.
- Explores how soil origin and symbionts affect ecosystem carbon flux and nutrient pools.

## Experimental design
- Mesocosms created from intact soil cores collected from three stands in Crathes Estate, Aberdeenshire: alder (home soil), birch (family soil), and Douglas fir (away soil).
- 10 mesocosms per stand (N=30 total); cores collected on a grid, with root-excluding in-growth cores inserted to capture belowground processes while excluding roots.
- One non-mycorrhizal alder seedling transplanted into each mesocosm; plants measured monthly for 6 months.
- Growth conditions: climate chamber at 20°C with 14 h light; seeds germinated under sterile conditions.

## Data collection and measurements
- Plant growth and morphology:
  - Seedling height and leaf number tracked from planting to harvest.
  - Specific leaf area (SLA) measured.
  - Biomass components separated and weighed: shoots, coarse roots, lateral roots, fine roots; roots categorized by type.
- Nutrient status:
  - Foliar C, N, P; leaf N and P content; g_core and soil nutrient pools (C, N, P).
  - Total and exchangeable nutrients in soil: K, Ca, Mg, P, NO3−, NH4+; pH measured; S, Fe, Mn, Zn, etc. also quantified.
- Symbiotic status:
  - Ectomycorrhizal (ECM) colonization percentage measured from fine root tips; ECM morphotypes classified; subsamples subjected to molecular analysis.
  - Frankia nodulation counted; nodules analyzed per seedling.
- Carbon flux and isotopes:
  - 13C pulse-labelling: 6 hours of 99 atom% 13C-CO2 exposure; leaf samples taken before, immediately after, and every 12 hours up to 48 hours post-labelling.
  - 13C measured in leaves, fine roots, and Frankia nodules; 13C allocation belowground quantified as mg 13C.
  - 13C and 12C ratios in NaOH trap CO2 measured to track belowground microbial respiration; whole-system CO2 flux recorded pre-harvest under light and dark conditions.
- Plant and soil tissue analysis:
  - Leaf tissue 13C concentration via cavity ring-down laser spectrometry; 15N natural abundance measured on a subset.
  - Root and shoot tissues dried and weighed; leaf and root samples milled for elemental and isotopic analyses.
- Molecular ecology:
  - ECM fungal DNA extracted from representative tips; ITS region amplified (ITS1f/ITS4), sequenced; data compared to UNITE database; representative ECM taxa deposited in GenBank (MT499907–MT499914).

## Data structure and variables
- Data organized in columns; rows correspond to individual replicate cores.
- Soil origin labels: Ag = Alnus glutinosa (home), Bp = Betula pendula (family), Pm = Pseudotsuga menziesii (away).
- Key units:
  - Biomass, above/below ground, coarse/lateral/fine roots: mg dry weight (dwt)
  - Carbon fluxes: mg CO2/m2/h
  - ECM: percentage colonization
  - 13C and 15N metrics: mg, per mil (‰)
  - Leaves: number, leafC (%), leafN (%), leafP (%)
  - Soil pools: C, N, P (% or µg 10 cm−2 21 days−1 for some nutrients)
  - pH and other mineral concentrations (µg 10 cm−2 21 days−1 where specified)
  - 13C_fixed, d13C_leaf, d13C_fineroot, d13C_Frankia, d13C_NaOH, etc.
- Molecular data: ECM morphotypes, accession numbers, and GenBank entries for representative taxa.

## Methods and analytical approaches
- Soil and plant chemical analyses performed with elemental analyzers (C, N) and colorimetric/flow analyzers (P); nutrient exchange measured with in situ ion exchange membranes.
- Isotope analyses conducted via cavity ring-down spectroscopy and CF-IRMS; isotopic data calibrated against standards.
- ECM fungal identifications via ITS sequencing; taxa annotated against UNITE; representative sequences deposited in GenBank.
- Data quality considerations noted: small leaf tissue samples for isotopes; potential minimal impact on fluxes; cross-instrument calibration for isotopic measurements.

## Data products and potential use
- A comprehensive multi-layer dataset linking soil origin, plant growth, nutrition, carbon flux, and microbial symbioses.
- Enables exploration of:
  - How soil origin and symbiont communities influence seedling performance and nutrient use efficiency.
  - Spatial and temporal patterns of carbon allocation from shoot to roots and symbionts.
  - Relationships between leaf nutrient status and belowground carbon/nutrient partitioning.
  - Interactions between ECM diversity, Frankia nodulation, and plant growth under different soil backgrounds.
- Suitable for model validation of plant–soil–microbe interactions and for developing dashboards that enable self-service exploration of carbon flux and nutrient dynamics in relation to soil origin.