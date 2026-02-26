# Turf2Surf WP2 Supporting documentation for data

## Overview
- The Turf2Surf project studies coupled nutrient cycling in terrestrial and freshwater ecosystems, focusing on nitrogen and phosphorus impacts on carbon exchange between land and atmosphere.
- WP2 aims to link plant and soil nutrients to ecosystem processes and to inform parameterization for the JULES land-surface model.

## Study area
- Conwy catchment, North Wales (~500 km²) with diverse landscapes and a strong climatic gradient.
- Habitats include blanket bog, moorland, conifer and broadleaf woodlands, grasslands, lakes, flood plains, and salt marshes.
- Wide range of stakeholders (water industries, farmers, foresters, fisheries, tourism, conservation groups).

## Datasets and files
- Five data files comprising plant and soil data:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Each file is tied to a unique Site number and includes habitat, site name, ecosystem component (plant, soil, or roots), species (where applicable), plot and replicate identifiers, and soil depth for soil/root data.
- Missing values are indicated as NA.

## Habitat and sampling design
- 17 sampling sites across Conwy catchment with varied habitats (as listed in Table 1).
- For aboveground measurements:
  - Annual aboveground net primary productivity (NPP) measured 2013–2015 for dominant species.
  - Four plots per site to represent main species; winter clipping with grazing exclusion in fenced plots where applicable.
  - Aboveground biomass measured across habitats; tree biomass estimated in woodland plots via cores and allometric calculations.
- Sampling locations mapped for aboveground biomass and soil cores.

## Data components and measurement methods

- 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
  - NPP measured annually (2013–2015) for dominant species; four plots per site; plots caged in winter to control grazing.
  - Standing biomass: grasses/bog plant biomass cut and weighed; woodland biomass via tree cores and 200 m² plots; litter added to totals.
  - Data processed to align with ecosystem processes and potential integration into JULES.

- 3.1.2 Plant photosynthesis measures
  - Vcmax (max carboxylation rate at 25°C), Jmax (electron transport capacity at 25°C), and Asat (photosynthetic rate at saturating irradiance and CO2) measured for dominant species.
  - Instruments include CIRAS-I with CO2 chambers and LICOR 6400; CO2 curves from 50–2000 ppm; temperature corrections applied.
  - Data processing uses a Farquhar-based model; scripts available (GitHub link provided) for fitting A-Ci curves and extracting parameters.

- 3.1.3 Leaf traits and plant community traits
  - Leaf N and P, leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover.
  - LMA measured from 10 leaves per sampled plant; leaf area via ImageJ; N and P analyzed with standard lab methods.
  - Leaf trait data contribute to characterizing plant functional strategies and informing model parameters.

- 3.2.1 General soil measures
  - Intact soil cores collected to 1 m depth across 17 habitats; sections split into depth intervals (0–15, 15–30, ..., 90+ cm).
  - Measurements include soil water content (SWC), bulk density (BD), loss on ignition (LOI) and LOI-C, pH, electrical conductivity (EC), total C and N.
  - QA/QC and multi-site depth-resolved data support soil process interpretation and model inputs.

- 3.2.2 Phosphorus
  - Olsen P, root-available P, complex-P, enzyme-extractable P measured using multiple extraction schemes (Malachite Green colorimetry for P; standard references provided).
  - Root-P measured with CaCl2 extraction to simulate plant/root-accessible P pools.
  - Enzyme-P and various P pools targeted to represent dynamic soil P availability and plant access.

- 3.2.3 Available carbon and nitrogen
  - Soil available C and N measured after 0.5 M K2SO4 extraction; NO3 and NH4 quantified with colorimetric assays.
  - DOC and total dissolved nitrogen (TDN) quantified at CEH Bangor using standard high-temperature catalytic oxidation methods.
  - Data describe immediately available soil C and N pools relevant to short-term nutrient cycling.

- 3.2.4 Soil available cations (Ca, Na, K)
  - 0.5 M acetic acid extraction followed by flame photometry to determine Ca, Na, and K concentrations.
  - Provides insight into cation exchange capacity and nutrient availability in different habitats.

- 3.2.5 Root biomass
  - Total and fine root biomass quantified at six sites using 15 cm cores; roots scanned with WinRhizo for morphometrics; dry weights obtained after oven-drying.
  - In-growth root cores deployed to measure root growth over a growing season; morphological and biomass data used to evaluate belowground carbon and nutrient storage.

- 3.2.6 Soil elements – TXRF
  - Total elemental analysis (Al, Fe, Ca, K, Ti, S, etc.) by TXRF for all sites.
  - Detailed sample prep and analysis workflow described; limitations discussed in a dedicated file.
  - Supports integration of trace elements into ecosystem nutrient models.

## Dataset structure and metadata
- Dataset consists of five CSV files with consistent site-based indexing:
  - Site number, habitat description, site name, ecosystem component (plant, soil, roots)
  - For plants: species information; for soils/roots: NA in the species column
  - Plot number and replicate number
  - Soil depth interval applicable to soils and roots
- Missing data labeled as NA; metadata notes data availability constraints (e.g., soil depth restrictions, limited replicates).

## Data provenance and versioning
- Data responsibilities assigned to project members across CEH, Bangor University, and Exeter University.
- Versioned documentation with multiple dates in 2016 (01/06/2016; 25/08/2016; 04/11/2016).

## Potential uses for analysis
- Enables cross-dataset analyses linking plant traits, biomass, photosynthesis, soil chemistry, and root dynamics.
- Supports parameterization and validation of the JULES land-surface model by providing empirical inputs for above- and below-ground processes and soil nutrient pools.
- Useful for examining correlations between N/P cycling and carbon exchange across diverse habitats within the Conwy catchment.