# Historic Gridded Standardised Precipitation Index for the United Kingdom 1862-2015 (generated using gamma distribution with standard period 1961-2010)

## Overview
- 5 km gridded Standardised Precipitation Index (SPI) dataset for the United Kingdom, covering 1862–2015.
- SPI is a drought index based on the probability of precipitation for specified accumulation periods: 1, 3, 6, 12, 18, and 24 months.
- Each accumulation period is calculated for all twelve calendar months; data are stored as normal scores (mean 0, standard deviation 1) with no units.
- The gamma distribution (fitted with L-moments) is used to derive the SPI; values outside -5 to 5 are truncated.
- Data are provided in NetCDF4 format on the British National Grid.

## Motivation and Applications
- Developed within the Historic Droughts project to enhance cross-disciplinary understanding of past UK droughts and to improve tools for managing droughts in the future.
- SPI supports drought monitoring and the assessment of drought rarity at multiple timescales, as well as identifying periods of anomalously wet conditions.
- Enables spatial analysis of drought propagation, identification of severely affected areas, and multi-timescale assessments relevant to water resources, agriculture, and climate resilience.

## Data Sources
- Met Office 5 km monthly rainfall gridded data.
- Composition includes: UKCP09 data (1910–2011), unpublished 2012–2015 updates, and rescued data for 1862–1909 (Historic Droughts project data recovery).

## Methodology
- SPI calculation follows McKee et al. (1993): for each location and accumulation period, the cumulative precipitation is modeled with a gamma distribution (parameters estimated by L-moments).
- The precipitation series ending in each calendar month is used to assign the SPI value to that month.
- The Sci (R) package SCI is used (modified to apply L-moments estimator).
- Data are transformed to a standard normal distribution (normal scores) with mean 0 and sd 1.
- Extreme values are truncated at ±5 to mitigate issues with distribution tails.
- Acknowledges that gamma distribution may not always be the most adequate for UK data (references to alternative distributions like Pearson Type 3 or Tweedie); current dataset uses gamma, with potential future updates.

## Data Format and Structure
- Stored in NetCDF4 format, following CEH gridded dataset conventions.
- Structure: two-dimensional UK grids with twelve monthly grids per year; one yearly file per accumulation period.
- Projection: British National Grid.
- SPI values are normal scores (no units), with a typical range approximately within -2 to +2, though the dataset allows -5 to +5 due to truncation.

## Temporal Coverage and Standard Period
- Coverage: 1862–2015.
- The standard period used to fit the gamma distribution: 1961–2010.

## Limitations and Considerations for Monitoring Frameworks
- Serial correlation and autocorrelation: especially for accumulation periods longer than 12 months due to overlapping data; affects trend analyses and independent significance testing.
- Overlapping data across years for longer accumulation periods can introduce autocorrelation in time series; interpret trend/peak analyses with appropriate statistical adjustments.
- The gamma distribution assumption, while widely used, may not always be optimal for UK precipitation; future versions could explore alternative distributions if justified.
- Data management considerations: metadata completeness, data provenance, and the need to share underlying data transparently, in line with monitoring governance and open-data principles.

## Acknowledgments and References
- Projects: DrIVER (NE/L010038/1), Historic Droughts (NE/L01016X/1), IMPETUS (NE/L010267/1).
- Funding and collaboration: Natural Environment Research Council (NERC) and associated Belmont Forum initiatives.
- Key references include Barker et al. (2015), Gudmundsson & Stagge (2014), Hayes et al. (2011), Keller et al. (2015), McKee et al. (1993), National Drought Mitigation Center (2015), Stagge et al. (2015), Svensson et al. (2017), and Tanguy et al. (2015, 2014).