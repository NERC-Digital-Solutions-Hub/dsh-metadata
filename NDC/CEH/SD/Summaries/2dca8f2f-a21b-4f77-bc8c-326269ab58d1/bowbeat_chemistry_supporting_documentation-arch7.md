# Bowbeat cloud and rain chemistry dataset 2003-2006

## Overview and purpose
- Weekly pollutant concentrations and depositions in cloud and rain samples from the Bowbeat field site (2003–2006).
- Collected to monitor and model cloud/rain water composition and deposition at high elevation; linked to seeder-feeder atmospheric processes.
- Data include ion chemistry, heavy metals, and bacteria analyses, with cloud samples partly requiring correction for rain content.

## Experiment location
- Bowbeat site located at UK Grid reference NT283473 (N55:42:51 W3:08:35), ~580 m above sea level.
- Site 3.5 km north of Dunslair Heights; in open moorland near Bowbeat wind farm.
- Map reference available; Bowbeat was the replacement site for cloud/rain monitoring in the Scottish Southern Uplands (2003–2006). Sampling ended in 2007.

## Fieldwork instrumentation and sampling
- Cloud sampling: passive cloud sampler with a stainless-steel frame, polyurethane coating, polypropylene toothed edge disc and fine polypropylene filaments to intercept cloud droplets, funnel, and 5 L collecting bottle.
- Rain sampling: 20 cm HDPE funnel at 1.5 m height feeding into a 20 L bottle.
- Sampling cadence: approximately weekly from 03/09/2003 to 28/06/2006.
- Handling: for each weekly sample, bottle+sample weight recorded, then four sub-samples placed into 150 mL bottles for ion analysis or long-term storage.
- Analysis: ion chromatography for Na, K, Ca, Mg, NO3, NH4, Cl, SO4 (as S), and related parameters; cloud samples adjusted for rain content to reduce cross-contamination.

## Data structure and values
- Three CSV files:
  - Bowbeat_cloud_rain_chemistry_2003-2006.csv: weekly concentrations/depositions in cloud samples (before rain content adjustment).
  - Bowbeat_cloud_chemistry_2003-2006.csv: weekly concentrations/depositions in cloud samples adjusted for rain content (derived from rain and cloud+rain data; “Total” refers to cloud+rain contributions).
  - Bowbeat_rain_chemistry_2003-2006.csv: weekly concentrations/depositions in rain samples.
- Common fields (examples by file):
  - Collection_Date: sample collection date.
  - Depth: depth of the sample (for cloud, rain, and cloud+rain derived data).
  - Na_Conc, Na_Dep; K_Conc, K_Dep; Ca_Conc, Ca_Dep; Mg_Conc, Mg_Dep; NO3-N_Conc, NO3-N_Dep; NH4-N_Conc, NH4-N_Dep; Cl_Conc, Cl_Dep; SO4-S_Conc, SO4-S_Dep; SO4-S_NON-MARINE_Conc, SO4-S_NON-MARINE_Dep.
  - Sample_Volume; Weight_Bottle; Weight_Bottle+Sample; Data_Flag; Reason.
- Units and basic formulas:
  - Depth: depth of cloud sample = (sample volume) / 31.42 (in mm).
  - Concentrations: mg/L; Depositions: mg/(m^2).
  - Depth used to compute depositions: deposition = concentration × depth.
- Non-marine sulphate: derived by separating sea-salt contributions using sea-water concentrations (Na = 10.773 g/kg and SO4-S = 2.712 g/kg). Non-marine SO4-S = (Na concentration in sample) × (2.712/10.773) divided by 3 to account for the sulphate as S.

## Derived quantities and data processing notes
- Cloud samples adjusted for rain content to yield cloud-only and total (cloud+rain) estimates.
- Non-marine sulphate estimation uses sea-salt correction to separate natural sea-salt sulphate from pollutant-derived sulphate.
- Cloud chemistry data are derived from rain/cloud data; excluded from ion balance except where flagged.

## Data cleaning and quality control
- Cleaning performed in 2023 by S. Ferguson with guidance from J. Neil Cape.
- Process: separate and combine yearly tables, create continuous time series, convert to CSVs.
- Quality control: ion balance = (Σcations − Σanions) / (Σcations + Σanions).
  - Acceptable range: −10% to +20% (or −10% to +30% if total ion concentration < 200 µeq L−1).
  - Data removed if ion imbalance > +40% or < −40%.
- Data flags explain potential issues (RAT, HCA, HNH, MH, LMG, LCL, LIS, HK, LV, LNA, HMG, CAT, UNK, REM*, MV*, PM, NA*).
- Cloud chemistry data: excluded from ion balance except when rain/cloud or rain data were removed for large ion imbalance.
- Reasons for data removal (noted in the dataset): ion imbalance > 40% or < −40%, analytical reporting errors, bottle overflow, etc.

## Completeness and data availability
- Cloud&rain: 147 total points; 104 complete; ~70–79% completeness.
- Rain: 147 total points; 120 complete; ~81–83% completeness.
- Cloud: 147 total points; 107 complete; ~73% completeness.
- Missing data are due to unknown sampling gaps, removals, or partial records in the original dataset.

## References
- Cape, J.N.; Smith, R.I.; Fowler, D.; Beswick, K.; Choularton, T. (2010). Long-term monitoring of cloud chemical composition in the UK and implications for estimating wet deposition.
- Cape, J.N.; Smith, R.I.; Leaver, D. (2015). Missing data in spatiotemporal datasets: the UK rainfall chemistry network.
- Fowler, D. et al. (2006). UK Heavy Metal Monitoring Network.
- Fowler, D. et al. (2007). Acid Deposition Processes. Final report to Defra.