# Sampling design

- Timeline and scope
  - Soils sampled in CS in 1978, 1998, 2007, and 2019+.
  - 1978 and 1998 used the same 256 squares; 2007 sampled all 591 CS squares.
  - 2019 marked the start of a rolling survey targeting ~100 squares per year for five years before repeating.

- Sample location and plot structure
  - Sampling from CS x-plots; each CS square contains 5 x-plots.
  - x-plots within a square are not replicates (they may differ in land use, soil type, etc.).
  - Some x-plots are relocated over time due to land-use changes, access, or land destruction; each location has a unique repeat identifier (e.g., 2RPT1).
  - Locations with the same identifier are treated as the same site across years, though exact sampling points are ~2–3 m apart.
  - Within each square, sampling occurs in a permanently marked 2m x 2m plot at the four corners; exact positions vary slightly within the plot.

- Sampling design and planned coverage
  - In 2019 onward, a rolling approach aims to measure approximately 100 squares per year for five years before repeating.
  - The sample structure balances broad national coverage with long-term monitoring at repeat locations.

- Sampling methods and depth
  - Top 15 cm of soil sampled consistently (8 cm for the invertebrate sample).
  - 1998, 2007, and 2019 used soil cores hammered into the soil and extracted; 1978 used a soil pit to sample the top 15 cm.
  - Some cores could not be collected fully due to stones or shallow soils; records note these limitations.
  - In 2007, core photographs and detailed measurements of core dimensions were taken for two of the four cores.

- Measurements and laboratory analyses
  - 1978: only pH and loss-on-ignition (LOI).
  - By CS1990, some soil mapping occurred.
  - 1998, 2007, and 2019: multiple cores per x-plot; different cores carry different measurements.
  - No chemical analyses are performed by soil horizons; samples are homogenised before pH and LOI measurements.
  - Bulk density measured in 2007 and 2019, but not using ISO bulk density methods (which would require a whole core).
  - A detailed methods report is Emmett et al. 2008.

- Data analysis considerations and guidance
  - Analyses should account for land class structure; ignoring it biases results toward stock and change of the overall population.
  - If land classes are incorporated, results are weighted to produce national estimates of stock and change.
  - Bootstrapping is not consistently used across analyses.
  - CS data are hierarchical: multiple x-plots within each square; use mixed models with square as a random factor to reflect this structure.
  - In CS, a dispersed set of observations is efficient for regional estimates, even though spatial structure is not the primary focus.
  - For analysis and interpretation, consult CEH prior to analysis and review publications that already exploit CS data (listed on the CS website).

- Practical notes and cautions
  - The sampling design aims to balance temporal consistency with practical access issues.
  - Data users should be aware of relocations and potential spatial misalignment when tracking repeat locations.
  - The methods emphasize cross-year comparability while accommodating changes in sample availability and land access.

- Reference
  - Emmett, B.A., et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.