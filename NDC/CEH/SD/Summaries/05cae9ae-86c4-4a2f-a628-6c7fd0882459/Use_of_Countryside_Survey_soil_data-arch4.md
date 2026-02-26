# Sampling design

- Overview
  - Soils were sampled in the Countryside Survey (CS) in 1978, 1998, and 2007.
  - The same 256 squares were sampled in 1978 and 1998; in 2007, soils were collected from all 591 CS squares, though not all measurements were made on every sample.
  - Power analyses (Emmett et al. 2008) determined the number of samples needed to detect significant change.

- Sample location
  - Sampling from CS x-plots, with 5 x-plots per CS square.
  - X-plots within a square are not replicates (they may represent different land uses or soil types).
  - Some plots are relocated over time due to destruction, access, or uncertainty; each location has a unique repeat identifier (e.g., 2RPT1).
  - Samples from the same identifier come from the same location, though actual sampling points are ~2–3 m apart around a 2m x 2m plotting grid.

- Sampling
  - Soils collected from the top 15 cm (8 cm for invertebrate samples).
  - 1998 and 2007 used a hammered soil core; 1978 used a soil pit.
  - In some cases, full core collection was not possible due to stones or shallow soils.
  - Core photographs and detailed core-dimension measurements were taken in 2007 for some cores.

- Measurements
  - 1978: pH and loss-on-ignition (LOI) only.
  - 1990: some soil mapping performed.
  - 1998 and 2007: multiple cores per x-plot, with different measurements made on different cores (Table 1).
  - No chemical analyses by soil horizon; samples homogenised before pH and LOI measurements.
  - Bulk density measured in 2007 (not using ISO bulk-density method due to core requirements).
  - Full method description and implications discussed in Emmett et al. 2008.
  - A wide range of measurements were recorded across cores (e.g., %C, %N, Olsen P, metals, mineralisable N, moisture, texture, etc.) with some measurements limited to specific plots or years.

- Data structure and availability
  - In 2007, measurements were taken across all 591 squares; some measurements were limited to subsets (e.g., original 256 squares for certain variables).
  - Table 1 lists measurements and the number of samples per category; data release notes indicate some data are released only after the Soils Report (November 2009).
  - Core-level data exist for multiple measurements across years, with a mix of sample scope (whole square vs. subset of plots).

- Statistical analysis guidance
  - Analyses should account for land-class structure; ignoring it yields population stock/change rather than national estimates weighted by land classes.
  - Bootstrapping is not consistently used; preferred approach includes mixed models with square as a random factor to account for multiple x-plots per CS square.
  - For CS-style design, spatial structure is not typically the primary focus; dispersed sampling can improve efficiency and regional precision.
  - Users are advised to consult CEH prior to analysis and interpretation and to review CS publications available on the CS website.

- Data governance and notes
  - The CS dataset emphasizes careful documentation of sampling designs, plot reliability, and measurement scope across years.
  - Some data are year- and plot-specific, requiring careful alignment when combining across years or moments in time.
  - Detailed methodological references: Emmett et al. (2008) on method development, power analyses, and protocols.

- References
  - Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.