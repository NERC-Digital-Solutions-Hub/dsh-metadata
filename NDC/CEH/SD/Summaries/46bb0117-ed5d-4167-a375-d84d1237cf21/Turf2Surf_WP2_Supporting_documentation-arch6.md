# Turf2Surf WP2 Supporting documentation for data

- The Turf2Surf project WP2 focuses on coupled nutrient cycling in terrestrial and freshwater ecosystems, linking nitrogen and phosphorus impacts to carbon exchange between land and atmosphere. Data are intended to support parameterization and integration with the JULES model.

## Project scope and data stewardship

- Data responsible individuals span multiple institutions (CEH, Bangor University, Exeter University) and cover plant and soil measurements across the Conwy catchment.
- Outputs are designed to enable cross-site comparison and to facilitate data use by researchers with broader aims (e.g., policy, ecology, carbon cycling).

## Datasets and data files

- Five data files constitute the dataset:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Data columns include site, habitat, site name, ecosystem component (plant/soil/root), plant species (when applicable), plot and replicate numbers, and soil depth intervals (for soil/root components).
- Missing values are denoted as NA.

## Study area and sampling context

- Conwy catchment, North Wales (~500 km2), with diverse landscapes, climatic gradient, and a range of habitats from blanket bogs to woodlands and agricultural land.
- The catchment provides extensive baseline data for ecological, biogeochemical, and hydrological processes and includes a broad set of stakeholders (water industry, agriculture, conservation, tourism).

## Habitats and sampling design

- Site and habitat information (Table 1) includes 17 core habitats with site-specific plot counts and dominant vegetation types (e.g., blanket bog, acid grassland, conifer woodland, broadleaf woodland, improved grassland, montane/gill habitats, hay meadows, etc.).
- Sampling locations span 23 site entries, with multiple plots per habitat where applicable.

## Data themes and measurement programs

- 3.1 Plant data
  - 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
    - NPP measured 2013–2015 on dominant species across sites; four plots per site represent main species.
    - Winter clipping and protective cages; biomass measured at 10 of 17 sites; woodland/bos habitats use tree cores and litter measurements; biomass per m2 calculated from tree volumes, densities, and leaf biomass.
    - Purpose: link plant productivity to soil and nutrient parameters; support integration with JULES.
  - 3.1.2 Plant photosynthesis measures
    - Vcmax (max carboxylation rate), Jmax (electron transport capacity), and Asat (photosynthesis rate) measured for dominant species.
    - Field measurements at CO2 levels of 400 and 2000 ppm; additionally, CO2 curves up to 2000 ppm with 1500 μmol m-2 s-1 light.
    - Data processing uses Farquhar-based models; temperature-corrected parameters to 25°C.
    - Data processing scripts linked to the fitting tools (GitHub: mdekauwe/FitFarquharModel).
  - 3.1.3 Leaf traits and plant community traits
    - Leaf N and P (%), leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover.
    - LMA derived from scanned leaves and dry mass; SLA as inverse of LMA; nutrient analyses via standard lab methods.
    - Data processing contributes parameters to JULES; measurements by CEH Bangor and partners.

- 3.2 Soil measurements
  - 3.2.1 General soil measures
    - Intact cores collected to 1 m depth across 17 habitats; subsampled at depth intervals (0–15, 15–30, …, 90+ cm).
    - Measurements include soil water content (SWC), bulk density (BD), loss-on-ignition (LOI and LOI-C), pH, electrical conductivity (EC), total C (C_tot) and total N (N_tot).
  - 3.2.2 Phosphorus
    - Olsen P, root-available P (CaCl2 extractable), complex-P (citric acid extractable), enzyme-P (phosphatase and phytase), proton-P (1 M HCl extraction).
    - Colorimetric analyses largely use Malachite Green method; standard conditions and plate-based assays described in detail.
    - Purpose: characterize P pools and accessibility relevant to plant-microbe interactions and nutrient cycling.
  - 3.2.3 Available carbon and nitrogen
    - Soil available C and N assessed via 0.5 M K2SO4 extraction; nitrate (NO3-N) and ammonium (NH4-N) measured with colorimetric/microbial assay methods; DOC and TDN measured at CEH Bangor using thermal oxidation with NDIR detection.
  - 3.2.4 Soil available cations (Ca, Na, K)
    - 0.5 M acetic acid extraction; cations measured with flame photometry.
  - 3.2.5 Root biomass
    - Total and fine root biomass measured at six sites; soil cores (0–15 cm depth, 15 cm interval) processed and roots scanned with WinRhizo; dry weights calculated.
    - In-growth root cores deployed to assess root growth over a season; detailed deployment and retrieval procedures described.
  - 3.2.6 Soil elements – TXRF
    - Total element analysis (Al, Fe, Ca, K, Ti, S, Ba, Mn, P, Sr, Zr, Cl, V, Rb, Zn, Cr, Nd, La, Cu, Y, Ni, Pb, Ga, Nb, Th, Co, Sc, As, Cs, U, Sn, Ge, I, Br, Sb, Se, Cd, Hg) by TXRF (Bruker S2 PicoFOX).
    - Sample preparation includes grinding, suspension in TritonX, deposition on silicon discs, and gain calibration with standards.
- Across soil components, WP2 aims to link plant and soil nutrients to above- and belowground processes for incorporation into JULES; QA/QC and lab responsibilities are documented per measurement type.

## Dataset structure and metadata

- The dataset comprises five CSV data files listed above.
- Column-level details (as described):
  - Column A: unique Site number
  - Columns B–C: Habitat name and detailed habitat description
  - Column D: Site name
  - Column E: Ecosystem Component (plant, soil, or roots)
  - Column F: Plant species (for Plant component; NA for soil/roots)
  - Columns G–H: Plot number and Replicate number
  - Column I: Soil depth interval (for Soil and Roots)
- Missing values are indicated as NA, reflecting restricted depths, limited replicates, or outliers.

## Data processing, QA, and integration

- Data processing and analysis are performed by designated leads for each data type (e.g., NPP by Simon Smart; photosynthesis by Lina Mercado; leaf traits by Lina Mercado and Simon Smart; soil measurements by Helen Glanville and colleagues; TXRF by Glanville and team).
- Some processing scripts and methodological references are provided (e.g., Fitting routines for photosynthesis models; remaining documentation on TXRF limitations).
- A key aim is to supply data and derived parameters to integrate into JULES for ecosystem-level simulations of nutrient cycling and carbon exchange.

## Usage and accessibility notes

- The data are suitable for cross-site comparison of plant productivity, photosynthesis, leaf traits, soil nutrient pools, and root dynamics, with explicit linkage to soil nutrient availability and element pools (N, P, C, Ca, etc.).
- Some methodological tools and example code are publicly referenced (e.g., GitHub repository for photosynthesis modeling).
- Limitations and caveats noted for TXRF analyses are discussed in a dedicated file (Turf2Surf_WP2_TXRF_Limitations_Glanville.rft).