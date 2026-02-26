# Site Description

- Stordalen mire is a subarctic peatland (68°20' N, 19°03' E) near Abisko, Northern Sweden.
- Landscape is heterogeneous with permafrost thaw features (pål­sas), wetter areas expanding over time, and a mix of freshwater lakes, ponds, bogs, and non-inundated areas.
- Vegetation categories at a finer scale include moss hummocks with shrubs, semiwet bogs, wet bog pools, and graminoid-dominated bogs; forested areas include birch with various moisture regimes.

## Experimental Design and Sampling

- Sampling campaigns in 2013: 16–27 June (n=4), 11–22 August (n=5), 16–29 September (n=5 wetland; 4 birch forest).
- 60 static chambers measured: 14 in birch forest, 46 in wetland. Four wetland chambers were relocated during the study.
- Chamber locations are documented in oneoff_data.csv; total chamber count can reach 64 due to relocations.
- Vegetation and site characteristics recorded per chamber; soil temperature and air temperature measured; volumetric soil moisture content (VMC) recorded near chamber bases.
- Nutrient data collected with PRS probes adjacent to each chamber base; deployment and correction details noted.

## Collection Methods

- Static chambers: 40 cm diameter opaque PP pipes with 10 cm deep bases inserted a day before first sampling; lids sealed during ~45 min flux measurements.
- Gas sampling: 100 mL chamber air collected 4 times during the 45-minute period and stored in 20 mL glass vials for lab analysis.
- Measurements recorded: soil temperature at 10 cm depth, chamber-height air temperature, VMC at four replicate points near bases; vegetation visually recorded within each chamber.
- PRS probes deployed near chamber bases from late June to mid/late August; post-deployment processing conducted by Western Ag Innovations Inc.
- Chambers 61–64 were submerged; no PRS probes installed there.

## Fieldwork and Instrumentation

- Gas analysis: HP5890 Series II GC with electron capture detector (N2O) and flame ionisation detector (CH4).
- Detection limits: CH4 < 70 μg L−1; N2O < 7 μg L−1.
- In-situ measurements: Omega HH370 soil temperature probe; CS616 Soil Water Content Reflectometer for VMC.
- PRS probes supplied by Western Ag Innovations Inc.

## Calibration and Quality Control

- Gas concentrations converted using a 4-point calibration with CH4 and N2O standards, run roughly every 20 samples.
- CH4 and N2O standard concentrations provided (four standard levels).

## Data Structure, Nature, and Units

- RCfluxOutput.csv: CH4 fluxes calculated by GCFlux v2, with multiple model fits per chamber (linear, quadratic, linear2nd, quadratic2nd, asymptotic); best-fit model selected per chamber; instantaneous flux units: nmol CH4 m−2 s−1.
  - Columns include flux_linear, flux_quadratic, flux_linear2nd, flux_quadratic2nd, flux_asymptotic, bestFitMethod, chamberID, and related model statistics (e.g., adjR², 95% CI).
- oneoff_data.csv: chamber-specific parameters measured once; includes chamber_id, Total_N_PRS, NO3-N, NH4-N, various nutrient concentrations (Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd, etc.), veg_class, lat, long.
  - veg_class corresponds to vegetation types listed in Table 2.
- Table 2: Site vegetation classifications for wetlands (Hummock/Tall shrub; Semiwet; Wet; Tall graminoid; Water; Stone pits) with subcategories and representative species.
- forest parameters_daily.csv: daily CH4 parameters per chamber; fields include Date, chamberID, sm_vmc_mean, soil_temp, air_temp.
  - Describes parameters for forest chambers (1–14) across varying moisture regimes (very wet to dry).

## Site and Vegetation Characteristics

- Forest chambers (1–14) cover a gradient from very wet to dry conditions; vegetation and moisture regime recorded for context.
- Wetland chambers cover diverse microhabitats including hummocks, sedges, and waterlogged areas; PRS nutrient fluxes include an array of measured elements.

## References

- Clough et al. 2015: Chamber Design guidelines; Nitrous Oxide Chamber Methodology.
- Jammet et al. 2017; Year-round CH4 and CO2 flux dynamics in subarctic freshwater ecosystems.
- Johansson et al. 2006; Decadal vegetation changes and net radiative forcing in northern peatlands.
- Levy et al. 2011; Quantification of uncertainty in trace gas fluxes measured by static chambers.
- Malmer et al. 2005; Vegetation and climatic changes affecting net carbon sequestration in subarctic mires.