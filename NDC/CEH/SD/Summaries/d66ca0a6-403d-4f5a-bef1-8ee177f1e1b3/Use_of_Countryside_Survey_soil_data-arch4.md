# Sampling design

- Overview and purpose
  - Longitudinal soil monitoring across CS years (1978, 1998, 2007) to detect significant change.
  - Power analyses used to determine the required number of samples (Emmett et al. 2008).

- Sample framework and coverage
  - Soils sampled from CS x-plots within CS squares.
  - Each CS square contains 5 randomly spaced x-plots; x-plots are not replicates due to diverse land uses and soil types.
  - In 1978 and 1998 the same 256 squares were sampled; in 2007 sampling extended to all 591 CS squares.
  - Some x-plots are relocated over time due to land changes or access issues; each location has a unique repeat identifier (e.g., 2RPT1) linking repeated observations from the same location.

- Sampling design and location details
  - Sampling locations are within permanently marked 2m x 2m plots; within each plot, measurements are taken around the corners (samples may be 2–3 m apart).
  - Depth and method: soil is collected from the top 15 cm (8 cm for invertebrate samples).
  - Methods evolved: 1998/2007 used soil cores; 1978 used a soil pit. Core photos and dimension measurements were recorded in 2007 for some cores.

- Measurements and data collected
  - 1978: limited laboratory measurements (pH and LOI).
  - 1990: some soil mapping conducted.
  - 1998 and 2007: multiple cores per x-plot with different measurements per core; samples homogenised before pH and LOI measurements.
  - 2007: bulk density measured (not via ISO whole-core method); core dimensions, photographs, and several core-specific measurements recorded.
  - Table 1 (and accompanying notes) lists measurements across core types:
    - Measurements include pH (in water and CaCl2), LOI, %C, %N, bulk density, core dimensions, depth of organic layer, hand texture, soil moisture, Olsen P, metals, mineralisable N, and invertebrates (mainly Collembola and mites) for select x-plots.
  - Data release caveat: many data types are released only after the Soils Report (November 2009).

- Data structure and identifiers
  - Original sampling focused on 256 squares in earlier years, expanded to all 591 squares in 2007.
  - Different x-plots within a square are associated with the same repeat location via the repeat identifier; exact sampling positions vary but are anchored to fixed plots.

- Statistical analysis considerations
  - Analyses should account for land class structure; ignoring land classes can bias results toward stock and change of the population rather than national estimates.
  - Bootstrapping is not consistently used across analyses; at minimum, mixed models with square as a random factor are recommended to handle multiple x-plots per CS square.
  - For CS design-based analyses (where spatial structure is not the primary focus), a dispersed sampling approach can improve precision and regional coverage.
  - Users should consult CEH before analysis and review published CS data analyses available on the CS website.

- Governance, interpretation, and usage notes
  - Emphasis on careful interpretation due to heterogeneity in land use, sample availability, and year-to-year changes.
  - Encourage consultation with CEH and review of existing CS publications for context and methodological alignment.