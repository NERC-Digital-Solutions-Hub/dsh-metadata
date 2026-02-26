# A brief description/overview of the data being described

## Overview
- PULA sediments characterization data folder contains 14 files with results from sedimentological and geochemical analyses of 7 sediment cores from the Notwane Reservoir.
- Cores have documented locations, depths, coordinates, and collection dates (22-Nov-2017 and 19-Feb-2018).
- Analyses cover grain size distribution, organic matter content, and trace metals (Cr, Fe, Ni, Cu, Zn, Pb).

## Sampling and sample handling
- Seven sediment cores were collected using a push corer with extension rods from shore or a small boat.
- Cores (50 mm diameter PVC) were stored at 4 °C for water retention, split in half, photographed, and sub-sampled for grain size and geochemical analyses.

## Analytical techniques
- Grain size: a Malvern Mastersizer 3000 laser diffractions particle size analyzer; reports D50 (median) grain size for each subsample.
- Organic matter (OM): loss on ignition (LOI) method after drying at 105 °C and subsequent calcination at 550 °C; detail: crucibles pre-heated, dried, weighed, and re-weighed.
- Trace metals: 95 sediment samples analyzed for Fe, Zn, Cu, Cr, Pb using an Agilent 4200 MP-AES following digestion with 65% nitric acid at 60 °C, then filtration and dilution to 50 mL. Reported: instrument detection limits and typical run precision (RSD) for each element.

## Data structure and content
- Data are organized into two main data sets, stored as CSV spreadsheets.
- Dataset 1: Core_*_Grain_size_details.csv
  - Contains grain size measurements at multiple depths for each core (Dv10, Dv50, Dv90 in µm) and three measurements per interval plus averaged values.
- Dataset 2: Core_*_Grain_size_avg_and_metals.csv
  - For each core and depth (starting at 0 cm from the sediment–water interface):
    - Column 3: average Dv50 grain size (µm)
    - Column 4: Organic Matter (OM in %)
    - Columns 5–9: Fe, Cu, Pb, Cr, Zn (µg kg-1)
- Notes:
  - Blank cells indicate data below detection limits or results lost.
  - All data originate from the sediment cores collected from Notwane Reservoir and analyzed at BIUST (Botswana).