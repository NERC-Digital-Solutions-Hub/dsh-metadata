# Sampling design

## Overview
- Soils were sampled in the Countryside Survey (CS) in 1978, 1998, and 2007.
- 256 squares sampled in 1978 and 1998; 591 CS squares sampled in 2007, with all measurements not necessarily available for every sample.
- Power analyses were conducted to determine the number of samples needed to detect significant change (Emmett et al. 2008).

## Sampling design and location
- Sampling units are CS x-plots; each CS square contains five x-plots randomly spaced.
- X-plots within a square are not replicates due to differing land uses, soils, etc.
- Plots may be relocated over time due to land changes or access issues; each location has a unique repeat identifier (e.g., 2RPT1) referring to square 2, repeat plot 1.
- Samples from the same unique identifier come from the same location, though exact sampling points are ~2–3 m apart around a permanently marked 2 m × 2 m plot.

## Sampling methodology
- Soils sampled from the top 15 cm (8 cm for invertebrate samples).
- 1998 and 2007 used a soil core inserted and withdrawn; 1978 used a soil pit to sample the top 15 cm.
- Some instances prevented full core collection due to stones or shallow soils.
- In 2007, core photographs and measurements of core dimensions were taken for 2 of the 4 cores.

## Measurements and laboratory analyses
- 1978: laboratory measurements limited to pH and loss-on-ignition (LOI).
- 1990: some soil mapping conducted.
- 1998 and 2007: multiple cores per x-plot; different cores carry different measurements (see Table 1).
- No chemical analyses by soil horizon; samples homogenised before pH and LOI.
- Bulk density measured in 2007 but not via ISO bulk density methods.
- A full description and implications of methods are provided in Emmett et al. (2008).

## Data structure and measurements (Table 1)
- Measurements include LOI, pH (in water and CaCl2), %C, %N, bulk density, core dimensions, photographs, depth of organic layer, hand texture, soil moisture, Olsen P, metals, mineralisable N, among others.
- The number of samples varies by measurement and year:
  - Some measurements cover all 591 squares (e.g., pH, LOI, core measurements).
  - Others cover only original 256 squares or a subset of x-plots per square.
  - Certain measurements were restricted to specific core types (e.g., 2 of 5 x-plots in original 256 squares).
- Some data were released only after the Soils Report published in November 2009.

## Statistical analysis considerations
- Analyses should account for land class structure; ignoring it yields stock/change of the population rather than regional estimates.
- When land classes are weighted, results become national estimates of stock and change.
- Bootstrapping is not consistently used; a mixed-model approach with square as a random factor is recommended to account for multiple x-plots within each square.
- CS uses a dispersion-based design; broad, widespread sampling increases precision and regional coverage.
- Users are advised to consult CEH before analysis and to review published CS analyses accessible via the CS website.

## Data availability and access considerations
- Some measurements are limited to subset of samples; data coverage varies by year and core type.
- Certain data are restricted and released only after publication (noted with asterisk in Table 1).
- Documentation and methods are described in Emmett et al. (2008); additional publications exploiting CS soils data are listed on the CS website.

## Data governance implications for Data Stewards
- Ensure robust metadata capturing sampling year, plot identifiers (e.g., 2RPT1), sampling depth, core type, and measurement types.
- Track data lineage across years (1978 pit vs. 1998/2007 cores) and note changes in measurement protocols (e.g., pH methods, LOI, bulk density methods).
- Manage data release constraints and ensure access controls reflect publication-based restrictions.
- Maintain links between measurements and corresponding core samples, x-plots, and squares to enable reproducible analysis and proper cross-year harmonization.
- Document data quality considerations arising from plot relocations, varying measurement sets, and non-uniform sampling coverage.

## References
- Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA.