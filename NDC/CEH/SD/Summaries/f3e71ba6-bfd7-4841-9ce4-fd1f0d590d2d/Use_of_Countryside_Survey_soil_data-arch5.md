# Sampling design

- Longitudinal soil sampling conducted in 1978, 1998, and 2007. 
- 1978 and 1998 used the same 256 CS squares; 2007 expanded to 591 CS squares, with not all measurements taken on every sample. Power analyses were used to determine sample sizes for detecting significant change (Emmett et al. 2008).
- Data structure evolves over time, with differing measurement sets and sampling coverage across years.

## Sampling framework and site location

- Soils are sampled from CS x-plots; each CS square contains 5 randomly spaced x-plots.
- X-plots are not replicates due to variation in land use and soil types across plots.
- Some plots are relocated over time due to destruction, access denial, or uncertain relocation; each location has a unique repeat identifier (e.g., 2RPT1) referring to a square and a repeat plot.
- Sampling locations are approximately 2–3 m apart around a permanently marked 2 m × 2 m plot at each sampling point.

## Sampling method

- Top 15 cm of soil sampled in 1998 and 2007 (8 cm for invertebrate samples); 1978 used a soil pit to sample the top 15 cm.
- Core sampling predominantly; some soils prevented full core collection due to stones or shallow depth.
- In 2007, core photographs and detailed core-dimension measurements were recorded for 2 of the 4 cores in use.

## Measurements and laboratory analyses

- 1978: laboratory measurements limited to pH and loss-on-ignition (LOI).
- 1990: some soil mapping activities occurred.
- 1998 and 2007: multiple cores per x-plot, with different measurements per core (see Table 1). Samples are homogenised before pH and LOI measurements; chemical analyses by horizons were not performed.
- Bulk density measured in 2007, but not using ISO whole-core bulk density methodology.
- A CS Soils report (Emmett et al., 2008) provides full methods and implications for measurement approaches.

## Measurements and data scope (Table 1)

- Measurements include LOI, pH (in water and CaCl2), %C, %N, bulk density, core dimensions, photographs, depth of organic layer, hand texture, soil moisture, Olsen P, metals, mineralisable N, and others.
- Data availability varies by year and by square:
  - Some measurements available for all 591 squares; others restricted to original 256 squares.
  - Certain data (notably some detailed core measurements) were released only after the Soils Report (November 2009).

## Statistical analysis and interpretation

- Analyses should consider land class structure; ignoring it yields stock and change estimates for the population, while accounting for land classes yields weighted national estimates.
- Bootstrapping is not consistently used across analyses.
- The CS design emphasizes spatial structure less than dispersed, regionally representative sampling; a mixed model with square as a random factor is recommended to account for multiple x-plots per square.
- Practitioners are advised to consult CEH before analysis and to review CS publications available on the CS website.

## Data governance and stewardship implications

- Unique repeat identifiers are crucial for cross-year comparability; metadata should document relocation history and exact sampling logic per year.
- Document the evolution of measurement schemes and which variables are available for which squares/years.
- Note that some data are release-limited (post-2009) and subject to access restrictions; track versioning and data availability.
- Ensure clear provenance, measurement methods, and any deviations from ISO or standard protocols are captured in metadata.
- Provide guidance on appropriate analysis approaches (e.g., mixed models with square as random factor) and references (e.g., Emmett et al. 2008) to data users.

## References

- Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.