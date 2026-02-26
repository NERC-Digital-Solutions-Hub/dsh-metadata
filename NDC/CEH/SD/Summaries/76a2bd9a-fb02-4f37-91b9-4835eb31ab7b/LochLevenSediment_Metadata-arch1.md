# LochLeven_SedimentDataset.csv

## Overview
- Dataset from a project on cycling of phosphorus between bed sediments and the overlying water column in Loch Leven, Scotland (2004–2005).
- Includes indicators of benthic microalgal biomass.
- Used in multiple publications to describe phosphorus mobilisation and the regulatory role of benthic microalgae.

## Sampling regime
- Monthly sampling from April 2004 to April 2005.
- Six permanent sites forming a water-depth transect.
- At each visit: field measurements and laboratory analyses on collected samples.
- Sediment cores collected (approx. 30 cm water, 20 cm sediment); upper 3 cm of sediment homogenised for analyses.

## List of sampling sites
- Six sites with UK OS grid references, depths, and counts:
  - Depths: 2.0, 2.5, 3.5, 5.5, 10.0, 22.0 m
  - Counts: 500 for the shallowest site; 405 for the remaining sites

## List of determinands
- Measured in surface, bottom, pore water, and sediment where applicable:
  - Dissolved Oxygen (%sat), Conductivity (mS/cm), pH, Temperature (°C)
  - Soluble Reactive Phosphorus (SRP; µg/l)
  - Total Soluble Phosphorus (TSP) and Total Phosphorus (TP)
  - Ammonium-N (NH4-N; µg/l)
  - Silicate (SiO2; mg/l)
  - Chlorophyll a (µg/l; and conversion to µg/g dry weight)
  - Sediment P fractions: labile P, reductant-soluble P, reductant-soluble SRP, metal oxide P, organic P, apatite-bound P, residual P
  - Sediment Total Phosphorus (TP) and related fractions (gdw = per gram dry weight)

## Sampling, measurement and analysis methods
- In situ measurements at each site using Hydrolab probes for DO, conductivity, pH, and temperature.
- Water and sediment sampling:
  - Surface water collected in acid-washed bottles; bottom water sampled from sediment cores.
  - Filters (Whatman GF/C) used for some analyses; pigments stored for chlorophyll a.
- Laboratory analyses:
  - SRP and TP using colorimetric methods based on Murphy & Riley (1962) and Wetzel & Likens (2000).
  - NH4-N via phenol-hypochlorite method; SRSiO2 via specified method.
  - Chlorophyll a quantified spectrophotometrically with pigment corrections.
  - Sediment P fractionation: sequential extractions for labile, reductant-soluble, metal oxide-bound, apatite-bound, and residual P; organic P derived from differences; extractions performed in dark at 20°C with detailed steps and post-extraction processing.
- Sediment and water samples prepared by grinding, centrifugation, and filtration as appropriate for each fraction.

## Data format and storage
- Data stored in a single ASCII CSV file.
- Columns include: Site, Depth, Month, Date, DO (%sat), Cond (mS cm-1), pH, Temp (°C), SRP (µg/l), TSP (µg/l), TP (µg/l), NH4 (µg/l), SiO2 (mg/l), Chl a (µg/l), SRP (µg/l), TSP (µg/l), NH4-N (µg/l), labile (mg P.gdw), red sol (mg.gdw), red sol surp (mg.gdw), Metal oxide (mg.gdw), Organic (mg.gdw), apatite bound (mg.gdw), Residual (mg.gdw), TP (mg gdw), Chl a (µg/gdw).
- Note: dataset includes detailed breakdown of sediment P fractions alongside water-column chemistry and chlorophyll data.

## Applications and references
- Enables analysis of phosphorus mobilisation from bed sediments and the regulatory role of epipelon/benthic microalgae on phosphorus cycling.
- Foundational for understanding spatial (depth-related) and temporal variations in phosphorus pools in a large shallow temperate eutrophic lake.
- Related publications: Spears et al. (2006, 2007a, 2007b, 2009, 2010, 2012); with supporting methodologies from APHA (1992) and other cited sources.