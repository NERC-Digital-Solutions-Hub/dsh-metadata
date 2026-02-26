# Sampling design

- Purpose and scope
  - Describes the Countryside Survey (CS) soil sampling design across years (1978, 1998, 2007, 2019 rolling survey) to detect significant change and support long-term soil monitoring.
  - Power analyses informed the number of samples needed (Emmett et al. 2008); rolling survey aims to sample ~100 squares per year for five years before repeating.

- Sampling design and units
  - Years and coverage:
    - 1978 and 1998: same 256 squares sampled.
    - 2007: soils collected from all 591 CS squares, not all measurements on every sample.
    - 2019 onward: rolling survey targeting ~100 squares per year for five years before repetition.
  - Plot structure:
    - Soils sampled from CS X-plots; each CS square contains 5 X-plots, randomly spaced.
    - X-plots are not replicates due to land-use and soil-type heterogeneity.
    - Relocation of some plots over time (e.g., destruction, access issues) but each location has a unique repeat identifier (e.g., 2RPT1).

- Sample location and repeat identifiers
  - Each repeat plot (e.g., 2RPT1) refers to a specific square and repeat within that square; same location across years, though exact sampling points may shift ~2–3 m around a permanently marked 2 m × 2 m plot corners.
  - Sampling locations are within the permanent CS square framework.

- Sampling methods and depth
  - Depths:
    - Top 15 cm (8 cm for invertebrate samples) targeted in 1998, 2007, and rolling survey (2018/19–2023); 1978 used a soil pit to sample the top 15 cm.
    - Some soils prevented full 15 cm core collection due to stones or shallow soils.
  - Core collection:
    - 1998, 2007, and rolling survey used soil cores hammered into the soil; in 1978 a pit method was used.
    - Core photographs and dimension measurements recorded in 2007 for selected cores (black cores and N mineralization cores).
  - Relocation and access issues cause occasional deviations from the original location, but the sampling design maintains a standardized structure for longitudinal analysis.

- Measurements and laboratory work
  - 1978: only pH and loss-on-ignition (LOI).
  - 1990: some soil mapping data collected.
  - 1998, 2007, and rolling survey (2018/19–2023): multiple cores per X-plot; different cores have different measurements.
  - Bulk density:
    - Measured in 2007 and 2018/19–2023, but not using ISO bulk density method (would require full core).
  - Processing:
    - Samples homogenised before pH and LOI analyses; no chemical analyses by horizon.
  - Documentation:
    - Full method details and implications discussed in Emmett et al. (2008).

- Data quality, processing, and comparability
  - Measurement comparability:
    - Across years, methods and measurements vary; some cores have different measurement sets, requiring careful harmonisation.
  - Data structure and analysis considerations:
    - CS results can be influenced by land class structure; analyses should account for land classes to produce national estimates of stock and change.
    - Bootstrapping is not consistently applied; design and model choices affect precision and inferences.
    - The hierarchical sampling (X-plots within squares) necessitates models that reflect this structure.
  - Recommended approach:
    - Use mixed models with square as a random factor to account for multiple X-plots per square.
    - For regional estimates, a dispersed design-based approach improves overall precision and coverage.
    - Always consider land class structure and consult UKCEH prior to analysis; review CS publications accessible via the CS website.

- Practical guidance for analysts
  - When analysing CS soils data, consult UKCEH to understand data structure and prior analyses.
  - Review published CS work to align methods and interpretation with established practice.
  - Check the CS website for available publications and data usage notes.

- References
  - Emmett, BA, et al. 2008. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.