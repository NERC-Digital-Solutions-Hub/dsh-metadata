# Bowbeat cloud and rain chemistry dataset 2003-2006

## Overview
- Weekly pollutant concentration and deposition data in cloud and rain samples from the Bowbeat field site (now retired).
- Cloud-only concentrations derived from cloud and rain data.
- Collected to monitor and model cloud/rain water composition and deposition at high elevation; relates to the known seeder-feeder mechanism where rain from high-level clouds shows enhanced deposition.
- Bowbeat contributed to long-running high-elevation monitoring of atmospheric chemistry in the Scottish Southern Uplands.

## Location and Site
- Bowbeat site coordinates: UK Grid NT283473 (N55:42:51 W3:08:35).
- Located 3.5 km north of the Dunslair Heights monitoring site, in open moorland at about 580 m above sea level.
- Adjacent to the Bowbeat wind farm; data collection moved to Bowbeat due to forest growth affecting Auchencorth data.
- Sampling at Bowbeat occurred 2003/2004 as a replacement cloud/rain monitoring site; data collection ended in 2007 when seeder-feeder enhancement diminished.

## Fieldwork instrumentation and sampling
- Cloud sampler: stainless-steel frame, polyurethane coating, polypropylene toothed edge disc; fine polypropylene filaments form an inverted cone to intercept cloud droplets and funnel into a 5 L bottle.
- Rain sampler: 20 cm HDPE funnel at 1.5 m height, feeding a 20 L container.
- Sampling cadence: approximately weekly from 03/09/2003 to 28/06/2006.
- Processing: for each weekly sample, bottle weight recorded, sub-sampled into four 150 mL LDPE bottles; one for UKCEH lab ion analysis, others stored.
- Laboratory analyses: ion chromatography for SO4 2-, NO3-, Cl-, NH4+, Na+, K+, Mg2+, and Ca2+.
- Cloud samples are corrected for rain contamination to better estimate true cloud concentrations.

## Data structure and content
- Three CSV data files:
  - Bowbeat_cloud_rain_chemistry_2003-2006.csv: weekly concentrations and depositions in cloud samples (before adjusting for rain content).
  - Bowbeat_cloud_chemistry_2003-2006.csv: cloud data adjusted for rain content (derived from rain and cloud&rain data); totals refer to cloud-only or cloud+rain totals as indicated.
  - Bowbeat_rain_chemistry_2003-2006.csv: weekly concentrations and depositions in rain samples.
- Variables cover:
  - Collection date, sample weights, sample volume, depth (calculated from volume and funnel geometry), and concentrations (e.g., Na_Conc, K_Conc, Ca_Conc, Mg_Conc, NO3-N_Conc, NH4-N_Conc, Cl_Conc, SO4-S_Conc, and non-marine sulfate components).
  - Depositions (e.g., Na_Dep, K_Dep, Ca_Dep, Mg_Dep, NO3-N_Dep, NH4-N_Dep, Cl_Dep, SO4-S_Dep, SO4-S_NON-MARINE_Dep).
- Depth calculations: depth of a sample computed from sample volume using the funnel cross-section (depth ≈ sample volume / 31.42 mm).
- Non-marine sulfate: sea-salt correction uses sea-water sodium and sulfate constants to estimate non-marine sulfate from total sulfate.

## Non-marine sulfate calculation
- Sea-salt correction uses sea-water concentrations: Na = 10.773 g/kg, SO4 = 2.712 g/kg.
- Non-marine sulfate concentration in a sample is calculated as: [Na] × (2.712/10.773) × (1/3).
- This accounts for the marine contribution to sulfate, allowing estimation of non-marine (pollution-origin) sulfate.

## Data cleaning and quality control
- Cleaning conducted in 2023 by S. Ferguson with guidance from J. Neil Cape.
- Original data separated into three yearly worksheets; an R script combined years into a continuous time series and converted to CSVs.
- Quality control via ion balance: (Σcations − Σanions) / (Σcations + Σanions).
  - Acceptable: −10% to +20% (or −10% to +30% when total ion concentration < 200 µeq L−1).
  - Imbalances between −40% and −10% or between +20% and +40% flagged; data removed if imbalance > +40% or < −40%.
- Data flags to indicate potential issues (e.g., RAT, HCA, HNH, MH, LMG, LCL, LIS, HK, LV, LNA, HMG, CAT, UNK, REM*, MV*, PM, NA*).
- Cloud chemistry data excluded from ion balance when rain/cloud data were removed due to large imbalances; only cloud data with flags marked by an asterisk apply to cloud chemistry.
- Reasons for data removal include: ion imbalance thresholds, analytical reporting errors, bottle overflow, and other data quality concerns.
- H+ not measured; data flags also indicate possible contamination or balance issues (e.g., unusual Na ratios, high Ca or NH4-N).

## Completeness
- Cloud&rain: 147 total possible data points; 104 complete data points (~70–79% completeness); 14 missing; 13 partially missing; 16 removed.
- Rain: 147 total; 120 complete (~81–83%); 14 missing; 3 partially missing; 10 removed.
- Cloud: 147 total; 107 complete (~73%); 15 missing; 0 partially missing; 25 removed.
- Overall, data completeness varies by dataset, with rain generally more complete than cloud-related data.

## References
- Cape, J.N.; Smith, R.I.; Fowler, D.; Beswick, K.; Choularton, T. 2010. Long-term monitoring of cloud chemical composition in the UK and implications for estimating wet deposition.
- Cape, J.N.; Smith, R.I.; Leaver, D. 2015. Missing data in spatiotemporal datasets: the UK rainfall chemistry network.
- Fowler, D. et al. 2006. UK Heavy Metal Monitoring Network.
- Fowler, D. et al. 2007. Acid Deposition Processes. Final report to Defra.