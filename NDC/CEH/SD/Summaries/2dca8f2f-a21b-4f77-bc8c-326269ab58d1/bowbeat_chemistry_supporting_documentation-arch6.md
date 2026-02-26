# Bowbeat cloud and rain chemistry dataset 2003-2006

- Provides weekly pollutant concentrations and depositions in cloud, rain, and combined (cloud&rain) samples from the Bowbeat field site (2003–2006).
- Aims to monitor and model cloud and rain water composition and deposition at high elevation, including the seeder-feeder effect where rain composition increases with altitude.
- Data derived from field campaigns at Bowbeat to support understanding of atmospheric chemistry and wet deposition processes in the UK.

## Experiment location
- Bowbeat site located at UK Grid reference NT283473 (N55:42:51 W3:08:35), ~580 m above sea level, near Bowbeat wind farm.
- Replaced nearby Dunslair monitoring site in 2003/4 due to forest growth affecting data quality; sampling ended in 2007 as seeder-feeder enhancement diminished.
- Site setup included a 25 m x 25 m enclosure for cloud and rain collection equipment.

## Fieldwork instrumentation and sampling
- Cloud sampler: stainless-steel frame with a polyurethane coating, polypropylene toothed edge disc, and fine polypropylene filaments forming an inverted cone to intercept cloud droplets; collected into a 5 L bottle.
- Rain sampler: 20 cm diameter HDPE funnel at 1.5 m height feeding into a 20 L collection container.
- Sampling cadence: approximately weekly between 03/09/2003 and 28/06/2006.
- Sample handling: weekly bottle weights recorded manually, data transferred to Excel; four sub-samples prepared (one for UKCEH lab ion analysis, three stored long-term).
- Laboratory analysis: ion chromatography for ions including SO4^2-, NO3^-, Cl^-, NH4^+, Na^+, K^+, Mg^2+, Ca^2+; resulting data provided as CSVs.
- Cloud samples required correction for rain contamination to better reflect true cloud concentrations; cloud data are derived from rain and cloud&rain data.

## Data structure, values, and units
- Three CSV files:
  - Bowbeat_cloud_rain_chemistry_2003-2006.csv (cloud, rain, and combined concentrations/depositions before rain adjustment)
  - Bowbeat_rain_chemistry_2003-2006.csv (weekly rain concentrations/depositions)
  - Bowbeat_cloud_chemistry_2003-2006.csv (cloud data adjusted for rain content, derived from cloud&rain and rain data)
- Key fields (examples):
  - Collection_Date, Depth, Sample_Volume, Weight_Bottle, Weight_Bottle+Sample
  - For each ion: Concentration (e.g., Na_Conc, K_Conc, Ca_Conc, Mg_Conc, NO3-N_Conc, NH4-N_Conc, Cl_Conc, SO4-S_Conc) and Deposition (e.g., Na_Dep, K_Dep, Ca_Dep, Mg_Dep, NO3-N_Dep, NH4-N_Dep, Cl_Dep, SO4-S_Dep)
  - SO4-S_NON-MARINE_Conc and SO4-S_NON-MARINE_Dep (non-marine sulphate estimates)
  - Data_Flag and Reason (quality control flags and reasons for data removal)
- Cloud chemistry data are adjusted for rain content; concentrations are derived from depositions and depths as described in the dataset documentation.
- Depth calculations:
  - Depth of sample is derived from sample volume and funnel geometry; formulas are provided for precise depth in mm.
- Sea-water correction:
  - Non-marine sulphate is estimated using sea-water concentrations: Na in sea water ≈ 10.773 g/kg and SO4 in sea water ≈ 2.712 g/kg; non-marine SO4 is calculated as [Na] × (SO4/Na) in order to separate sea-salt sulphate from atmospheric sulphate.

## Derived adjustments and quality control
- Cloud chemistry is derived from rain and cloud&rain data; cloud depth and concentrations are adjusted accordingly.
- Non-marine sulphate (SO4-S_NON-MARINE) is computed to account for sea-salt contributions to overall sulphate.
- Quality control approach (H+ not measured):
  - Ion balance check: (Σ cations − Σ anions) / (Σ cations + Σ anions)
  - Acceptable balance: -10% to +20% (or -10% to +30% if total ion concentration < 200 µeq L^-1)
  - Data flagged if ion balance lies outside typical range; data removed if imbalance > +40% or < -40%.
- Data flags explain potential issues:
  - RAT (Unusual Na ratios), HCA (High Ca), HNH (High NH4-N), MH (Imbalance from missing H+), LMG (Low Mg), LCL (Low Cl), LIS (Low ionic strength), HK (High K), LV (Low volume), HMG (High Mg), CAT (Low cations), UNK (Unknown reason), REM*, MV*, PM, NA* (various removal or data quality reasons)
- Cloud chemistry data excluded from the ion balance if rain-related data were removed due to large imbalance; cloud-specific flags with * indicate cloud data specifics.

## Completeness and data availability
- Cloud&rain data: 147 possible weekly data points; complete data ~104 points (about 70-79% complete).
- Rain data: 147 possible; complete data ~120 points (about 81-83% complete); missing/removed data noted.
- Cloud data: 147 possible; complete data ~107 points (about 73% complete); some data removed or flagged.

## Data removal and completeness notes
- Some data removed due to:
  - Ion imbalance >40% or < -40%
  - Analytical reporting errors
  - Bottle overflow (validated via volume vs. time graphs)
  - Other flagged issues (as documented in the Reason column)
- Cloud chemistry data removal tied to dates with large ion imbalances in rain-related data.

## References
- Cape, J.N.; Smith, R.I.; Fowler, D.; Beswick, K.; Choularton, T. (2010). Long-term monitoring of cloud chemical composition in the UK and implications for estimating wet deposition.
- Cape, J.N.; Smith, R.I.; Leaver, D. (2015). Missing data in spatiotemporal datasets: the UK rainfall chemistry network.
- Fowler, D. et al. (2006-2007). UK Heavy Metal Monitoring Network and Acid Deposition Processes (unpublished CEH reports).