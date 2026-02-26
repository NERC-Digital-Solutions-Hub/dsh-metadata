# PULA sediments characterization data folder

## Overview
- A dataset comprising 14 files from 7 sediment cores collected from the Notwane Reservoir.
- Analyses cover sedimentological (grain size) and geochemical properties (organic matter and trace metals: Fe, Zn, Cu, Cr, Pb).

## Location, sampling, and core details
- Cores collected from Notwane Reservoir at multiple spots (Notwane Dam). Notable core entries include:
  - Core 1: Length 35 cm
  - Core 3: Length 60 cm
  - Core 7: Length 85 cm
  - Core 8: Length 70 cm
  - Core 9: Length 35 cm
  - Core 10: Length 50 cm
  - Core 11: Length 35 cm
- Coordinates provided for each core (latitude and longitude in decimal degrees, e.g., S24.x, E025.x).
- Dates of collection: 22-Nov-2017 and 19-Feb-2018.
- Sampling method: push corer (50 mm diameter) with extension rods, from shore or a small boat; cores stored at 4°C for water retention; cores split in half, photographed, and sub-sampled for grain size and geochemical analyses.

## Analytical techniques
- Grain size
  - Instrument: Malvern Mastersizer 3000 (laser diffraction) at BIUST.
  - Output: grain size distribution with D50 (median) reported for each subsample.
- Organic matter
  - Method: loss on ignition (LOI) after calcination.
  - Procedure: pre-weighed crucibles heated to 375°C, dried at 105°C, then heated to 550°C for 16 h.
- Trace metals
  - Subset: 95 samples across selected intervals.
  - Analysis: Microwave Plasma-Atomic Emission Spectrometry (MP-AES) after acid digestion (65% HNO3, 60°C, 4 h).
  - Data: concentrations of Fe, Zn, Cu, Cr, Pb (µg kg-1, dry sediment basis).
  - Quality: reported standard deviations for metals (Fe ~1.81%, Zn ~4.02%, Cu ~1.43%, Cr ~0.82%, Pb ~1.72%); detection limits provided (Cr 0.8 µg kg-1, Fe 1.7 µg kg-1, Cu 0.5 µg kg-1, Zn 28 µg kg-1, Pb 2.5 µg kg-1).

## Data structure and variables
- GrainSize_details dataset (7 spreadsheets, Core_*_Grain_size_details.csv)
  - Depths (in cm)
  - Grain size measurements: Dv(10), Dv(50), Dv(90) for 3 measurements per interval
  - Averages calculated for each core
- GrainSize_avg_and_metals dataset (7 spreadsheets, Core_*_Grain_size_avg_and_metals.csv)
  - Column 1: Core number
  - Column 2: Depth (cm) from sediment–water interface (0 cm)
  - Column 3: Average Dv(50) (µm)
  - Column 4: Organic Matter (OM, %)
  - Columns 5–9: Metals (Fe, Cu, Pb, Cr, Zn) in µg kg-1
  - Blank cells indicate data below detection limits or lost results

## Data quality and caveats
- Some data are below detection limits or missing (blanks in the datasets).
- Reported measurement uncertainties include explicit standard deviations for metals.
- Data are depth-resolved and core-specific, enabling vertical profiling across cores.

## GIS and data use implications
- Spatially explicit core locations with depth-resolved grain size, OM, and metal concentrations enable mapping of sediment characteristics and contamination patterns within the Notwane Reservoir.
- Data can support visualization of spatial gradients in grain size and geochemistry across the study area.
- Suitable for integration into GIS workflows to compare with other spatial layers (e.g., hydrology, land use) and to inform policy or environmental assessments.