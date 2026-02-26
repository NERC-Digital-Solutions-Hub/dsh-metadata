# Sampling design

- The Countryside Survey (CS) soils data come from multiple survey rounds: 1978, 1998, 2007, and 2019 rolling survey, with a pilot in 2018 and rolling starting in 2019 to measure ~100 squares per year for five years before re-measurement.
- In 1978 and 1998, the same 256 squares were sampled; in 2007 soils were collected from all 591 CS squares, though not all measurements were made on every sample.
- Sampling units are CS X-plots within each square; there are 5 X-plots per CS square. X-plots are not replicates and can be in very different land uses or soil types. Some X-plots are relocated over time due to land-use changes, access issues, or uncertainty in original locations. Each location has a unique repeat identifier (e.g., 2RPT1), referring to square 2, repeat plot 1; repeat plot 1 is a known location, though exact sampling points may be ~2–3 m apart around the 2 m x 2 m plot corners.
- Each sampling location is sampled within the top 15 cm of soil (8 cm for invertebrate samples). In 1978, a soil pit was used to sample the top 15 cm; in 1998, 2007, and the rolling survey (2018/19–2023), soil cores were hammered in and extracted. If stones or shallow soils prevent full 15 cm cores, shorter cores are collected.

- Measurements and lab methods:
  - 1978: laboratory measurements included pH and loss-on-ignition (LOI) only.
  - 1990: some soil mapping activities occurred.
  - 1998, 2007, and the rolling survey (2018/19–2023): multiple cores taken per X-plot; different cores carry different measurements; samples are homogenised before pH and LOI analyses.
  - Bulk density measured in 2007 and in 2018/19–2023, but not using the ISO bulk density method (which would require a whole core).
  - Core photographs and detailed core dimension measurements were performed in 2007 for selected cores.
  - A full description of methods and implications is given in Emmett et al. (2008).

- Statistical analysis considerations:
  - Analyses should account for land class structure; ignoring land classes can yield stock-and-change estimates for the population, whereas including land classes provides national estimates weighted by land classes.
  - Bootstrapping is not always used in CS soil analyses.
  - The CS design should be considered, with at least a mixed model approach using square as a random factor to account for multiple X-plots within each CS square.
  - CS emphasizes a dispersed set of observations rather than a strict spatially explicit structure; design-based approaches are efficient for regional estimates.
  - For analysis and interpretation, users are advised to consult UKCEH and review CS publications listed on the CS website to understand prior analyses.

- Practical guidance for data users:
  - Be aware that data are drawn from multiple cores per X-plot and not all measurements are performed on all samples; missing data across years are possible.
  - The non-replicate nature of X-plots within a square and potential relocations should be considered in analyses and interpretation.
  - When aiming for regional or national estimates, ensure proper weighting by land classes and consider using a mixed-model framework with square as a random effect.

- References:
  - Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.