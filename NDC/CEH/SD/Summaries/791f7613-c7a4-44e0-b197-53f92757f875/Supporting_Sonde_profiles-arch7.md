# BLEL_Sonde_profiles.csv

## Overview
- Describes profiles of multiple water quality parameters collected with a YSI EXO2 sonde at Blelham Tarn.
- Parameters include Chlorophyll a (phytoplankton biomass indicator), Phycocyanin (cyanobacteria indicator), temperature, conductivity, specific conductivity, oxygen (% saturation and mg/L), and pH.
- Profiles recorded at 0.5 m depth intervals in the water column at the lake’s deepest point (monitoring buoy).
- Data collected weekly during the stratified period (May/June–November) and at fortnightly or monthly intervals outside of this period in 2016 and 2017.
- Chlorophyll a (µg/L) from fluorescence compared to chemically determined measurements with a reported R² = 0.56 (p < 0.05).

## Location and sampling design
- Site: Blelham Tarn, Lake District, North West England.
- Monitoring buoy located at the deepest point of the lake (14.5 m) as shown in Figure 1.
- Bathymetry reference: Ramsbottom (1976).

## Instrumentation
- Instrument: YSI EXO2 sonde.
- Calibration: Sensors calibrated at least every six weeks per manufacturer specifications.

## Data structure and fields
- Date (dd/mm/yyyy)
- Chlorophyll a (µg/L) determined using fluorescence measurements
- Phycocyanin (µg/L) determined using fluorescence (not quality checked)
- Water temperature (°C)
- Conductivity (µS/cm)
- Specific conductivity (µS/cm)
- Oxygen (% saturation)
- Oxygen (mg/L)
- pH
- Depth (m - raw measurement)
- Depth (m - rounded to 0.5 m)

## Data quality and notes
- Chlorophyll a values obtained from fluorescence show a measurable relationship to chemically determined chlorophyll (R² = 0.56, p < 0.05).
- Phycocyanin data are not quality checked.
- Depth data include both raw measurements and 0.5 m rounded depths.

## Spatial and GIS relevance
- Provides high-resolution vertical profiles suitable for 3D visualization and time-series mapping of water quality.
- Data can support spatial analyses of stratification and vertical distribution of parameters over time.
- Requires attention to data resolution differences and quality status (especially phycocyanin and depth rounding) when integrating with other GIS layers.

## References
- Ramsbottom, A. (1976) Depth charts of the Cumbrian lakes, Freshwater Biological Association, Kendal.