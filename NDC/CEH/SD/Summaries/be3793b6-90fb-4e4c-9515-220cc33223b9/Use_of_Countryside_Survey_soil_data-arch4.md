# Countryside Survey Soils 2007: Method development, power analyses and protocols

- A long-term soil monitoring program sampling CS squares across three time points (1978, 1998, 2007) with power analyses used to determine sample sizes for detecting significant change.
- In 1978 and 1998 the same 256 squares were sampled; in 2007 all 591 CS squares were sampled, though not every measurement was made on every sample.

## Sampling Design and Scope
- The CS soil data are designed to enable detection of change over time, with explicit power analyses guiding sample numbers.
- Data structure supports national estimates of stock and change when land-class structure is accounted for; otherwise, results reflect population stock and change without weighting.

## Sample Location and Plot Structure
- Soils are sampled from CS x-plots within each CS square, using five x-plots per square.
- X-plots within a square are not treated as replicates due to heterogeneity in land use and soil types.
- Plots can be relocated due to land-use changes, access issues, or plot destruction; each location has a unique repeat identifier (e.g., 2RPT1).
- Sample locations within a square are approximately 2–3 meters apart around a permanently marked 2m x 2m plot.

## Sampling Methods
- Soil cores are collected from the top 15 cm (8 cm for invertebrates). In 1998/2007 cores were used; 1978 used a soil pit.
- When full cores could not be collected (stones, shallow soils), exceptions occurred.
- Core photographs and measurements of core dimensions were recorded in 2007 for selected cores.

## Measurements and Laboratory Analysis
- 1978 measurements focused on pH and loss-on-ignition (LOI); later years included more variables.
- In CS1990, some soil mapping occurred; in 1998 and 2007 multiple cores per x-plot were taken, with different cores having different measurements (see Table 1).
- Chemical analyses by horizon were not performed; samples were homogenised before pH and LOI measurements.
- Bulk density was measured in 2007 (not by ISO standard methods due to resource considerations).
- A broad set of properties has been measured across samples (examples include pH, LOI, %C, %N, bulk density, depth of organic layer, moisture, Olsen P, metals, texture, mineralisable N, etc.), with the exact measurements varying by core and year. Some data were released only after the Soils Report published in November 2009.

## Data Structure, Availability and Documentation
- Data are distributed across different years and sample types; not all measurements were taken on all cores or all x-plots.
- The CS dataset emphasizes comprehensive metadata and cross-year comparability, but users should consult CEH and related publications to understand context and prior analyses.
- The Soils Report (November 2009) contains detailed methods and data release notes that accompany the dataset.

## Statistical Analysis Guidance
- Analyses should consider land-class structure; ignoring it can bias results toward stock and change rather than national estimates.
- Bootstrapping is not consistently used; a mixed-model approach is recommended, with square treated as a random factor to account for multiple x-plots within each square.
- In design-based contexts where spatial structure is not central, dispersed sampling can improve regional precision and coverage.
- Users are advised to consult CEH prior to analysis and to review existing CS publications for context and appropriate methodologies.

## Data Governance and Utilisation Implications for Data Leaders
- Ensure rigorous metadata standards: unique identifiers (e.g., 2RPTx), sampling depth, core dimensions, measurement methods, and per-year measurement coverage.
- Manage data versioning and release timelines (noting that some data were released only after 2009 report).
- Align data analyses with the intended use (national stock/change estimates vs. local/application-specific insights) by incorporating land-class structure and appropriate statistical models.
- Maintain awareness of data limitations due to non-replicate plots, plot relocations, and variable measurement sets across years.

## Key Challenges Highlighted
- Tracking user needs and ensuring data products serve diverse audiences across years.
- Achieving a comprehensive overview of available data due to fragmentation and varying measurement sets.
- Dealing with gaps in data, especially for certain properties or years.
- Navigating barriers to data access and ensuring robust data standards and metadata to enable reuse.
- Coordinating across the sector to avoid duplicated effort and to foster stronger data-sharing communities.

## References
- Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.