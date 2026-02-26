# Sampling design

## Overview
- Longitudinal soil sampling across four campaigns: 1978, 1998, 2007, and 2019.
- Consistent sampling of 256 CS squares in 1978 and 1998; all 591 CS squares sampled in 2007 with selective measurements; 2019 introduces a rolling survey targeting ~100 squares per year for five years before repetition.
- Power analyses conducted to determine the number of samples needed to detect significant change (Emmett et al. 2008).

## Sample locations and plots
- Soils are sampled from CS x-plots, with 5 x-plots randomly spaced within each CS square.
- X-plots within a square are not replicates due to land-use and soil-type differences.
- Some plots are relocated over time due to destruction, access permissions, or uncertainty in original location.
- Each sampling location has a unique repeat identifier (e.g., 2RPT1) referring to a square and a repeat plot; samples from the same identifier come from the same location.
- Within each square, sampling occurs near the corners of a permanently marked 2m x 2m plot (4 corners).

## Sampling units and depth
- Soil samples are taken from the top 15 cm of the profile (8 cm for invertebrate samples).
- In 1998, 2007, and 2019, cores are hammered into the soil and extracted; 1978 used a soil pit.
- When full core collection is not possible (stones or shallow soils), adjustments are made.
- Core locations sometimes include additional measurements or photographs (e.g., core dimension details in 2007; black cores and N mineralization cores).

## Measurements and laboratory analyses
- 1978: only pH and loss-on-ignition (LOI).
- 1990: some soil mapping activity.
- 1998, 2007, 2019: multiple cores per x-plot with different measurements per core; samples are homogenised before pH and LOI analyses.
- Bulk density measured in 2007 and 2019 (not using ISO whole-core method).
- Core photographs and measurements (e.g., 2007) provide additional context for core dimensions and methods.
- Not all chemical analyses are performed by horizon; emphasis on aggregate measurements from homogenised samples.

## Data structure and identifiers
- Data are organized around CS squares, x-plots, and repeat identifiers, enabling longitudinal and spatial tracking.
- Unique repeat identifiers track same locations across years, with occasional relocations noted.

## Analytical considerations for GIS
- Statistical approaches must account for land class structure to avoid biased estimates; analyses ignoring land classes yield population stock/change, while weighting by land classes yields national estimates.
- Bootstrapping is not consistently used; a mixed-model approach with square as a random factor is recommended to account for up to 5 x-plots per CS square.
- CS design emphasizes dispersed sampling for regional precision rather than detailed spatial autocorrelation; suitable for broad regional estimates rather than fine-scale spatial structure.
- Users should consult CEH prior to analysis and review CS-specific publications for context and methodology.

## Data quality, standards, and limitations
- Data are distributed across multiple locations and datasets, with varying depths, measurements, and methods by year.
- Differences in data standards and measurement practices require careful data cleaning and harmonisation for cross-year analyses.
- The 2007 report provides full methodological details and discusses implications of non-ISO bulk density methods.

## Reference
- Emmett, BA et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA.