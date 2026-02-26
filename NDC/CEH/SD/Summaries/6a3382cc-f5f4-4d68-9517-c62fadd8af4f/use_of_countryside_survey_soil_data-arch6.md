# Sampling design

- Purpose and scope
  - Countryside Survey (CS) soils were sampled in 1978, 1998, 2007, and 2019, with a rolling survey starting in 2019 to measure ~100 squares per year for five years before repeating.
  - Power analyses (Emmett et al. 2008) informed the number of samples needed to detect significant change.
  - The rolling approach aims to enable ongoing monitoring and national estimates of stock and change.

- Sampling framework and location
  - Soils are sampled from CS X-plots, with 5 plots per CS square, randomly spaced.
  - X-plots within a square are not replicates due to differing land uses/types across plots.
  - Some X-plots are relocated over time due to destruction, access issues, or uncertainty in original locations.
  - Each sampling location has a unique repeat identifier (e.g., 2RPT1: square 2, repeat plot 1), indicating the same location across years; exact sampling positions are ~2–3 m apart within a permanently marked 2 m × 2 m plot.

- Sampling methods
  - Top 15 cm of soil is collected (8 cm for the invertebrate sample); in 1998, 2007, and rolling surveys (2018/2019–2023) cores are hammered in and pulled out.
  - In 1978, soil pits were used to collect from the top 15 cm.
  - Stones or shallow soils can prevent obtaining a full 15 cm core.
  - Core photographs and measurements of core dimensions were taken in 2007 for some cores (2 of 4 cores: black cores and N mineralization cores). The rolling CS survey adopts the core-based approach.

- Measurements and laboratory analyses
  - 1978: only pH and loss-on-ignition (LOI) were measured.
  - 1990: some soil mapping occurred.
  - 1998, 2007, and rolling 2018/2019–2023: multiple cores per X-plot with varying measurements; samples are homogenised before pH and LOI analyses.
  - Bulk density: measured in 2007 and 2018/19–2023, but not using ISO bulk density methods (which would require full cores).
  - No chemical analyses are performed by soil horizons; the method emphasizes homogenisation prior to measurements.
  - A formal documentation of methods and implications is provided by Emmett et al. (2008).

- Data structure, identifiers, and provenance
  - Each CS square contains up to 5 X-plots, each with potentially multiple cores and measurements.
  - The repeat identifier (e.g., 2RPT1) tracks the same location across years, though exact sampling points may shift slightly (2–3 m).
  - Sampling data are associated with the CS website and related publications; core photos and detailed core measurements are part of the data record.

- Statistical analysis considerations
  - Analyses should account for land class structure; ignoring land classes can misrepresent stock and change, whereas including them yields national estimates weighted by land classes.
  - Bootstrapping is not universally applied; when analyzing, consider the CS design and structure.
  - A mixed-effects model with square as a random factor is advised to account for multiple X-plots within each CS square.
  - In CS design-based analyses, only one core per location is typical; dispersion of observations across regions can improve precision and coverage for regional estimates.
  - Users are advised to consult UKCEH prior to analysis and to review existing CS publications available on the CS website.

- Data quality and caveats
  - Across years, not all measurements are available for all samples; data completeness varies.
  - Relocation and non-replicate nature of X-plots introduce heterogeneity; interpretation should consider land-use and plot-level context.
  - The rolling survey design emphasizes broad coverage and comparability over time, but methodological differences across years (e.g., core methods, depth, and bulk density protocols) should be accounted for in analyses.

- Outputs and usage
  - The dataset supports national stock and change estimates and regional assessments through a dispersed sampling framework.
  - Findings and methodologies are documented in Emmett et al. (2008) and related CS publications, guiding interpretation and downstream data products.

- References
  - Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.