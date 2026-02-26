# Bowbeat cloud and rain chemistry dataset 2003-2006

## Overview
- Weekly measurements of pollutant concentrations and depositions in cloud and rain samples from the Bowbeat field site (2003–2006).
- Collected to monitor and model cloud/rain water composition and deposition at high elevation; relates to the seeder-feeder effect showing higher rain composition at altitude.
- Data produced by independent lab analysis (ion chromatography) and assembled into CSV formats for long-term monitoring and policy-relevant interpretation.
- Site history: Bowbeat replaced nearby Dunslair for cloud/rain monitoring in 2003/04 due to forest growth; monitoring ended at Bowbeat in 2007 as seeder-feeder enhancement diminished relative to other sites.

## Experiment Location
- Bowbeat site: UK Grid NT283473 (N55:42:51 W3:08:35), 580 m above sea level, open moorland near Bowbeat wind farm.
- Proximity: ~3.5 km north of Dunslair Heights; fenced equipment area on Bowbeat Rig.
- Context: Data collected as part of long-running high-elevation monitoring in the Scottish Southern Uplands; forest growth compromised nearby sites, justifying Bowbeat’s use during 2003–2006.

## Fieldwork Instrumentation and Sampling
- Cloud sampler: stainless-steel frame, polyurethane coating, polypropylene filament edge disc, inverted cone of filaments guiding cloud droplets to a 5-L bottle.
- Rain sampler: 20 cm HDPE funnel, mounted at 1.5 m, feeding a 20-L collecting container.
- Sampling cadence: approximately weekly from 03/09/2003 to 28/06/2006.
- Sample handling: weekly bottle weights recorded, four sub-samples sent for ion analysis (UKCEH) and remaining kept for storage; lab results provided as CSV and imported into Excel.
- Analytes: ions including SO4 2-, NO3-, Cl-, NH4+, Na+, K+, Mg2+, Ca2+ (ion chromatography).
- Cloud sample correction: cloud concentrations adjusted to account for partial rain content (clouds ~90–95% of rain collector efficiency); cloud data corrected to reflect true atmospheric deposition.

## Data Structure, Nature and Units
- Three CSV data files:
  - Bowbeat_cloud_rain_chemistry_2003-2006.csv: weekly concentrations and depositions in cloud samples (before rain-content adjustment).
  - Bowbeat_rain_chemistry_2003-2006.csv: weekly concentrations and depositions in rain samples.
  - Bowbeat_cloud_chemistry_2003-2006.csv: weekly cloud concentrations/depositions adjusted for rain content (total values also provided for cloud+rain combinations).
- Key data concepts:
  - Depth calculations for samples (depth = sample volume / 31.42; depth in mm).
  - Sea-salt correction: non-marine sulphate derived by accounting for sea-water contributions using Na and SO4 measurements with a standard sea-water composition (Na = 10.773 g/kg; SO4 = 2.712 g/kg).
  - Non-marine sulphate = [Na] × (2.712/10.773); non-marine sulphur (as S) further adjusted by dividing by 3 to reflect sulfur content in the sulphate ion.

## Data Cleaning and Quality Control
- Cleaning performed in 2023 by S. Ferguson with guidance from J.N. Cape; involved separating annual tables, combining years, and converting to CSV.
- Quality control: ion balance computed as (sum cations − sum anions) / (sum cations + sum anions).
  - Acceptable range: −10% to +20% generally; if total ion concentration < 200 µeq L−1, range widened to −10% to +30%.
  - Flags for potential issues: ranges of −40% to −10% or +20% to +40% flagged (RAT, HCA, HNH, MH, LMG, LCL, LIS, HK, LV, LNA, HMG, CAT, UNK, REM*, MV*, PM, NA*).
  - Cloud data excluded from ion balance when rain or rain+cloud data were removed for imbalance; cloud-only data flagged accordingly.
  - Common removal reasons: ion imbalance >40% or <−40%; analytical errors; bottle overflow (assessed via volume vs. time graphs).
- Data flags indicate possible contamination sources (e.g., unusual Na ratios, high Ca/NH4, ion-imbalance-related issues).
- Cloud chemistry data were not included in the ion balance; removed on dates where rain-related data were removed due to imbalance.

## Completeness
- Cloud&rain data: 147 possible points; 14 missing; 13 partially missing; 16 removed; 104 complete (approx. 70–79% complete).
- Rain data: 147 possible; 14 missing; 3 partially missing; 10 removed; 120 complete (approx. 81–83% complete).
- Cloud data: 147 possible; 15 missing; 0 partially missing; 25 removed; 107 complete (approx. 73% complete).

## Processing Notes for Analysts
- Data provenance: direct laboratory measurements back to field sampling with clear methods for sample collection, storage, and transport.
- Standardised outputs: three CSV files enabling separation of cloud, rain, and combined (cloud+rain) chemistry, with explicit definitions of depth, concentration, and deposition.
- Quality assurance: explicit ion-balance QC steps and data-flag taxonomy; transparent criteria for data removal and flagging.
- Reuse potential: datasets designed for integration with other monitoring data streams, enabling temporal trend analysis, inter-site comparisons, and deposition modelling; alignment with standard monitoring portals and data-sharing practices.

## Non-marine Sulphate (Sea Salt Correction)
- Purpose: separate sea-salt-derived sulphate from non-marine (anthropogenic) sulphate in rain and cloud samples.
- Calculation: non-marine sulphate concentration derived from sodium content using sea-water composition; non-marine sulphate deposition computed from non-marine concentration and sample depth.

## References
- Cape, J.N.; Smith, R.I.; Fowler, D.; Beswick, K.; Choularton, T. 2010. Long-term monitoring of cloud chemical composition in the UK and implications for estimating wet deposition.
- Cape, J.N.; Smith, R.I.; Leaver, D. 2015. Missing data in spatiotemporal datasets: the UK rainfall chemistry network.
- Fowler, D. et al. 2006. UK Heavy Metal Monitoring Network.
- Fowler, D. et al. 2007. Acid Deposition Processes. Final report to Defra.