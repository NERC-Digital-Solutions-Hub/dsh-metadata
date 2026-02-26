# PULA sediments characterization data folder

## Overview
- 14 files containing results from sedimentological and geochemical analyses of 7 cores from the Notwane Reservoir.
- Cores: 1, 3, 7, 8, 9, 10, 11 with lengths 35, 60, 85, 70, 35, 50, 35 cm respectively.
- Collection dates: 22-Nov-2017 (cores 1, 3, 7) and 19-Feb-2018 (cores 8, 9, 10, 11).
- Core coordinates provided (latitude/longitude) around Notwane Dam.
- Analyzed for grain size distribution, organic matter content, and concentrations of heavy metals Cr, Fe, Ni, Cu, Zn, Pb.

## Sampling techniques and Analytical methods
- Sampling: seven sediment cores collected from shore or a small boat using a push corer with extension rods; 50 mm PVC cores stored at 4°C for water retention; cores split, photographed, and sub-sampled for grain size and geochemical analyses.
- Grain size: analyzed with Malvern Mastersizer 3000 laser diffractometer; Reported as D50 for each subsample.
- Organic matter (OM): determined by loss on ignition (LOI) with calcination sequence: pre-heat, dry at 105°C, then combustion at 550°C for 16 h.
- Trace metals: 95 sediment samples from selected intervals analyzed for Fe, Zn, Cu, Cr, Pb using an Agilent 4200 MP-AES after acid digestion (65% HNO3, ~60°C, 4 h); filtration to <0.45 µm and brought to 50 mL with Milli-Q water.
- Quality metrics: reported detection limits (Cr 0.8 µg/kg, Fe 1.7 µg/kg, Cu 0.5 µg/kg, Zn 28 µg/kg, Pb 2.5 µg/kg) and average %RSDs (Fe 1.81%, Zn 4.02%, Cu 1.43%, Cr 0.82%, Pb 1.72%).

## Data structure
- Grain size details: 7 spreadsheets named Core_*_Grain_size_details.csv reporting grain size measurements at different depths (cm); includes Dv(10), Dv(50), Dv(90) for each of 3 measurements and the averaged values per core.
- Avg and metals: 7 spreadsheets named Core_*_Grain_size_avg_and_metals.csv with:
  - Column 1: core sequential number
  - Column 2: depth from sediment-water interface (0 cm)
  - Column 3: average Dv(50) (µm)
  - Column 4: Organic Matter content (OM %) 
  - Columns 5–9: concentrations of Fe, Cu, Pb, Cr, Zn (µg/kg)
- Data gaps: blank cells indicate values below detection limits or data lost during processing.

## Data quality and considerations
- Standardised methods enable cross-core comparisons and integration with other monitoring datasets.
- Detection limits are explicitly stated; non-detects are represented as blanks.
- Variability across measurements is captured via multiple grain-size measurements per interval and reported %RSDs for metals.

## Potential use for monitoring and policy analysis
- Enables assessment of sediment characteristics and metal deposition patterns over depth and across cores in the Notwane Reservoir.
- Can be integrated with ancillary environmental datasets to evaluate reservoir health, contamination trends, and compliance with standards.
- Structured data format supports reuse, cross-study comparisons, and meta-analyses when shared on appropriate data portals.