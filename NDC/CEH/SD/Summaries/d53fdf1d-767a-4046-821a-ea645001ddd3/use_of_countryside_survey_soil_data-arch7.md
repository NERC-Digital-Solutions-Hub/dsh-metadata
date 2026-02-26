# Countryside Survey Soils

- Overview
  - Soils were sampled during Countryside Survey (CS) in 1978, 1998, 2007, and the rolling survey starting in 2019.
  - Early years used a fixed number of squares; 1978 and 1998 used 256 squares, 2007 used 591 squares.
  - Power analyses (Emmett et al. 2008) guided the number of samples needed to detect significant change.
  - Rolling survey aims to measure ~100 squares per year for five years before repeating.

- Sampling design
  - Sampling scope spans multiple CS years with evolving square counts.
  - A pilot occurred in 2018; rolling survey launched in 2019.

- Sample location
  - Soils are sampled from CS X-plots within each CS square; there are 5 X-plots per square.
  - X-plots are not replicates due to differing land uses and soil types.
  - Some plots are relocated over time due to destruction, access denial, or relocation uncertainty.
  - Each location has a unique repeat identifier (e.g., 2RPT1: square 2, repeat plot 1).
  - Repeats indicate the same location across years, but exact sampling positions shift ~2–3 m within a permanently marked 2 m × 2 m plot.

- Sampling
  - Top 15 cm of soil is sampled (8 cm for invertebrate samples) in 1998, 2007, and the 2019 rolling survey.
  - 1978 used a soil pit with sampling from the top 15 cm of the pit side.
  - Full 15 cm sometimes not possible due to stones or shallow soils.
  - Core photographs and detailed measurements were made in 2007 on two of the four cores (black cores and N mineralization cores).
  - The rolling CS survey adopted this core-sampling method.

- Measurements
  - 1978: pH and loss-on-ignition (LOI) only.
  - 1990: some soil mapping; multiple cores per X-plot with different measurements; samples homogenised before pH/LOI.
  - Bulk density measured in 2007 and 2018/19–2023 (not via ISO bulk density method).
  - No chemical analyses by horizons; homogenisation before analysis.
  - A report on implications and full method description available (Emmett et al. 2008).

- Statistical analysis implications for GIS
  - Analyses should consider land class structure; ignoring it yields stock/change estimates, while accounting for land classes yields weighted national estimates.
  - Bootstrapping not consistently used in analyses.
  - Use mixed models with square as a random factor to account for multiple X-plots per square (up to 5).
  - Only one core per location, but the dispersed design can improve regional precision and coverage when estimating regional stocks.
  - Design-based approaches without strong spatial structure favor dispersed observation placement for efficiency.
  - Researchers should consult UKCEH prior to analysis and review CS publications listed on the CS website.

- References
  - Emmett, BA et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.