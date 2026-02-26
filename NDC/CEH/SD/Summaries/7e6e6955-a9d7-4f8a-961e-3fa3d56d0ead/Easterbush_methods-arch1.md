# Carbon and nitrogen flux, meteorological, management, and soil data from a grazed, cut and fertilised temperate grassland in south east Scotland

## Site description and overview
- Location: Easter Bush, South East Scotland, 10 km south of Edinburgh; two adjacent fields (South and North); South field data included; meteorological and eddy covariance measurements between fields.
- Climate/soils: mean annual rainfall 947 ± 234 mm; mean annual temperature 9.0 ± 0.4 °C (2002–2010); soil is imperfectly drained Macmerry soil series (Eutric Cambisol), pH 5.1, 20–26% clay; groundwater ~0.85 m depth; main rooting depth ~0.31 m.
- Land use: permanent grassland (>20 years) with >99% Lolium perenne and <0.5% Trifolium repens.
- Timeframe: measurements January 2002–May 2011; South field data focus; key data periods: 2002–2010 (with some one-off soil sampling in 2004 and 2011).

## Data regime and structure
- Data regime: a suite of carbon and nitrogen fluxes, meteorology, management, and soil measurements collected at the site.
- Primary data files (with general focus):
  - livestock_yield_fertiliser_daily.csv (2002–2010): grazing activity, stocking densities, animal numbers, yield and nutrient offtake, and fertilizer inputs.
  - N_C_leaching_flux_daily.csv and N_C_leaching_conc_sampling_period.csv (2006–2008): soil leaching fluxes and concentrations for C and N species; includes modelled groundwater recharge and precipitation/ET context.
  - Dry_N_conc_monthly.csv (2002–2010): monthly concentrations of dry-deposition N species (NH3, HNO3, NH4+, NO3-).
  - Flux_daily.csv (2002–2010): ecosystem fluxes including GPP, NPP, EcoResp, NEE, CH4, N2O (chamber and EC), NOx; also provides NOx flux context.
  - metdata_daily.csv (2002–2010): meteorological and soil-physical context (soil temp at multiple depths, soil moisture, precipitation, air temp).
  - soil_C_N_oneoff.csv (May 2004 and May 2011): soil total N and C by depth (0–60 cm) from grid sampling.
  - metdata_daily.csv (see above for contents) and additional metadata on units.
- Scope: data cover the South field during the grazing/cutting/fertilising experiment, with blank values where measurements were not taken.

## Management and sampling regime
- Grazing and stock management: continuous grazing by ewes and lambs; occasional cows/heifers; stocking densities varied by year; lambs present April–September.
- Forage management: silage cuts on 1 June 2002, 8 August 2002, and 29 May 2003.
- Fertilisation: ammonium nitrate or urea fertiliser 3–4 times per year (typical 56 kg N ha^-1 per application); 2008 included a fifth mineral N application using urea; cattle slurry applied on 28 September 2004 and 27 March 2005.
- Slurry nutrient analysis: three samples per application analyzed for NH3/NH4, dry matter, total N, total C, pH, NO3^-; total N and C import calculated from slurry volume and analyses.
- Plant sampling: a subsample of harvested vegetation dried for plant N and C analysis.
- Yield expectations: harvest yields ~15 t fresh weight ha^-1 y^-1 (first cut) and ~10 t FW ha^-1 y^-1 (second cut).

## Measurements and methods
- Gas fluxes:
  - CO2: Net Ecosystem Exchange (NEE) via eddy covariance; GPP and TER partitioned using standard gap-filling, with NEE interpreted as GPP minus TER; NPP approximated as 50% of GPP.
  - CH4: soil CH4 fluxes via closed chambers (weekly to fertiliser events).
  - N2O: soil N2O fluxes via eddy covariance (2002–2003) and closed chambers (2006–2009).
  - NOx: soil NOx fluxes (June 2009–Aug 2010) using autochamber system with multiple chambers and control.
- Soil and leaching:
  - Leaching cups installed at slope and hollow locations; data reported for DIC, DOC, DON, DIN, NH4+, NO3-; groundwater recharge estimated via a soil water model.
  - Dry deposition: nearby DELTA system measures NH3, HNO3, NH4+, NO3- concentrations with a denuder-based setup.
  - Soil cores: May 2004 and May 2011 sampled across a grid (10 m spacing) to determine total soil C and N; 0–60 cm depth segmented into multiple layers; dry combustion used to quantify SOC and SON.
- Metadata and environmental context:
  - Soil temperature and volumetric water content recorded at 3.5, 7.5, 15, and 30 cm; rainfall by tipping bucket; air temperature recorded by integrated transmitter.
- Data quality:
  - Quality control steps for EC/NEE data; standard flux calculation procedures; explicit notes on data gaps and missing values.

## Data fields and primary units (highlights)
- Flux_daily.csv: GPP, NPP, EcoResp, NEE (g C m^-2 d^-1); CH4 (g C-CH4 m^-2 d^-1); N2O (g N-N2O m^-2 d^-1); NOx (g N-NO m^-2 d^-1).
- metdata_daily.csv: Precipitation (mm d^-1); Temperature (°C daily average, min, max); Soil temperature (°C); Volumetric water content (%).
- livestock_yield_fertiliser_daily.csv: Stocking density (LSU m^-2 d^-1); animal numbers; YIELD DM (g DM m^-2 d^-1); YIELD N (g N m^-2 d^-1); YIELD C (g C m^-2 d^-1); mineral/organic N and C fertiliser inputs.
- Dry_N_conc_monthly.csv: DELTA NH3, HNO3, NH4+, NO3- concentrations (μg m^-3).
- N_C_leaching_flux_daily.csv: DIC/DOC/DON/NH4/NO3- leaching fluxes (g C or g N m^-2 d^-1); modelled groundwater recharge (mm d^-1); precipitation and ET context.
- N_C_leaching_conc_sampling_period.csv: DIC/DOC (mg C L^-1); TN/NH4/NO3- (mmol N L^-1) concentrations.
- soil_C_N_oneoff.csv: SOC and SON (kg C m^-2; kg N m^-2) by depth.
- metdata and references provide the methodological context for data interpretation.

## Data usage and potential analyses
- Enables construction of a comprehensive carbon and nitrogen budget for a grazed, cut, and fertilised temperate grassland.
- Enables analysis of how management actions (grazing, cuts, fertiliser events, slurry applications) affect GPP, TER, NEE, and greenhouse gas fluxes (CH4, N2O, NOx).
- Facilitates linking aboveground production, carbon and nitrogen allocation, soil C/N pools, and leaching to flux dynamics.
- Supports assessment of dry deposition contributions to atmospheric N deposition at a nearby site and integration with soil/surface flux measurements.
- Data gaps are documented; some years have limited or no measurements for certain fluxes (e.g., NOx, EC fluxes), which should be considered in analyses.

## Notes and references
- The dataset references several methodological and instrumentation papers for flux calculations, QC, and measurement techniques (e.g., Reichstein et al., Foken & Wichura, Di Marco et al., Sutton et al., etc.).
- Soil and management details, including fertilizer composition and slurry analysis, are described to support interpretation of nutrient fluxes and budget calculations.