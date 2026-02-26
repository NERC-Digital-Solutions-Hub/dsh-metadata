# Supporting Documentation

- Site context
  - Stordalen mire is a subarctic peatland in Northern Sweden with heterogeneous habitats (wetlands, birch forest, permafrost–affected zones) and vegetation types including hummocks, semiwet bogs, wet bog pools, and graminoid-dominated bogs.
  - In recent years, wetter conditions have increased due to permafrost thaw and pålsas collapse.

- Experimental design and sampling regime
  - Sampling campaigns in 2013: 16–27 June (n=4 occasions), 11–22 August (n=5), 16–29 September (n=5 wetland, 4 birch forest).
  - 60 static chambers measured simultaneously (14 in birch forest, 46 in wetlands); 4 wetland chambers were relocated after initial sampling, bringing total possible chamber count to 64 at times.
  - Exact chamber locations documented in oneoff_data.csv.

- Data collection methods
  - Static chambers: 40 cm diameter opaque polypropylene, shallow bases inserted 10 cm depth the day before first sampling; lids sealed during ~45 min flux measurements.
  - Gas sampling: 100 ml chamber air drawn 4 times during the 45-minute period; samples stored in 20 mL glass vials and analyzed in Edinburgh within about one month.
  - Environmental covariates: soil temperature at 10 cm depth (4 replicate points), chamber-height air temperature (subset coverage), and 4 replicate volumetric soil moisture content (VMC) measurements adjacent to each chamber base.
  - Vegetation within each chamber recorded by visual inspection.
  - PRS probes: cation and anion PRS probes deployed adjacent to each of the 60 chamber bases (deployment 26/06/2013–13/08/2013 and 21/08/2013–23/09/2013). Some chambers (61–64) were submerged, so no PRS probes installed there.
  - Forest chamber 1–14 parameters indicate very wet to dry conditions.

- Field equipment and laboratory instrumentation
  - Gas chromatography: HP5890 Series II GC with electron capture detector (N2O) and flame ionisation detector (CH4).
  - In-situ measurements: Omega HH370 soil temperature probe; CS616 VMC detector for soil moisture.
  - PRS probes supplied by Western Ag Innovations Inc.

- Calibration, quality control, and data processing
  - GC calibration: four-point calibration with standards at listed CH4 and N2O concentrations (Table 1 standards provided).
  - Flux calculation: GCFlux software v2, which tests multiple models (linear, quadratic, linear2nd, quadratic2nd, asymptotic) and uses the best-fit for each chamber. Reported CH4 fluxes are in nmol CH4 m^-2 s^-1.
  - Data products include multiple flux estimates per chamber from different models, along with best-fit selection and fit diagnostics.

- Data structure, files, and units
  - RCfluxOutput.csv: contains CH4 fluxes computed by GCFlux, with columns for various model fluxes (flux_linear, flux_quadratic, flux_linear2nd, flux_quadratic2nd, flux_asymptotic), best-fit selections, fit quality metrics (Adj R^2, 95% CI), chamber identifiers, and related metadata.
  - oneoff_data.csv: chamber-specific parameters measured once (e.g., chamber_id, Total_N_PRS, individual PRS nutrient fluxes, lat/long, vegetation class).
  - Table 2 and veg_class coding describe vegetation types used in site characterization.
  - nutrients (anions and cations) from PRS probes: include NO3--N, NH4+-N, and multiple element concentrations (Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd) with units micrograms/10 cm^2/burial length; includes veg_class, lat, long.
  - parameters_daily.csv (forest subset): daily CH4-related parameters per chamber, including date, chamberID, sm_vmc_mean, soil_temp, and air_temp.
  - Date formats and unit conventions are documented within the data files’ descriptions.

- Metadata and site characteristics
  - Location: Stordalen mire, near Abisko, Northern Sweden (approximate coordinates provided in oneoff_data.csv).
  - Site classification for vegetation and habitat types linked to Table 2 references (global change biology classification).
  - The dataset captures both gas flux measurements and supporting environmental context (soil moisture, temperature, nutrients, vegetation).

- Data quality considerations and limitations
  - Incomplete coverage due to chamber replacements (4 wetlands relocated) and underwater chambers (61–64) lacking PRS data.
  - Heterogeneous habitat and presence of older/legacy databases necessitate bespoke, non-interoperable solutions for some parameters.
  - The PRS nutrient data represent mean values across two deployment windows; care should be taken when aligning to flux measurements outside those windows.
  - Flux calculations rely on multiple models with best-fit selection per chamber, which may affect comparability across chambers and campaigns.

- References and methodological context
  - Chamber design and methodology guidance (Clough et al., 2015) for static chambers.
  - CH4 and CO2 flux dynamics in subarctic ecosystems (Jammet et al., 2017; Malmer et al., 2005; Johansson et al., 2006) providing site context.
  - Uncertainty quantification in trace gas fluxes measured by static chamber methods (Levy et al., 2011).

- Practical notes for data users and stewards
  - Verify chamber IDs align across RCfluxOutput.csv, oneoff_data.csv, and parameters_daily.csv (especially with the 61–64 underwater instances and chamber replacements).
  - Reference Table 2 vegetation classifications when analyzing habitat-specific flux patterns.
  - Use the best-fit flux estimates (flux_bestfit) when reporting CH4 fluxes, while consulting the accompanying model diagnostics (adjr2, ci95) for quality checks.
  - Ensure alignment of spatial metadata (lat/long) with flux measurements to enable habitat- and site-scale analyses.