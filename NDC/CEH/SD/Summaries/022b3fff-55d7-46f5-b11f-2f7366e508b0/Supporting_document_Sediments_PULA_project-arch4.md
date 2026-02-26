# A brief description/overview of the data being described

## Overview
- PULA sediments characterization data folder comprising 14 files from 7 sediment cores.
- Cores collected from the Notwane Reservoir at multiple locations, with coordinates, depths, and collection dates provided.
- Data capture includes grain size, organic matter content, and trace metal concentrations (Cr, Fe, Ni, Cu, Zn, Pb).

## Sampling techniques
- Seven cores collected from the Notwane Reservoir using a push corer with extension rods (shore or small boat).
- Core diameter: 50 mm; stored at 4 °C for water retention.
- Cores split in half, photographed, and subsampled for grain size and geochemical analyses.
- Sediment samples analyzed for:
  - Particle size distribution
  - Organic matter content
  - Trace metal concentrations (Fe, Zn, Cu, Cr, Pb)

## Analytical techniques
- Grain size: Measured with Malvern Mastersizer 3000 laser diffraction analyzer at BIUST; reporting the median D50 per subsample.
- Organic matter: Loss on ignition (LOI) after calcination (375 °C pre-heating; 105 °C drying; 550 °C final heating).
- Trace metals: About 1 g of sample digested with 65% HNO3 at 60 °C for 4 hours; filtered and brought to 50 ml with Milli-Q water.
  - Instrument: Agilent 4200 MP-AES at BIUST.
  - Metals reported: Fe, Zn, Cu, Cr, Pb.
  - Quality: Average standard deviations (Fe 1.81%, Zn 4.02%, Cu 1.43%, Cr 0.82%, Pb 1.72%); detection limits (Cr 0.8 µg/kg, Fe 1.7 µg/kg, Cu 0.5 µg/kg, Zn 28 µg/kg, Pb 2.5 µg/kg).

## Data structure
- Seven spreadsheets: Core_*_Grain_size_details.csv
  - Contain grain size measurements at different depths (cm).
  - Report Dv(10), Dv(50), Dv(90) for each of the 3 measurements and the averages for the seven cores.
- Additional dataset: Core_*_Grain_size_avg_and_metals.csv
  - Column 1: core sequential number.
  - Column 2: sample depth in cm from sediment–water interface (0 cm).
  - Column 3: average Dv(50) grain size (µm) across the 3 measurements.
  - Column 4: Organic Matter content (OM %) per interval.
  - Columns 5-9: abundances of Fe, Cu, Pb, Cr, Zn (µg/kg).
- Notes: Blank cells indicate data below detection limits or data loss.