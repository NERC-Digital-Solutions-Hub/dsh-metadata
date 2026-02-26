# Supporting Documentation

- Overview
  - Subarctic peatland (Stordalen mire) near Abisko, Northern Sweden; heterogeneous landscape with thawing permafrost features.
  - Study focused on methane (CH4) fluxes using static chamber methodology across wetland and birch forest microhabitats during three campaigns in 2013.
  - Data generated include chamber fluxes, environmental covariates, and nutrient proxies; intended for analysis of CH4 dynamics and relation to vegetation and soil conditions.

- Site description
  - Location: 68°20' N, 19°03' E.
  - Landscape: freshwater lakes, pools, and non-inundated bog; fine-scale vegetation types include moss hummocks with shrubs, semiwet bog, wet bog pools, and graminoid-dominated bog.
  - Permafrost thaw/colonization processes increasing wetter areas.

- Experimental design and sampling regime
  - Campaigns: 16–27 June, 11–22 August, 16–29 September 2013.
  - Sampling occasions: n=4 (June), n=5 (August), n=5 for wetland and n=4 for birch forest (September).
  - Chambers: 60 static chambers measured concurrently (14 in birch forest, 46 in wetland); 4 wetland chambers relocated during the study, resulting in up to 64 chamber locations tracked in data.
  - Exact chamber locations documented in oneoff_data.csv.

- Collection methods
  - Static chambers: 40 cm diameter opaque polypropylene pipes; shallow 10 cm bases inserted a day before first sampling; 25 cm lid with pressure compensation plug sealed during 45-minute flux measurement.
  - Gas sampling: air (100 mL) drawn from chambers 4 times during each 45-minute period; samples stored in 20 mL glass vials and analyzed within ~1 month.
  - Ancillary measurements: soil temperature at 10 cm depth (4 replicates per occasion); chamber-height air temperature; volumetric soil moisture content (VMC) at 4 replicate points near bases; vegetation recorded visually within each chamber.
  - PRS probes: cation and anion probes deployed adjacent to each of the 60 chamber bases from late June to mid/late August and again in September; nutrient proxies include NO3--N, NH4+-N, and other elements.

- Fieldwork and laboratory instrumentation
  - Gas analysis: HP5890 Series II GC with electron capture detector (N2O) and flame ionisation detector (CH4).
  - In-situ measurements: Omega HH370 soil temperature probe; CS616 VMC probe.
  - PRS probes supplied by Western Ag Innovations Inc.

- Calibration steps and quality control
  - GC calibration: four-point calibration with standards approximately every 20 samples.
  - Detection limits: CH4 < 70 μg L-1; N2O < 7 μg L-1.
  - Standard concentrations documented for each calibration level.

- Analytical methods and data processing
  - Flux estimation: GCFlux version 2; evaluates five models per chamber group and selects the best-fitting model (linear, quadratic, and asymptotic variants; and an HMR-based model).
  - Output: instantaneous CH4 fluxes reported as nmol CH4 m^-2 s^-1; multiple flux estimates per chamber (best-fit, linear, quadratic, asymptotic, plus statistics).
  - Data quality indicators: adjusted R^2, confidence intervals (95%), and model fit indicators included for each chamber’s flux estimation.

- Data structure / content and units
  - RCfluxOutput.csv: fluxes for CH4 with columns for different models, best-fit method, chamber ID, chamber file name, HMR flux, 95% CIs, and model fit statistics.
  - oneoff_data.csv: chamber-level parameters measured once (e.g., chamber_id, lat/long, total NO3-N, NH4-N, and other PRS-derived nutrients, vegetation class).
  - Nutrients (PRS probes): per-chamber nutrient supply rates (NO3-N, NH4-N, Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd), total N+P proxies, vegetation class, and location coordinates.
  - veg_class: site vegetation category mapping (Hummock/Tall shrub, Semiwet, Wet, Tall graminoid, Water, Stone pits) with corresponding codes.
  - Table of per-forest daily CH4 parameters: Date, chamberID, sm_vmc_mean, soil_temp, air_temp (for forest chambers 1–14).
  - Metadata and data dictionary references included to aid interpretation of fields and units.

- Data governance, sharing, and framework considerations (aligned with monitoring framework authors)
  - Data are structured with explicit metadata on chamber geometry, deployment timing, environmental covariates, and methodology, enabling reproducibility and cross-site comparability.
  - Data processing relies on standardized models and transparent reporting of which model is used as best-fit, along with fit statistics and uncertainties.
  - Data sharing considerations highlighted by similar monitoring framework challenges include ensuring metadata completeness, avoiding data silos, and sharing raw and processed data to support policy scrutiny and future decision-making.
  - Primary data sources (GC outputs, chamber measurements, PRS nutrient data) are organized in clearly named CSV files with descriptive fields to facilitate governance, auditing, and re-use.

- References
  - Clough et al. 2015; Chamber Design guidelines
  - Jammet et al. 2017; Year-round CH4 and CO2 flux dynamics
  - Johansson et al. 2006; Decadal vegetation changes and net radiative forcing
  - Levy et al. 2011; Uncertainty quantification in static chamber fluxes
  - Malmer et al. 2005; Vegetation, climate changes, and net carbon sequestration

- Notes for monitoring framework relevance
  - Demonstrates end-to-end data lifecycle: site description, rigorous sampling design, standardized collection protocols, instrument calibration, data processing with model selection, and comprehensive data documentation.
  - Illustrates practical challenges encountered (e.g., chamber relocations, complex metadata needs, integration of biological and chemical proxies) and how these were addressed through structured data files and documentation.
  - Provides a model for ensuring data openness, traceability, and governance in environmental health monitoring datasets.