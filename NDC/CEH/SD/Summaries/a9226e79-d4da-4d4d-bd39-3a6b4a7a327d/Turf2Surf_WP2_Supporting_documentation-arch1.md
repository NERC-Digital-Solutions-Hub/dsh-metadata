# Turf2Surf WP2 Supporting documentation for data

- Purpose and scope
  - The Turf2Surf project studies coupled nutrient cycling in terrestrial and freshwater systems, focusing on nitrogen and phosphorus influences on carbon exchange between land and atmosphere.
  - WP2 specifics: linking plant and soil nutrients to aboveground and belowground ecosystem processes to inform the JULES land surface model.

- Project team (authors)
  - Bridget Emmett, CEH; Davey Jones, Bangor University; Simon Smart, CEH; Lina Mercado, Exeter University; Helen Glanville, Bangor University; Maria C Blanes, CEH; Harry Harmens, CEH; Sabine Reinsch, CEH
  - Authors: Sabine Reinsch (corresponding author), Helen Glanville, Simon Smart

- Information about the Conwy catchment (1.0)
  - Location: North Wales, ~500 km²; main river drains 380 km² to tidal limit; 200 km² to estuary.
  - Climate gradient: 500 mm to >1000 mm annual precipitation; varied topography (Snowdonia mountains to lowland).
  - Land use and soils: mixture of agricultural, woodland, moorland; soils neutral to acidic; diverse habitats including bogs, moorland, woodlands, grasslands, lakes, flood plains, and salt marshes.
  - Stakeholders: water industries, fisheries, farmers, foresters, conservation groups, local communities.
  - Map: sampling locations across the catchment shown in Figure 1.

- Habitats and sampling sites (2.0)
  - 17 habitats, with unique site numbers and descriptions; a total of 21 sampling sites listed.
  - Examples of habitats: blanket bog (Nant-y-Brwyn; Juncus effusus or Eriophorum), heath on blanket bog (Llyn Serw), valley bogs, acid grasslands, conifer woodland, broadleaved woodlands, upland oakwood, juniper gill, hay meadow, improved/semi-improved grasslands, Montane sites.
  - Sampling design includes plots per habitat (1–4 plots per site; 3–9 replicates per habitat for some measurements).

- Aboveground net primary productivity and standing biomass (3.1.1)
  - Data responsibility: Simon Smart
  - NPP: measured annually (2013–2015) for dominant species across all sites; four plots per site to represent main species; winter clipping and grazing-exclusion cages used in grazed habitats.
  - Standing biomass: measured at 10 of 17 sites (3–9 replicates per habitat); procedure varies by habitat (grassy/bog vs woodland); bleaching/wood core methods used for trees; leaf biomass added to total biomass.
  - Purpose: link plant productivity to soil nutrients for integration into JULES.

- Plant photosynthesis measures (3.1.2)
  - Data responsibility: Lina Mercado
  - Parameters: Asat (saturating irradiance, CO2), Vcmax (maximum carboxylation rate at 25°C), Jmax (electron transport capacity at 25°C)
  - Field methods: CIRAS-I with cuvette for CO2 ranges; LICOR 6400 in 2014–2016; canopy-level A-Ci curves fitted to Farquhar model; temperature corrections using Bernacchi et al. parameters.
  - Analysis: Vcmax, Jmax estimated with fitting routines; links to JULES parameterization.
  - References provided for photosynthesis models and temperature corrections.

- Leaf traits and plant community traits (3.1.3)
  - Data responsibility: Lina Mercado and Simon Smart
  - Traits measured: leaf nitrogen and phosphorus (%), leaf dry matter content (LDMC), specific leaf area (SLA), leaf area per leaf mass (LMA), canopy height (cht), bryophyte cover (Bcov)
  - Methods: LMA from 10 leaves per sampling area; image analysis for leaf area; chemical analyses for N and P; SLA from inverse of LMA.
  - Purpose: integrate leaf economics into nutrient–process relationships for model parameterization.

- General soil measures (3.2.1)
  - Data responsibility: Helen Glanville
  - Soil sampling: intact cores (17 habitats) down to 1 m; cores split into depth intervals (0–15, 15–30, …, 90+), total 300 samples
  - Measurements: soil water content (SWC), bulk density (BD), LOI and LOI-C, pH, EC, total C and N
  - QA/QC and team: multiple researchers; data tied to Turf2SurfWP2 aims to integrate soil parameters into JULES

- Phosphorus (3.2.2)
  - Data responsibility: Helen Glanville
  - Phosphorus fractions: Olsen P, Root-P (CaCl2 extractable), Complex-P (10 mM citrate extractable), Enzyme-P (phosphatase and phytase activity), Protons-P (1 M HCl extractable)
  - Analytical approach: colorimetric malachite green method (630 nm) with standard curves; multiple extraction methods to represent various bioavailable P pools
  - Purpose: characterize soil P pools relevant to plant uptake and microbial processes; data intended for JULES integration

- Available carbon and nitrogen (3.2.3)
  - Data responsibility: Helen Glanville
  - Extractants and analyses: soil available C and N via 0.5 M K2SO4 extractant; NO3 via vanadate colorimetric method; NH4 via salicylate-nitroprusside/hypochlorite method; DOC and TDN measured by CEH Bangor (Thermalox/NDIR for C; TDN via NH4-N standards)
  - Procedure details: extraction, centrifugation, processing timelines, QA
  - Purpose: quantify readily available soil C and N pools for coupling with plant data

- Soil available cations (Ca, Na, K) (3.2.4)
  - Data responsibility: Helen Glanville
  - Extraction: 0.5 M acetic acid; measurement by flame photometry
  - Purpose: characterize exchangeable cations for nutrient availability context in the ecosystem

- Root biomass (3.2.5)
  - Data responsibility: Helen Glanville
  - Methods: total and fine root biomass across six sites; soil cores 0–15 cm depth sliced into 0–5, 5–10, 10–15 cm; roots scanned with WinRhizo for architecture; biomass after oven-drying
  - Belowground dynamics: in-growth root cores to measure root growth over a season
  - Purpose: compare aboveground and belowground carbon/nutrient stocks; inform root dynamics in models

- Soil elements – TXRF (3.2.6)
  - Data responsibility: Helen Glanville
  - Elemental analysis: 34+ elements (e.g., Al, Fe, Ca, K, P, Zn, Pb, etc.) by TXRF (Bruker S2 PICOFOX)
  - Sampling: same 17 sites; cores down to 1 m; samples ground to <70 µm; prepared on silicon discs with internal standards
  - Data processing: team-based data handling; notes on limitations in Turf2Surf_WP2_TXRF_Limitations_Glanville.rft
  - Purpose: broad elemental context for soils and potential nutrient interactions with biota

- Dataset structure (4.0)
  - Data files: five CSVs
    - Turf2Surf_Plant_biomass_data.csv
    - Turf2Surf_Plant_structural_data.csv
    - Turf2Surf_Plant_physiological_data.csv
    - Turf2Surf_Soil_Carbon_data.csv
    - Turf2Surf_Soil_raw data.csv
  - Column descriptions (summary):
    - Column A: Site number (as in Table 1)
    - Column B: Habitat
    - Column C: Habitat description
    - Column D: Site name
    - Column E: Ecosystem Component (Plant, Soil, Roots)
    - Column F: If Plant, the species; otherwise NA
    - Column G: Plot number
    - Column H: Replicate number
    - Column I: Soil depth interval (for Soil and Roots)
  - Data status: missing values indicated as NA; some sites have restricted depths or fewer replicates; values reflect restricted or outlier data accordingly

- Data provenance, processing, and integration notes
  - Data collectors and processing teams are listed for each dataset component
  - The WP2 work aims to incorporate measured plant and soil nutrient parameters into the JULES model
  - Detailed methodology documents and scripts are referenced (e.g., NPP_Smart.rft, JULES integration references, and relevant photosynthesis model papers)
  - Version history: document versions dated 01/06/2016, 25/08/2016, 04/11/2016

- Data access and usage considerations for analysts
  - Rich, multi-temporal, and multi-factor data across a single catchment with diverse habitats
  - Spatial and depth-resolved soil data enabling local-scale analyses and model parameterization
  - Data allow exploration of links between plant productivity, leaf/plant traits, soil nutrient pools, and atmospheric carbon exchange
  - Gaps and limitations noted: data are concentrated in one catchment and may have uneven replication across sites; some measurements are NA in places; TXRF limitations documented separately
  - Datasets designed to be integrated into JULES for ecosystem process modeling and scenario analysis