# Malaysian heath forest tree DBH growth and change in leaf chemistry after fertilization.

## Overview
- Heath forests are a rare, low-productivity tropical forest type on weathered, acidic soils with low nutrients.
- Study location: Kabili-Sepilok Forest Reserve, Sabah, Malaysia.
- Objectives: assess the importance of soil pH and soil nitrogen for heath forest tree growth; examine changes in leaf element concentrations after increasing soil pH and soil nitrogen.
- Data focus: tree DBH growth over three censuses (2016, 2017, 2018) and foliar chemistry (a suite of elements) across a nitrogen and lime fertilization experiment.

## Experimental design and sampling regime
- Setup: 16 plots, each 15 m x 15 m.
- Climate: equatorial, mean annual ~26°C, ~3000 mm/year rainfall.
- Baseline: all stems ≥1 cm DBH tagged and identified to species; initial homogeneous distribution checked (no significant differences in species composition, pH, NH4+, NO3−).
- Treatments: factorial design with four treatments and four replicate plots each:
  - Control (no fertilization)
  - N addition (urea)
  - CaCO3 (lime) addition
  - N + CaCO3
- Lime application details: adjusted to avoid overshooting pH beyond surrounding forest levels; three lime application events with decreasing rates (75 kg/plot → 50 kg/plot → 25 kg/plot); one year with no lime (January 2018), then 25 kg lime in July 2018.
- Nitrogen application: consistent across lime events (1.215 kg urea per plot per application; ~50 kg N ha−1 yr−1).
- Focal species: ten most common across plots (representing 57% of stems ≥1 cm DBH and 49% of basal area); species listed in the study.
- Leaf sampling: about ten fresh leaves per focal species per plot, collected per census interval.
  - Sampling times: April 2016 (pre-treatment), February 2017, July 2017, June 2018 (pre–July 2018 fertilization); January 2018 had no leaf sampling.
  - One individual per species per plot; if dead, samples taken from another tree of the same species in the same plot.
  - Leaves collected at ~7 m height; canopy not fully shaded.
  - Leaves dried at 50°C, ground per collection before chemical analysis.
- DBH measurements: recorded for 2016, 2017, and 2018 (June 2016, August 2017, August 2018); notes on mortality, missing trees, or measurement issues (e.g., broken stems, regrown sections).

## Measurements and laboratory methods
- DBH: measured with tapes/calipers; location details captured; notes on validity of measurements if stem position changes were made.
- Leaf chemistry analyses:
  - Elemental concentrations measured by ICP-OES after acid digestion (Al, Ca, Cu, Fe, K, Mg, Mn, Na, Ni, P, S, Zn).
  - Carbon and nitrogen concentrations measured with CN analyzer.
  - Quality controls: blanks and certified reference materials included in each batch.
  - Elements reported: N, C, Mg, P, Al, Ca, Cu, Fe, K, Mn, Na, Ni, S, Zn; plus CN and NP ratios.
- Data structure and identifiers:
  - Plot: A–P (16 plots).
  - Treatment: Control, N, CaCO3, N+CaCO3.
  - Tree_Field_Number: unique tag per tree; special rules for new recruits and close-by trees; some trees added mid-study and tagged with decimals (e.g., 818.2).
  - Taxonomy: Family, Genus, Species columns (may be empty for some late-identified recruits).
  - DBH columns: DBH_2016, DBH_2017, DBH_2018.
  - Comments: status notes (died, not found, broken, broken/regrown, liana, etc.); caveats for using measurements taken at alternate stem locations.
  - Leaf chemistry file includes: Plot, Treatment, Month, Year, Tree_Field_Number, taxonomy, then 16 element concentration columns plus CN and NP ratios.
- Data access notes:
  - Datasets are CSV files with headers in the first row; no quotation marks around headers.
  - No geographic coordinates included for stems in the dataset.

## Data structure and integrity notes
- Two primary datasets:
  - Heath forest DBH growth file: longitudinal DBH measurements by year, with treatment and plot-level context.
  - Leaf chemistry file: cross-sectional leaf element concentrations aligned to plot, treatment, species, and sampling time.
- Data challenges and peculiarities:
  - Some trees added after initial census; tag numbers reflect proximity to earlier trees (e.g., 818.2).
  - A missing tree field number for one Pimelodendron griffithianum leaf sample was replaced with a dummy value (636.665).
  - Some measurements may be taken from different stem positions (noted as “broken, regrown”); such entries should be used cautiously for growth calculations.
  - Coordinates are not provided; location is plot-based rather than tree-mapped.

## Data quality, governance, and usage notes
- Baseline checks: ANOVA confirmed similar starting conditions across plots prior to treatment allocation.
- Data applicability: designed for examining effects of soil pH and nitrogen on growth and foliar chemistry; suitable for cross-dataset analyses linking soil chemistry, growth rates, and leaf nutrient status.
- Metadata considerations: detailed notes on measurement protocols, tree tagging, and sampling schedule facilitate reproducibility and re-analysis.
- References and provenance:
  - Related publications and doctoral work provide deeper context on soil characteristics, species responses, and decomposition dynamics.
  - Acknowledgements credit funding and field/lab collaborators.

## References and acknowledgements
- Key references include works on soil characteristics influencing species composition, ecological responses to lime and nitrogen addition, and decomposition under altered soil chemistry.
- Funding: Manchester Metropolitan University Environmental Science Research Centre.
- Acknowledgements to Sabah Biodiversity Council and university laboratory staff for field and lab assistance.