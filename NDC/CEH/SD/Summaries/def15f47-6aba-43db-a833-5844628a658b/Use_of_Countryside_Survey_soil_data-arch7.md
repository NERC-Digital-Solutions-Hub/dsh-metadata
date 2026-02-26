# Sampling design

## Overview
- Soils in CS were sampled in 1978, 1998 and 2007.
- 256 squares were sampled in 1978 and 1998; in 2007, soils were collected from all 591 CS squares, though not every measurement was made on every sample.
- Power analyses were conducted to determine the number of samples needed to detect significant change (Emmett et al. 2008).

## Sampling framework and spatial structure
- Soils are sampled from CS x-plots; each CS square contains 5 randomly spaced x-plots.
- The x-plots within a square are not replicates (they may vary by land use, soil type, etc.).
- Plots can be relocated over time due to land changes or access issues; each location has a unique repeat identifier (e.g., 2RPT1).
- Samples with the same repeat identifier come from the same location, though exact sampling positions are ~2–3 m apart around a permanently marked 2 m × 2 m plot.
- For 2007, all 591 squares were sampled; however, not all measurements were made on all samples.

## Sample locations and repeats
- The CS x-plots are the primary sampling units within each CS square.
- Relocation occurs when original plots are destroyed or access is denied; repeat plots maintain the same identifier.
- Sample locations aim to cover diverse land uses and soil types within each square.

## Sampling methods and depth
- Depths: top 15 cm sampled in 1998 and 2007 (8 cm depth for invertebrate samples); in 1978 a soil pit was dug and the top 15 cm sampled in the pit side.
- Sampling tools: cores hammered into soil and pulled out; full cores may be impractical due to stones or shallow soils.
- In 2007, core photographs and measurements of core dimensions were recorded for 2 of the 4 cores.

## Measurements and laboratory analyses
- 1978: measurements limited to pH and LOI (loss-on-ignition).
- 1998 and 2007: multiple cores per x-plot, with different measurements per core (Table 1).
- Samples are homogenised before pH and LOI measurements.
- Bulk density measured in 2007 (not by ISO bulk density method).
- Laboratory notes and a full methods description available (Emmett et al. 2008).

## Data structure and availability
- Table 1 lists measurements across cores; measurements include pH (in water & CaCl2), LOI, %C, %N, bulk density, core dimensions, photographs, depth of organic layer, hand texture, soil moisture, Olsen P, metals, mineralisable N, etc.
- Some data are released only after the Soils Report published in November 2009 (denoted by * in the table).
- For 2007, 591 squares were targeted; however, several measurements are available only for a subset of x-plots (e.g., metals measured on 2 of the 5 x-plots in each original 256 squares).

## Statistical analysis considerations
- Analyses should account for land class structure; ignoring land classes yields population stock/change estimates rather than land-class-weighted national estimates.
- Bootstrapping is not consistently applied across analyses.
- Recommended approach: use a mixed model with square as a random factor to account for multiple x-plots per square (up to 5).
- Design-based approaches: when spatial structure is not of interest, a dispersed sampling design can improve regional precision and coverage.
- Users are advised to consult CEH before analysis and to review relevant CS publications available on the CS website.

## Implications for GIS and data integration
- Spatial linkage relies on unique repeat identifiers and precise, though occasionally relocated, sampling locations.
- Data from 1978–2007 vary by depth, core type, and measured variables; not all measurements are available for all samples, requiring careful metadata handling.
- Some measurements become available only after publication of the Soils Report (2009), affecting historical GIS analyses and time-series consistency.
- The dataset supports mapping of soil properties across time and space, with attention to square-level random effects and land-class weighting in spatial analyses.

## References
- Emmett, BA, ZL Frogbrook, PM Chamberlain, R Griffiths, R Pickup, B Reynolds, E Rowe, P Rowland, D Spurgeon, J Wilson, CM Wood. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.