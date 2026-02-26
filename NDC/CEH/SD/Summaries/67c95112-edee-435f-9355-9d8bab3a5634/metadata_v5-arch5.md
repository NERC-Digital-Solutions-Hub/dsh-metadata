# Metadata for:
Herbivory rates, species traits and leaf traits across symbiotic nitrogen-fixing and non-fixing species from a Panamanian tropical forest, 2007-2019

## Overview and scope
- Dataset of herbivory measurements and potential controls on herbivory for nitrogen-fixing and non-fixing trees in a mature Panamanian tropical forest.
- Includes herbivory data on 1,626 leaves from 350 seedlings across 43 species (23 nitrogen-fixers, 20 non-fixers).
- Data granularity: leaf-level and seedling-level herbivory, plus leaf chemical and physical traits and seedling traits (e.g., stem length, growth rate).
- Timeframe: primary collection in 2017–2018, with additional data from 2007–2019.
- Collected by a multi-institution team (Will Barker, S. Joseph Wright, Liza Comita, Oliver L. Phillips, Brian E. Sedio, Sarah A. Batterman) within Barro Colorado Island (BCI) 50-ha plot, Panama.
- Purpose aligned with examining whether nitrogen fixers have different herbivory and identifying trait-based drivers of herbivory; supports data discovery and reuse.

## Context, governance and accessibility
- Data come with a structured metadata and a defined data dictionary to support reuse across studies and systems.
- Five CSV files comprising the dataset, with explicit column definitions, units, and data provenance.
- Includes model-based predictions of species-average herbivory and species-level trait data to enable cross-species comparisons.
- Methods documented to aid interoperability, replication, and potential integration with other datasets from the same plot or region.
- Documentation includes references to foundational studies and software used for analysis (R 3.5.1).

## Experimental design and sampling
- Sampling frame: 23 nitrogen-fixing fixer species and 20 non-fixer species in the 50-ha BCI plot.
- Location: Barro Colorado Island, Panama (approx. 9.125° N, -79.8553° W).
- Temporal scope: wet seasons of 2017 and 2018; nearly all fixer species present at the site sampled (23 of 26); non-fixers selected to span abundance ranges.
- Seedlings used: part of a long-term census of freestanding woody seedlings (≥20 cm stem height and <1 cm diameter at 1.3 m) collected 2001–2018.
- Environmental context: mean annual rainfall ~2600 mm; mean temperature ~27°C; light environments considered for leaf trait sampling.

## Measurements and data capture
- Herbivory measures:
  - Mature leaves: non-destructive scans (up to six leaves per individual) to quantify leaf area loss using ImageJ; edge reconstruction used for undamaged area estimation.
  - Young leaves: 226 leaves scanned (one per seedling) to capture higher herbivory; two measurement timings (2017 and 2017) to assess turnover.
  - Two herbivory metrics: incidence (binary: any herbivory vs none) and proportion of leaf area lost (continuous, 0–1).
- Growth data:
  - Relative growth rate calculated from stem length change between 2017 and 2018.
- Species attributes and leaf traits:
  - Leaf nutrient concentrations (N, C, P, K, Ca) and physical traits (cellulose, hemicellulose, lignin, silicon).
  - Leaf toughness metrics and leaf mass per area (LMA).
  - Chemical similarity metrics (nnCSCS and mCSCS) based on leaf secondary metabolites analyzed via UHPLC-ESI-MS/MS; networks built from molecular fragment similarity with cosine similarity > 0.6.
  - Shade-leaf trait measurements used to align with seedling data under canopy conditions.
- Data processing and models:
  - Predictive models for species-average herbivory using incidence (logistic regression) and proportion (beta regression); fixed effects include species and seedling size; plot included as a random effect to account for spatial autocorrelation.
  - Software: analyses performed in R (v3.5.1).

## Data structure, content and units
- Five CSV files:
  - Leaf_herbivory_BCI_2017.csv: leaf-scale herbivory; fields include spp, plot, p5, tag, leaf, fix, area, stem_length, incidence_of_herbivory, proportion_of_herbivory.
  - seedling_herbivory_BCI_2017.csv: seedling-scale herbivory; fields include spp, plot, p5, tag, fix, area, stem_length, incidence_of_herbivory, proportion_of_herbivory, gr_rate.
  - herbivory_rate_BCI_2017.csv: herbivory rate on young leaves; fields include spp, fix, plot, p5, tag, area, stem_length, incidence_of_herbivory, proportion_HR, proportion_of_herbivory_perc_diff.
  - simulated_species_herbivory.csv: predicted species-average herbivory; fields include spp, fix, pred_prob, pred_prob_se, pred_prop, pred_prop_se.
  - spp_leaf_traits.csv: species-level leaf traits; fields include spp, fix, n_shad, c_shad, p_shad, Ca_shad, k_shad, mCSCS, nnCSCS, Shade_cellulose, Shade_hemicellulose, Shade_lignin, Shade_silicon.
- Column definitions and units:
  - Incidence_of_herbivory: binary (0/1); Proportion_of_herbivory and Proportion_HR: 0–1 proportions.
  - Growth rate (Gr.rate): relative growth rate computed as natural log difference in stem length between 2018 and 2017.
  - Nutrient contents and leaf traits expressed as per unit tissue (e.g., mg g-1, g g-1, or g per g, with shade-leaf values noted).
  - Leaf area and stem length held in cm2 and cm, respectively.
- Metadata and data dictionary:
  - Column title key provides exact field meanings (e.g., spp, fix, p5, leaf, gr_rate, etc.) and the measurement semantics.

## Quality control and provenance
- Herbivory measurements in ImageJ automated, then manually verified against leaf images for accuracy.
- Two methods used to estimate herbivory on young leaves to account leaf growth and tissue loss, ensuring comprehensive rate estimation.
- Documentation and data dictionary included to support reproducibility and validation.

## Provenance, references and related materials
- Primary authors and affiliations listed.
- References to foundational work and methods, including:
  - Comita et al. (2010) on density dependence in tropical tree communities.
  - Sprent (2009) on legume nodulation.
  - Westbrook et al. (2011) on leaf toughness traits.
- Related long-term census data and modeling approaches noted to support context and reuse.

## Usage considerations for data stewardship
- Ensure consistent interpretation of incidence vs. proportion metrics across analyses.
- Maintain the five CSV file structure and the accompanying data dictionary for interoperability.
- Preserve the detailed trait measurement context (shade leaves, sampling from crown, and methodological notes) to support comparability with other datasets.
- Be mindful of the spatial random effect (20 m plot) when integrating with other plots for meta-analyses.
- Track updates or extensions (e.g., additional years or datasets) to maintain lineage and versioning in data catalogs.