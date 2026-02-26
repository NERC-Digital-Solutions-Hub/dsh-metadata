# Turf2Surf WP2 Supporting documentation for data

## Purpose and scope
- Turf2Surf focuses on coupled nutrient cycling in terrestrial and freshwater ecosystems and links these processes to water quality, carbon sequestration, and biodiversity.
- WP2 investigates nitrogen and phosphorus related impacts on carbon exchange between land and atmosphere.
- The documentation aims to outline data collection, structure, processing, and governance to enable discovery, reuse, and integration (e.g., with the JULES model).

## Project and data stewardship
- Project members and authors listed; corresponding author: Sabine Reinsch.
- Data responsibilities assigned to specific researchers for each data area (e.g., NPP: Simon Smart; Plant photosynthesis: Lina Mercado; Leaf traits: Lina Mercado & Simon Smart; Soil measures and components: Helen Glanville and colleagues).
- Data are baseline, consistent, and available to other research projects; aims to support broader reuse and integration.
- Versioned documentation with dates: 01/06/2016; 25/08/2016; 04/11/2016.

## Datasets and content
- Five data files comprise the dataset:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Column A: Site number; B–C: Habitat and detailed habitat description; D: Site name; E: Ecosystem component (Plant, Soil, Roots); F: Species (for Plant) or NA (soil/roots); G–H: Plot and Replicate numbers; I: Soil depth interval (for Soil/Roots).
- Missing data are indicated as NA.
- The dataset structure is designed to support integration with JULES and related analyses.

## Sampling sites and habitats
- Conwy catchment, North Wales (~500 km²) with diverse landscapes and climatic gradients (precipitation from ~500 mm to >1000 mm).
- Diverse habitats included: blanket bog, moorland, conifer woodlands, broadleaf woodland, grasslands, lakes, flood plains, salt marshes.
- Table 1 lists 23 sites with unique site numbers, plot counts, locations, and dominant vegetation where applicable.
- Sampling across a range of habitats facilitates cross-site comparisons and holistic process understanding.

## Measurements and data processing

### 3.1 Aboveground net primary productivity (NPP) and standing biomass
- Data responsible: Simon Smart.
- NPP measured annually (2013–2015) for dominant species at all sites; four plots per site; winter clipping with grazing protection in some habitats.
- Aboveground standing biomass measured at 10 of 17 sites (3–9 replicates per habitat); biomass estimation varied by habitat type (grassland/bog vs. woodland) and included tree cores for woody vegetation.
- NPP data linked to Turf2SurfWP2 for integration with JULES; detailed methodology in Turf2Surf_WP2_NPP_Smart.rft.

### 3.1.2 Plant photosynthesis measures
- Data responsible: Lina Mercado.
- Parameters: Asat, Vcmax, Jmax (25°C) measured for dominant species.
- Methods: field measurements with CIRAS-I, Rice Cuvette, Conifer chamber, and LICOR 6400 across various years; CO2 curves and temperature corrections applied.
- Data processed with De Kauwe’s photosynthesis package; links to GitHub repo for model fitting.
- Measurements and processing also support JULES parameterization.

### 3.1.3 Leaf traits and plant community traits
- Data responsible: Lina Mercado and Simon Smart.
- Traits: leaf N and P (%), leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover.
- Leaf area and LMA determined from scanned leaves; N and P via standard chemical analyses; SLA derived from LMA; SLA and LMA values used to characterize plant functional traits.
- Data processing contributes to JULES parameterization.

### 3.2 Soil and soil-related measurements

#### 3.2.1 General soil measures
- Data responsible: Helen Glanville and team.
- Methods: 17 habitats sampled; intact soil cores to 1 m depth; depth intervals defined; measurements include soil water content (SWC), bulk density (BD), loss-on-ignition (LOI and LOI-C), pH, electrical conductivity (EC), and total C and N.
- QA/QC and data processing support ongoing integration with WP2 objectives.

#### 3.2.2 Phosphorus (P) fractions
- Data responsible: Helen Glanville and team.
- Olsen P, Root-P, Complex-P, Enzyme-P, and Proton-P fractions measured via standardized extraction and colorimetric methods (Malachite Green, 630 nm readouts).
- Protocols detail extraction reagents, volumes, and plate-based measurement steps; aims to partition soil P into fractions accessible to roots/microbial processes.

#### 3.2.3 Available carbon and nitrogen
- Data responsible: Helen Glanville and team.
- DOC and TDN measured from 0.5 M K2SO4 extracts; detailed extraction, centrifugation, storage, and analytical steps described; analyses conducted on CEH Bangor equipment.

#### 3.2.4 Soil available cations (Ca, Na, K)
- Data responsible: Helen Glanville and team.
- 0.5 M acetic acid extraction used to quantify Ca, Na, K; flame photometry used for measurements; standard curves applied for concentration calculations.

#### 3.2.5 Root biomass
- Data responsible: Helen Glanville and team.
- Methods: 15 cm soil cores; roots separated into <2 mm and >2 mm; roots scanned with WinRhizo for biomass/length metrics; in-growth cores to measure root growth over a season; dry weights calculated for total and fine roots.
- Root measurements connected to aboveground biomass comparisons and WP2/JULES parameterization.

#### 3.2.6 Soil elements – TXRF
- Data responsible: Helen Glanville and team; analysis by TXRF (Bruker S2 PICOFOX).
- Comprehensive multi-element analysis (Al, Fe, Ca, K, etc.) across all sites; sample prep includes grinding, sieving, and suspension on silicon discs.
- Documented by contributors; limitations noted in Turf2Surf_WP2_TXRF_Limitations_Glanville.rft.

## Data structure, availability, and provenance

### 4.0 Dataset structure
- Five data files as described above.
- Column semantics (Site number, Habitat, Habitat description, Site name, Ecosystem component, Plant species, Plot, Replicate, Soil depth interval) facilitate cross-dataset linking.
- Missing data indicated as NA; depth/class restrictions and replicates may limit coverage in some records.

### Additional references and metadata
- Abbreviations list provided (e.g., N, P, NPP, LDMC, SLA, Vcmax, Jmax, Asat, LOI, BD, SWC, etc.).
- Figure 1 (map of sampling locations) and detailed habitat/site descriptions accompany the data.

## Data quality, limitations, and governance

- TXRF data have documented limitations (see Turf2Surf_WP2_TXRF_Limitations_Glanville.rft).
- Some site groupings (e.g., different Llyn Serw heather ages) were combined for soil analyses, potentially affecting site-level granularity.
- Replicate numbers and accessible soil depths vary by site and habitat, leading to NA entries where data are unavailable.
- Versioned documentation indicates ongoing updates and refinement; data processing scripts and methodologies are referenced (e.g., NPP methodology, photosynthesis fitting scripts, and links to GitHub).

## Usage notes and contact

- The documentation identifies data responsibilities and provides contact points (e.g., data responsible emails and corresponding authors) for specific data areas.
- The dataset is designed to support parameterization of JULES and integration with plant–soil–ecosystem process studies.
- Version history and supporting documents are provided to aid reproducibility and data reuse.