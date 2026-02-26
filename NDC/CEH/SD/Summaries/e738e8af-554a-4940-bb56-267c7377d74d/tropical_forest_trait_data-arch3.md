# Danum Valley Seedling Traits

- Aim and scope
  - Document and compare seedling traits for environmental monitoring to inform management decisions between primary and logged/restored forests.
  - Data supports understanding of how silvicultural practices and restoration influence seedling trait expression and potential forest recovery.

- Study context and sites
  - Location: Danum Valley Conservation Area (DVCA), Sabah, Malaysia, and adjacent Ulu Segama Forest Reserve (USFR).
  - DVCA: unlogged primary forest (approx. 438 km2) with high rainfall (~2305 mm/year) and mean temp ~25.8°C.
  - USFR: area adjacent to DVCA that was selectively logged (1981–1993); includes a trial of Reduced Impact Logging (RIL) in 1993 and restoration interventions under the Innoprise-FACE Foundation Rainforest Rehabilitation Project.
  - Forest conditions include a mix of primary forest and logged forests with varying restoration statuses.

- Plot design and management regimes
  - Seedling plots established during mast fruiting in Sep–Oct 2019:
    - Primary forest: 87 plots within the Danum Valley 50 ha ForestGEO plot.
    - Logged forest: 96 plots within INDFORSUS project plots (52 actively restored; 44 naturally regenerating).
  - Sampling occurred Jan–Feb 2020, ~6 months after mast fruiting.

- Seedling sampling
  - Measured traits on 399 seedlings from 15 species (195 in primary forest; 204 in logged forest).
  - Sampling included three individuals per seedling plot (or up to three if fewer available), with additional material collected outside plots for replication.
  - Mortality and access issues reduced sampling in some logged plots; some species represented only in primary or only in logged forest.

- Species coverage and distribution
  - Seven species sampled in multiple plots across forest types; Dryobalanops lanceolata sampled only in logged forest due to absence in primary plots.
  - Several species limited to either primary or logged forest; most are canopy/emergent species, with some smaller species (e.g., B. sessifolia, Agelaea sp., Spatholobus sp.).

- Trait measurements and methods
  - 14 traits measured per seedling:
    - Biomass components: Leaf Mass Fraction (LMF), Root Mass Fraction (RMF), Total Biomass.
    - Leaf traits: Leaf Mass per Area (LMA), Leaf Thickness, Leaf Force to Punch (LFP), Leaf Area to Shoot Area (LA:SA).
    - Root/shoot architecture: Root Length to Shoot Length (RL:SL), Specific Maximum Root Length (SMRL).
    - Foliar nutrients: Leaf Nitrogen (Nleaf), Phosphorus (Pleaf), Calcium (Leaf Cale), Magnesium (Leaf Mg), Potassium (Leaf K), plus Leaf N:P ratio.
  - Measurements and processing
    - Leaves scanned for area; LMA calculated from dry mass and leaf area.
    - Leaf thickness measured at multiple leaves; LFP measured with a force gauge.
    - Biomass and masses determined after oven-drying; moisture content estimated for dry-basis corrections.
    - Foliar nutrients analyzed via digestion and colorimetric/spectrometric methods.
  - Sampling details
    - Seedlings collected outside seedling plots; additional 10 seedlings per plot combined with plot samples for foliar analyses.
    - When nearby seedlings were unavailable due to mortality or access, samples were taken 20–40 m away to improve trait estimates.

- Data structure and fields
  - Dataset: Danum_Valley_Seedling_Traits.csv
  - Key fields and descriptions
    - Date, Forest (primary vs logged), Management (Natural Regeneration vs Active Restoration), Species, Family, Seedling.Plot, Individual.
    - Measurements: Biomass, RL:SL, LMF, RMF, LMA, Leaf.Thickness, LFP, LA:SA, Leaf.N, Leaf.P, Leaf.Ca, Leaf.K, Leaf.Mg, Leaf.N:P, SMRL.
    - Unit specifications for each field (e.g., g for biomass, mm/mm for RL:SL, etc.).
  - Data provenance notes
    - Clear definitions and methods linked to each trait (how measurements were obtained and calculated).
    - Leaves analyzed after collection; standardized processing and drying protocols documented.
  - Purpose of the data dictionary
    - Enables reuse for cross-site comparisons, meta-analyses, and monitoring frameworks, with explicit metadata to support interpretation and replication.

- Data quality, limitations, and considerations
  - Challenges
    - High mortality in logged forests and access constraints reduced sampling in some plots.
    - Not all species represented in both forest types; some species unique to primary or logged sites.
  - Metadata and standardization
    - Comprehensive data dictionary and method details enhance transparency and comparability.
    - Activity restoration status and forest type captured to support monitoring of restoration outcomes.
  - Implications for monitoring
    - Provides baseline and comparative trait data across management regimes (primary vs logged; natural regeneration vs active restoration).
    - Facilitates assessment of restoration effectiveness on early seedling trait expression and potential forest regeneration trajectories.

- Applications for monitoring frameworks and policy
  - Supports evidence-based decision-making on restoration approaches (e.g., active restoration vs natural regeneration) and silvicultural practices.
  - Enables tracking of functional trait changes in seedling communities as indicators of ecosystem recovery and resilience.
  - Demonstrates how detailed trait data and standardized metadata can underpin transparent data governance and data-sharing practices within environmental monitoring programs.