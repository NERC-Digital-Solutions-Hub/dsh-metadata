# Sampling design

- Purpose and scope: Describes the Countryside Survey (CS) soils sampling design, measurement protocol, and analytical considerations; includes power analyses (Emmett et al. 2008) and a rolling survey initiated in 2019 to measure ~100 squares per year for five years before repeating.

- Temporal design across years: 
  - Sampling years: 1978, 1998, 2007, 2019.
  - 1978 and 1998 used the same 256 squares; 2007 sampled all 591 CS squares but not all measurements were made on every sample.
  - 2019 started a rolling survey with a target of ~100 squares per year for five years.

- Spatial sampling framework: 
  - Soils are sampled from CS x-plots; each CS square contains 5 randomly spaced x-plots.
  - X-plots within a square are not replicates (different land uses, soil types, etc.).
  - X-plots may be relocated over time due to plot destruction, access denial, or relocation uncertainty.
  - Each location has a unique repeat identifier (e.g., 2RPT1) indicating square and repeat plot; locations used across years may be 2–3 m apart around a 2 m × 2 m permanent plot.

- Sampling protocol:
  - Depth: top 15 cm of soil (8 cm for invertebrate samples).
  - 1998, 2007, 2019: soil cores hammered in and pulled out.
  - 1978: soil pit dug; samples taken from top 15 cm of pit side.
  - Some soils may prevent full-core collection due to stones or shallow soils.
  - In 2007, core photographs and detailed measurements of core dimensions were taken for 2 of the 4 cores (black cores and N mineralization cores).

- Measurements and laboratory analyses:
  - 1978: only pH and loss-on-ignition (LOI).
  - 1990: some soil mapping conducted.
  - 1998, 2007, 2019: multiple cores per x-plot; different cores have different measurements.
  - No chemical analyses by soil horizons; samples homogenised before pH and LOI.
  - Bulk density measured in 2007 and 2019 (not via ISO bulk density method).
  - A detailed methods report and implications available (Emmett et al. 2008).

- Data structure and identifiers:
  - Each sampling location has a fixed, unique repeat ID (e.g., 2RPT1); exact sampling spots within the plot may shift by a few meters but remain within the permanent 2 m × 2 m plot.

- Statistical analysis guidance:
  - Analyses should account for land class structure; ignoring land classes yields stock/change of the population, while including them provides weighted national estimates.
  - Bootstrapping is not consistently used across analyses.
  - Use a mixed model with square as a random factor to capture multiple x-plots within a CS square.
  - In design-based CS approaches, dispersed observations can increase regional precision and coverage; note that usually only one core is taken per location.
  - For analyses, consult CEH prior to interpretation and review CS publications exploiting the data (CS website).

- References:
  - Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.