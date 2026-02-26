# Amplitude maps of annual vegetation phenology derived from MODIS NDVI and EVI in Meso- and South America

- Purpose
  - Map the average amplitude (maximum minus minimum) of annual greenness cycles to indicate the degree of synchrony in leaf phenology across plant individuals and species within each pixel.
  - Help interpret areas with weak or varying annual greenness signals, which may reflect diverse phenology timing or constant canopy with mixed-age leaves.
  - Support environmental monitoring and policy planning by providing a robust, data-driven phenology metric.

- Data sources
  - MODIS NDVI and EVI time series (MOD13A1, 16-day composites) from 2000–2013 (13-year window)
  - Spatial resolutions: 500 m and 1000 m
  - Coverage: Mesoamerica and South America
  - Data provenance: USGS/NASA MODIS products; data retrieved via NASA LP DAAC

- Methodology
  - Data quality screening per pixel: exclude values flagged as poor quality, NDVI/EVI < 0.01, and outliers beyond ±3 standard deviations
  - Inclusion criteria: at least 100 observations (out of 320 possible) with at least one observation per month
  - Spectral analysis: Lomb-Scargle periodogram to detect annual cycles in irregularly spaced data
  - Pre-processing: linear detrending; split cosine taper on first and last 5% of the series to reduce spectral leakage
  - Smoothing: apply a three-point Hanning window to the periodogram
  - Detection criterion: an annual cycle is considered significant if the spectral peak exceeds 95% confidence
  - Output: per-pixel average amplitude (max – min) derived from the power spectral estimates

- Outputs and interpretation
  - Spatial maps of average amplitude of annual greenness cycles
  - Legend includes significance thresholds and data quality indicators
  - Amplitude values serve as a robust indicator of phenological strength and synchronization across the landscape

- Validation and evaluation
  - Comparisons with independent IGBP land cover map (class-based histograms of amplitude values)
  - Cross-checks with in situ observations describing canopy leaf life cycles, LAI, leaf flushing/falling, and litter fall

- Regional characteristics and data specifics
  - Projection: Sinusoidal coordinates specified for the region
  - Data quality considerations: quality flags, outlier handling, and monthly observation requirements
  - Dataset lineage: derived from MODIS MOD13A1 inputs and compared against established land cover datasets and field observations

- Implications for monitoring frameworks
  - Provides a transparent, repeatable metric for tracking vegetation phenology changes over time
  - Facilitates monitoring of ecosystem health, climate-vegetation interactions, and potential impacts on biodiversity and carbon dynamics
  - Can inform policy decisions related to land management, agriculture, and climate adaptation through spatially explicit phenology insights

- Acknowledgments and data access
  - MODIS MOD13A1 product accessed via NASA LP DAAC
  - Recognizes NASA EROS/LP DAAC and USGS data providers
  - Cites related land cover datasets and methodological references linked in the study