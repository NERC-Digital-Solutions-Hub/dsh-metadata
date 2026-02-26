# Carbon and nitrogen flux, meteorological, management, and soil data from a grazed, cut and fertilised temperate grassland in south east Scotland

## Overview
- Multi-parameter data package from Easter Bush, South East Scotland, focusing on a grazed, cut and fertilised temperate grassland.
- Only data from the South field are included; measurement equipment located between the two fields.
- Data cover meteorology, soil properties, carbon and nitrogen fluxes, leaching, deposition, and management practices across the study period.

## Spatial and temporal coverage
- Location: Easter Bush field site, 10 km south of Edinburgh; coordinates 03°02'W, 55°52' N; 190 m a.s.l.
- Site description: two adjacent fields (South and North); South field data are provided here.
- Climate of the site: mean annual rainfall 947 ± 234 mm; mean annual temperature 9.0 ± 0.4 °C.
- Soil: imperfectly drained Macmerry soil series, Eutric Cambisol; pH 5.1, clay 20–26%; groundwater table ~0.85 m; rooting depth ~0.31 m.
- Sampling period: extensive measurements from 2002–2011 for most datasets; N leaching data 2006–2008; soil C/N cores from May 2004 and May 2011.

## Data holdings and file types
- livestock_yield_fertiliser_daily.csv: stocking/density, animal numbers, forage yield and nutrient offtake, fertiliser inputs.
- N_C_leaching_flux_daily.csv: leaching fluxes for DIC/DOC/DON, NH4, NO3, plus modeled groundwater recharge and evapotranspiration.
- N_C_leaching_conc_sampling_period.csv: leaching concentrations (DIC, DOC, TN, NH4, NO3).
- Dry_N_conc_monthly.csv: monthly concentrations of dry-deposition N species (NH3, HNO3, NH4+, NO3-).
- Flux_daily.csv: patch-scale fluxes including GPP, NPP, ecosystem respiration, NEE, CH4, N2O (chamber and EC), NOx; also related flux metrics.
- metdata_daily.csv: meteorological and soil sensors data (precipitation, temperature, soil temperature, volumetric water content, rain gauge, etc.).
- soil_C_N_oneoff.csv: total soil N and C contents from May 2004 and May 2011 across depth layers (0–60 cm).
- metdata_daily.csv & additional metadata fields described in the dataset documentation.

## Key variables and units (selected examples)
- Flux_daily.csv: GPP (g C m^-2 d^-1), NPP (g C m^-2 d^-1), EcoResp (g C m^-2 d^-1), NEE (g C m^-2 d^-1), CH4 (g C-CH4 m^-2 d^-1), N2O (g N-N2O m^-2 d^-1), NOx (g N-NO m^-2 d^-1).
- metdata_daily.csv: precipitation (mm d^-1), temperature (°C; daily avg/min/max), soil temperature (°C; daily avg), soil volumetric water content (%; daily avg).
- livestock_yield_fertiliser_daily.csv: stocking density (LSU m^-2 d^-1), animal counts, YIELD DM offtake (g DM m^-2 d^-1), YIELD N/C offtake (g N/C m^-2 d^-1), fertiliser inputs (N, C).
- N_C_leaching_flux_daily.csv: DIC/DOC leaching flux (g C m^-2 d^-1), DON/NH4/NO3 leaching flux (g N m^-2 d^-1), modeled groundwater recharge (mm d^-1), precipitation (mm d^-1), ET (mm d^-1).
- N_C_leaching_conc_sampling_period.csv: DIC/DOC leaching concentrations (mg C L^-1), TN/NH4/NO3 concentrations (mmol N L^-1).

## Sampling regime and management details
- Management: continuous grazing by predominately ewes and lambs; occasional heifers; variable stocking densities; silage cuts on specific dates; ammonium nitrate fertiliser 3–4 times/year (56 kg N ha^-1 per application); in 2008 an additional mineral N application using urea; cattle slurry applied in 2004 and 2005.
- Harvest and inputs: yield estimates, N and C content analyses of vegetation; slurry inputs with triplicate sampling for NH3/NH4, dry matter, total N, total C, pH, NO3.
- Leaching measurements: installed suction cups at 30 cm and ~90 cm depths; slope and hollow locations tracked, but leaching data focused on slope for dataset inclusion.
- Dry deposition measurements: DELTA system located ~300 m from the field, sampling NH3, HNO3, NH4+, NO3- at 1.5 m height.
- Flux measurement methods:
  - CO2 exchange: eddy covariance system (3D ultrasonic anemometer + LI-COR 7000 IRGA); QC using standard fouling/quality checks; u* filtering (u* < 0.2 m s^-1 flagged); gap-filled using online Reichstein et al. method.
  - N2O and CH4: closed chambers with GC analysis; weekly to fertilisation events.
  - NOx: autochamber system, multiple chambers, measurements four times per day in cycling sequence.

## Data quality and processing
- Quality control: standard procedures for eddy covariance data; removal of implausible values; gap-filling for NEE; linearity checks for N2O/CH4 chambers.
- Missing data: blank values indicate days with no measurements or data unavailable.
- Data integration: datasets span different temporal resolutions (daily, monthly, one-off soil cores); users may need temporal harmonisation to combine layers.

## GIS-specific considerations and potential uses
- Spatial layer ideas: flux maps for NEE, N2O, CH4, NOx; soil C/N stock maps by depth; precipitation and soil moisture overlays; fertiliser and grazing intensity layers.
- Temporal analyses: link flux patterns to management events (fertiliser applications, silage cuts, slurry applications) and weather sequences.
- Data fusion: combine with site-level elevation, slope, and drainage patterns to contextualise leaching and gas flux variability.
- Data preparation: align time stamps, manage missing values, regrid to common temporal resolution (e.g., daily or monthly) for map-based visualization.

## References and provenance
- Documented methodological references for flux calculations, QC procedures, and data interpretation (e.g., Reichstein et al., Foken & Wichura, Di Marco et al., Sutton et al., Amthor, etc.).
- Specific site and dataset metadata described in the data description and accompanying figures/notes.