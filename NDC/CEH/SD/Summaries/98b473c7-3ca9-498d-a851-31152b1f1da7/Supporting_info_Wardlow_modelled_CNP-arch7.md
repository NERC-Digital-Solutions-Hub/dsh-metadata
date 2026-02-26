# Supporting documentation for data: 'Empirical and modelled carbon, nitrogen and phosphorus content of plants and soils from Wardlow Hay Cop, UK'

## Overview
- Datasets accompany a Taylor et al. (2021) Biogeosciences manuscript; empirical data used to calibrate a mechanistic C, N and P cycling model.
- Site: Wardlow Hay Cop, Derbyshire, UK, a long-term nutrient manipulation experiment on two grassland communities (acidic and limestone) established in the 1990s.
- Data focus: soil organic carbon (SOC), total nitrogen (SON/total N), and total phosphorus (P) stocks; also includes model outputs and comparisons.
- Sampling and data origins:
  - Soil C and N analyzed from 2019 samples (depths: limestone 10 cm, acidic 20 cm).
  - P data from 2003 (Horswill et al. reference) used for model initialization.
- Purpose: provide empirical data to calibrate the N14CP C–N–P model and to generate model outputs for comparison and interpretation of nutrient dynamics under long-term N deposition and experimental treatments.
- Timeframe:
  - Empirical data collected in 2019 after ~24 years of nutrient treatment.
  - Model outputs cover pre-industrial to present-day timescales, with 2020 as the current model year for C, N and P budgets.

## Site and treatments
- Wardlow hay cop long-term experiment: two grassland types (acidic and limestone) with four nutrient treatments:
  - 0N: control (background N deposition)
  - LN: low nitrogen
  - HN: high nitrogen
  - P: phosphorus addition
- Treatments replicated across three blocks (A, B, C). 
- Nutrient additions:
  - Nitrogen as NH4NO3; phosphorus as NaH2PO4·H2O.
  - Treatments applied monthly (1995–2017) or bi-monthly (from 2017); annual totals equivalent across time steps.

## Data and methods: empirical to model conversion
- Depth and sampling:
  - Limestone soil: analyzed to 10 cm.
  - Acidic soil: analyzed to 20 cm.
  - Organic and mineral horizons separated for analysis.
- Processing:
  - Samples dried, ground, and acid-stripped to remove inorganic carbon prior to IRMS analysis for C and N.
- Conversion to model units:
  - Empirical C, N, P data converted to model-compatible topsoil units (15 cm depth) in g m-2.
  - Soil mass per horizon estimated from horizon depth and bulk density; % C and % N converted to g m-2; P data converted using molecular weight and referenced conversions.
  - Limestone SOC assumed to apply to entire modeled topsoil depth; acidic SOC adjusted to reflect 15 cm topsoil (first 10 cm organic horizon + portion of mineral horizon).
- Model input data:
  - Empirical data calibrate two phosphorus cycling parameters: P Weath0 and P CleaveMax.
  - Model outputs reflect calibrated C, N and P pools, and budgets, plus responses to N deposition and nutrient treatments.

## The N14CP model
- Type: mechanistic C, N and P cycling model.
- Pools and flows: exchanges among plants, topsoil, subsoil, atmosphere, and leachate; stoichiometry governs C, N, P fluxes.
- Nutrient limitation: Liebig’s law-of-the-minimum framework with N–P interaction considerations.
- Model description reference: Davies et al. (2016) Global Biogeochemical Cycles.
- Inputs required: background N deposition, climate (temperature, precipitation), and plant functional history (land-use history analog).
- Outputs: modeled C, N and P pools and budgets; comparisons with empirical data; simulated responses to N deposition and nutrient treatments.
- Implementation: MATLAB-based; outputs and figures generated in MATLAB.

## Data files and contents (CSV)
- Wardlow_empirical_vs_modelled_CNP.csv
  - Content: figure 2 comparison of empirical vs. modelled C, N, P stocks; includes Obs, Sim, SE, Diff, Percent; separate for Acid and Limestone grasslands and treatments (0N, LN, HN, P).
- Wardlow_mean_CNP_difference.csv
  - Content: mean differences between simulated and observed data by grassland and nutrient treatment; includes SE.
- Wardlow_modelled_P_cleaving.csv
  - Content: P CleaveMax used by the model and total cleaved P in 2020; per grassland-treatment combination.
- Wardlow_modelled_N_deposition.csv
  - Content: effects of simulated N deposition (1800–2020) on C, N, P pools for 0N treatment; includes Y_1800, Y_2020, differences.
- Wardlow_modelled_nutrient_treatments.csv
  - Content: differences in modeled C, N, P stocks among nutrient treatments relative to 0N; after 1995 in the time series.
- Wardlow_modelled_CNP_budgets.csv
  - Content: modeled pool sizes for subsoil/topsoil SOC, SON; plant Biomass C and N; available/fixed N; weatherable/available P; sorbed P; SOP; other P pools; budgets for C, N and P; all in g m-2.

## Data completeness and limitations
- Phosphorus data: available for only half of the nutrient treatments (control 0N and high N HN); other P data were not collected empirically.
- Most data are model outputs calibrated to empirical data; the majority of the dataset comprises modelled results rather than raw observations.
- Data conversion to model units introduces assumptions about depth, bulk density, and horizon mixing.

## Temporal and spatial coverage
- Temporal:
  - Empirical data: 2019 sampling during ~24-year experimental timeline.
  - Model data: 1800–2020 for C, N and P budgets and deposition responses; 2020 values commonly used as model year.
- Spatial:
  - Two co-located grassland types (Acid, Limestone) within Wardlow Hay Cop site; three experimental blocks (A, B, C) with four nutrient treatments.

## Data access, provenance, and references
- Data are associated with a manuscript currently accepted for publication; DOI not available yet; refer to the catalogue record for full citation.
- Data collector: Christopher Taylor (PhD), supervised by Gareth Phoenix and Jessica Davies.
- Wardlow experimental setup references:
  - Morecroft et al. (1994), Journal of Ecology
  - Horswill et al. (2008), Environmental Pollution

## Relevance for GIS and map-based data products
- Data are in CSV format with clearly labeled variables across two grassland types and four treatments, enabling spatially-informed comparisons if linked to site coordinates or strata.
- Converted to consistent topsoil units (g m-2) at 15 cm depth, facilitating map-based visualization of soil C, N and P stocks and their changes over time and treatments.
- Outputs include model-predicted vs empirical values, budgets, and deposition responses, useful for creating thematic maps of nutrient pools, as well as time-series visualizations by treatment and grassland type.
- Although exact spatial coordinates are not provided, the structured design (two grassland types, three blocks, four treatments) supports GIS-layered representations when linked to site maps or field plots.