# Sampling design

- Scope and timeline
  - Soil sampling conducted in Countryside Survey (CS) across 1978, 1998, 2007, and 2019 rolling survey.
  - 1978 and 1998 used the same 256 squares; 2007 sampled all 591 CS squares (not all measurements on all samples); rolling survey began in 2019 with aim to measure ~100 squares per year for five years before repeating.
  - Power analyses informed sample size to detect significant change (reference: Emmett et al. 2008).

- Data structure and identifiers
  - Samples collected from CS X-plots; each square contains 5 X-plots.
  - X-plots are not replicates due to differing land uses and soil types; locations may relocate due to land use changes or access permissions.
  - Each location has a unique repeat identifier (e.g., 2RPT1: square 2, repeat plot 1). Same identifier indicates the same location, though core positions shift ~2–3 m around a permanently marked 2 m × 2 m plot.

- Sampling location and plots
  - Sampling conducted within CS squares using the X-plot framework; repeat plots tracked by unique identifiers to preserve longitudinal linkage.

- Sampling protocol
  - Depth: soils sampled from the top 15 cm (8 cm for the invertebrate sample) in 1998, 2007, and rolling survey 2018/19–2023.
  - Methods:
    - 1998, 2007, rolling survey: soil cores hammered in and extracted.
    - 1978: soil pit dug with sampling from top 15 cm of pit side.
  - Practical adjustments:
    - Some soils prevented full 15 cm core collection due to stones or shallow soils.
    - In 2007, core photographs and measurements of core dimensions were taken for two cores (black cores and N mineralization cores).

- Measurements and laboratory analyses
  - 1978: only pH and loss-on-ignition (LOI).
  - 1990: some soil mapping conducted.
  - 1998, 2007, rolling survey: multiple cores per X-plot; different cores carry different measurements.
  - Horizons: no chemical analyses by soil horizon; samples homogenised before pH and LOI.
  - Bulk density:
    - Measured in 2007 and in rolling survey 2018/19–2023, but not using ISO bulk density method (which would require a whole core).
  - Documentation: full method description and implications discussed in Emmett et al. 2008.

- Statistical analysis considerations
  - Analyses should account for land class structure; ignoring land class can yield population stock/change estimates rather than national estimates weighted by land classes.
  - Bootstrapping not consistently applied across analyses.
  - Recommend mixed-model approaches with square as a random factor to account for multiple X-plots within each CS square.
  - Spatial structure: CS design is not inherently spatially focused; dispersed observations can improve precision and regional coverage.
  - Guidance: CS data users should consult UKCEH prior to analysis and review CS publications listed on the CS website for prior analyses.

- Data governance and metadata notes
  - Longitudinal dataset with evolving methods and measurements across years; metadata should capture year, square, X-plot, repeat ID, exact sampling depth, measurement types, core IDs, and any method changes.
  - Documentation reference: Emmett et al. 2008 provides full protocol context; dataset provenance should link to this and to the CS website for related publications.

- References
  - Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.