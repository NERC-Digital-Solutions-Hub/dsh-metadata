# Sampling design

- Outline of the long-term soil sampling program across multiple years (1978, 1998, 2007, 2019+), with a shift to a rolling survey in 2019 aiming to measure about 100 squares per year for five years before repeating.
- Power analyses were used to determine the number of samples needed to detect significant change (reference: Emmett et al. 2008).
- Data leadership takeaway: plan for longitudinal data consistency, document sampling cadence, and maintain a clear protocol for detecting temporal trends.

## Sample location

- Soil samples are taken from CS x-plots, with 5 x-plots randomly spaced within each CS square.
- X-plots within a square are not replicates because they may differ in land use, soil type, etc.
- Some locations are relocated over time due to land use change, access issues, or uncertainty; each location has a unique repeat identifier (e.g., 2RPT1) corresponding to square and repeat plot.
- Within a square, sampling locations are approximately 2–3 m apart around a permanently marked 2 m x 2 m plot.
- Data leadership takeaway: ensure robust traceability with repeat identifiers, capture location changes, and document sampling geometry for reproducibility and metadata quality.

## Sampling

- Soil is collected from the top 15 cm of the profile (8 cm for invertebrate samples).
- Methods evolved: 1998, 2007, 2019 used a soil core; 1978 used a soil pit.
- In some cases, a full core couldn’t be collected due to stones or shallow soils.
- Core photographs and measurements of core dimensions were taken in 2007 for a subset of cores.
- Data leadership takeaway: record method variation and practical constraints, maintain provenance of each sample, and capture any deviations from standard protocols for transparent data interpretation.

## Measurements

- In 1978, laboratory measurements were limited to pH and loss-on-ignition (LOI); later years included more comprehensive measurements.
- In CS1990, some soil mapping occurred; multiple cores were taken per x-plot in 1998, 2007, and 2019, with different cores carrying different measurements.
- No chemical analyses by soil horizons; samples were homogenised before pH and LOI measurements.
- Bulk density was measured in 2007 and 2019, but not using ISO bulk density methods (which would require a whole core).
- A report on implications and full method description is available (Emmett et al. 2008).
- Data leadership takeaway: track measurement types, methods, and any non-ISO procedures; ensure homogenisation and sample provenance are documented to support data quality and comparability over time.

## Statistical analysis

- Analyses should account for land class structure; ignoring it yields stock/change of the population, while including land classes yields national estimates of stock and change.
- Bootstrapping is not consistently used across analyses.
- The CS data structure suggests using mixed models with square as a random factor to account for multiple x-plots within each CS square.
- For CS-type designs where spatial structure is not the primary interest, a dispersed set of observations can improve regional precision and coverage.
- Users are advised to consult CEH before analysis and to review publications that already exploit the CS data (listed on the CS website).
- Data leadership takeaway: adopt analysis approaches that reflect the hierarchical sampling design, document model choices, and ensure users understand how to incorporate land-class structure and spatial considerations for credible inferences.

## References

- Emmett, BA, ZL Frogbrook, PM Chamberlain, R Griffiths, R Pickup, B Reynolds, E Rowe, P Rowland, D Spurgeon, J Wilson, CM Wood. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.