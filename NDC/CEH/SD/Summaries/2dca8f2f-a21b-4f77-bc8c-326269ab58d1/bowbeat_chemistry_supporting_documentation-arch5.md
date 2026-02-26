# Bowbeat cloud and rain chemistry dataset 2003-2006

- Overview: Weekly pollutant concentrations and depositions in cloud and rain from the Bowbeat field site (2003–2006). Data were collected to monitor and model cloud/rain water composition and deposition at high elevation, with cloud-only concentrations derived from the cloud collector data.

- Experiment location: Bowbeat site (UK grid NT283473; N55:42:51 W3:08:35), around 580 m above sea level, in open moorland near the Bowbeat wind farm. Bowbeat replaced Dunslair Heights for cloud/rain monitoring in 2003/4 and was abandoned in 2007 when seeder–feeder enhancements diminished.

- Fieldwork instrumentation and sampling:
  - Cloud sampler: stainless-steel frame, polyurethane coating, polypropylene toothed edge disc, fine polypropylene filaments intercepting cloud droplets, funnel to a 5 L collecting bottle.
  - Rain sampler: 20 cm HDPE funnel at 1.5 m height feeding into a 20 L container.
  - Sampling frequency: roughly weekly from 03/09/2003 to 28/06/2006.
  - Sample handling: weekly bottle weights recorded, four sub-samples stored (one for lab ion analysis; others for long-term storage); ion chromatography performed for SO4 2-, NO3-, Cl-, NH4+, Na+, K+, Mg2+, Ca2+.
  - Cloud vs rain: cloud samples slightly contaminated by rain; cloud concentrations corrected for rain content.
  - Data processing: lab results provided as CSVs and copied into Excel; depth and deposition calculations derived from sample volumes.

- Data structure, values, and units:
  - Bowbeat_cloud_rain_chemistry_2003-2006.csv: concentrations and depositions in cloud samples before rain-content adjustment (per ion listed: Na, K, Ca, Mg, NO3-N, NH4-N, Cl, SO4-S, non-marine SO4, etc.).
  - Bowbeat_rain_chemistry_2003-2006.csv: weekly concentrations/depositions in rain samples.
  - Bowbeat_cloud_chemistry_2003-2006.csv: cloud-only data adjusted for rain content (total refers to cloud+rain samples).
  - Key calculated fields: depth (mm) from sample volume, deposition (mg/m2) from concentration × depth, non-marine sulphate calculated using sea-water Na and SO4 concentrations (Na as 10.773 g/kg; SO4 as 2.712 g/kg; non-marine SO4 = [Na] × 2.712/10.773 ÷ 3 for sulfate as S).
  - Important notes: depth of cloud+rain sample and cloud-only depth derived as described; cloud data derived from rain and cloud+rain data; several fields use standard units (mg/L for concentrations, mg/(m2) for deposition).

- Data cleaning and quality control (QC):
  - QC performed in 2023 by S. Ferguson with guidance from J.N. Cape.
  - Process: separate three-year tables, combine into a continuous time series, convert to three CSV files.
  - Ion balance QC: (Σcations − Σanions)/(Σcations + Σanions) should be between −10% and +20% (or −10% to +30% if total ion concentration < 200 µeq/L). Imbalances >40% or <−40% lead to data removal; other imbalances receive data flags.
  - Data flags (RAT, HCA, HNH, MH, LMG, LCL, LIS, HK, LV, LNA, HMG, CAT, UNK, REM*, MV*, PM, NA*) indicate potential issues (e.g., unusual Na ratios, low Ca/Mg/Na, analytical errors, missing values, etc.). Cloud data were excluded from ion balance if rain-related removals occurred; cloud-specific flags with asterisks indicate cloud chemistry flags.
  - Reasons for data removal include ion imbalance thresholds, analytical reporting errors, and bottle overflow (assessed via volume vs. concentration plots).
  - Cloud chemistry data are not independently balanced but are removed on dates where rain-related data were removed due to ion imbalance.

- Completeness and data availability:
  - Cloud&rain dataset: 147 total points; 14 missing, 13 partially missing, 16 removed; 104 complete (~70–79% complete).
  - Rain dataset: 147 total; 14 missing, 3 partially missing, 10 removed; 120 complete (~81–83% complete).
  - Cloud dataset: 147 total; 15 missing, 0 partially missing, 25 removed; 107 complete (~73% complete).

- Usage considerations and governance:
  - Sea-salt correction and non-marine sulphate calculations documented to separate natural sea-water contributions from anthropogenic sulphate.
  - Data underwent retrospective QC and reformatting (R-based) for clarity and reproducibility; methods and references to Cape et al. (2010, 2015) and Fowler et al. (2006–2007) underpin the processing and interpretation.
  - Data provenance: collected by Alan Crossley and Frank Harvey; approved by project investigators; archived under UKCEH/CEH framework with published methodological references.
  - Documentation includes explicit formulas, units, data flags, and completeness metrics to support data governance, discoverability, and reuse.

- References:
  - Cape, J.N. et al. 2010; Cape, J.N. et al. 2015; Fowler, D. et al. 2006–2007; CEH project reports and publications cited in the dataset description.