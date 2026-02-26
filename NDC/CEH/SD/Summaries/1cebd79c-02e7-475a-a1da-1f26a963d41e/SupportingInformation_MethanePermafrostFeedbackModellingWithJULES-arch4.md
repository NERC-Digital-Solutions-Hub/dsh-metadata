# Background, Experiment Design and Analytical Methods

## What the dataset is and its purpose
- Describes the dataset used in Comyn-Platt et al. (2018), providing a summary of data used to analyze climate-carbon cycle interactions.
- Uses the JULES land surface model (version 4.8) coupled with IMOGEN climate-carbon cycle emulator to explore fossil fuel emission budgets under different warming pathways.
- Contains 12 model output sets from JULES/IMOGEN to calculate anthropogenic fossil fuel emissions as the residual of yearly changes.
- Includes global warming variables, fractional land-cover, natural wetlands extent, CH4 flux, soil temperature and moisture, for additional analyses.

## Experimental design (three warming pathways and four model configurations)
- Three global warming pathways (scenarios):
  - 2deg: Stabilisation at 2°C by 2100 from below
  - 1p5deg: Stabilisation at 1.5°C by 2100 from below
  - 1p5degOS: 1.5°C stabilisation with an overshoot to 1.75°C
- Four model configurations (methane feedback variants):
  - BLco: Baseline without methane feedback
  - CH4_lowQ10: CH4 feedback with low methane-temperature sensitivity
  - CH4_poorFEN: CH4 feedback with poor fen-like wetlands sensitivity
  - CH4_richFEN: CH4 feedback with rich fen-like wetlands sensitivity

## Data content and outputs
- Outputs provide carbon stocks across land, atmosphere, and ocean needed to derive fossil fuel emission budgets.
- Additional outputs include global warming indicators, fractional land-cover, natural wetland extent, CH4 flux, and soil temperature/moisture data for analysis.
- Data cover 1850–2099 and include a range of variables essential for climate and carbon-cycle analysis:
  - Vegetation carbon (cv), soil carbon (cs_gb), labelled soil carbon (cs_old_gc)
  - Wetland methane flux (fch4_wetl_cs), fractional cover (frac)
  - Soil temperature (t_soil), soil moisture (smcl)
  - Wetland fraction (fwetl), wood products carbon (wood_products)
  - Atmospheric CO2 (co2_ppmv), CH4 (ch4_ppbv)
  - Global/global-like warming indicators (dtemp_g, dtemp_o, dtemp_l)
  - Ocean uptake of perturbed CO2 (Ocean_uptake)

## Data structure, accessibility and interoperability
- NetCDF files are self-describing and accessible with standard tools (R, Python, nco, etc.), aiding visualization and reuse.
- File naming and structure:
  - exp/scenario/exp_CEN_center_MOD_model_scenario.CarbonStocks.1850-2099.nc
  - Exp: one of BLco, CH4_lowQ10, CH4_poorFEN, CH4_richFEN
  - Scenario: 2deg, 1p5deg, 1p5degOS
  - Center and model correspond to CMIP5 data portal naming
- Data centered on a global grid with explicit dimensions (time, latitude, longitude) and global variables for some outputs.

## Data quality, provenance and governance
- JULES and IMOGEN are maintained to high standards due to ties to UK Earth System Modelling efforts; emphasis on numerical stability and accuracy.
- References to underlying studies and model components (JULES, IMOGEN) and related literature for methanogenesis and permafrost feedbacks.
- The dataset is tied to peer-reviewed work (Comyn-Platt et al. 2018) and foundational components (Gedney 2004; Burke 2018; Clark 2011; Huntingford & Cox 2000/2010; Taylor et al. 2012).

## Appendix: Centre and GCM catalogue
- List of climate modelling centres and associated GCM names used to drive IMOGEN/JULES (e.g., BCC, BNU, CCCma, CMCC, CNRM-CERFACS, CSIRO-BOM, IPSL, MIROC, MOHC, MPI-M, MRI, NASA-GISS, NCAR, NCC, NOAA-GFDL, NSF-DOE-NCAR) with their respective model designations.

## Implications for data leadership and governance
- Demonstrates a well-structured, multi-model ensemble with clear experiment design, enabling reproducibility and cross-model analyses.
- Highlights the importance of comprehensive metadata, self-describing data formats, and standardized file naming for discoverability and re-use.
- Shows integration of data products across land, atmosphere, and ocean components, emphasizing provenance and traceability to CMIP5 frameworks.
- Underlines the need for robust quality control and documentation when coordinating data from multiple modelling groups and configurations.