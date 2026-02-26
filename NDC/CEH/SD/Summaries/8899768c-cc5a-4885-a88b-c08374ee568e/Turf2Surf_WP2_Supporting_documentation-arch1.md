# Turf2Surf WP2 Supporting documentation for data

- Purpose and scope
  - The Turf2Surf project investigates coupled nutrient cycling in terrestrial and freshwater ecosystems and its link to water quality, carbon sequestration, and biodiversity.
  - WP2 studies nitrogen and phosphorus impacts on carbon exchange between land and atmosphere and aims to link plant and soil nutrients to aboveground and belowground ecosystem processes, integrating findings into the JULES model.

- Project team and versions
  - Authors: Sabine Reinsch (corresponding), Helen Glanville, Simon Smart, plus others from CEH, Bangor University, and Exeter University.
  - Project members: Bridget Emmett, Davey Jones, Simon Smart, Lina Mercado, Helen Glanville, Maria C Blanes, Harry Harmens, Sabine Reinsch.
  - Version dates: 01/06/2016; 25/08/2016; 04/11/2016.

- Study area: Conwy catchment, North Wales
  - ~500 km2 river catchment with diverse landscapes enabling comparative study from gene to landscape scale.
  - Climatic gradient: 500 mm to >1000 mm annual rainfall; soils neutral to acidic.
  - Habitats include blanket bog, moorland, forests, grasslands, lakes/reservoirs, floodplains, and salt marshes.
  - Stakeholders: water industries, shell fisheries, farmers, foresters, tourism, conservation groups, and local communities.
  - Data are tied to extensive baseline data across multiple habitat types and sampling sites.

- Habitats and sampling sites
  - 17 soil habitats sampled across Conwy catchment (sites 1-10, 14-21; Llyn Serw sites grouped for soil analysis).
  - Table 1 lists 22 site descriptions with dominant plant communities (e.g., Nant-y-Brwyn blanket bog, Llyn Serw blanket bog/heather, Capel Curig bog/acid grassland, Ingleborough NNR limestone grassland, various woodlands and grasslands, arable sites, etc.).

- 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
  - Data responsibility: Simon Smart.
  - NPP measured annually (2013–2015) for dominant plant species at all sites; four plots per site to represent main species.
  - Winter vegetation cutting and protective cages in grazed habitats; no cages where grazing absent.
  - Standing biomass measured at 10 of 17 sites across 3–9 replicates per habitat; aboveground biomass quantified by harvesting herbaceous layers and/or tree cores (woodland) to estimate biomass per m2.
  - NPP data linked to plant life strategies and used to inform ecosystem modelling (JULES).

- 3.1.2 Plant photosynthesis measures
  - Data responsibility: Lina Mercado.
  - Parameters: Asat (saturating irradiance, CO2), Vcmax (maximum carboxylation rate), Jmax (electron transport capacity) at 25°C.
  - Measurements on dominant species using CIRAS-I with CO2 chambers, later using LI-6400 with a leaf temperature of 20°C and CO2 range 50–2000 ppm.
  - Temperature corrections to 25°C using established methods; data processed with a Farquhar model-based approach; scripts available on GitHub.
  - References to methodological foundations provided (Farquhar et al., De Pury & Farquhar, Medlyn et al., Kattge & Knorr).

- 3.1.3 Leaf traits and plant community traits
  - Data responsibility: Lina Mercado and Simon Smart.
  - Traits measured: leaf N and P (%), leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover.
  - LMA determined from 10 leaves per site; leaf area via ImageJ; dry weight after drying; SLA = 1/LMA.
  - Leaf N and P analyzed in lab; part of efforts to parameterize plant–soil nutrient links for JULES.
  - Leaf trait data collected in 2013–2014 and processed accordingly.

- 3.2.1 General soil measures
  - Data responsibility: Helen Glanville.
  - Soil cores (to 1 m) collected from 17 habitats; depths split into intervals (0–15, 15–30, 30–45, 45–60, 60–75, 75–90, 90+ cm).
  - Analyses cover: soil water content (SWC), bulk density (BD), loss on ignition (LOI) and LOI-C, pH, electrical conductivity (EC), total C and N.
  - Sampling and QA/QC procedures detailed; multiple researchers involved in field sampling and laboratory processing.

- 3.2.2 Phosphorus
  - Data responsibility: Helen Glanville.
  - Phosphorus fractions measured in 17 habitats: Olsen P, Root-P, Complex-P, Enzyme-P, Proton-P.
  - Olsen P measured by 0.5 g soil extraction with 0.5 M NaHCO3; colorimetric determination (Malachite Green method).
  - Root-P measured with 0.01 M CaCl2 extraction; Complex-P, Enzyme-P, and Proton-P measured via colorimetry or established extraction protocols; detailed reagent prep provided.

- 3.2.3 Available carbon and nitrogen
  - Data responsibility: Helen Glanville.
  - Soil available C and N measured after 0.5 M K2SO4 extraction; DOC and TDN quantified (laboratory methods described); NO3 and NH4 analyzed via standard colorimetric/multisubstrate approaches.
  - Analytical workflow includes sample handling and QA steps.

- 3.2.4 Soil available cations (Ca, Na, K)
  - Data responsibility: Helen Glanville.
  - Extraction with 0.5 M acetic acid; cations measured by flame photometry; standard curves used to convert absorbance to concentrations.

- 3.2.5 Root biomass
  - Data responsibility: Helen Glanville.
  - Methods: 15 cm soil cores at 6 sites; roots separated into large (>2 mm) and fine (<2 mm); roots scanned with WinRhizo for length, diameter, branching; dried for biomass.
  - In-growth cores deployed to measure root growth over a growing season; specific locations and procedures described; biomass data linked to belowground processes.

- 3.2.6 Soil elements – TXRF
  - Data responsibility: Helen Glanville; laboratory work by Glanville, Havelange, Chesworth.
  - Total elemental analysis (Al, Fe, Ca, K, Ti, S, Ba, Mn, P, Sr, Zr, Cl, V, Rb, Zn, Cr, Nd, La, Cu, Y, Ni, Pb, Ga, Nb, Th, Co, Sc, As, Cs, U, Sn, Ge, I, Br, Sb, Se, Cd, Hg) via TXRF (Bruker S2 PICOFOX).
  - Sample prep includes drying, grinding, suspension in TritonX, deposition on discs, and gain correction.
  - Acknowledges limitations of TXRF method (documented in Turf2Surf_WP2_TXRF_Limitations_Glanville.rft).

- 4.0 Dataset structure
  - The data are organized into five CSV files:
    - Turf2Surf_Plant_biomass_data.csv
    - Turf2Surf_Plant_structural_data.csv
    - Turf2Surf_Plant_physiological_data.csv
    - Turf2Surf_Soil_Carbon_data.csv
    - Turf2Surf_Soil_raw data.csv
  - Column A: Site number (as in Table 1).
  - Columns B–C: Habitat name and detailed habitat description.
  - Column D: Site name.
  - Column E: Ecosystem Component (plant, soil, or roots).
  - Column F: If Plant, the species; otherwise NA.
  - Columns G–H: Plot number and Replicate number (plots 1–4; replicates used when measurements were not co-located with plots).
  - Column I: Soil depth interval for Soil and Roots components.
  - Missing values indicated as NA (due to restricted depths, limited replicates, or outliers).