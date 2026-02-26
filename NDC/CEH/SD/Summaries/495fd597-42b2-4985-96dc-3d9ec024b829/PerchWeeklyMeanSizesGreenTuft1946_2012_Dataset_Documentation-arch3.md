# Perch weekly mean sizes from Green Tuft 19462012

## Overview
- A dataset of weekly mean sizes of Perch (Perca fluviatilis) from trapping at Green Tuft, Windermere, Cumbria, sampled 1946–2012.
- Originally collected by the Freshwater Biological Association (FBA); data have been maintained by the Centre for Ecology & Hydrology (CEH) and its predecessor IFE since 1989.
- Related to broader work on perch phenology and population response (cited in Ohlberger et al. 2014).

## Dataset details
- File: PerchWeeklyMeanSizesGreenTuft1946_2012.csv
- Size: 10 kB
- Format: CSV
- Columns:
  - Year: year of catch
  - Week: week of year
  - Mean_size: mean size (cm) of mature perch caught
  - QA_code: 'NS' = week not sampled; 'ID' = week with insufficient data
- Sampling site: Green Tuft, Windermere lake, Cumbria (OS Grid NY374019 / OSGB36 Easting 337402, Northing 501968)

## Sampling design and methods
- Long-running monitoring in Windermere’s north basin (with variations in sampling sites/effort since 1943).
- Collected at Green Tuft using unbaited, wire-netting traps (dimensions approx. 740 × 590 × 640 mm; 12 mm mesh; opening 80 mm).
- Trap deployment: six sets per spawning season, typically 5 traps per gang, deployed 2–7 m deep, during daylight; retrieved about 7 days later.
- Processing: all perch counted, measured (total length to 1 mm), weighed (to 1 g), and sex/reproductive state determined.
- Outcome: weekly mean size of mature perch computed for each sampling week.

## Data structure and quality control
- Measurements taken from the entire catch; sub-sampling by length class only when numbers were large.
- Quality control uses permutations of three individuals to check measurements.
- Data are tied to a historic time series with some weeks not sampled or with insufficient data, as indicated by QA_code.

## provenance and related datasets
- This dataset is one of several related datasets (e.g., Perch weekly catches Green Tuft 1946-2012; Windermere monthly temperatures 1946-2012) archived in the NERC Environmental Information Data Centre.
- Related literature:
  - Paxton et al. 2004 (biotic and abiotic influences on perch recruitment in Windermere)
  - Ohlberger et al. 2014 (uses the dataset within broader analyses)

## Relevance for monitoring frameworks
- Demonstrates long-term, site-specific biological monitoring data useful for assessing population structure and phenology over decades.
- Highlights governance considerations for environmental data: data provenance, metadata, data sharing, and QA processes.
- Illustrates challenges common to monitoring data: changing sampling sites/effort, incomplete weeks (NS/ID), and the need for clear data codes to indicate sampling status.
- Provides a concrete example of the type of data that can inform policy decisions, trend analyses, and future monitoring design.

## References
- Winfield, I. J., Fletcher, J. M. & James, J. B. (2014). Perch weekly mean sizes from Green Tuft 1946-2012.
- Winfield, I. J., Fletcher, J. M. & James, J. B. (2014). Perch weekly catches Green Tuft 1946-2012. NERC Environmental Information Data Centre.
- Ohlberger, J. et al. (2014). When phenology matters: Age-size truncation alters population response to trophic mismatch. Proceedings of the Royal Society B.
- Paxton, C. G. M. et al. (2004). Biotic and abiotic influences on the recruitment of perch in Windermere. Journal of Fish Biology.