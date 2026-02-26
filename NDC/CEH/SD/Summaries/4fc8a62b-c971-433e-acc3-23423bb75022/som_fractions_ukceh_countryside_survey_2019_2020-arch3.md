# Soil organic matter fractions

- Purpose and relevance for monitoring frameworks
  - Demonstrates a national-scale monitoring approach to assess soil health and inform policy decisions by tracking soil organic matter (SOM) dynamics through distinct SOM pools.
  - Aligns with the aim of identifying environmental health measures that reveal changes in soil condition and function over time, supporting evidence-based decision making.

- Monitoring framework and design
  - Uses density fractionation to separate SOM into discrete pools: dissolved organic carbon (DOC), free/light particulate (LF), occluded particulate (OF), and mineral-associated organic matter (MAOM).
  - In this study, DOC and OF were discarded from analyses; LF and MAOM were analyzed for carbon and nitrogen, with OF derived by mass balance.
  - Part of the UK Countryside Survey 2019–2020, implemented as a rolling national programme (2019–2023) supported by UK-SCAPE to monitor changes in soil status and dynamics.
  - Rolling survey design: 500 one-km squares across Great Britain, sampled over five years; 100 squares visited per year; squares stratified by Land Classification; urban/seaward exclusions applied.

- Sampling, measurements, and analysis
  - Within each square, topsoil samples collected from up to 5 random vegetation X-Plots locations; 15 cm cores used.
  - SOM density fractionation performed on archived soils using sodium polytungstate (density 1.8 g cm-3) to separate LF and MAOM; OF obtained by mass balance.
  - Additional soil properties measured: Loss-on-Ignition (LOI), hygroscopic water content, and CaCO3 by thermogravimetric analysis (TGA 25–1000°C).
  - Total carbon and nitrogen measured on LF, MAOM, and archived soils using CNS elemental analysis; SOC calculated as total carbon minus calcite-C content.
  - Fractions corrected for hygroscopic water; LF-C, MAOM-C, and other fractions expressed per gram of oven-dry soil; OF and POM fractions derived from calculations.
  - Quality control: use of internal standards, 10% replicated samples; full method described in Reinsch et al. 2024.

- Data structure and outputs
  - Dataset comprises 13 columns and 101 rows per described batch; key metrics include:
    - LF_C_gperg, MAOM_C_gperg, OF_C_gperg, POM_C_gperg
    - LF_N_gperg, MAOM_N_gperg, OF_N_gperg, POM_N_gperg
    - SOC_gperg, TN_gperg, SOM_gperg
    - Year, SQ_ID (square identifier)
  - Data are structured to enable cross-site and temporal comparisons, with NA entries where measurements were not performed.

- Context, impact, and governance
  - Countryside Survey provides a long-running, scientifically rigorous audit of the UK countryside, enabling detection of subtle changes in soil condition and function over time.
  - The rolling design enhances temporal and spatial coverage, buffering against year-to-year climate variability while maintaining cost-effectiveness.
  - The program aims to deliver data and maps of soil stock and change at national scales, informing land management, agricultural policy, and climate-related soil dynamics.
  - Data handling emphasizes openness and standardization, with the UK-SCAPE platform underpinning data provision, sharing, and governance to support transparent, comparable metrics across years.

- Funding and references
  - Funded by the Natural Environment Research Council as part of UK-SCAPE National Capability (award NE/R016429/1) and supported by the AI4SoilHealth project.
  - Builds on and cites foundational work on SOM fractions, density fractionation, and the Countryside Survey lineage.