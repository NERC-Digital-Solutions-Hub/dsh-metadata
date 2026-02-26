# Metadata for: Herbivory rates, species traits and leaf traits across symbiotic nitrogen-fixing and non-fixing species from a Panamanian tropical forest, 2007-2019

- Dataset focuses on herbivory and potential controls on herbivory for nitrogen-fixing and non-fixing trees in a mature Panamanian tropical forest.
- Contains herbivory measurements on 1,626 leaves from 350 seedlings across 43 species (23 nitrogen-fixers, 20 non-fixers).
- Includes leaf chemical and physical traits hypothesized to influence herbivory, plus seedling-level traits (stem length, growth rate).
- Data collected primarily in 2017-2018 with additional data spanning 2007-2019.
- Collected by Will Barker, S. Joseph Wright, Liza Comita, Brian Sedio, and colleagues.

## Experimental design and sampling regime

- Location: Barro Colorado Island (BCI), Panama, within the 50-ha plot; 23 fixer species and 20 non-fixer species sampled.
- Timeframe: Wet seasons 2017 and 2018; additional data from 2007-2019.
- Coverage: Nearly all fixer species present at the site (23 of 26) and a range of non-fixer species across plot abundances.
- Seedling census: Seedlings included were part of a long-term woody seedling census (≥20 cm stem height, <1 cm stem diameter at 1.3 m) from 2001-2018.

## Measures of herbivory

- Tissues measured: Mature and young leaves separately.
- Methods:
  - Mature leaves: Up to six leaves per seedling scanned (mean ~4.9) in 2017 using a handheld scanner (1050 DPI); leaf area lost to herbivory quantified with ImageJ; undamaged area estimated from damaged edges to compute proportion of leaf area lost.
  - Young leaves: 226 leaves tagged and scanned again in Nov 2017 to capture higher herbivory on young tissue and turnover.
- Metrics:
  - Incidence of herbivory: binary (any herbivory vs none) per leaf.
  - Proportion of leaf area lost to herbivory: continuous (0-1).
- Species-level predictions:
  - Models predict probability of herbivory (incidence) and mean leaf area lost to herbivory (proportion) across fixer vs non-fixer species.
  - Fixed effects: species identity, seedling size measures (standardized leaf area, stem length); random effect: 20 m plot to account for spatial autocorrelation.
  - Modeling approaches: binary logistic regression for incidence; beta regression for proportion; predictions via bootpredictlme4 and glmmTMB packages in R.

## Growth rate and species attributes

- Growth rate: Relative growth rate calculated from stem length changes between 2017 and 2018 (natural log of length difference over the interval).
- Leaf traits and species attributes:
  - Nutrients: leaf nitrogen, carbon, phosphorus, potassium, calcium concentrations.
  - Physical defenses: cellulose, hemicellulose, lignin, silicon concentrations.
  - Toughness metrics: lamina toughness, vein toughness, lamina density, work to shear, leaf mass per area (LMA).
  - Chemical similarity: molecular network-based metrics (nnCSCS and mCSCS) describing leaf secondary metabolite similarity between focal species and others in the plot.
- Trait data collection:
  - Nutrient and defense traits collected from leaves at crown tops across light environments (shade leaves used for congruence with seedling data); samples dried and analyzed with established methods.

## Nature and units of recorded values

- Herbivory:
  - Incidence: 0 or 1.
  - Proportion of leaf area lost: 0-1.
  - Predicted species averages follow the same structure (incidence or proportion).
  - Growth rate: cm2 per day? (described as relative growth rate based on stem length difference between years).
- Leaf traits:
  - Nutrients: mg per g leaf tissue (nitrogen and carbon reported as 100 * g/g).
  - Structural traits: g cellulose/g leaf tissue, g hemicellulose/g leaf tissue, g lignin/g leaf tissue, g silicon/g leaf tissue.
  - LMA: g cm^-2; lamina density in g cm^-3; toughness metrics in corresponding units; work to shear in J cm^-1 or J cm^-2 depending on metric.
- Chemical similarity:
  - nnCSCS and mCSCS are dimensionless similarity metrics derived from LC-MS data.

## Quality control and data processing

- Automated leaf herbivory measurement in ImageJ with manual verification against leaf images.
- Young-leaf herbivory rate calculations use two methods to account for leaf loss and growth:
  - Rate based on difference in leaf area divided by initial total leaf area.
  - Rate based on percentage leaf area missing, accommodating leaf growth; both methods converge for non-changing leaves.
- Data structure integrity ensured by careful cross-checks between time points and trait measurements.

## Data structure and files

Five CSV files comprising the dataset:

- Leaf_herbivory_BCI_2017.csv
  - Leaf-scale herbivory: spp, plot, p5, tag, leaf, fix, area, stem_length, incidence_of_herbivory, proportion_of_herbivory.
- seedling_herbivory_BCI_2017.csv
  - Seedling-scale herbivory: spp, plot, p5, tag, fix, area, stem_length, incidence_of_herbivory, proportion_of_herbivory, gr_rate.
- herbivory_rate_BCI_2017.csv
  - Herbivory rate on young leaves: spp, fix, plot, p5, tag, area, stem_length, incidence_of_herbivory, proportion_HR, proportion_of_herbivory_perc_diff.
- simulated_species_herbivory.csv
  - Predicted species-level herbivory: spp, fix, pred_prob, pred_prob_se, pred_prop, pred_prop_se.
- spp_leaf_traits.csv
  - Species-level leaf traits: spp, fix, n_shad, c_shad, p_shad, Ca_shad, k_shad, mCSCS, nnCSCS, Shade_cellulose, Shade_hemicellulose, Shade_lignin, Shade_silicon.

Column descriptors (example highlights):
- spp: species code; fix: fixation status per Sprent (2009); plot/p5/tag: hierarchical spatial identifiers; area: leaf area; stem_length: seedling stem length; incidence_of_herbivory / proportion_of_herbivory: herbivory metrics.
- Proportions and rates described with precise units as noted above.
- Trait columns indicate shade-leaf measurements and chemical similarity metrics (mCSCS, nnCSCS).

## References

- Comita et al., 2010; R Core Development Team (2018); Sprent (2009); Westbrook et al., 2011.