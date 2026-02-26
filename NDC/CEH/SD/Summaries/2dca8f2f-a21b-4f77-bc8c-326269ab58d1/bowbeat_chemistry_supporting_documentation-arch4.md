# Bowbeat cloud and rain chemistry dataset 2003-2006

## Overview
- Weekly pollutant concentrations and depositions in cloud and rain samples from the Bowbeat field site (UK) collected 2003–2006; site used for monitoring Ion chemistry, Heavy Metals, and Bacteria in cloud water.
- Measurements contributed to understanding how rain composition increases with altitude via the seeder-feeder mechanism; rain from high-level clouds is less effective at scavenging particles, with enhanced deposition when activated into cap-cloud droplets.
- Bowbeat was selected as a replacement high-elevation monitoring site in the Scottish Southern Uplands (replacing data impacted by adjacent forest growth); sampling ended in 2007 as seeder-feeder enhancement diminished.

## Experiment Location
- Bowbeat site coordinates: UK Grid NT283473 (N55:42:51 W3:08:35); 3.5 km north of Dunslair Heights monitoring site; open moorland at ~580 m above sea level; near Bowbeat wind farm.
- Site enclosed within a 25m x 25m fenced area on Bowbeat Rig.
- Sampling ceased in 2007 due to reduced seeder-feeder enhancement; Bowbeat replaced Auchencorth for ongoing monitoring.

## Fieldwork Instrumentation and Sampling
- Cloud sampler: stainless-steel frame, polyurethane coating, polypropylene toothed edge disc with fine polypropylene filaments forming an inverted cone to intercept cloud droplets; intercepts guided to a 5 L collecting bottle.
- Rain sampler: 20 cm HDPE funnel at 1.5 m height feeding a 20 L collecting container.
- Sampling frequency: approximately weekly from 03/09/2003 to 28/06/2006.
- Sample handling: weekly bottle weights recorded, sub-sampled into four 150 mL LDPE bottles (one for UKCEH lab ion analysis; others archived); ion chromatography analyzed for SO4 2-, NO3-, Cl-, NH4+, Na+, K+, Mg2+, Ca2+.
- Cloud vs. rain: cloud samples are ~90–95% as concentrated as rain; cloud samples may be contaminated by rain water; concentrations corrected to estimate true values.

## Data Structure and Nature and Units of Recorded Values
- Bowbeat_cloud_rain_chemistry_2003-2006: weekly concentrations and depositions in cloud samples (before rain adjustment) across multiple ion species (Na, K, Ca, Mg, NO3-N, NH4-N, Cl, SO4-S, non-marine SO4, etc.).
  - Includes fields for collection date, weights, sample volumes, depths, ion concentrations (mg/L), depositions (mg/(m^2)), and data quality flags.
  - Complex derivations include deposition from concentration and sample depth; non-marine sulphate calculated from sea-water Na and SO4 to separate marine vs. non-marine contributions.
- Bowbeat_rain_chemistry_2003-2006: weekly concentrations and depositions for rain samples (similar ions as above).
- Bowbeat_cloud_chemistry_2003-2006: cloud chemistry data adjusted for rain content (derived values: “Total” refers to combined rain and cloud contributions); depth-based calculations used to separate cloud from rain contributions.
- Key calculation notes:
  - Depth of sample = sample volume / 31.42 (mm) derived from geometry of the 20 cm funnel.
  - Non-marine sulphate = (Na concentration in sample) × (2.712 / 10.773) [sea-water constants] divided by 3 (to account for sulphate’s sulphur component).
  - Depth-based deposition uses depth and concentration values to compute deposition mass.
- Data organization included explicit units per field (e.g., mg/L, mg/(m^2), mm, g) and formulas where applicable.

## Data Cleaning and Quality Control
- Quality control performed in 2023 by S. Ferguson with guidance from J. N. Cape; used an R-based workflow to separate and standardize tables, produce continuous time series, and generate the public CSV files.
- Ion balance QC (based on Cape et al., 2015): (Σcations − Σanions) / (Σcations + Σanions) within -10% to +20% generally; if total ion concentration < 200 µeq L⁻¹, range extends to -10% to +30%; imbalances between -40% to -10% or +20% to +40% flagged; >+40% or < -40% removed.
- H+ not measured; multiple data quality flags used to indicate potential issues (e.g., RAT, HCA, HNH, MH, LMG, LCL, LIS, HK, LV, LNA, HMG, CAT, UNK, REM*, MV*, PM, NA*).
- Cloud chemistry data were excluded from ion balance if corresponding rain/cloud data were removed due to imbalance; cloud data with star flags only appear in cloud chemistry.
- Reasons for data removal included ion imbalance >40%, analytical reporting error, bottle overflow, and other flagged issues.
- Completeness (roughly):
  - Cloud&rain: 104 complete of 147 total (about 70–79% complete).
  - Rain: 120 complete of 147 total (about 81–83% complete).
  - Cloud: 107 complete of 147 total (about 73% complete).

## Completeness and Coverage
- Dataset completeness varies by component:
  - Cloud&rain: ~70–79% complete
  - Rain: ~81–83% complete
  - Cloud: ~73% complete
- Some data points missing due to unknown sampling gaps; some data removed due to data quality concerns.

## References
- Cape, J.N.; Smith, R.I.; Fowler, D.; et al. 2010. Long-term monitoring of cloud chemical composition in the UK and implications for estimating wet deposition.
- Cape, J.N.; Smith, R.I.; Leaver, D. 2015. Missing data in spatiotemporal datasets: the UK rainfall chemistry network.
- Fowler, D.; et al. 2006–2007. UK Heavy Metal Monitoring Network; Acid Deposition Processes (unpublished reports).