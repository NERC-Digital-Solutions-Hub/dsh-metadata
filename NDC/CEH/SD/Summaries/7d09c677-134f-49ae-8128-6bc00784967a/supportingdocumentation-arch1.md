# Repeat electrical resistivity tomography (ERT) measurements over four sites to capture the changing resistivity of the soil throughout the agricultural growing season

## Purpose and project context
- Repeated ERT measurements across four sites to track how soil resistivity changes through the agricultural growing season (spring, summer, autumn).
- Aimed at detecting transitions across crop growth stages (construction, production, post-harvest).
- Data collection supports the Land Management in Lowland Catchments for Integrated Flood Risk Reduction (LANDWISE) NFM research project.

## Methods and instrumentation
- ERT setup: 19 m transects with 96 electrodes spaced 20 cm apart, using a Campus Tigre system.
- Electrode configuration: Wenner Array for subsurface data collection.
- Depth: approximately 1 m below ground level (bgl) per transect.
- Data per transect: about 660 apparent resistivity readings.
- Field and processing tools: data collected with ImagerPro2006, processed with Geotomo’s Res2DInv.
- Positioning accuracy: Leica GNSS system with ~0.01 m accuracy to ensure repeatability.

## Survey layout and timing
- Four survey locations along start-end lines (BNG):
  - Lower Hampen Farm – Barn Ground
  - Lower Hampen Farm – Flat Ground
  - Manor Farm – Whittington Hill
  - Hendred Farm – Lockinge (Untraffic)
  - Hendred Farm – East Hendred (Traffic A and Traffic B)
- Survey timeline by season in 2021:
  - April/May: initial measurements
  - June/July: summer measurements
  - September: final measurements (post-harvest)

## Data collection and quality control
- Each transect: 19 m with 96 electrodes; 0.2 m electrode spacing; Wenner Array; depth ~1 m.
- Field data collected with ImagerPro2006.
- Quality control: software checks for poor ground contact; electrodes retested/re-established as needed.
- Post-processing: data cleaned of noisy points prior to inversion in Res2DInv.

## Data structure and formats
- Data stored in Res2DInv format (example: BarnGround_April.dat).
- Key structure details:
  - Survey file name, electrode spacing (0.2 m), Wenner Array flag, number of data points (660), mid-point x-location.
  - Data blocks: for each data point, X-location, a-electrode spacing, apparent resistivity value (Ohm.m).
  - Data end indicated by end-of-survey flags.
- Interpretation focus: apparent resistivity (Ohm.m) values derived from the Wenner array data, enabling resistivity cross-sections of the subsurface.

## Notes on data relevance and use
- Resistivity variations reflect soil structure, interstitial water, and salinity—informing soil moisture and health across crop growth stages.
- Data are designed to be used for analyses related to soil process understanding and to support flood risk management and land management decisions within the LANDWISE project.
- Spatial coordinates for transects and site-specific details are documented to enable reproducibility and cross-site comparisons.