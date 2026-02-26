# Sampling design

- Objective and scope
  - Soils sampled in Countryside Survey (CS) in 1978, 1998, 2007, and 2019+, with evolving scope.
  - 1978 and 1998 used the same 256 squares; 2007 sampled all 591 CS squares (not all measurements on all samples); 2019 begins a rolling survey aiming for ~100 squares per year for five years before repeating.

- Sample location and structure
  - Soils sampled from CS x-plots; each CS square contains 5 x-plots randomly spaced.
  - x-plots within a square are not replicates (varying land use, soil types, etc.).
  - Relocation of x-plots over time due to land changes or access issues; each location has a unique repeat identifier (e.g., 2RPT1: square 2, repeat plot 1).
  - Repeated locations are treated as the same site, with sampling locations typically ~2–3 m apart within a permanently marked 2 m x 2 m plot at each visit.

- Sampling design and timing
  - 2019 onward: rolling survey approach; around 100 squares sampled per year for five years, then repeated.
  - Across years, sampling locations may shift, but the repeat identifiers link samples to the same location conceptually.

- Field sampling methods
  - Top 15 cm of soil collected (8 cm for the invertebrate sample); cores hammered into soil and pulled out (1998, 2007, 2019).
  - In 1978, a soil pit was dug and top 15 cm collected from the pit side.
  - Some cores were not fully collected due to stones or shallow soils.
  - In 2007, core photographs and measurements of core dimensions were taken for some cores (black cores and N mineralization cores).

- Measurements and laboratories
  - 1978: laboratory measurements limited to pH and loss-on-ignition (LOI).
  - 1990: some soil mapping conducted.
  - 1998, 2007, 2019: multiple cores per x-plot; different cores have different measurements.
  - No chemical analyses by soil horizon; samples homogenized before pH and LOI measurements.
  - Bulk density measured in 2007 and 2019 (not using ISO bulk density method due to core constraints).
  - A detailed methods report is available (Emmett et al. 2008).

- Data structure and GIS considerations
  - Sample coordinates approximate due to relocation; exact sampling locations within a 2 m x 2 m plot may vary by ~2–3 m between visits.
  - Each CS square contains multiple x-plots; samples from the same repeat location may be spatially clustered.
  - Data include a mix of years with varying measurement sets; careful harmonization needed for GIS analyses and temporal comparisons.

- Statistical analysis considerations (relevant to GIS data users)
  - Analyses should account for land class structure; failing to do so may bias stock/change estimates.
  - If land classes are not included, results reflect population stock/change; including land classes yields weighted national estimates.
  - Bootstrapping is not consistently used; recommended to consider mixed models with square as a random factor to account for multiple x-plots per square.
  - Design-based approaches (dispersed sampling) can improve regional precision and coverage when estimating regional parameters.
  - Users are advised to consult CEH prior to analysis and to review existing CS-related publications (CEH CS website).

- References
  - Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.