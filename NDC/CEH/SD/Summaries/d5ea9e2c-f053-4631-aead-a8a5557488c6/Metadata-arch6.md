# Malaysian heath forest tree DBH growth and change in leaf chemistry after fertilization.

- Purpose: Examine how soil pH and soil nitrogen (N) affect heath forest tree growth and leaf element concentrations after N and lime (CaCO3) fertilization in a Sabah, Malaysia heath forest. Data include tree diameter growth (DBH) over three years (2016–2018) and changes in leaf chemistry for the ten most abundant species during the fertilization experiment.

- Experimental design:
  - 16 plots (15 m x 15 m) in Kabili-Sepilok Forest Reserve, Sabah.
  - Factorial four treatments with four replicates each: Control, N addition, lime (CaCO3) addition, and N + lime.
  - Lime application rates adjusted each time to avoid excessive pH rises; first lime dose 75 kg plot⁻¹, then 50 kg plot⁻¹, then 25 kg plot⁻¹, with no lime in Jan 2018 and a 25 kg plot⁻¹ lime dose in Jul 2018.
  - N added as urea at 1.215 kg per plot per application (≈50 kg N ha⁻¹ yr⁻¹) because N is rapidly lost.
  - Ten most common species identified across plots (representing ~57% of stems ≥1 cm DBH and ~49% of basal area).

- Data collection and sampling regime:
  - DBH measurements taken three times: 2016, 2017, 2018 (June 2016; August 2017; August 2018).
  - Leaves collected for the ten focal species before fertilization (April 2016) and again before fertilizer applications in Feb 2017, Jul 2017, and Jun 2018 (except Jan 2018).
  - For each plot, ~10 fresh leaves per focal species from a single individual, collected ~7 m high; leaves oven-dried at 50°C and ground per collection.
  - Leaves analyzed for elements: Al, Ca, Cu, Fe, K, Mg, Mn, Na, Ni, P, S, Zn; C and N measured separately. Analyses performed with ICP-OES and CN elemental analyzer, with blanks and reference materials included.

- Data structure and files:
  - Heath forest DBH growth file (CSV)
    - Plot: plot identifier (a–p)
    - Treatment: Control, N, CaCO3, N+CaCO3
    - Tree_Field_Number: unique tag number; decimals (e.g., 818.2) indicate new or nearby recruits; some trees added mid-study
    - Family, Genus, species: taxonomic names (may be empty if not identified for recruits)
    - DBH_2016, DBH_2017, DBH_2018: DBH (cm) at 1.3 m
    - Comments: status notes (e.g., dead, not found, broken, regrown)
  - Leaf chemistry file (CSV)
    - Plot, Treatment
    - Month, Year: collection timing
    - Tree_Field_Number: tag as in DBH file; one dummy sample 636.665 created when a field tag was lost
    - Family, Genus, species: taxonomic names
    - 16 element concentrations per sample: N, C, Mg, P, Al, Ca, Cu, Fe, K, Mn, Na, Ni, S, Zn (with respective units)
    - CN (ratio) and NP (ratio: nitrogen to phosphorus)
  - Note: No GPS coordinates or plot-level geolocation; tree positions not mapped.

- Key data details and caveats:
  - Some DBH measurements may be taken from different stem locations or be marked as broken/regrown; such measurements should be treated cautiously in growth calculations.
  - Leaf data include multiple collection times; one artificial sample used due to lost tag; ensure correct linkage by Tree_Field_Number and plot.
  - Leaves were collected from the ten most common species, representing a subset of plots; not all plots may contain every focal species.
  - Coordinates are not provided; the dataset relies on plot and tag identifiers for location.

- Data use and potential products:
  - Enable self-serve analyses of how N and lime fertilization influence DBH growth across years, treatments, and focal species.
  - Track leaf element concentration changes over time by treatment and species to explore soil N and pH effects on foliar chemistry.
  - Combine with soil chemistry context (pH, NH4+, NO3−) to model relationships between soil amendments and tree/leaf responses.
  - Potential dashboards or pivot-table style summaries by plot, treatment, species, and year; note limitations due to missing geospatial coordinates.

- References and acknowledgments:
  - Data originate from work by Sellan et al. (2019, 2020) and related PhD research.
  - Funded by Manchester Metropolitan University's Environmental Science Research Centre; field and laboratory assistance acknowledged from Sabah institutions and MMU staff.