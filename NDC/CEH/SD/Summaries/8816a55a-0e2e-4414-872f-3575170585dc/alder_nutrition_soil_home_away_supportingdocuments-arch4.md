# Plant biomass, nutrition, ecosystem carbon fluxes and soil nutrients in common alder growing on home and away soil from Aberdeenshire, Scotland. 2018

- ## Overview
  - Investigates how soil origin (home alder soil vs. family birch soil vs. away Douglas fir soil) influences alder seedling performance, nutrition, and carbon allocation.
  - Tests relationships between seedling nutritional status, 13C allocation to fine roots and symbionts (ECM fungi and Frankia), and above-/below-ground allocation in different soil origins.
  - Hypotheses include superior performance in home soils due to specialist symbionts and linked belowground 13C allocation to leaf N and Frankia nodulation; higher leaf P in home soils due to ECM-facilitated P acquisition.

- ## Experimental design and sampling
  - 30 intact soil cores collected from three stands (alder, birch, Douglas fir) at Crathes Estate, Aberdeenshire.
  - Within-stand grid: 10 mesocosms per stand; roots excluded in certain cores to capture microbial respiration.
  - One sterilized alder seedling transplanted into each mesocosm (10 per stand).
  - Growth conditions: 20°C with 14 h daylight; 6 months until harvest.
  - Measurements included seedling height, leaf count, and monthly growth data.

- ## Isotope tracing and carbon/nitrogen flux measurements
  - 13C pulse-labelling: 13C-enriched CO2 provided for 6 hours prior to harvest.
  - Leaf sampling: pre-labelling and at multiple post-labelling intervals to track 13C uptake, allocation, and respiration.
  - Root exclusion cores collected 13C-CO2 in NaOH traps to gauge microbial activity and carbon release.
  - Whole-system CO2 flux measured pre-harvest under light and dark conditions.
  - Allocation of 13C belowground partitioned to fine roots and Frankia nodules; additional 15N natural abundance measured in a subset.

- ## Plant and tissue measurements
  - Biomass components: shoots, roots (coarse, lateral, fine), dry weight.
  - Functional traits: Specific leaf area (SLA); ectomycorrhizal (ECM) colonization (%) assessed microscopically; ECM morphotyping and subsampling for molecular analyses.
  - Nutrients: foliar C, N, P; leaf N and P content; 13C in leaves and selected root tissues; nodulation status for Frankia.

- ## Soil nutrient pools and chemical analyses
  - Total and exchangeable nutrient pools: K, Ca, Mg, P, NO3−, NH4+.
  - In situ ion-exchange membrane probes used to estimate nutrient supply rates.
  - Post-harvest soil analyses: total C, total N, total P; soil pH.
  - Nutrient data reported per soil origin (Ag = Alnus glutinosa, Bp = Betula pendula, Pm = Pseudotsuga menziesii).

- ## Molecular analysis of ectomycorrhizal fungi
  - DNA extraction from representative ECM tips; ITS1f/ITS4 primers used for fungal amplification.
  - Sequencing performed and processed (BioEdit; FASTA conversion) and compared against UNITE database.
  - Representative ECM taxa sequences submitted to GenBank (MT499907–MT499914).

- ## Data structure and variables
  - Data organized in columns; rows correspond to replicate cores.
  - Soil origin encoded as Ag (Alnus glutinosa), Bp (Betula pendula), Pm (Pseudotsuga menziesii).
  - Key variables and units include:
    - Biomass metrics (mg dry weight): aboveground, belowground, coarse/ lateral/ fine roots.
    - Carbon flux metrics (mg CO2/m2/h; C_flux_Bio): respiration and photosynthate dynamics.
    - Isotope data (d13C, 13C_fixed; per mil; mg 13C): leaves, fine roots, Frankia nodules; NaOH trap data (d13C_NaOH).
    - Nutrients: leaf N, leaf C, leaf P; soil N, soil C, soil P; micro-nutrient concentrations (Ca, Mg, K, etc.).
    - ECM metrics: colonization (%); nodulation counts (Al, etc.).
    - Sampling metadata: leaf count, SLA, pH, and other soil chemical properties.
  - Data sources include plant tissue analyses, soil chemistry, isotope tracing results, and DNA sequence data.

- ## Data handling, accessibility, and references
  - Fungal sequence data linked to GenBank accession MT499907–MT499914.
  - Fungal identifications aligned with UNITE database (sequence-based identification).
  - Methods align with standardized trait measurements (e.g., Pérez-Harguindeguy et al. 2013) for plant functional traits.

- ## Implications for data leadership and governance
  - Demonstrates integration of multi-modal data: physical plant measurements, isotope tracing, soil chemistry, and molecular biology.
  - Highlights the importance of clear metadata, standardized units, and documentation for reproducibility (e.g., explicit soil origin coding and measurement units).
  - Emphasizes data provenance and traceability across diverse data streams, including external database references (GenBank, UNITE).
  - Points to potential data-collection challenges relevant to data strategy: coordinating heterogeneous data types, ensuring consistency across sampling times and mesocosms, and managing small-tample tissue analyses with robust QA/QC.