# Sampling design

- Purpose and scope
  - Describes the Countryside Survey (CS) soils sampling design across 1978, 1998, and 2007.
  - Includes sampling locations, depth, measurements, and statistical guidance.

- Sampling framework and location
  - Years and squares: 1978 and 1998 used 256 squares; 2007 expanded to 591 CS squares.
  - x-plots: Each CS square contains 5 randomly spaced x-plots. X-plots are not replicates due to differing land uses, soil types, etc.
  - Relocation and tracking: x-plots may be relocated or destroyed; each location has a unique repeat identifier (e.g., 2RPT1) linking to the square and repeat plot, though exact positions shift ~2–3 m around a fixed 2 m × 2 m plot.

- Sampling methods and depth
  - Depths: Top 15 cm of soil sampled (8 cm for invertebrate samples).
  - Methods by year: 1998 and 2007 used soil cores; 1978 used a soil pit.
  - Practical notes: Full cores may be unattainable due to stones or shallow soils; core photographs and dimensions were recorded in 2007 for some cores.

- Measurements and laboratory work
  - 1978: Only pH and loss-on-ignition (LOI) measured.
  - 1998 and 2007: Multiple cores per x-plot with different measurements per core; samples homogenised before pH (in water and CaCl2) and LOI analyses.
  - 2007 specifics: Bulk density measured (not via ISO method); core dimensions and photographs recorded; Table 1 lists a broad set of measurements, including:
    - %C, %N, pH (in water and CaCl2), metals, Olsen P, mineralisable N, soil moisture, soil texture (hand texture), depth of organic layer, %C, %N, and other core-specific measurements.
  - Data scope: Measurements vary by year and by whether all 591 squares or only original 256 squares were sampled for a given variable; some datasets released only after the Soils Report (Nov 2009).

- Data structure and notes on measurements
  - Many measurements are available for all 591 squares (e.g., pH, LOI, soil moisture, %C, %N); some measurements are limited to original 256 squares or a subset of x-plots.
  - Table 1 summarises the measurements across core types and years; some data were collected on only a subset of x-plots.

- Statistical analysis guidance
  - Consider land class structure: ignoring land classes yields stock/change estimates for the population; incorporating land classes yields national estimates weighted by land class.
  - Use of bootstrapping varies; recommended to use mixed models with square as a random factor to account for multiple x-plots per square.
  - Design-based CS aims for dispersed observations; spatial structure is not the primary focus; broader regional estimates benefit from widespread sampling to improve precision and coverage.
  - Analysts are advised to consult CEH before analysis and to review CS publications available on the CS website for context.

- Data usage notes
  - The CS design emphasizes careful interpretation with attention to sampling design, measurement scope, and potential data limitations.
  - Data availability includes published methods, protocols, and results, with some measurements released only after 2009.

- References
  - Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. CEH project and DEFRA contact details.
  - Soils Report published November 2009 (data release context).