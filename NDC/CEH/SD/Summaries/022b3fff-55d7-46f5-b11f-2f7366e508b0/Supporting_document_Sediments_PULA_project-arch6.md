# PULA sediments characterization data folder

## Overview
- Contains 14 files with sedimentological and geochemical analyses from 7 cores of sediments.
- Cores collected from the Notwane Reservoir, with depth, location coordinates, and collection dates recorded for each core.
  - Dates: 22-Nov-17 and 19-Feb-18.
  - Locations correspond to Notwane Dam area; each core has a recorded length in cm.
- Data cover grain size, organic matter content, and trace metal concentrations (Cr, Fe, Ni, Cu, Zn, Pb) across core depths.

## Sampling techniques
- Seven sediment cores collected using a push corer with extension rods from shore or from a small boat.
- Core details: 50 mm diameter PVC pipes; stored at 4 °C for water retention.
- Cores split in half, photographed, and sub-sampled for grain size and geochemical analysis.

## Analytical techniques
- Grain size: dispersion in distilled water analyzed with Malvern Mastersizer 3000 (reported as Dv(10), Dv(50), Dv(90) in µm).
- Organic matter (OM): loss on ignition (LOI) method after drying (105 °C) and calcination (550 °C).
- Trace metals: 95 sediment samples from selected intervals analyzed by MP-AES after acid digestion (65% nitric acid, ~60 °C, 4 hours); filtration to <0.45 µm and dilution to 50 ml.
- Quality metrics:
  - Reported average standard deviations: Fe 1.81% RSD, Zn 4.02% RSD, Cu 1.43% RSD, Cr 0.82% RSD, Pb 1.72% RSD.
  - Detection limits for metals: Cr 0.8 µg/kg, Fe 1.7 µg/kg, Cu 0.5 µg/kg, Zn 28 µg/kg, Pb 2.5 µg/kg.

## Data structure
- 7 spreadsheets named Core_*_Grain_size_details.csv:
  - Grain size measurements at different depths (in cm).
  - Dv(10), Dv(50), Dv(90) values for each of the 3 measurements and their average per core.
- 7 spreadsheets named Core_*_Grain_size_avg_and_metals.csv:
  - Column 1: core sequential number.
  - Column 2: depth from sediment–water interface (0 cm).
  - Column 3: average Dv(50) grain size (µm) across the three measurements.
  - Column 4: Organic Matter content (OM %)).
  - Columns 5–9: concentrations of Fe, Cu, Pb, Cr, Zn (µg/kg).
- Note: Blank cells indicate data below detection limits or data loss.

## Data quality and limitations
- Some data are at or below instrument detection limits (blanks in the datasets).
- Reported uncertainties include RSDs for metals and measurement details for LOI and grain size.
- Data are provided as CSV spreadsheets for cross-core comparison and depth profiling; ensure consistent alignment when merging datasets.

## Potential data products and use
- Depth-profile dashboards comparing grain size, OM, and metal concentrations across cores.
- Self-serve exploration tools to identify correlations between sediment texture, organic content, and trace metal distribution.
- Documentation and metadata to support data reuse, quality assessment, and integration with other datasets.