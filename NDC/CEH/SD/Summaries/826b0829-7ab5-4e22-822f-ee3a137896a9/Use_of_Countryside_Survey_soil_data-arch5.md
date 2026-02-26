# Sampling design

## Overview
- Long-running soil monitoring component of the Countryside Survey (CS) with measurement campaigns in 1978, 1998, and 2007.
- 1978 and 1998 used the same 256 CS squares; 2007 expanded to all 591 CS squares.
- Power analyses were performed to determine the number of samples needed to detect significant change (Emmett et al. 2008).
- Data collection supports assessment of soil properties and change over time; data are intended for national-scale stock and change estimates and require careful statistical handling.

## Sampling design and scope
- Multiple sampling campaigns span 1978, 1998, and 2007 with evolving scope (256 vs 591 squares).
- Each CS square contains five randomly spaced x-plots; x-plots within a square are not replicates due to differences in land use and soil type.
- Locations may be relocated over time due to land use change, permission, or access issues; each location has a unique repeat identifier (e.g., 2RPT1) linking to a known square and repeat plot.
- Sampling locations are typically within a 2m x 2m permanently marked plot; exact sampling points may shift by 2–3 meters around the plot corners.

## Sampling methods and depth
- Soils sampled from the top 15 cm (8 cm depth for invertebrate samples); 1998/2007 used soil cores hammered into the ground; 1978 used soil pits to collect from the top 15 cm.
- In some cases, full cores could not be collected due to stones or shallow soils.
- Core photographs and measurements of core dimensions were taken in 2007 for select cores (black cores and N mineralization cores).

## Measurements and data structure
- 1978: laboratory measurements limited to pH and loss-on-ignition (LOI).
- 1990s–2007: multiple cores per x-plot with different measurements per core (Table 1); no chemical analyses by soil horizon; samples homogenised prior to pH and LOI.
- 2007: additional measurements included bulk density (not via ISO whole-core method), core dimensions, photographs, depth of organic layer, hand texture, soil moisture, Olsen P, metals, mineralisable N, and other variables.
- Data coverage varies: some measurements apply to all 591 squares; others limited to original 256 squares or specific x-plots.
- Data release caveat: some measurements are released only after the Soils Report published in November 2009.

## Data governance, provenance, and metadata
- Data are gathered across multiple years with evolving measurement protocols; important to document method changes, cores per x-plot, and depths to ensure comparability.
- Unique identifiers (square number, repeat plot, and within-square plotting) are essential for traceability across years.
- The CS project provides methodological references (Emmett et al. 2008) detailing protocol development, power analyses, and data collection procedures; data users are advised to consult CEH prior to analysis and review existing publications.
- Some data are embargoed or released progressively (notably after 2009), affecting data availability and use in early analyses.

## Statistical analysis considerations for data stewards
- Analyses should account for land class structure; failure to do so can bias estimates toward the population stock and change rather than national estimates.
- When land classes are included, analyses yield weighted national estimates of stock and change.
- Bootstrapping is not consistently used; recommended practice is to use mixed models with square as a random factor to account for multiple x-plots within each CS square.
- The CS design emphasizes spatial dispersion for regional estimates; design-based approaches with dispersed sampling can improve precision and coverage.
- Users should verify sample depth, core selection, and measurement methods across years; consider consulting CEH and review prior CS publications for context and methods.

## Practical takeaways for data custodians
- Maintain stable, well-documented repeat identifiers to enable cross-year linkage (e.g., 2RPT1).
- Preserve detailed metadata about sampling depth, core type, measurement methods, and any deviations (e.g., pits vs cores, incomplete cores).
- Clearly indicate which measurements are available for which squares/plots and the years they apply to.
- Document data release status and embargoes, and provide data access pathways consistent with project policies.
- Provide guidance on appropriate statistical models and analysis cautions to end users, including potential need for mixed models and consideration of land class structure.