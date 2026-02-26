# Turf2Surf WP2 Supporting documentation for data

- The Turf2Surf project focuses on coupled nutrient cycling in terrestrial and freshwater ecosystems and links nitrogen and phosphorus impacts to carbon exchange between land and atmosphere.
- WP2 aims to connect plant and soil nutrients to aboveground and belowground processes, with data intended for integration into the JULES model.
- Timeframe and leadership: Data collected and processed 2013–2016; key authors include Sabine Reinsch (corresponding author), Helen Glanville, Simon Smart, Lina Mercado, Bridget Emmett, and colleagues from CEH and partner universities.
- Data governance: Data are organized around site, habitat, plots, replicates, and depth intervals; detailed methodologies and dataset structure are documented to support reuse and integration with models.

## Study area and context

- Conwy catchment, North Wales (~500 km2) with diverse landscapes and a climatic gradient affecting hydrology and biogeochemical processes.
- Habitats include blanket bog, moorland, heath, grasslands, woodlands, lakes, reservoirs, flood plains, and salt marshes.
- Stakeholders include water industries, farmers, foresters, conservation groups, and local communities.
- Goal: develop a holistic understanding of pressures on natural resources and ecosystem services, enabling data-driven management and model parameterization.

## Data collection and organization

- Five data files comprise the dataset structure, each with site-, habitat-, and plot-level metadata, plus depth information for soil components.
- Data responsibility and contact points are provided for each data subsystem, with specific methods and QA/QC procedures described per dataset.

## Key data components and methods

- 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
  - Annual NPP measured for dominant species at all sites (2013–2015) using 4 plots per site; winter clipping and grazing exclusion via cages where applicable.
  - Aboveground biomass measured at 10 of 17 sites, with selective sampling for grasses/bogs (dry weight in 1 m2 quadrats) and woody components (tree cores in 200 m2 plots). Biomass scaled to m2.
  - NPP data linked to plant life strategies and integrated with Turf2Surf WP2 objectives; detailed methodology available in Turf2Surf_WP2_NPP_Smart.rft.

- 3.1.2 Plant photosynthesis measures
  - Metrics: Asat, Vcmax (25°C), Jmax (25°C); collected for dominant species at most sites.
  - Measurements via CIRAS-I with CO2 chambers and LICOR 6400; CO2 curves from 50 to 2000 ppm; temperature corrections following Bernacchi et al. and Medlyn et al.
  - Data processing and model integration performed to derive photosynthetic parameters; scripts provided (GitHub link).

- 3.1.3 Leaf traits and plant community traits
  - Traits measured: leaf N and P (%), leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover.
  - LMA derived from 10 leaves per area; SLA is the inverse of LMA.
  - Leaf chemistry analyses conducted with standard lab protocols; data incorporated into JULES parameterization.

- 3.2.1 General soil measures
  - Intact soil cores collected from 17 habitats (0–1 m depth, multiple depth intervals) for 300 samples total.
  - Parameters: soil water content (SWC), bulk density (BD), loss-on-ignition (LOI, and LOI-C), pH, electrical conductivity (EC), total carbon and nitrogen (C_tot, N_tot).
  - QA/QC and processing described; labs and personnel defined.

- 3.2.2 Phosphorus (P) fractions
  - Olsen P, Root-P, Complex-P, Enzyme-P, and Protons-P fractions measured via colorimetric methods (Malachite Green) and various extraction protocols (Olsen, CaCl2, citrate, enzyme extracts, etc.).
  - Detailed procedures described for each P pool to reflect different bioavailability and weathering processes.

- 3.2.3 Available carbon and nitrogen
  - Soil available C and N analyzed after extraction with 0.5 M K2SO4; NO3 and NH4 analyzed with colorimetric assays; DOC and TDN measured with thermal oxidation and NDIR detection.
  - Protocols specify sample handling, storage, and QA steps.

- 3.2.4 Soil available cations (Ca, Na, K)
  - Extraction with 0.5 M acetic acid; cations quantified via flame photometry.
  - Methods and QA details provided.

- 3.2.5 Root biomass
  - Standing root biomass: 15 cm cores; roots separated into >2 mm and <2 mm; scanned with WinRhizo for biometric traits; dry weight determined.
  - In-growth cores used to quantify root growth over a growing season; method details and site assignments described.
  - Root analyses and in-growth cores designed and executed by dedicated team.

- 3.2.6 Soil elements – TXRF
  - Total elemental analysis for a broad suite of elements (e.g., Al, Fe, Ca, K, Mn, P, Zn, etc.) using TXRF (Bruker S2 PICOFOX).
  - Sample preparation includes grinding, suspension, internal standards, and disc deposition; limitations noted with a follow-up document.

## Dataset structure and data files

- Five data files:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Column schema highlights:
  - Column A: Site number
  - Column B: Habitat
  - Column C: Habitat description
  - Column D: Site name
  - Column E: Ecosystem component (Plant, Soil, Roots)
  - Column F: Plant species (if Ecosystem component is Plant; NA for soil/root)
  - Columns G-H: Plot number and Replicate number
  - Column I: Soil depth interval (for Soil and Roots)
- Data quality notes:
  - Missing values indicated as NA
  - Structure supports cross-site comparisons and model parameterization

## Data governance and usage notes for Data Leaders

- Data are organized to support holistic data system thinking, with emphasis on discoverability and reuse.
- The dataset design facilitates integration with ecosystem models (notably JULES) through explicit links between plant and soil processes and measured parameters.
- Clear documentation of sampling design (sites, habitats, plots, depth intervals) and measurement protocols aids data quality assessment and reproducibility.
- Limitations include multi-depth soil sampling across 17 habitats, TXRF method limitations noted in accompanying file Turf2Surf_WP2_TXRF_Limitations_Glanville.rft, and potential data gaps due to restricted depths or replicates in certain habitats.

## Authorship and data responsibilities

- Project members and data stewards:
  - Bridget Emmett, CEH; Davey Jones, Bangor University; Simon Smart, CEH; Lina Mercado, Exeter University; Helen Glanville, Bangor University; Maria C Blanes, CEH; Harry Harmens, CEH; Sabine Reinsch, CEH.
- Data responsibility by section (e.g., NPP, photosynthesis, leaf traits, soil measures, phosphorus, C/N, cations, roots, TXRF) with designated leads and contact emails.
- Documentation and analysis scripts available (e.g., GitHub repository for photosynthesis modeling).