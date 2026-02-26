# Sampling design

- The Countryside Survey (CS) soils program has historical sampling in 1978, 1998, 2007, and 2019+, with 2019 initiating a rolling survey to measure about 100 squares per year for five years before repeating.
- Early years used a fixed set of squares (256 in 1978/1998) while 2007 sampled all CS squares (591); power analyses (Emmett et al. 2008) informed the number of samples needed to detect significant change.
- Data stewardship implication: maintain historic and current sampling scope, with clear versioning and documentation of design changes over time.

## Sample location and plot design

- Soils are sampled from CS x-plots, with 5 x-plots randomly distributed within each CS square.
- x-plots within a square are not replicates due to differences in land use and soil types.
- Some plots are relocated over time (e.g., destroyed, access denied, or relocation uncertainty); each location has a unique repeat identifier (e.g., 2RPT1) indicating square 2, repeat plot 1.
- Samples with the same unique identifier originate from the same location, though exact sampling points shift about 2–3 m within a permanently marked 2m x 2m plot.
- Data governance note: preserve and document unique repeat identifiers, exact square and plot references, and any relocation history to ensure traceability across years.

## Sampling method

- Soil collected from the top 15 cm (8 cm for invertebrate samples).
- 1998, 2007, and 2019 used a soil core hammered into the soil and pulled out; 1978 used a soil pit to sample the top 15 cm.
- In some soils, full cores were not possible due to stones or shallow soils.
- In 2007, core photographs and detailed measurements of core dimensions were taken for 2 of the 4 cores (black cores and N mineralization cores).
- Data stewardship note: capture method variant (core vs pit) and any limitations in sampling depth or core completeness; store core photographs and dimension metadata where available.

## Measurements and laboratory analysis

- 1978 had pH and loss-on-ignition (LOI) measurements only; in CS1990 some soil mapping occurred.
- In 1998, 2007, and 2019, multiple cores were taken per x-plot, with different cores having different measurements.
- No chemical analyses are performed by soil horizons; samples are homogenised before pH and LOI measurements.
- Bulk density was measured in 2007 and 2019, but not using ISO bulk density methods (which require full cores).
- A full methodological discussion and implications are described in Emmett et al. 2008.
- Data stewardship note: document which measurements exist for each core, homogenisation procedures, and any deviations from ISO methods; provide clear metadata on measurement types by year and core.

## Statistical analysis and data interpretation guidance

- Analyses should consider land class structure; ignoring it yields stock and change estimates that may not be representative.
- If land classes are accounted for and weighted, results become national estimates of stock and change.
- Bootstrapping is not consistently used across analyses; consult CEH prior to analysis and interpretation.
- The CS data structure typically uses a mixed model with square as a random factor to account for up to five x-plots per CS square.
- Design-based approaches (dispersed observations) can improve precision and regional coverage, even when spatial structure is not the primary interest.
- For regional estimates, widespread sampling increases precision.
- Data users should review CS publications and the CS website for existing analyses and datasets.
- Data stewardship note: provide analysis-ready metadata, including the statistical approach recommended for combining years, treatment of land classes, and provenance of core-specific measurements.

## Data governance and provenance considerations

- Maintain a clear lineage of samples across years, including the exact square, repeat plot identifier, and any relocations.
- Preserve method changes and measurement sets by year to enable reproducible analyses and valid cross-year comparisons.
- Link measurements to their respective cores and sampling events, with clear flags for any cores missing measurements or altered sampling depth.
- Ensure metadata captures sampling depth, core type (core vs pit), presence of core photographs, and any deviations from standard protocols.
- Reference materials: Emmett et al. 2008; Emmett et al. 2007 (Method development, power analyses, and protocols).

## References

- Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.
- Emmett et al. 2008 (as cited for power analyses and protocols).