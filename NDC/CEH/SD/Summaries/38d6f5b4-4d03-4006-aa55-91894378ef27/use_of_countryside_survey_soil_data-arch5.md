# Sampling design

## Overview
- Soil sampling for Countryside Survey (CS) conducted in 1978, 1998, 2007, and 2019.
- Sample coverage expanded over time: 256 squares (1978/1998) vs 591 squares (2007); 2019 launched rolling survey aiming to sample ~100 squares per year for five years before repeating.
- Power analyses guided the number of samples (Emmett et al. 2008); a 2018 pilot preceded the rolling survey.

## Sample location and X-plots
- Soils collected from CS X-plots, with 5 X-plots randomly spaced within each CS square.
- X-plots are not replicates; they may differ in land use and soil type.
- Some X-plots are relocated due to plot destruction, access denial, or uncertainty in original locations.
- Each location has a unique repeat identifier (e.g., 2RPT1: square 2, repeat plot 1).
- Samples from the same unique identifier are from the same location, typically within 2–3 m of the marked plot corners.

## Sampling method
- Top 15 cm of soil sampled (8 cm for invertebrate samples); 1998/2007 rolling survey used a hammered-in soil core; 1978 used a soil pit.
- Full 15 cm sometimes not achievable due to stones or shallow soils.
- Core photographs and core-dimension measurements were taken in 2007 for a subset of cores (black cores and N mineralization cores).
- Rolling CS survey adopted the core-based method.

## Measurements and laboratory analyses
- 1978: only pH and loss-on-ignition (LOI).
- 1990: some soil mapping conducted.
- 1998, 2007, and rolling survey (2018/2019–2023): multiple cores per X-plot with different measurements per core.
- Chemical analyses by horizon are not performed; samples are homogenised before pH and LOI.
- Bulk density measured in 2007 and 2018/19–2023, but not by ISO method (which would require a whole core).
- Full methodological notes are provided in Emmett et al. (2008).

## Statistical analysis considerations
- Analyses should account for land-class structure; ignoring it yields stock/change estimates for the population, while including it yields weighted national estimates.
- Bootstrapping is not always used.
- Use mixed models with square as a random factor to reflect multiple X-plots within each CS square.
- CS design emphasizes dispersed observations for regional estimates; typically only one core per location.
- Users planning regional estimates should consult UKCEH and review CS publications listed on the CS website.

## Data governance and user guidance (Data Stewards focus)
- Document and version changes in sampling design across years to support longitudinal data use.
- Maintain and track unique repeat identifiers (e.g., 2RPT1) and relocation events for reproducibility.
- Record method changes (core vs pit, measurement suites) and homogenization steps to preserve data provenance.
- Flag non-ISO bulk density methods and any related limitations.
- Provide guidance on analysis approaches (e.g., mixed models, accounting for land-class structure) and link to recommended analyses.
- Direct users to UKCEH and the CS website for methodological details and published analyses.

## Limitations and caveats
- X-plots are not replicates; relocations introduce spatial-temporal uncertainty.
- Differences in sampling methods across years (pit vs core) and measurement coverage may affect comparability.
- Not all soil cores are measured for every variable; some years have limited measurements per core.

## References
- Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.