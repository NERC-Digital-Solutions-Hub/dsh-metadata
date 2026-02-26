# Digestate_HF_and_NW_pH_NH4_NO3_v2.csv

- Overview
  - Dataset of 8 columns and 950 rows from the digestate wheat trial 2017 conducted at Henfaes Research Center (HF) and North Wyke Research Station (NW), associated with Rothamsted Research.
  - Measures soil pH, ammonium (NH4) and nitrate (NO3) content.

- Dataset scope and content
  - Site: HF or NW (North Wyke).
  - Date: date the soil sample was collected from the field.
  - Plot: experimental plot number.
  - Block: block identifier in a randomized block design (1–5).
  - Treatment: C (zero N control), D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), ADNI (acidified digestate with DMPP).
  - Soil_pH: pH of the soil sample.
  - Soil_NH4_mg_kg: NH4 content in mg N per kg of dry soil.
  - Soil_NO3_mg_kg: NO3 content in mg N per kg of dry soil.
  - NA = Not assessed (indicates missing data for specific entries).

- Experimental design context
  - Randomised block design with multiple plots per site.
  - Two sites with potentially different plot sizes and harvest area configurations:
    - HF: 1.2 m × 6.5 m (nitrogen addition rate plots) and 1.2 m × 14 m (for certain treatments).
    - NW: 2 m × 4.5 m (nitrogen addition rate plots) and 2 m × 9 m (for certain treatments).
  - Treatments cover a range of nitrogen inputs and chemical treatments to assess effects on soil chemistry.

- Data structure and documentation
  - Column headers and explanations provided, including units.
  - Clear encoding of site, date, plot, block, and treatment to support integrative analyses.
  - This file is a data structure supplement to broader supporting documentation (for CINAg experiments).

- Data quality and governance considerations for data leaders
  - Ensure consistent site coding (HF vs NW) and standardized date formats.
  - Validate units (NH4 and NO3 in mg N kg-1 dry soil; pH unitless).
  - Address NA values and document where data were not assessed.
  - Capture methodology details (sampling depth, timing, and analytical methods) in metadata to enable proper interpretation and cross-study comparability.
  - Maintain linkage to related documents (Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf) for full experimental context.

- Potential uses
  - Analyze how digestate treatments influence soil pH, NH4, and NO3 across two sites.
  - Compare treatment effects within and between HF and NW under a randomized block framework.
  - Integrate with broader data series to study nutrient dynamics in digestate-based agronomic systems.

- Caveats and gaps
  - Depth of soil sampling and exact measurement protocols not specified in this summary; refer to accompanying documentation for methods.
  - Some plots or dates may have NA values; treat accordingly in analyses.
  - Differences in plot sizes between HF and NW may affect cross-site comparisons and should be accounted for in modeling.