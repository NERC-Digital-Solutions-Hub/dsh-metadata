# Herbivory rates, species traits and leaf traits across symbiotic nitrogen-fixing and non-fixing species from a Panamanian tropical forest, 2007-2019

## Overview
- Dataset measuring herbivory and potential controls on herbivory for nitrogen-fixing and non-fixing trees in a mature Panamanian tropical forest.
- Includes herbivory measurements on 1,626 leaves from 350 seedlings across 43 species (23 fixing, 20 non-fixing).
- Leaf-scale and seedling-scale herbivory data, plus species-level leaf traits and seedling traits (e.g., stem length, growth rate).
- Data collected mainly in 2017–2018 (BCI 50-ha plot); supplementary data from 2007–2019.
- Collected by Will Barker, S. Joseph Wright, Liza Comita, Brian Sedio and colleagues.

## Experimental design and sampling
- Location: Barro Colorado Island (BCI), Panama; 50-hectare plot within the tropical forest.
- Species: 23 fixer species (per Sprent 2009) and 20 non-fixer species.
- Sampling: nearly all fixer species present at the site (23 of 26) and non-fixer species spanning abundance ranges; seedlings included in a long-term census (2001–2018).
- Timing: wet seasons 2017 and 2018; climate context provided (mean ~27°C, ~2600 mm annual rainfall).

## Measures of herbivory
- Mature leaves: up to six leaves per seedling scanned non-destructively (mean ~4.9); 184 fixer and 166 non-fixer seedlings; June–July 2017.
- Young leaves: 226 leaves tagged and scanned in November 2017 to capture higher herbivory and turnover.
- Method: leaf area lost to herbivory quantified with ImageJ; undamaged leaf area reconstructed for accurate herbivory estimates.
- Metrics:
  - Incidence of herbivory: binary (leaf affected or not).
  - Proportion of leaf area lost to herbivory: continuous (0–1).
- Additional data: herbivory on young leaves to measure rate over time.

## Growth rate
- Relative growth rate calculated from stem length changes between 2017 and 2018 (natural log of length difference divided by time interval).

## Species attributes and leaf traits
- Traits integrated with herbivory data:
  - Leaf nutrient concentrations: nitrogen, carbon, phosphorus, potassium, calcium.
  - Physical defense traits: cellulose, hemicellulose, lignin, silicon.
  - Leaf toughness metrics: lamina toughness, vein toughness, lamina density, work to shear, leaf mass per area (LMA).
  - Chemical similarity metrics: chemical structure/compositional similarity (nnCSCS and mCSCS), derived from leaf metabolite profiling.
- Trait sampling:
  - Shade leaves collected from the highest crown points of the six largest and six smallest individuals per species (sampling across light environments; July 2007–January 2008).
  - Measurements performed on leaves under shade conditions.

## Nature and units of recorded values
- Herbivory:
  - Incidence: 0 or 1.
  - Proportion: 0–1 (leaf area lost).
  - Growth-rate-related herbivory: proportion rate measures (see files for specifics).
- Leaf traits:
  - Nutrients (mg per g leaf tissue or equivalent for N and C), physical traits (g per g leaf tissue or related units), LMA (g cm^-2), density, and toughness metrics.
- Growth rate: natural log difference in stem length between 2018 and 2017, divided by days.
- Chemical similarity: nnCSCS and mCSCS indices describing similarity of leaf secondary metabolites across species.

## Quality control
- ImageJ-based herbivory measurements automated, with manual checks against leaf images for accuracy.
- For young leaves, two approaches to calculate herbivory rate:
  - Method 1: difference in leaf area between time points divided by estimated total leaf area at time point one.
  - Method 2: for negative rates, recalculate using percentage missing at time point one vs. time point two.
- Both methods yield the same values for leaves with no change, ensuring robust whole-dataset coverage.

## Details of data structure
- Five CSV files:
  - Leaf_herbivory_BCI_2017.csv: leaf-scale herbivory data (columns include spp, plot, p5, tag, leaf, fix, area, stem_length, incidence_of_herbivory, proportion_of_herbivory).
  - seedling_herbivory_BCI_2017.csv: seedling-scale herbivory data (columns include spp, plot, p5, tag, fix, area, stem_length, incidence_of_herbivory, proportion_of_herbivory, gr_rate).
  - herbivory_rate_BCI_2017.csv: herbivory rate on young leaves (columns include spp, fix, plot, p5, tag, area, stem_length, incidence_of_herbivory, proportion_HR, proportion_of_herbivory_perc_diff).
  - simulated_species_herbivory.csv: predicted species-average herbivory (columns include spp, fix, pred_prob, pred_prob_se, pred_prop, pred_prop_se).
  - spp_leaf_traits.csv: species-level leaf traits (columns include spp, fix, n_shad, c_shad, p_shad, Ca_shad, k_shad, mCSCS, nnCSCS, Shade_cellulose, Shade_hemicellulose, Shade_lignin, Shade_silicon).
- Legend of key columns provided to aid interpretation (e.g., spp, fix, p5, tag, Incidence_of_herbivory, Proportion_of_herbivory, Gr.rate, mCSCS, nnCSCS, shade traits).

## Column title key (highlights)
- spp: species code; fix: fixation status (nitrogen-fixing or not).
- Plotting and sampling: plot, p5, tag, leaf (leaf identifier), area (leaf area).
- Growth and herbivory: stem_length, Incidence_of_herbivory, Proportion_of_herbivory, Proportion_HR, Proportion_HR_perc_diff, gr_rate.
- Traits data: N_shad, C_shad, P_shad, Ca_shad, K_shad, Shade_cellulose, Shade_hemicellulose, Shade_lignin, Shade_silicon, mCSCS, nnCSCS.

## References
- Comita, L. S., Muller-Landau, H. C., Aguilar, S. & Hubbell, S. P. Asymmetric density dependence shapes species abundances in a tropical tree community. Science. 329, 330-332 (2010).
- R Core Development Team. R: A Language and Environment for Statistical Computing.
- Sprent, J. I. Legume nodulation: a global perspective. John Wiley & Sons (2009).
- Westbrook, J. W. et al. What makes a leaf tough? Am Nat (2011).