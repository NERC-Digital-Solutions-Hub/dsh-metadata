# Turf2Surf WP2 Supporting documentation for data

- Purpose and scope
  - Focus: coupled nutrient cycling in terrestrial and freshwater ecosystems; links nitrogen and phosphorus impacts to carbon exchange between land and atmosphere.
  - WP2 role: measure plant and soil nutrient parameters to inform ecosystem processes and support data integration into JULES models.

- Project team and documentation
  - Project members and authors listed (CEH, Bangor University, Exeter University) with corresponding authors and version dates (01/06/2016; 25/08/2016; 04/11/2016).

- Study area: Conwy catchment
  - Location and size: North Wales, ~500 km2 catchment with diverse landscapes.
  - Climate and soils: strong gradient (500–1064 mm annual rainfall); soils from neutral to acidic, typical upland UK.
  - Land use and habitats: blanket bog, moorland, conifer woodlands, grasslands, lakes/reservoirs, flood plains, salt marsh; wide range of stakeholders (water, farming, forestry, conservation, tourism).

- Habitats and sampling sites
  - Representation: 17 soil habitats sampled across multiple sites (and 23 habitat entries listed in the table) to capture diverse ecological conditions (e.g., blanket bog, heath, acid grassland, conifer woodland, broadleaf woodland, arable, improved grassland, moorland).
  - Sampling design: multiple plots per site, with plots/replicates chosen to reflect dominant species per habitat.

- Measurements and data processing

  - 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
    - Data responsibility: Simon Smart.
    - NPP: annual NPP measured for dominant species at all sites (2013–2015); four plots per site; winter clipping with grazing protection in cages.
    - Biomass: aboveground standing biomass measured at 10 of 17 sites; grasses/bog habitats sampled in 1 m x 1 m quadrats; woodland biomass via 200 m2 plots and tree cores; biomass converted to per m2.

  - 3.1.2 Plant photosynthesis measures
    - Data responsibility: Lina Mercado; analysis by L. Mercado.
    - Parameters: Asat, Vcmax, Jmax measured for dominant species.
    - Methods: field and laboratory gas-exchange measurements (CIRAS-I with CO2 chambers; Licor 6400); A-Ci curve fitting using Farquhar model; temperature corrections to 25°C; data processed with specific scripts (GitHub repository referenced).

  - 3.1.3 Leaf traits and plant community traits
    - Data responsibility: Lina Mercado and Simon Smart.
    - Traits: leaf N, leaf P, LDMC, SLA, LMA, canopy height, bryophyte cover.
    - Methods: leaf sampling across sites; LMA from scanned leaves; leaf area via ImageJ; N and P analyses in respective labs; SLA is inverse of LMA; part of data integrated into JULES.

  - 3.2.1 General soil measures
    - Data responsibility: Helen Glanville.
    - Sampling: intact soil cores (to 1 m) from 17 habitats; depth intervals defined.
    - Measurements: soil water content, bulk density, LOI and LOI-C, pH, EC, total C and N; QA/QC described; details of calculation and calibration.

  - 3.2.2 Phosphorus
    - Data responsibility: Helen Glanville.
    - Phosphorus fractions: Olsen P, Root-P, Complex-P, Enzyme-P, Proton-P.
    - Methods: colorimetric analyses (Malachite Green) and various extraction protocols (Olsen P, CaCl2 extractable P, citrate extractable P, enzyme extractions with phosphatase/phytase, 1 M HCl for recalcitrant P); detailed steps and reagents provided.

  - 3.2.3 Available carbon and nitrogen
    - Data responsibility: Helen Glanville.
    - Measures: DOC and TDN; extraction with 0.5 M K2SO4; subsequent colorimetric or instrumental analyses; QA details including batch standards and QA samples.

  - 3.2.4 Soil available cations (Ca, Na, K)
    - Data responsibility: Helen Glanville.
    - Methods: extraction with 0.5 M acetic acid; analysis by flame photometry; standard curve-based quantification.

  - 3.2.5 Root biomass
    - Data responsibility: Helen Glanville.
    - Measurements: total and fine root biomass across 6 sites; 15 cm soil cores; root washing, sieving, WinRhizo scanning for total/diameter/branching; dry weight for biomass; in-growth root cores to assess root growth over a season.

  - 3.2.6 Soil elements – TXRF analysis
    - Data responsibility: Helen Glanville; analysis by lab personnel.
    - Elemental suite: broad set of elements (Al, Fe, Ca, K, Ti, S, Mn, Zn, P, etc.); TXRF methodology with sample preparation, internal standards, and disc preparation; limitations discussed in separate TXRF document.

- Dataset structure
  - Five data files:
    - Turf2Surf_Plant_biomass_data.csv
    - Turf2Surf_Plant_structural_data.csv
    - Turf2Surf_Plant_physiological_data.csv
    - Turf2Surf_Soil_Carbon_data.csv
    - Turf2Surf_Soil_raw data.csv
  - Column scheme:
    - Site number (unique identifier), Habitat and detailed Habitat description, Site name, Ecosystem Component (Plant, Soil, Roots).
    - If component is Plant: species information provided; otherwise NA.
    - Plot number (1–4) and Replicate number (where measurements were not co-located with plots).
    - For Soil and Roots: Soil depth interval column present (I).
  - Data quality notes:
    - Missing values indicated as NA due to restricted depths, limited replicates, or outliers.
  - Purpose:
    - Enables integrated analyses of plant and soil variables to support ecosystem process understanding and model parameterization (e.g., JULES integration).