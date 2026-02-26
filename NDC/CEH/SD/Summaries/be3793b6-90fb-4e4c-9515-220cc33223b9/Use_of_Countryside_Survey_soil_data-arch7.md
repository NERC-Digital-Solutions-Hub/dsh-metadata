# Sampling design

- The Countryside Survey soils dataset covers sampling years 1978, 1998, and 2007. In 1978 and 1998, the same 256 CS squares were sampled; in 2007, soils were collected from all 591 CS squares, with not all measurements made on every sample. Power analyses were used to determine the number of samples needed to detect significant change (refer to Emmett et al. 2008).

## Spatial sampling framework

- Soils are sampled from CS x-plots, with 5 x-plots randomly spaced within each CS square.
- The 5 x-plots within a square are not replicates; they may be in different land uses or soil types.
- Over time, x-plots may be relocated due to land-use changes, access issues, or location certainty. Each sampling location has a unique repeat identifier (e.g., 2RPT1) referring to square 2, repeat plot 1.
- Measurements for the same unique identifier come from the same location, though exact sampling points are typically about 2–3 meters apart, positioned within a permanently marked 2m x 2m plot in each sampling location.
- In 1998/2007, sampling includes all 591 squares; in 1978/1990-era data, the number of samples/squares differs as described in the methods.

## Sampling methodology

- Depth of sampling: top 15 cm of soil (8 cm for invertebrate samples).
- 1998/2007: soil cores hammered into the soil and pulled out; 1978: soil pit used to sample top 15 cm.
- Some soils prevented full core collection due to stones or shallow soils.
- In 2007, core photographs and detailed core dimension measurements were made for two of the four cores (black cores and N mineralization cores).

## Measurements and data

- Laboratory measurements by year:
  - 1978: pH and loss-on-ignition (LOI).
  - 1990: some soil mapping; partial dataset.
  - 1998/2007: multiple cores per x-plot; different cores have different measurements (Table 1). Samples are homogenised before pH and LOI measurements; chemical analyses by horizon are not performed.
  - 2007: bulk density measured (not via ISO core method); core dimensions, photographs, and a broad set of measurements collected (e.g., %C, %N, pH, metals, Olsen P, moisture, texture, etc.).
- Measurements are listed per table in the dataset (Table 1), with measurements made and the number of samples aligned to either all 591 squares or the original 256 squares.
- Some measurements are limited to subsets:
  - e.g., measurements labeled for "Original 256 squares" or "2 of the 5 x-plots in each of the original 256 squares" for specific variables.
- Note: Some data were released only after the Soils Report published in November 2009.

## Statistical analysis considerations for GIS

- Analyses should account for data structure and land class effects:
  - If land classes are ignored, results reflect stock/change of the population.
  - If land classes are accounted for, results are weighted by land classes and provide national estimates of stock/change.
- Bootstrapping is not always used; dataset structure should be considered.
- The CS design is often not focused on spatial structure; a dispersed sampling approach (across many locations) can improve regional precision and coverage.
- A mixed-effects model with square as a random factor is recommended to account for multiple x-plots within each CS square.
- Where possible, users should consult CEH before analysis and interpretation and review prior publications using CS soils data (linked on the CS website).

## Data availability notes

- Some measurements are released only after the 2009 Soils Report.
- The 2007 dataset includes measurements across all 591 squares, with varying coverage by measurement type (e.g., pH, LOI, %C, %N, bulk density, etc.).

## References

- Emmett, BA et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.