# Carbon and nitrogen flux, meteorological, management, and soil data from a grazed, cut and fertilised temperate grassland in south east Scotland

## Overview and site context
- Experimental site: Easter Bush, South East Scotland (near Edinburgh), two adjacent fields (South and North); data in this dataset pertain to the South field.
- Climate and soils: mean annual rainfall ~947 ± 234 mm; mean annual temperature ~9.0 ± 0.4 °C. Imperfectly drained Macmerry soil (Eutric Cambisol) with pH ~5.1, clay 20–26%, groundwater table around 0.85 m; main rooting zone ~0.31 m.
- Land management: permanent grassland (>20 years) dominated by Lolium perenne (>99%); occasional clover; grazing by sheep (ewes and lambs) with some heifers in calf; silage cuts in 2002–2003; variable mineral and organic fertilisation; cattle slurry applied in 2004–2005.

## Sampling regime and data collection period
- Measurements span January 2002 to May 2011.
- Data files with defined start and end dates include:
  - livestock_yield_fertiliser_daily.csv (2002-2010)
  - N_C_leaching_flux_daily.csv (2006-2008)
  - N_C_leaching_conc_sampling period.csv (2006-2008)
  - Dry_N_conc_monthly.csv (2002-2010)
  - Flux_daily.csv (2002-2010)
  - metdata_daily.csv (2002-2010)
  - soil_C_N_oneoff.csv (May 2004 and May 2011)

## Data objects and contents (grouped by file type)

- livestock_yield_fertiliser_daily.csv
  - Management and grazing data: Date; stocking density (LSU and head per field); animal numbers by species; YIELD DM offtake; N, C offtake; mineral and organic fertiliser inputs.
  - Practices: continuous grazing, silage cuts (1 June 2002, 8 August 2002, 29 May 2003); fertiliser application roughly 56 kg N ha-1 per event; 2008 included an additional mineral N application with urea; cattle slurry applied in Sept 2004 and Mar 2005.
  - Sub-samples of slurry analyzed for NH3/NH4, dry matter, total N, total C, pH, NO3.

- N_C_leaching_flux_daily.csv and N_C_leaching_conc_sampling_period.csv
  - Leaching measurements: DIC, DOC (carbon), DON, DIN (N), NH4, NO3 fluxes; modelled groundwater recharge; precipitation and evapotranspiration data.
  - Sampling setup: suction cups installed at slope and hollow positions (only slope data included); sampling every 2–3 weeks; leachate determined using soil-water model (Kindler et al., 2011).

- Dry_N_conc_monthly.csv
  - Dry deposition concentrations: NH3, HNO3, NH4+, NO3- from a nearby DELTA system (300 m away) measured monthly.
  - System description: denuder-based sampling with a calibrated flow and a high-sensitivity monitor.

- Flux_daily.csv
  - N2O fluxes: measured 2002–2003 by eddy covariance with a TDLas instrument; 2006–2009 via closed static chambers.
  - NOx fluxes: measured June 2009–Aug 2010 using an autochamber system with multiple chambers and a control chamber.
  - CO2 exchange: Net Ecosystem Exchange (NEE) via eddy covariance (3D ultrasonic anemometer + IRGA); data quality control filters applied (friction velocity, plausible CO2 concentration and flux ranges, LE, H flux ranges); NEE partitioning into GPP and TER; NPP estimated as 50% of GPP.
  - CH4 and NOx: CH4 fluxes measured with GC; NOx measurements described above.
  - Data cadence: typically weekly measurements, more frequent around fertilisation events.

- metdata_daily.csv
  - Meteorological and soil context: daily date; precipitation; air temperature (daily average, min, max); soil temperature at depths (3.5, 7.5, 15, 30 cm) and volumetric soil moisture; soil moisture via TDR; rainfall via tipping bucket; HUMITTER for air temperature.

- soil_C_N_oneoff.csv
  - Soil carbon and nitrogen stocks: soil mass and SOC and SON (kg C m-2 and kg N m-2) by depth layers (0–5, 5–10, 10–20, 20–30, 30–40, 40–50, 50–60 cm) from two sampling events (May 2004 and May 2011).

- N_C_leaching_flux_daily.csv and N_C_leaching_conc_sampling_period.csv (conceptual data fields)
  - Concentrations: DIC, DOC (mg C L-1) at sampling; TN, NH4, NO3 concentrations (mmol N L-1) in leachate.
  - Flux calculations: leachate constituents per time period, with model-derived groundwater recharge and daily meteorological context.

## Data quality, standards, and units
- Units and value definitions are provided for each dataset in the metdata_daily.csv and flux files.
  - GPP, NPP, EcoResp, NEE, CH4, N2O, NOx fluxes are reported with specific units (e.g., g C m-2 d-1; g N-N2O m-2 d-1; g N-NO m-2 d-1).
  - Temperature (°C), soil moisture (%), precipitation (mm d-1), and other meteorological variables are specified.
- Blank values indicate days with no measurements or data gaps.
- Data undergo quality control for flux measurements (e.g., minimum turbulence u* thresholds; plausible CO2 concentration ranges; sensible and latent heat flux bounds) and standard gap-filling approaches for NEE (Reichstein et al., 2005).

## Data governance, provenance, and availability
- The dataset comprises multi-year, multi-method measurements of carbon and nitrogen fluxes, meteorology, and soil/management variables from a grazed, cut and fertilised temperate grassland.
- Data descriptions include detailed methodologies, instrumentation, sampling schemes, calibration references, and data processing notes (e.g., NEE gap-filling and flux partitioning methodology; chamber vs. EC measurement approaches; sample depths and core handling for soil C and N).
- File naming conventions and explicit start/end dates support traceability, integration, and re-use in subsequent analyses.
- Documentation notes indicate that blank values reflect missing measurements; several datasets are one-off or cover sub-intervals within the broader monitoring window.
- The dataset is accompanied by a robust set of references for methods and data interpretation, enabling proper governance, reuse, and reproduction of analyses.

## References and related work
- Includes methodological references for NEE partitioning, flux measurement techniques, and related soil and gas analysis methods (e.g., Reichstein et al. 2005; Di Marco et al. 2004; Butterbach-Bahl et al. 1997; Kindler et al. 2011; Helfter et al. 2015; several site-specific studies).