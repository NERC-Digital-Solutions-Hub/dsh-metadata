# Metadata for:
Herbivory rates, species traits and leaf traits across symbiotic nitrogen-fixing and non-fixing species from a Panamanian tropical forest, 2007-2019

## Overview
- Dataset of herbivory measurements and the potential controls on herbivory for nitrogen-fixing and non-fixing trees in a mature tropical forest in Panama.
- Includes herbivory data at leaf and seedling levels for 1,626 leaves from 350 seedlings across 43 species (23 nitrogen-fixers, 20 non-fixers).
- Associated species-level leaf traits and seedling traits (e.g., stem length, growth rate) to explore drivers of herbivory.
- Data collected mainly in 2017–2018 (BCI 50-hectare plot); additional data spanning 2007–2019.
- Aimed at understanding whether fixers have higher herbivory and what traits govern herbivory; data are suitable for GIS-based visualization and spatial analyses within the 50-ha plot.

## Spatial and sampling context
- Location: Barro Colorado Island (BCI), Panama; within the 50-ha forest dynamics plot.
- Sampling window: wet seasons 2017 and 2018; nearly all fixer species present at the site (23 of 26) and a range of non-fixer species by abundance.
- Plot design: 20 m × 20 m fixed plots subdivided into 16 1 m × 1 m subplots (p5). Seedlings included if ≥20 cm stem height and <1 cm diameter at 1.3 m.
- Environment: annual rainfall ~2600 mm; mean temperature ~27°C.
- Experimental design accounts for spatial structure with plot-level random effects in models.

## Data files and key content
- Leaf_herbivory_BCI_2017.csv
  - Leaf-scale herbivory data
  - Columns: spp, plot, p5, tag, leaf, fix, area, stem_length, incidence_of_herbivory, proportion_of_herbivory
- seedling_herbivory_BCI_2017.csv
  - Seedling-scale herbivory data
  - Columns: spp, plot, p5, tag, fix, area, stem_length, incidence_of_herbivory, proportion_of_herbivory, gr_rate
- herbivory_rate_BCI_2017.csv
  - Herbivory rate on young leaves
  - Columns: spp, fix, plot, p5, tag, area, stem_length, incidence_of_herbivory, proportion_HR, proportion_of_herbivory_perc_diff
- simulated_species_herbivory.csv
  - Predicted species-scale herbivory
  - Columns: spp, fix, pred_prob, pred_prob_se, pred_prop, pred_prop_se
- spp_leaf_traits.csv
  - Species-level leaf traits and chemical similarity metrics
  - Columns: spp, fix, n_shad, c_shad, p_shad, Ca_shad, k_shad, mCSCS, nnCSCS, Shade_cellulose, Shade_hemicellulose, Shade_lignin, Shade_silicon

Column title key (sample of what each field represents)
- spp: six-letter species code; fix: nitrogen-fixation status per Sprent (2009)
- plot: 20 m × 20 m plot within the 50-ha site
- p5: 1 m × 1 m subplots within each 20 m plot
- tag: unique seedling/leaf identifier within each plot
- leaf: leaf identifier within a seedling
- area: leaf area (cm²)
- stem_length: seedling stem length at census
- incidence_of_herbivory: 0/1; whether herbivory is observed
- proportion_of_herbivory: proportion of leaf area lost (0–1)
- Proportion_HR: herbivory rate for young leaves (area difference over time divided by initial leaf area)
- Proportion_HR_perc_diff: alternative herbivory rate metric (percentage difference)
- gr_rate: relative growth rate (ln(stem length 2018) – ln(stem length 2017)) divided by days between censuses
- Trait fields (Shade_*, n_shad, c_shad, etc.) refer to shade-leaf measurements; mCSCS/nnCSCS quantify chemical similarity between species

## Methods and data quality
- Leaf herbivory measurement: non-destructive leaf scans (1050 DPI) with ImageJ; edge-corrected leaf area to estimate undamaged area; incidence and proportion metrics computed for mature and young leaves.
- Young-leaf herbivory: two measurement approaches to account for leaf growth and complete leaflet loss; ensures comprehensive herbivory rate estimates.
- Trait data collection: leaf chemistry (N, C, P, K, Ca, etc.) and physical defenses (cellulose, hemicellulose, lignin, silicon); leaf toughness metrics; shading environment considerations; samples collected from the tallest and shortest individuals across light environments; shade-leaf data used to align with seedling under-canopy conditions.
- Chemical similarity: structural/compositional similarity of leaf metabolites via LC-MS-based networks; nnCSCS and mCSCS metrics quantify cross-species chemical similarity.
- Analyses (for context): logistic regression for incidence of herbivory; beta regression for mean proportion of leaf area lost; mixed-effects models with species and plot as fixed/random effects; predictions derived via bootpredictlme4 and glmmTMB packages in R.
- Quality control: automated ImageJ measurements with manual verification; two methods for young-leaf herbivory to reduce bias; data curated to ensure consistency across methods.

## Data structure and formats
- Five CSV data files with explicit column definitions; designed for joinable integration with species traits and plot-level GIS layers.
- Structure supports both fine-grained (leaf- and seedling-level) and aggregate (species-level) analyses.
- Species-level trait file enables linking herbivory outcomes to leaf chemistry and structural traits for spatially enabled visualizations.

## Applications for GIS and map-based data products
- Create spatial maps of herbivory incidence and severity by plot, p5, or seedling location within the 50-ha BCI plot.
- Visualize fixer vs. non-fixer species patterns across space, potentially overlaying canopy/environmental layers.
- Link herbivory data to leaf trait layers to produce thematic maps of trait-driven herbivory risk across the forest.
- Develop species-level herbivory heatmaps or choropleth layers by species, using predicted herbivory (pred_prob, pred_prop) to illustrate expected spatial patterns.
- Combine with growth-rate data to map growth-derivative interfaces with herbivory risk.
- Use the geographic structure (20 m plots, 1 m subplots) to create scalable GIS layers from fine-scale to plot-scale summaries, accounting for spatial autocorrelation.

## References
- Comita, L. S., Muller-Landau, H. C., Aguilar, S. & Hubbell, S. P. Asymmetric density dependence shapes species abundances in a tropical tree community. Science. 329, 330-332 (2010).
- R Core Team. R: A language and environment for statistical computing. (2018).
- Sprent, J. I. Legume nodulation: a global perspective. (Wiley, 2009).
- Westbrook, J. W. et al. What makes a leaf tough? Am Nat. 177, 800-811 (2011).