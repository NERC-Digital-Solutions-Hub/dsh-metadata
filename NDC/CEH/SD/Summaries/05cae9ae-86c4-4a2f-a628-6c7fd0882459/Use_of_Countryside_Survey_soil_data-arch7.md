# Countryside Survey Soils 2007: Method development, power analyses and protocols

- Purpose: Describe how soils were sampled, measured, and analyzed across CS years to support map-based data products and spatial analyses.
- Timeframe and scope: Sampling conducted in 1978, 1998, and 2007; emphasis on design, power analyses, and protocols for soils data collection and analysis (Emmett et al. 2008).

## Sampling design
- Years and samples:
  - 1978 and 1998: same 256 CS squares sampled.
  - 2007: soils sampled from all 591 CS squares; not all measurements were made on all samples.
- Power analyses: Performed to determine the number of samples needed to detect significant change (refer to Emmett et al. 2008).
- Data completeness: Some measurements are available for all 591 squares, others only for subsets (e.g., original 256 squares).

## Sample location and x-plots
- Sampling locations: Soils sampled from CS x-plots within each CS square.
- x-plots: Five x-plots per CS square, randomly spaced; x-plots within a square are not replicates due to land-use and soil-type differences.
- Relocation: x-plots may be relocated over time due to land-use changes, access permissions, or locating certainty issues.
- Repeat identifiers: Each location has a unique repeat ID (e.g., 2RPT1). Samples with the same ID come from the same location, though precise sampling positions shift ~2–3 m within the permanently marked 2 m × 2 m plot at each sampling occasion.

## Sampling method
- Depth and cores:
  - Top 15 cm sampled in most years (8 cm for the invertebrate sample).
  - 1998 and 2007 used soil cores hammered into the soil; 1978 used a soil pit with sampling from the top 15 cm.
- Practical constraints: Full cores may be blocked by stones or shallow soils; some cores not fully collected.
- Ancillary data: In 2007, core photographs and detailed core dimension measurements were taken for 2 of the 4 cores sampled.

## Measurements and data collected
- 1978: pH and loss-on-ignition (LOI).
- 1990: some soil mapping activities.
- 1998 and 2007: multiple cores per x-plot; different cores have different measurements (varies by core).
- Lab practices: No chemical analyses by soil horizon; samples homogenised before pH and LOI.
- Bulk density: Measured in 2007 (not using ISO bulk density method).
- Data presentation: A CS Soils Table (Table 1) lists measurements across cores (e.g., pH, LOI, %C, %N, bulk density, core dimensions, photographs, depth of organic layer, texture proxies, moisture, Olsen P, metals, mineralisable N).
- Coverage notes: 
  - Measurements labeled as “All 591 squares” or “Original 256 squares” indicate the spatial extent available for that measurement.
  - Some measurements are available for only a subset of x-plots within original 256 squares (e.g., 2 of the 5 x-plots).

## Data structure and coverage
- Spatial structure: Data organized around CS squares and their constituent x-plots; multiple cores per x-plot.
- Resolution and scope:
  - Broad spatial coverage across 591 squares (2007) with varying measurement availability.
  - Datasets include multi-core data per location and a mix of core-based measurements and site-level observations.
- Data availability: Certain data released only after the Soils Report published in November 2009.

## Data analysis considerations
- Accounting for land class: Analyses should consider land class structure to avoid biased estimates; weighting by land class may yield national stock/change estimates.
- Statistical approaches: Mixed models with square as a random factor to account for multiple x-plots per square; design-based approaches emphasize dispersed sampling for regional estimates.
- Bootstrapping: Not always used in CS soils analyses.
- Guidance: Users are advised to consult CEH prior to analysis and interpretation and to review published CS data using the CS website.

## Practical notes for GIS and data users
- Data relationships: Spatial linkage is via square and x-plot identifiers and repeat location IDs (e.g., 2RPT1); exact sample positions vary within a fixed plot.
- Data integration: Some variables are available across all squares, while others are restricted to the original 256 squares, affecting GIS analyses that require uniform data coverage.
- Documentation: Detailed method development, power analyses, and protocols are documented in Emmett et al. 2008 for users requiring reproducibility and methodological justification.