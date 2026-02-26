# Supporting Documentation

## Overview
- Describes the Stordalen mire study site in subarctic Northern Sweden, a heterogeneous peatland with various vegetation types and hydrological conditions.
- Documents sampling campaigns, chamber-based flux measurements for CH4, supporting environmental data, and nutrient probes, along with data structures and calibration/processing details.

## Experimental Design and Sampling
- Three campaigns in 2013:
  - 16–27 June (n = 4 sampling occasions)
  - 11–22 August (n = 5)
  - 16–29 September (n = 5 for wetland; 4 for birch forest)
- Total chambers: 60 measured simultaneously (14 in birch forest, 46 in wetland); 4 wetland chambers removed and relocated (up to 64 chamber counts recorded overall).
- Exact chamber locations listed in oneoff_data.csv.

## Collection Methods and Measurements
- Static chambers:
  - 40 cm diameter opaque polypropylene, shallow bases inserted 10 cm depth the day before first sampling.
  - Lids sealed during ~45-minute flux measurements; air samples (100 ml) drawn 4 times and stored for laboratory analysis.
- Environmental measurements:
  - Soil temperature at 10 cm depth around chamber bases; air temperature at chamber height (subset data due to proximity).
  - 4 replicate volumetric soil moisture content (VMC) near each chamber base.
  - Visual vegetation assessment within each chamber.
- Plant Root Simulator (PRS) probes:
  - Pair of cation and anion PRS probes deployed adjacent to each of the 60 chamber bases.
  - Deployment periods: 26/06/2013–13/08/2013 and 21/08/2013–23/09/2013.
  - PRS data adjusted for deployment length; some chambers (61–64) were submerged and lacked PRS data.

## Fieldwork and Laboratory Instrumentation
- Gas chromatography:
  - HP5890 Series II GC with Electron Capture Detector (ECD) for N2O and Flame Ionisation Detector (FID) for CH4.
  - Detection limits: CH4 < 70 μg L−1; N2O < 7 μg L−1.
- In-situ measurements:
  - Soil temperature: Omega HH370 probe.
  - Volumetric soil moisture: CS616 Water Content Reflectometer.
- PRS probes supplied by Western Ag Innovations.

## Calibration Steps and Quality Control
- GC data calibrated with a four-point standard series, run roughly every ~20 samples.
- Standards provided for CH4 and N2O concentrations (Table 1 in the dataset).

## Data Structure / Nature and Units of Recorded Values
- RCfluxOutput.csv
  - Contains CH4 fluxes calculated by RCflux (nmol CH4 m−2 s−1).
  - Key columns:
    - gasName, filename
    - flux_linear, flux_quadratic, flux_linear2nd, flux_quadratic2nd, flux_asymptotic
    - flux_HMR (model-derived), flux_bestfit (best-fit model)
    - ci95lo_linear, ci95hi_linear
    - ci95l_bestfit, ci95h_bestfit, ci95hi_bestfit
    - adjr2_linear, adjr2_quadratic
    - bestFitMethod (code for chosen model)
    - chamberID
- oneoff_data.csv
  - Chamber-level parameters measured once:
    - chamber_id
    - Total_N_PRS (sum of NO3--N and NH4+-N)
    - NO3-N, NH4-N
    - Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd
    - veg_class (vegetation classification per Table 2)
    - lat, long (location)
- veg_class and Table 2 descriptions
  - Vegetation categories defined (e.g., Hummock and Tall shrub, Semiwet, Wet, Tall graminoid, etc.) with mappings to numerical codes.
- Table 1 (GC standards)
  - Standard CH4 and N2O concentrations used for calibration (various ppmv levels).
- parameters_daily.csv (For forest chambers 1–14)
  - Daily CH4 parameters per chamber with:
    - Date, chamberID, sm_vmc_mean, soil_temp, air_temp
  - Provides time-resolved context for flux measurements in forest plots.

## Data Processing and Outputs
- Flux estimation:
  - Using GCFlux version 2, which computes fluxes with multiple models (linear, quadratic, linear second-order, quadratic second-order, asymptotic) and selects the best fit per chamber.
  - Reported CH4 fluxes in nmol CH4 m−2 s−1; additional model-based flux estimates and best-fit selections included.
- PRS nutrient data:
  - Nutrient supply rates (micrograms/10 cm2/burial length) for multiple elements; total inorganic N is the sum of NO3−-N and NH4+-N.
- Metadata integration:
  - Link flux data (RCfluxOutput.csv) with chamber metadata (oneoff_data.csv) and vegetation/locations (veg_class, lat/long) for cross-analysis.
- Notes on data completeness:
  - PRS data unavailable for chambers 61–64 due to underwater conditions.
  - Chamber relocations result in varying chamber counts across sampling occasions.

## References and Methodology Notes
- Chamber design and methodology references:
  - Clough et al. 2015; Jammet et al. 2017; Johansson et al. 2006; Malmer et al. 2005; Levy et al. 2011.
- Data processing tool and modeling references:
  - GCFlux (Levy et al., 2011); best-fit model selection and uncertainty quantification.

## How to Use for Data Support / Analysis
- Build a dataset by joining:
  - RCfluxOutput.csv (flux values, model fits, uncertainties) with oneoff_data.csv (chamber context, location, vegetation, PRS nutrients).
  - Table 1 calibration data to verify standards usage.
  - parameters_daily.csv for forest-specific environmental conditions during flux measurements.
- Explore relationships between CH4 fluxes and:
  - Vegetation classes, soil moisture, temperature, and nutrient supply rates from PRS data.
- Consider data limitations:
  - Subset of chambers with full PRS data; temporal and spatial variability across campaigns; older data (2013) with standard QC documentation.