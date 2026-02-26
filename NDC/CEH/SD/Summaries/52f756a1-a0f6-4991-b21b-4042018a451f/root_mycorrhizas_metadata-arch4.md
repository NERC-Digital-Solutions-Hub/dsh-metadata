# AFEX Experiment

- Location and context: Conducted in the AFEX project area at the Biological Dynamics of Forest Fragments Project (BDFFP/INPA), about 80 km north of Manaus, Brazil. Tropical climate with mean temp ~26°C, mean annual rainfall ~2,400 mm, high humidity.

- Experimental design and data implications:
  - Full factorial nutrient addition experiment with eight treatments, including an untreated control and combinations of nitrogen (N), phosphorus (P), and cations (Potassium K, Magnesium Mg, Calcium Ca).
  - 4 independent blocks, each with 8 plots (32 plots total), spaced to minimize cross-treatment interference.
  - Each plot 50 m x 50 m; central measurement area 30 m x 30 m.
  - Data-relevant setup: clear documentation of blocks, plots, and treatment codes to support data lineage and reproducibility.

- Treatments and nutrient rates (data context):
  - Treatments: Control, N, P, cations (Ca, Mg, K), N+P, N+cations, N+P+cations.
  - Annual application rates (for data understanding and replication): N 125 kg ha^-1 year^-1 (urea), P 50 kg ha^-1 year^-1 (triple superphosphate), Ca 50 kg ha^-1 year^-1, Mg 20 kg ha^-1 year^-1 (dolomitic limestone), K 50 kg ha^-1 year^-1 (potassium chloride).

- Plot-level data collection and sampling design:
  - Root ingrowth cores: Five 12 cm diameter, 30 cm deep, root-free cores per plot installed August 2017 in the central 30 x 30 m area; sampled every three months (n=64 core samples per depth interval across plots).
  - Depth strata for analysis: 0–10 cm and 10–30 cm soil depths.
  - Temporal window for study-specific root sampling: November 2017 to February 2018 (middle of the wet season).
  - Biomass estimation: cumulative root biomass from four 15-minute sampling blocks (total 60 minutes) extrapolated to 180 minutes using Michaelis-Menten asymptotic curve to estimate total potential biomass sampled.

- Root processing and mycorrhizal assessment:
  - Fine-root focus: subsampling of 0–10 cm depth for mycorrhizal colonization assessment in root tips (<1 mm diameter).
  - Mycorrhizal assessment protocol: cleaning, clearing, staining, and microscopy (Trypan Blue staining; 40x magnification) to quantify the percentage of root length colonized by AM fungi.
  - Colonization metrics captured as percentages along the root length for different structures (hyphae, arbuscules, vesicles) and combinations (hyphae_arbuscule, hyphae_vesicle, etc.), plus a total colonization percentage.

- Data documentation and metadata:
  - Spreadsheet structure includes blocks and plots for identification; TRT for treatment; no_am (non-colonized length); hyphae, hyphae_arbuscule, hyphae_vesicle, hyphae_arb_ves (colonization components); total_col (total colonization); plus descriptive fields for blocks, plots, and treatments.
  - Units and data points embedded within the spreadsheet: nutrient application details, plant root biomass estimates, and colonization metrics.

- Data quality, standards, and references:
  - Methodological references provided for root sampling, mycorrhizal assessment, and biomass extrapolation (e.g., Metcalfe et al. 2007; Brundrett et al. 1984; McGonigle et al. 1990; McCormack et al. 2015; Wurzburger & Wright 2015).
  - Documentation supports traceability from blocks to plots to treatments and measurement outcomes, enabling reproducibility and cross-study comparisons within tropical forest nutrient manipulation experiments.

- Practical considerations for data leaders:
  - Data richness includes both below-ground biomass and symbiotic associations across multiple nutrient treatments, with detailed sampling timing and depths.
  - Structured data dictionary (spreadsheet fields) enhances discoverability and metadata completeness.
  - The design supports analyses of nutrient limitation, root foraging, and AM fungal responses across spatial (plot/block) and temporal (seasonal) scales.
  - Potential data integration needs: harmonizing units (kg ha^-1 year^-1, percentage colonization), matching depth layers, and aligning time points for cross-study comparisons.