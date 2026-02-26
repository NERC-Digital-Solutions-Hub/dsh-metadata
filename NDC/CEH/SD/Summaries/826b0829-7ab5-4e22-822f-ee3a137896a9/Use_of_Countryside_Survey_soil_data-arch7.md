# Sampling design

- Overview
  - Soils were sampled in the Countryside Survey (CS) during 1978, 1998 and 2007.
  - In 1978 and 1998, the same 256 squares were sampled; in 2007, soils were collected from all 591 CS squares, though not all measurements were made on all samples.
  - Power analyses were performed to determine the number of samples needed to detect significant change (Emmett et al. 2008).

- Sample location and plotting
  - Soils are sampled from the CS x-plots, with 5 x-plots randomly spaced within each CS square.
  - x-plots within a square are not treated as replicates due to differing land uses and soil types.
  - Over time, x-plots may be relocated if a plot is destroyed, access is denied, or exact relocation is uncertain.
  - Each location has a unique repeat identifier (e.g., 2RPT1): square 2, repeat plot 1.
  - Samples with the same identifier originate from the same location, though exact sampling points are typically 2–3 m apart around a permanently marked 2 m × 2 m plot.

- Sampling methodology
  - Top 15 cm of soil (8 cm for invertebrate samples) was sampled in 1998 and 2007 using a soil core; 1978 used a soil pit for the top 15 cm.
  - Some soils prevented full core collection due to stones or shallow soils.
  - In 2007, core photographs and detailed measurements of core dimensions were taken for 2 of the 4 cores.

- Measurements and laboratory analyses
  - 1978: limited to pH and loss-on-ignition (LOI).
  - 1998 and 2007: multiple cores per x-plot with different measurements on different cores.
  - No chemical analyses by soil horizon; samples were homogenised before pH and LOI measurements.
  - 2007: bulk density measured (not via ISO bulk density method).
  - A full description and implications are documented in Emmett et al. (2008).

- Data structure and coverage
  - Table 1 lists measurements across cores; measurements include pH (in water and CaCl2), LOI, %C, %N, bulk density, core dimensions, photographs, depth of organic layer, hand texture, soil moisture, Olsen P, metals, and other variables.
  - Coverage varies: some measurements apply to all 591 squares in 2007, others only to original 256 squares.
  - Some data were released later (data marked with an asterisk indicate release after the Soils Report published in November 2009).

- Statistical analysis considerations
  - Analyses should account for land class structure; ignoring land classes yields stock/change of the population, while incorporating land classes yields weighted national estimates.
  - Bootstrapping is not consistently used in analyses of CS soils data.
  - A mixed model is advised, with square treated as a random factor to reflect multiple x-plots per CS square.
  - In CS design-based contexts where spatial structure is not the primary interest, a dispersed set of observations enhances regional precision and coverage.
  - Users are advised to consult CEH prior to analysis and interpretation and to review CS publications listed on the CS website for prior analyses and methods.

- GIS-relevant notes
  - Spatial references include CS squares and repeat identifiers (e.g., 2RPT1), enabling temporal mapping across 1978, 1998 and 2007.
  - Relocation and non-replicate nature of x-plots require careful handling in GIS (tracking repeat IDs and spatial uncertainty ~2–3 m).
  - Data integration across years necessitates harmonization due to changes in sampling design, measurement sets, and coverage.
  - For map-based products, consider data availability by year, measurement type, and square/plot coverage; reference Emmett et al. 2008 for methodology and data processing details.