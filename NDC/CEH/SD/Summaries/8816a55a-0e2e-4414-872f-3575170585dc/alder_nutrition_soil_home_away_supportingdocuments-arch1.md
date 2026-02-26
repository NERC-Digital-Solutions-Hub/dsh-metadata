# Plant biomass, nutrition, ecosystem carbon fluxes and soil nutrients in common alder growing on home and away soil from Aberdeenshire, Scotland. 2018

- Aim and hypotheses
  - Test how conspecific (home) vs. heterospecific (family/away) soils and their associated symbionts shape alder seedling performance (growth, nutrition) and belowground carbon allocation.
  - Hypotheses:
    - (1) Seedlings in home soils perform better due to specialist symbionts, indicating positive plant–soil feedback.
    - (2) Seedling nutritional status influences 13C allocation belowground; specifically:
      - (2a) leaf N content relates to Frankia nodulation and belowground C allocation.
      - (2b) leaf P content is higher in home soils because specialist ectomycorrhizal (ECM) fungi enhance P acquisition.

- Study design
  - Field collection of intact soil cores from three stands in Crathes Estate, Aberdeenshire: alder (Alnus glutinosa), birch (Betula pendula), and Douglas fir (Pseudotsuga menziesii).
  - Establishment of mesocosms: 10 mesocosms per stand (3 stands), with root-excluding cores to allow in-growth of soil biota but prevent root ingrowth.
  - Seedling planting: one non-mycorrhizal alder seedling per mesocosm; growth monitored for 6 months.

- Experimental methods
  - 13C pulse-labelling: 2 days pre-harvest, exposure to 13C-enriched CO2 (99 atom%) for 6 hours in a controlled chamber; leaf tissues sampled before, immediately after, and at multiple post-labelling times to track 13C allocation.
  - Root-sampling and gas flux measurements:
    - In-growth root cores used to assess microbial activity and 13C release to CO2 in traps.
    - Whole-system CO2 flux measured with a Licor 8100 under light/dark conditions to estimate carbon accumulation.
  - Plant and tissue measurements:
    - Biomass partitioning: shoots, roots (primary, lateral, fine), and coarse roots separated and dried for weighing.
    - Leaf traits: leaf area-related measures (specific leaf area), total foliar C, N, and P.
    - Nutrient analyses: total and exchangeable soil C, N, P; macro- and micronutrients (K, Ca, Mg, NO3-, NH4+, Fe, Mn, Zn, S, Pb, Al), and soil pH.
    - ECM and Frankia assessment: ectomycorrhizal colonization percentage; morphotyping of ECM tips; sampling for molecular analysis; Frankia nodulation on roots.
  - Isotope and nutrient tracing:
    - 13C allocation: leaf, fine-root, and Frankia nodulation pools; 13C in NaOH traps to quantify microbial respiration and transfer.
    - 15N natural abundance measured on a subset for broader nutritional insights.
  - Molecular analyses:
    - DNA extraction from ECM tips; PCR amplification of fungal ITS region (ITS1f-ITS4); sequencing and identification against UNITE database.
    - Representative ECM taxa sequences submitted to GenBank.

- Data collection and structure
  - Data organized as columns; rows represent individual replicate cores.
  - Soil origin encoding: Ag = Alnus glutinosa, Bp = Betula pendula, Pm = Pseudotsuga menziesii.
  - Key variables and units (selected):
    - Biomass components: aboveground biomass (AboveG, mg dwt), belowground biomass (BelowG, mg dwt), coarse/lateral/fine roots (mg dwt).
    - Carbon flux: C_flux_Bio, C_flux (mg CO2 m-2 h-1).
    - ECM and nutrient metrics: ECM (%); leafN (%), leafC (%), leafP (%); g_core; soilN, soilC, soilP.
    - Isotopes and allocation: 13C_fixed (mg), d13C_leaf_t1 (per mil), d13C_fine_roots_t4 (per mil), d13C_Frankia_t4 (per mil), d13C_NaOH_t1 (per mil), d15N_NA (per mil).
    - Nutrients and pH: pH; total_N, NO3_N, NH4_N; Ca, Mg, K, P, Fe, Mn, Zn, S, Pb, Al (various units).
  - Sampling scale: multiple leaf samples per plant; biomass and chemical analyses for shoots, roots, soil, and in-growth cores.

- Analytical approach (design intent)
  - Compare seedling performance and C/N/P status across home, family, and away soils to assess potential positive plant–soil feedback.
  - Use 13C pulse-labelling to quantify allocation of recent photosynthate to belowground compartments (fine roots, Frankia nodules) and to microbial/soil pools.
  - Link ECM colonization and fungal community composition (via ITS sequencing) to nutrient uptake (P, N) and C allocation patterns.
  - Integrate soil nutrient pools and extractable ions to understand how soil origin mediates nutrient availability and uptake.

- Context and references
  - Builds on established methods for in-growth cores, 13C pulse-labelling, and ECM/fungal molecular identification (Agerer 2001; Johnson et al. 2001, 2002a, 2002b; Kõljalg et al. 2005, 2013; Pérez-Harguindeguy et al. 2013).