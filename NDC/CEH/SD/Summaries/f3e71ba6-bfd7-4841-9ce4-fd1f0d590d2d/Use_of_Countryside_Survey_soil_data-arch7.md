# Sampling design

- Soils were sampled in CS in 1978, 1998 and 2007.
  - 1978 and 1998: the same 256 squares were sampled.
  - 2007: soils collected from all 591 CS squares, though not all measurements were made on all samples.
  - Power analyses conducted to determine the number of samples needed to detect significant change (Emmett et al. 2008).

- Spatial sampling framework
  - Soils are sampled from CS x-plots, with 5 x-plots randomly spaced within each CS square.
  - The x-plots within a square are not replicates; they may represent very different land uses or soil types.
  - Over time, x-plots can be relocated due to destruction (e.g., land converted to a car park), permission issues, or relocation uncertainty.
  - Each sampling location has a unique repeat identifier (e.g., 2RPT1) that corresponds to square 2, repeat plot 1.
  - Locations within a square are approximately 2–3 m apart around a permanently marked 2 m × 2 m plot at each sampling location.

- Sampling methods
  - Soils collected from the top 15 cm (8 cm for invertebrate samples).
  - 1998 and 2007 used soil cores hammered into the soil; removed to collect samples.
  - 1978 used a soil pit with sampling from the top 15 cm of the profile at the pit side.
  - Some soils could not provide a full core due to stones or shallow soils.
  - Core photographs and detailed core-dimension measurements were taken in 2007 for two of the four cores.
  - In 1998 and 2007, multiple cores were taken per x-plot; different cores had different measurements.

- Measurements and laboratory analyses
  - 1978: pH and loss-on-ignition (LOI) only.
  - 1998 and 2007: a range of measurements per core (Table 1); not all cores have all measurements.
  - Measurements include: pH (in water and CaCl2), %C, %N, bulk density (measured in 2007, not via ISO full-core method), core dimensions, photographs, depth of organic layer, soil texture indicators (hand texture), soil moisture, Olsen P, metals, mineralisable N, etc.
  - In 1990, some soil mapping occurred (CS1990).
  - Not all measurements were made on all cores or squares; some data are tied to original 256 squares, some to all 591 squares.

- Data structure and availability (GIS relevance)
  - CS2007 data: measurements exist for all 591 squares for certain variables; some measurements restricted to the original 256 squares.
  - Some measurements were released only after the Soils Report published in November 2009.
  - The dataset includes per-core measurements, with variable coverage across x-plots and squares.
  - Table-style details indicate which measurements were made on which cores and how many samples were collected per category (e.g., all 591 squares vs. original 256 squares).

- Statistical and analytical considerations for GIS use
  - Analyses should account for land class structure; ignoring land classes can bias population estimates.
  - When land classes are included, results are weighted by land classes to reflect national estimates of stock and change.
  - Bootstrapping is not consistently used; spatial structure should be considered.
  - At minimum, use a mixed model with square as a random factor to account for multiple x-plots per CS square.
  - For CS-style design where specific spatial structure is not the primary focus, a dispersed sampling approach can improve regional precision and coverage.
  - For analysis and interpretation, consult CEH prior to analysis and review related publications that used the CS soils data (available on the CS website).

- Reference
  - Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology. Project No. C03042/ DEFRA Contact No. CR0334.