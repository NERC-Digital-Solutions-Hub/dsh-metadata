# Bowbeat cloud and rain chemistry dataset 2003-2006

## Overview
- Weekly pollutant concentrations and depositions in cloud and rain samples from the Bowbeat field site (2003–2006).
- Collected to monitor and model cloud/rain water composition and deposition at high elevation; demonstrates the seeder-feeder effect where rain composition increases with altitude.
- Data include cloud-only concentrations derived from a cloud sampler and corrections for rain content.

## Experiment location
- Bowbeat site, UK Grid NT283473 (N55:42:51 W3:08:35), ~3.5 km north of Dunslair Heights monitoring site.
- Open moorland, 580 m above sea level, near Bowbeat wind farm; site fenced (25 m × 25 m).
- Replaced nearby Auchencorth for cloud and rain monitoring in 2003/4 due to forest growth; sampling abandoned in 2007 as seeder-feeder enhancement diminished.

## Fieldwork instrumentation and sampling
- Cloud sampler: stainless-steel frame with polypropylene toothed edge disc and fine polypropylene filaments intercepting cloud droplets, funnel to a 5-L bottle.
- Rain sampler: 20 cm HDPE funnel at 1.5 m height feeding a 20-L container.
- Sampling frequency: approximately weekly from 03/09/2003 to 28/06/2006.
- Analyses: ion chromatography for SO4 2-, NO3-, Cl-, NH4+, Na+, K+, Mg2+, Ca2+; data stored as CSVs and linked to Excel records.
- Cloud samples have ~90–95% rain content; corrections applied to cloud concentrations to reflect true cloud values.

## Data structure, nature and units
- Three CSV files in this resource:
  - Bowbeat_cloud_rain_chemistry_2003-2006.csv (unadjusted for rain content; cloud+rain data)
  - Bowbeat_cloud_chemistry_2003-2006.csv (cloud data adjusted for rain content)
  - Bowbeat_rain_chemistry_2003-2006.csv (rain data)
- Variables include collection date, sample weights, volumes, depths, and ion concentrations/depositions (e.g., Na, K, Ca, Mg, NO3-N, NH4-N, Cl, SO4-S, and non-marine sulfate), with corresponding units (mg/L for concentrations; mg/(m^2) for depositions).
- Depth calculations rely on sample volume and funnel geometry; explicit formulas are provided (depth in mm ≈ sample volume / 31.42).

## Sea-salt correction and non-marine sulfate
- Sea water is a significant salt contributor; sea-salt correction separates sea-salt sulfate from non-marine sulfate.
- Sea-water reference concentrations: Na = 10.773 g/kg; SO4 = 2.712 g/kg.
- Non-marine sulfate is computed as the portion of sulfate not attributable to sea water, using Na concentration and the ratio 2.712/10.773, with an additional division by 3 to account for sulfate mass fraction in the sulfate ion.

## Data cleaning and quality control
- Cleaning and QC performed in 2023 by S. Ferguson with guidance from J.N. Cape.
- Processed by splitting the original year-based worksheets, combining years into a continuous time series, and converting to CSVs (via R).
- Ion balance QC: (Σcations − Σanions) / (Σcations + Σanions); acceptable range typically −10% to +20% (or −10% to +30% if total ions < 200 µeq L−1). Imbalances outside −40% to +40% lead to data removal.
- H+ not measured; data flags identify potential issues (e.g., RAT, HCA, HNH, MH, LMG, LCL, LIS, HK, LV, LNA, HMG, CAT, UNK, REM*, MV*, PM, NA*).
- Cloud chemistry data often excluded from ion balance if dates were removed due to imbalance; some flags marked with * pertain only to cloud chemistry.
- Other removals: analytical reporting errors, bottle overflow, or missing values.

## Completeness
- Cloud&rain: 147 possible points; 104 complete (~70–79%), 14 missing, 13 partially missing, 16 removed.
- Rain: 147 possible; 120 complete (~81–83%), 14 missing, 10 removed, 3 partially missing.
- Cloud: 147 possible; 107 complete (~73%), 15 missing, 0 partially missing, 25 removed.

## References
- Cape, J.N.; Smith, R.I.; Fowler, D.; et al. 2010. Long-term monitoring of cloud chemical composition in the UK and implications for estimating wet deposition.
- Cape, J.N.; Smith, R.I.; Leaver, D. 2015. Missing data in spatiotemporal datasets: the UK rainfall chemistry network.
- Fowler, D.; et al. 2006. UK Heavy Metal Monitoring Network.
- Fowler, D.; et al. 2007. Acid Deposition Processes.