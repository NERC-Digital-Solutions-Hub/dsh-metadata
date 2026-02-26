# Countryside Survey Soils 2007: Method development, power analyses and protocols

## Overview
- Documents the sampling design, field methods, measurements, and statistical considerations used in Countryside Survey (CS) soils across multiple years (1978, 1998, 2007) and during the rolling survey initiated in 2019.
- Describes the progression from fixed-square sampling to a rolling target of ~100 squares per year for five years before repetition.
- Emphasizes power analyses used to determine sample numbers and the need for appropriate statistical approaches to detect significant change.

## Sampling design and plot structure
- Soils are sampled within CS X-plots, with five X-plots randomly spaced inside each CS square.
- X-plots within a square are not replicates; they may represent very different land uses or soil types.
- Over time, X-plots can be relocated due to destruction, access denial, or uncertainty about original locations; each location has a unique repeat identifier (e.g., 2RPT1).
- While the exact sampling location shifts slightly (approximately 2–3 m), samples with the same identifier come from the same location in principle.

## Sample collection and depth
- Sampling depth: top 15 cm of soil (8 cm for invertebrate samples); 1978 used 15 cm pits, later years used core methods.
- Methods: 1998, 2007, and rolling survey used a soil core hammered into the ground and extracted; 1978 used a soil pit approach.
- Practicalities: some soils hinder full 15-cm cores due to stones or shallow depth; core photographs and measurements of core dimensions were taken in 2007 for selected cores.

## Measurements and laboratory analyses
- 1978: laboratory measurements limited to pH and loss-on-ignition (LOI).
- 1990: some soil mapping activities; multiple cores per X-plot across years with varying measurements.
- No horizon-specific chemical analyses reported; samples are homogenised before pH and LOI measurements.
- Bulk density: measured in 2007 and in the 2018/19–2023 rolling survey, but not by ISO bulk density methods (would require whole-core sampling).
- A full description and implications of methods are documented in Emmett et al. 2008.

## Data handling and analysis guidance
- Analytical approach should account for CS structure; failing to consider land class structure yields stock-and-change estimates rather than targeted national estimates.
- Bootstrapping is not consistently used across analyses; users should consider the CS design in their statistical approach.
- Recommended analysis framework: use a mixed-effects model with square as a random factor to accommodate multiple X-plots per CS square.
- Design-based approaches (with dispersed sampling) can improve overall precision and regional coverage, especially when spatial structure is not a primary interest.
- Users are advised to consult UKCEH prior to analysis and interpretation and to refer to CS publications listed on the CS website for prior analyses.

## Data governance, sharing, and guidance for users
- The document references comprehensive methods and prior publications (Emmett et al. 2008) and emphasizes consistency with established protocols.
- While explicit data-sharing requirements are not detailed in the excerpt, the emphasis on public dissemination of methods and adherence to data quality standards implies alignment with broader data governance and openness practices.
- For detailed methodology and site-specific considerations, users should consult the CS website and contact UKCEH as needed.

## Key takeaways for monitoring framework authors
- A rolling, statistically informed sampling design with well-documented plots (including non-replicate X-plots) can efficiently track change over time.
- Explicit handling of repeated locations and potential relocations is essential for longitudinal integrity.
- Depth, core-based sampling, and laboratory measurement choices must balance practicality with the need for consistent, comparable data across years.
- Statistical analyses should incorporate the hierarchical structure (X-plots within squares) and consider land-class effects to produce meaningful national or regional estimates.
- Documentation, metadata, and adherence to established protocols (with reference materials like Emmett et al. 2008) are critical for data quality, reusability, and governance.