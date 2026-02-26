# Sampling design

- Purpose and scope
  - Long-term soil sampling in Countryside Survey (CS) across years 1978, 1998, 2007, and 2019 to monitor environmental state.
  - 2019 marked the start of a rolling survey: ~100 squares sampled each year for five years, then repeated to enable detection of significant change.
  - Power analyses (Emmett et al. 2008) guided the number of samples required to detect change.

- Sample location and design
  - Sampling units are CS x-plots; each CS square contains 5 x-plots.
  - The 5 x-plots within a square are not replicates due to varying land uses, soils, etc.
  - Over time, x-plots can be relocated or removed due to land-use changes, access issues, or uncertainty in relocation.
  - Each location has a unique repeat identifier (e.g., 2RPT1): 2 indicates square, RPT1 indicates repeat plot 1.
  - Locations are within a permanently marked 2m x 2m plot; sampling position shifts ~2–3 m when moving around corners.

- Sampling methods by year
  - Soils sampled from the top 15 cm of the profile (8 cm for invertebrate sample).
  - 1978: soil pit excavated; top 15 cm sampled from pit side.
  - 1998, 2007, 2019: soil cores hammered into ground and extracted (with attempts to sample multiple cores per x-plot).
  - In 1978, full core collection could be impeded by stones or shallow soils.
  - In 2007, core photographs and measurements of core dimensions were taken for 2 of the 4 cores.

- Measurements and laboratory analyses
  - 1978: only pH and loss-on-ignition (LOI) measured.
  - 1990: soil mapping activities occurred (CS1990).
  - 1998, 2007, 2019: multiple cores per x-plot; different cores carry different measurements.
  - No chemical analyses by soil horizon; samples are homogenised before pH and LOI measurements.
  - Bulk density measured in 2007 and 2019; not performed using ISO bulk density method (would require a full core).
  - Full methodological details and implications described in Emmett et al. (2008).

- Data structure and interpretation considerations
  - Analyses should account for land class structure: ignoring it yields stock/change of the population; weighting by land class yields national estimates of stock and change.
  - Bootstrapping is not consistently used across analyses.
  - CS design supports mixed models: include square as a random factor to account for multiple x-plots within each CS square.
  - In CS, typically only one core is taken per location; however, a dispersed set of observations (design-based approach) increases regional precision and coverage when estimating national trends.
  - For regional estimates, broader, dispersed sampling improves precision; spatial structure is not the main focus of intention.

- Guidance and references
  - Researchers are advised to consult CEH (Centre for Ecology and Hydrology) prior to analysis and to review CS publications listed on the CS website for prior analyses using the data.
  - Key reference: Emmett et al. 2008 — Countryside Survey Soils 2007: Method development, power analyses and protocols (Project No. C03042/ DEFRA CR0334).