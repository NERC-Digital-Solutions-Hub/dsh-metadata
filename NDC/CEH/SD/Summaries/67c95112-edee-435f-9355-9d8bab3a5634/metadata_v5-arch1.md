# Herbivory rates, species traits and leaf traits across symbiotic nitrogen-fixing and non-fixing species from a Panamanian tropical forest, 2007-2019

## Overview
- Dataset measuring herbivory and potential controls on herbivory for nitrogen-fixing and non-fixing trees in a mature Panamanian tropical forest.
- Includes 1,626 leaves from 350 seedlings across 43 species (23 nitrogen-fixing, 20 non-fixing).
- Measurements occur at leaf and seedling levels; includes leaf chemical and physical traits at the species level and seedling traits (e.g., stem length, growth rate).
- Data collected in 2017–2018 with additional data spanning 2007–2019.
- Collected by Will Barker, S. Joseph Wright, Liza Comita, Oliver L. Phillips, Brian E. Sedio, and colleagues.

## Experimental design and scope
- Location: Barro Colorado Island (BCI), Panama, within the 50-ha plot; latitude 9.125, longitude -79.8553.
- Species: 23 fixer species (from Sprent 2009) and 20 non-fixer species (nearly all fixer species present in the site sampled; 23 of 26 fixer species represented).
- Timeframe: Wet seasons of 2017 and 2018; additional data collected between 2007 and 2019.
- Sampling frame: Seedlings part of a long-term census of freestanding woody seedlings (≥20 cm stem height, <1 cm diameter) in the 50-ha plot (2001–2018).

## Measures of herbivory
- Leaves: herbivory quantified on mature leaves (up to six per individual; mean ~4.9) and on young leaves (226 leaves; one per seedling) to capture age-related differences.
- Methods: leaf area scanned with a handheld scanner (1050 DPI); ImageJ used to estimate undamaged leaf area and leaf area lost to herbivory.
- Metrics:
  - Incidence of herbivory: binary (any leaf area missing vs. none).
  - Proportion of leaf area lost to herbivory: continuous (0–1).
- Growth context: growth rate derived from stem length changes between 2017 and 2018; relative growth rate calculated as ln(stem length2018 − stem length2017).

## Species attributes and leaf traits
- Leaf chemistry and structure: concentrations of nitrogen (N), carbon (C), phosphorus (P), potassium (K), calcium (Ca); cellulose, hemicellulose, lignin, silicon; leaf toughness metrics (lamina toughness, vein toughness, lamina density, work to shear, LMA).
- Trait sourcing: leaf traits measured on shade leaves to reflect seedling canopy conditions (samples from various light environments; 3 leaves per species per light condition from selected individuals).
- Chemical similarity: network-based metrics from leaf metabolite profiles:
  - nnCSCS: nearest-neighbour Chemical Structural and Compositional Similarity.
  - mCSCS: mean Chemical Structural and Compositional Similarity.
- Trait data collection window: 2007–2008, focusing on leaves from the highest crown points; samples stored on ice and oven-dried at 60°C; measurements include shade leaf values.

## Data structure and contents
- Five CSV files:
  - Leaf_herbivory_BCI_2017.csv: leaf-scale herbivory (spp, plot, p5, tag, leaf, fix, area, stem_length, incidence_of_herbivory, proportion_of_herbivory).
  - seedling_herbivory_BCI_2017.csv: seedling-scale herbivory (spp, plot, p5, tag, fix, area, stem_length, incidence_of_herbivory, proportion_of_herbivory, gr_rate).
  - herbivory_rate_BCI_2017.csv: herbivory rate on young leaves (spp, fix, plot, p5, tag, area, stem_length, incidence_of_herbivory, proportion_HR, proportion_of_herbivory_perc_diff).
  - simulated_species_herbivory.csv: predicted species-level herbivory (spp, fix, pred_prob, pred_prob_se, pred_prop, pred_prop_se).
  - spp_leaf_traits.csv: species-level leaf traits (spp, fix, n_shad, c_shad, p_shad, Ca_shad, k_shad, mCSCS, nnCSCS, Shade_cellulose, Shade_hemicellulose, Shade_lignin, Shade_silicon).
- Column details include:
  - spp: six-letter species code; fix: fixation status; plot/p5/tag: spatial identifiers; leaf: leaf identifier; area, stem_length, Incidence_of_herbivory, Proportion_of_herbivory, Gr.rate; Pred_prob/Pred_prop and SEs; shade trait measurements; mCSCS/nnCSCS.
- Units: herbivory incidence (0/1), proportion of herbivory (0–1); leaf area loss rate in cm2/day over three months; leaf nutrients in mg/g; toughness and mass-specific metrics in respective units; growth rate as ln(differences in stem length per day); all trait concentrations reported per leaf tissue.

## Data quality, processing, and validation
- Automated leaf-spot measurements with ImageJ, followed by manual verification against leaf images.
- Dual methods for young-leaf herbivory rates to account for leaf loss and possible leaf growth:
  - Rate based on difference in area divided by initial total leaf area.
  - Rate based on difference in percentage missing to handle leaf growth.
- Both methods converge for non-changing leaves, enhancing dataset robustness.
- Statistical analyses (described in text) use R 3.5.1 with appropriate packages (bootpredictlme4, glmmTMB); models include species identity as fixed effects and 20-m plot as a random effect to address spatial autocorrelation.

## Analytical opportunities for data-driven insights
- Compare herbivory between nitrogen-fixing and non-fixing species to test the central hypothesis about fixation status and herbivory rates.
- Explore relationships between leaf traits (nutrients, toughness, structural components) and herbivory incidence and intensity.
- Assess how seedling size (area, stem_length) mediates herbivory risk and whether size-adjusted effects differ by fix status.
- Utilize chemical similarity metrics (nnCSCS, mCSCS) to examine whether chemical relatedness among species predicts herbivory patterns.
- Validate and compare observed herbivory with species-level predictions (pred_prob, pred_prop) to evaluate model performance and extrapolate to unmeasured species.
- Investigate spatial autocorrelation with plot-level random effects and assess scale-dependent patterns across the 20 m × 20 m plots.

## Timeframe and scope of data
- Herbivory measurements: 2017–2018.
- Leaf trait and chemical-difference data: 2007–2008 (shade leaves) with broader measurements through 2019.
- Longitudinal context: seedlings have been part of a census from 2001–2018; 2017–2018 measurements anchored within this framework.

## References and methodological background
- Comita, Muller-Landau, Aguilar, Hubbell (2010): asymmetric density dependence in tropical tree communities.
- Sprent (2009): global perspective on legume nodulation and fixation.
- Westbrook et al. (2011): correlations between leaf toughness traits and demographic rates in shade-tolerant species.
- Analytical tools: R Core Development Team; bootpredictlme4; glmmTMB.