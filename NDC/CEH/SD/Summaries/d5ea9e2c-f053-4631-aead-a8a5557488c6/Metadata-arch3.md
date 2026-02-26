# Malaysian heath forest tree DBH growth and change in leaf chemistry after fertilization.

- Objective and scope
  - Investigates how soil pH and soil nitrogen availability influence tree growth and foliar chemistry in a Bornean heath forest.
  - Uses a fertilization experiment to assess responses in DBH growth and leaf element concentrations across the ten most abundant tree species.

- Experimental design
  - Location: Kabili-Sepilok Forest Reserve, Sabah, Malaysia; 16 plots (15 m x 15 m).
  - Treatments: four factorial fertilization treatments with four replicates each — Control, Nitrogen (N) addition, Lime (CaCO3) addition, and N + CaCO3.
  - Lime application: staged to avoid overshooting target soil pH (around pH 5); initially 75 kg/plot, then reduced in subsequent applications (50, then 25 kg/plot) with adjustments reflecting soil pH.
  - Nitrogen application: 1.215 kg urea per plot per application (≈50 kg N ha^-1 yr^-1); applied with each lime event.
  - Focal taxa: ten most common species representing 57% of stems ≥1 cm DBH.
  - Sampling: three DBH censuses (2016, 2017, 2018) and leaf sampling at four time points (before fertilization in 2016; Feb 2017; Jul 2017; Jul 2018; excluding Jan 2018).

- Measurements and data collected
  - DBH growth:
    - DBH_2016, DBH_2017, DBH_2018 for individual trees; notes on mortality, missing individuals, or measurement specifics (e.g., broken/regrown, new measurement spots).
  - Leaf chemistry:
    - Leaves collected from ~10 individuals per focal species per plot.
    - Analyzed elements: Al, Ca, Cu, Fe, K, Mg, Mn, Na, Ni, P, S, Zn; plus C and N.
    - Units: various (e.g., mg g^-1 for most minerals; % for C and N); CN and NP ratios included.
  - Sampling details:
    - Leaves collected at ~7 m height; leaves oven-dried at 50 °C; ground per individual for analysis.
    - Instrumentation: ICP-OES (iCAP 6300) for minerals; CN elemental analyzer (Leco TruSpec) for C and N.
    - Quality controls: blanks and certified reference materials in each batch.

- Data structure and metadata
  - DBH growth file:
    - Plot: lettered plots a–p.
    - Treatment: Control, N, CaCO3, N+CaCO3.
    - Tree_Field_Number: unique tree identifier; notes on re-tagging or追加 trees with decimal suffixes (e.g., 818.2).
    - Taxonomy: Family, Genus, Species (may be empty for some recruits).
    - DBH_2016, DBH_2017, DBH_2018: DBH measurements; Comments column documents mortality, not found, broken, regrown, or liana notation.
  - Leaf chemistry file:
    - Plot, Treatment, Month, Year.
    - Tree_Field_Number: same tagging conventions as DBH file; one missing tag case handled with a dummy value (636.665).
    - Taxonomy: Family, Genus, Species.
    - Elemental concentrations: 16 minerals/elements plus CN and NP ratios (units varied per element).
  - Data accessibility: CSV format with first-row headers; comprehensive documentation of field identifiers and measurement conditions.

- Data quality, governance and challenges
  - Explicit attention to metadata and provenance (plot, treatment, species, tree identifiers, measurement dates).
  - Potential data issues highlighted: missing trees, measurement location changes on stems, mortality, broken or regrown stems, and occasional missing leaf-tree linkage for one sample.
  - Transparency in methods supports reproducibility and future integration into broader monitoring datasets.
  - Grain of data supports longitudinal monitoring of growth and foliar nutrient status in response to soil amendments.

- Relevance for monitoring frameworks
  - Provides concrete environmental health measures for policy scrutiny and decision-making:
    - Growth response: DBH changes across three years under nutrient and pH manipulations.
    - Nutrient status: foliar concentrations of key elements across major species and plots.
  - Demonstrates data governance in a field experiment context:
    - Clear plot-treatment mappings, repeat measurements, and standardized sample processing.
    - Detailed data structure enabling traceability and re-use in synthesis and dashboards.
  - Highlights practical challenges common to monitoring programs:
    - Data gaps due to mortality or missing measurements.
    - Need for careful handling of atypical measurement records (e.g., broken stems, regrowth, liana entries).
  - Supports future decision-making regarding soil amendment practices in nutrient-poor heath forests and their potential to influence tree growth and ecosystem chemistry.