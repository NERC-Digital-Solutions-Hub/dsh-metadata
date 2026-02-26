# Sampling design

- Context and timeline
  - Soils sampled in Countryside Survey (CS) in 1978, 1998, 2007, and 2019.
  - 1978 and 1998 used the same 256 squares; 2007 sampled all 591 CS squares but not all measurements were made on all samples.
  - 2018 pilot survey; 2019–2023 marks the start of a rolling survey targeting ~100 squares per year for five years before repeating.

- Sample location and structure
  - Soils sampled from CS X-plots; each CS square contains 5 randomly spaced X-plots.
  - X-plots within a square are not replicates due to differing land uses, soil types, etc.
  - Plots can be relocated over time (e.g., due to destruction, access denial). Each location has a unique repeat identifier (e.g., 2RPT1: square 2, repeat plot 1).
  - Multiple samples from the same location are expected to be ~2–3 meters apart around a permanently marked 2 m × 2 m plot corner.

- Sampling design and depth
  - Soils collected from the top 15 cm of the profile (8 cm depth for invertebrate samples).
  - 1998/2007 and rolling survey (2018/19–2023) used soil cores; 1978 used a soil pit.
  - Some soils prevented full 15 cm due to stones or shallow soils; core photographs and measurements of core dimensions were taken in 2007 for some cores.

- Measurements and lab analyses
  - 1978: pH and loss-on-ignition (LOI) only.
  - 1998, 2007, and rolling survey: multiple cores per X-plot; not all cores have the same measurements.
  - Bulk density measured in 2007 and 2018/19–2023, but not by the ISO bulk density method (would require a whole core).
  - No chemical analyses by horizon; samples homogenised before pH and LOI.
  - Core dimension measurements and special cores (e.g., black cores, N mineralization cores) recorded in 2007.
  - References for methods and implications: Emmett et al. 2008.

- Statistical analysis considerations
  - Analyses should account for land class structure; ignoring land classes yields population stock and change rather than national estimates weighted by land classes.
  - Bootstrapping is not consistently used; the CS structure should be considered.
  - Recommended approach: use a mixed model with square as a random factor to account for multiple X-plots per CS square.
  - Design-based perspective: dispersion of observations increases regional precision and coverage; not every location requires multiple cores.
  - For analyses, consider consulting UKCEH prior to analysis and check CS publications for previously exploited datasets.

- Practical guidance for users
  - Check the CS website for listed publications that exploit CS soils data.
  - The reference framework for methodology and power analyses: Emmett et al. 2008 (Countryside Survey Soils 2007: Method development, power analyses and protocols).