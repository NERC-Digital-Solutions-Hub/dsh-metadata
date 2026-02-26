# Sampling design

- Survey timeline and scope
  - Soils were sampled in the Countryside Survey (CS) in 1978, 1998, 2007, and 2019.
  - 1978 and 1998 used the same 256 squares; 2007 sampled all 591 CS squares but not all measurements were performed on every sample; 2019 initiated a rolling survey aiming to measure ~100 squares per year for five years before repeating.

- Sampling locations and repetition
  - Sampling from CS x-plots; each CS square contains 5 x-plots randomly spaced.
  - x-plots within a square are not replicates due to differing land uses/types.
  - Over time, x-plots may be relocated or destroyed (e.g., car park) or access denied; each location has a unique repeat identifier (e.g., 2RPT1).
  - Samples with the same unique identifier come from the same location, though exact sampling positions within a permanently marked 2m x 2m plot are typically ~2–3 m apart.

- Sampling procedures
  - Soils collected from the top 15 cm (8 cm for invertebrate samples).
  - 1998, 2007, 2019 used soil cores hammered into the soil and pulled out; 1978 used a soil pit to collect from the top 15 cm.
  - In some soils, full core collection wasn’t possible due to stones or shallow soils.
  - Core photographs and measurements of core dimensions were taken in 2007 for 2 of the 4 cores.

- Measurements and laboratory analyses
  - 1978 measurements: pH and loss-on-ignition (LOI) only.
  - 1990: some soil mapping occurred.
  - 1998, 2007, 2019: multiple cores per x-plot with different measurements; no chemical analyses by soil horizon; samples homogenised before pH and LOI measurements.
  - Bulk density measured in 2007 and 2019, but not using ISO bulk density methods (which would require dedicated cores).
  - Full methodological implications and description available in Emmett et al. (2008).

- Data structure and provenance
  - Multiple cores per x-plot; different cores may have different measurements.
  - Not all cores have the same set of measurements; full data structure and method specifics described in Emmett et al. (2008).

- Statistical analysis considerations
  - Analyses should account for land class structure; ignoring land classes yields stock/change of the population rather than national estimates.
  - Bootstrapping not always used; connection to the CS design implies using a mixed model with square as a random factor to reflect multiple x-plots per CS square.
  - CS design emphasizes dispersed observations for increased precision and regional coverage rather than strict spatial structure.
  - Users are advised to consult CEH prior to analysis and to review CS publications available on the CS website for context and prior analyses.

- Data governance, updates, and provenance notes
  - Rolling 2019 survey implies ongoing data accrual and potential updates; maintain consistent unique repeat identifiers across years.
  - Documentation should capture sampling year, plot status (relocated/destroyed), measurement types per core, and any deviations from standard protocols.
  - Transparency about methods (e.g., non-ISO bulk density method) and cores per location is essential for reproducibility and meta-analyses.

- References
  - Emmett, BA et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.