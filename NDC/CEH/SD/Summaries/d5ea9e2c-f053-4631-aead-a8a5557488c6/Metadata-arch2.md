# Malaysian heath forest tree DBH growth and change in leaf chemistry after fertilization.

## Overview
- Investigates how soil pH and soil nitrogen affect tree growth and leaf element concentrations in a Bornean heath forest (Kabili-Sepilok, Sabah, Malaysia).
- Uses a controlled factorial fertilization experiment (N and lime) to assess growth (DBH) and foliar chemistry responses over time.

## Experimental design
- Location: Kabili-Sepilok Forest Reserve, Sabah, Malaysia; equatorial climate, ~26°C average, ~3000 mm annual rainfall.
- Plots: 16 plots of 15 m x 15 m.
- Treatments: four fertilization regimes in a factorial design – Control, N addition (urea), CaCO3 (lime), and N + CaCO3 – with four replicates per treatment.
- Lime management: initial high lime application, later reduced rates to maintain soil pH around 5 and avoid micronutrient deficiencies.
- Nitrogen: 1.215 kg urea per plot per application (50 kg N ha-1 yr-1).
- Timeline: fertilization and measurements conducted from 2016 to 2018.

## Focal species and sampling
- Ten most common tree species representing 57% of stems ≥1 cm DBH and 49% of basal area.
- Focal species: Actinodaphne borneensis, Chionanthus pluriflorus, Cotylelobium melanoxylon, Diospyros fusiformis, Dracaena elliptica, Gaertnera junghuhniana, Pimelodendron griffithianum, Syzygium sp., Ternstroemia aneura, Tristaniopsis obovata.
- Leaves sampled: ~10 fresh leaves per focal species per plot, from the same individual trees across sampling events.
- Sampling schedule: before fertilization (April 2016) and before each application (February 2017, July 2017) and in June 2018 (excluding January 2018).
- Leaf processing: oven-dried at 50°C, ground per individual tree, analyzed for elemental concentrations.

## Data collection and analytical methods
- Soil and leaf analyses:
  - Leaf elements: Al, Ca, Cu, Fe, K, Mg, Mn, Na, Ni, P, S, Zn (measured by ICP-OES after acid digestion).
  - Carbon and Nitrogen: measured by CN elemental analyzer.
- Quality assurance: blanks and certified reference materials included; standardised laboratory procedures.
- Data handling notes: same tree kept across sampling when possible; if a tree died or became unavailable, replacements sampled from same species in the plot; dummy values used when samples could not be matched (e.g., 636.665 for a lost leaf sample).

## Data structure and contents
- datasets are CSV files with headers.
- DBH growth file:
  - Plot: 16 plots labeled a–p.
  - Treatment: Control, N, CaCO3, N+CaCO3.
  - Tree_Field_Number: unique tag-based identifier (decimal suffixes for recruits or added trees).
  - Taxonomy: Family, Genus, species (some entries empty for newly recruited stems).
  - DBH_2016, DBH_2017, DBH_2018: diameter at breast height (cm) at three timepoints.
  - Comments: status notes (dead, not found, broken, regrown, etc.).
- Leaf chemistry file:
  - Plot and Treatment as above.
  - Month and Year: collection timing.
  - Tree_Field_Number and Taxonomy fields as above.
  - 16 element concentration columns: N (%), C (%), Mg (mg g^-1), P (mg g^-1), Al (mg g^-1), Ca (mg g^-1), Cu (mg g^-1), Fe (mg g^-1), K (mg g^-1), Mn (mg g^-1), Na (mg g^-1), Ni (mg g^-1), S (mg g^-1), Zn (mg g^-1).
  - CN and NP ratios provided.
  - Note: one dummy tree field number (636.665) used for a lost Pimelodendron griffithianum leaf sample.

## Study scope and outputs
- Focus: understanding how soil chemistry manipulations influence tree growth and foliar chemistry in heath forests.
- Outputs aligned with environmental monitoring aims: standardized datasets suitable for long-term comparison, verification, and cross-study integration; data are prepared for storage and portal upload as part of monitoring responsibilities.
- Temporal coverage spans 2016–2018, with multiple sampling events to capture immediate and short-term responses to fertilization.

## Context and references
- Background work on soil characteristics, forest structure, and ecological responses to lime and nitrogen addition in Bornean heath forests informs experimental design and interpretation.

## Acknowledgements
- Funded by Manchester Metropolitan University’s Environmental Science Research Centre; field and lab support acknowledged.