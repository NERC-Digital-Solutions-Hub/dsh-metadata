# Metadata for: Herbivory rates, species traits and leaf traits across symbiotic nitrogen-fixing and non-fixing species from a Panamanian tropical forest, 2007-2019

## Overview
- Dataset on herbivory and its potential controls for nitrogen-fixing and non-fixing trees in a mature Panamanian tropical forest.
- Includes herbivory measurements on 1,626 leaves from 350 seedlings across 43 species (23 nitrogen-fixers, 20 non-fixers).
- Leaf- and seedling-level herbivory metrics, plus leaf chemical/physical traits and seedling traits (e.g., stem length, growth rate).
- Data collected mainly in 2017–2018, with additional data spanning 2007–2019.

## Study design and sampling
- Location: Barro Colorado Island (BCI), Panama, in the 50-hectare forest plot.
- Species: 23 nitrogen-fixer species and 20 non-fixer species; near-complete sampling of fixer species (23 of 26) and diverse non-fixer representatives.
- Timeframe: Wet seasons of 2017–2018; supplementary trait data from 2007–2008; long-term seedling census (2001–2018).
- plot structure: Seedlings sampled within 20m × 20m subplots; data linked to the 50-ha plot census.

## Measurements and variables
- Herbivory measurements:
  - Mature leaves: up to six leaves per individual scanned (mean ~4.9); 184 fixer and 166 non-fixer seedlings assessed in 2017.
  - Young leaves: 226 leaves scanned in November 2017 to capture higher herbivory and turnover.
  - Metrics: incidence of herbivory (binary) and proportion of leaf area lost (continuous); measured per leaf and per seedling.
- Growth and size metrics:
  - Seedling growth: relative growth rate calculated as the natural log difference of stem length between 2017 and 2018.
  - Seedling size indicators: standardized leaf area, stem length included as fixed effects in species-average herbivory models.
- Trait data (species level):
  - Leaf nutrients: nitrogen, carbon, phosphorus, potassium, calcium.
  - Physical and structural traits: cellulose, hemicellulose, lignin, silicon; leaf toughness metrics and leaf mass per area (LMA).
  - Shade-leaf data: measurements taken from shade leaves to align with seedling-under-canopy herbivory context.
- Chemical similarity:
  - nnCSCS: nearest-neighbour Chemical Structural and Compositional Similarity.
  - mCSCS: mean Chemical Structural and Compositional Similarity across species.
  - Derived from untargeted metabolomics (UHPLC-ESI-MS/MS) and cosine similarity of fragmentation patterns.

## Data structure and files
- Five CSV files:
  - Leaf_herbivory_BCI_2017.csv: leaf-scale herbivory incidence and proportion, with fields including spp, plot, p5, tag, leaf, fix, area, stem_length, incidence_of_herbivory, proportion_of_herbivory.
  - seedling_herbivory_BCI_2017.csv: seedling-scale herbivory metrics, including spp, plot, p5, tag, fix, area, stem_length, incidence_of_herbivory, proportion_of_herbivory, gr_rate.
  - herbivory_rate_BCI_2017.csv: herbivory rate on young leaves with fields including spp, fix, plot, p5, tag, area, stem_length, incidence_of_herbivory, proportion_HR, proportion_of_herbivory_perc_diff.
  - simulated_species_herbivory.csv: predicted species-level herbivory (pred_prob, pred_prob_se, pred_prop, pred_prop_se).
  - spp_leaf_traits.csv: species-level leaf traits, including n_shad, c_shad, p_shad, Ca_shad, k_shad, mCSCS, nnCSCS, Shade_cellulose, Shade_hemicellulose, Shade_lignin, Shade_silicon.
- Column details provided (e.g., p5, tag, area, gr_rate, etc.), with shade-specific measurements clearly labeled.

## Data quality and processing
- Automated herbivory measurements performed in ImageJ, followed by manual validation against leaf images.
- Two methods for young-leaf herbivory rates to account leaf loss and growth:
  - Method 1: difference in leaf area divided by estimated initial total leaf area.
  - Method 2: percentage-area missing difference for leaves that grew; both methods yield identical values when no change occurs.
- Analyses conducted in R (v3.5.1) with appropriate mixed-effects modeling (logistic for incidence; beta for proportion) and bootstrapped predictions.

## Analytical methods and outputs
- Models:
  - Incidence of herbivory: binary logistic regression with species identity and seedling size as fixed effects; 20m plot as random effect.
  - Proportion of leaf area lost: beta regression with similar fixed effects and random effects.
  - Predictions: use bootpredictlme4 and glmmTMB for species-level outputs.
- Outputs intended for interpretation in terms of fixer vs. non-fixer differences in herbivory and the influence of seedling traits on herbivory susceptibility.

## Scope and context for environmental monitoring
- Provides a standardised, well-documented dataset linking herbivory to species traits and metabolomic similarity, enabling temporal monitoring and cross-site comparisons.
- Emphasizes data provenance, quality checks, and reproducible analyses, aligning with ongoing environmental health and policy performance monitoring.

## References and provenance
- Data collected by Will Barker, S. Joseph Wright, Liza Comita, Oliver L. Phillips, Brian E. Sedio, and Sarah A. Batterman.
- Related methods and context drawn from key studies on tropical tree communities and leaf trait ecology (e.g., Comita et al. 2010; Sprent 2009; Westbrook et al. 2011).