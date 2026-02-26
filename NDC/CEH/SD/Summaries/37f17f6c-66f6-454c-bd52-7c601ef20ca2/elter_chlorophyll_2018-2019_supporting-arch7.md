# Elter_chlorophyll_2018-2019.txt

## Overview
- Weekly to monthly vertical profiles of chlorophyll a collected May 2018 – December 2019.
- Sampling at the deepest point of Elterwater inner basin (Lat: 54.4287°, Long: -3.0350°).
- Data provide depth-specific chlorophyll a concentrations for time-series analysis.

## Sampling and Data Collection
- Water samples (500 mL) collected at depths: 0.5, 1, 2, 3, 4, 5, and 6 m.
- Frequency: weekly to monthly from May 2018 to December 2019.
- Sample processing: filtered immediately on a 5.5 cm GF/C filter, filter papers frozen, analyses performed within a month using a method based on Talling (1974).
- Chlorophyll a extraction: heated methanol extraction; spectrophotometric measurement.
- Wavelengths: 750 nm (background turbidity) and 665 nm (chlorophyll a maximum).
- Concentration calculation: Chlorophyll a concentration = (13.9 × A_corr665 × 1/d) × v/V
  - A_corr665 = corrected absorbance at 665 nm (A_corr665) minus A_corr750
  - d = cuvette pathlength in cm
  - V = volume of sample filtered (ml)
  - v = volume of extract (ml)

## Data Structure
- Date (yyyy-mm-dd)
- Depth (m)
- Concentration (μg L^-1)

## Spatial and Temporal Context
- Single sampling location: deepest point in Elterwater inner basin.
- Coordinates provided; data span May 2018 to December 2019.

## GIS Relevance and Potential Uses
- Can be incorporated into GIS as a time-series, depth-dimensional dataset for 3D visualization of chlorophyll distribution.
- Enables creation of vertical chlorophyll profiles, depth-resolved choropleth or heat maps over time.
- Suitable for integration with other hydrological or limnological layers (e.g., temperature, nutrients, bathymetry).

## Data Quality and Considerations
- Temporal resolution varies (weekly to monthly).
- Limited to a single site; spatial coverage is not broad.
- Methodology is standardized; consistent calibration is important when comparing with other datasets.