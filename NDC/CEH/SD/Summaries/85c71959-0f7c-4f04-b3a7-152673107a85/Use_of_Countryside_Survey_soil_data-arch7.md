# Sampling design

- Timeline and scope
  - Soils sampled in CS in 1978, 1998, and 2007.
  - 1978 and 1998 used the same 256 CS squares; 2007 expanded to all 591 CS squares, though not every measurement was taken on every sample.
  - Power analyses were conducted to determine the number of samples needed to detect significant change (Emmett et al. 2008).

- Sampling units and locations
  - Soils are sampled from the CS x-plots; each CS square contains 5 x-plots randomly spaced.
  - X-plots within a square are not replicates (they may differ in land use, soil type, etc.).
  - Each sampling location has a unique repeat identifier (e.g., 2RPT1) corresponding to square 2, repeat plot 1.
  - Although locations are recorded, exact sampling points within each 2m x 2m plot are ca. 2–3 m apart as plots are moved around the corners.
  - X-plots can be relocated over the years due to land-use changes, access issues, or uncertainty in initial placement.

- Sampling design and depth
  - Soils sampled from the top 15 cm (8 cm for the invertebrate sample).
  - 1998 and 2007 used soil cores; 1978 used a soil pit to sample the top 15 cm.
  - In 1998 and 2007, multiple cores were taken per x-plot; some cores had different measurements.
  - In 1978, some soils could not yield a full core due to stones or shallow soils; core photographs and measurements were collected in 2007 for some cores.

- Measurements and data collection
  - 1978: laboratory measurements included pH and loss-on-ignition (LOI).
  - 1990: some soil mapping occurred.
  - 1998 and 2007: multiple cores per x-plot with different measurements per core (not all measurements applied to all samples).
  - In 2007, bulk density was measured (not using ISO core method due to practical constraints); other measurements include pH, LOI, %C, %N, Olsen P, metals, mineralisable N, soil moisture, texture, and photodocumentation (Table 1).
  - Some measurements and core data are linked to specific core types (e.g., black cores, long white, short white) and are summarized in Table 1.
  - Data releases: some measurements were released only after the Soils Report published in November 2009 (denoted by asterisks in the table).

- Data structure and interpretation
  - For 2007, measurements cover all 591 squares for certain variables, while some measurements were conducted on subsets (e.g., data for Original 256 squares vs All 591 squares).
  - Different cores across years may have different measurement sets; data are not uniformly available for every measurement on every core.

- Statistical analysis considerations
  - Analyses should account for land class structure; ignoring land classes can bias results toward stock and change of the population.
  - Weighting by land classes can yield national estimates of stock and change.
  - Bootstrapping is not always used; where applicable, a mixed model with square as a random factor is recommended to handle multiple x-plots within a square.
  - In CS design-based contexts where spatial structure is not the primary focus, a dispersed sampling approach can improve overall precision and regional coverage for estimates.
  - Users are advised to consult CEH before analysis and interpretation and to review published CS soils data analyses (CEH CS website references).

- Practical GIS implications
  - Spatial alignment across years must consider relocation of x-plots and the evolving set of 256 vs 591 squares.
  - The spatial precision of sampling points within each 2m x 2m plot is limited to approximately 2–3 m from the nominal location.
  - The data framework supports multiple thematic layers (pH, LOI, C, N, P, metals, bulk density, moisture, texture, etc.) across different years and sampling units, but users should verify which measurements are available for each square and year.

- References
  - Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. CEH Project No. C03042/ DEFRA Contact No. CR0334.