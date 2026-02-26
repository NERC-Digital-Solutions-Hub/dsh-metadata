# Turf2Surf WP2 Supporting documentation for data

- The Turf2Surf project focuses on coupled nutrient cycling in terrestrial and freshwater ecosystems, linking nitrogen and phosphorus impacts to carbon exchange between land and atmosphere, with an emphasis on water quality, carbon sequestration and biodiversity.
- WP2 aims to integrate plant and soil nutrient data into ecosystem process models (notably JULES) to improve representation of nutrient and carbon dynamics.

## Study area and aims

- Conwy catchment in North Wales (~500 km2) with a climatic gradient and a wide range of habitats (bogs, moorland, forests, grasslands, lakes, estuary).
- Aims to develop a holistic understanding of how pressures influence natural resources and their benefits, and to provide baseline data for broader research projects.
- Data are intended to be available to other research projects and are used to parameterize JULES and related analyses.

## Habitats, sampling sites and data scope

- 17 sites within the Conwy catchment with diverse habitats (e.g., blanket bog, heaths, conifer woodland, lowland deciduous woodlands, grasslands, montane communities, arable land).
- Sampling locations cover a range of soil and vegetation types to enable cross-habitat comparisons and process linking.
- Sampling programs include aboveground productivity, plant and leaf traits, soil properties, root biomass and growth, and soil elemental composition.
- Data collected between 2013 and 2016, with ongoing data processing and model integration.

## Measurements and methods (principal data streams)

- 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
  - NPP measured annually for dominant species at all sites (2013–2015); four plots per site; winter clipping with grazing protection in some habitats.
  - Aboveground standing biomass measured at 10 of 17 sites across habitats; methods differ by habitat (field biomass for grasses/bogs; tree cores and allometry for woodland).
  - Data processing linked to ecosystem processes and incorporated into JULES; NPP processing by Simon Smart; methodology described in Turf2Surf_WP2_NPP_Smart.rft.

- 3.1.2 Plant photosynthesis measures
  - Parameters: Vcmax, Jmax, Asat for dominant species.
  - Field and lab measurements using CIRAS-I, Licor 6400; CO2 curves from 50–2000 ppm; temperature corrections to 25°C.
  - Data processing and modeling scripts available (GitHub: mdekauwe/FitFarquharModel); measurements by Lina Mercado and Harry Harmens; Vcmax/Jmax calculations by Lina Mercado.

- 3.1.3 Leaf traits and plant community traits
  - Traits measured: leaf N and P (%), leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover.
  - LMA derived from scanning leaves; N and P analyzed using standard lab methods; SLA = 1/LMA.
  - Data processing and integration into JULES via WP2; measurements by Lina Mercado and Simon Smart.

- 3.2.1 General soil measures
  - Intact soil cores collected to 1 m depth across 17 habitats; depth-stratified sampling (0–15, 15–30, …, 90+ cm); a total of 300 samples.
  - Parameters: soil water content (SWC), bulk density (BD), loss-on-ignition (LOI and LOI-C), pH, electrical conductivity (EC), total C and N.
  - QA/QC and data processing by a team including Helen Glanville and collaborators.

- 3.2.2 Phosphorus
  - Soil Olsen P, root-available P (root-P), complex-P (citrate-extractable), enzyme-P (phosphatase and phytase) and other inorganic P pools.
  - Methods involve colorimetric Malachite Green assays and various extraction procedures (Olsen, CaCl2, citrate, HCl) with detailed reagent preparations.
  - Data processing and QA/QC by team led by Helen Glanville and collaborators.

- 3.2.3 Available carbon and nitrogen
  - Soil available C and N measured via 0.5 M K2SO4 extraction; analysis of DOC and total dissolved nitrogen (TDN) using CEH Bangor facilities.
  - Nitrate (NO3) and ammonium (NH4) analyses via colorimetric methods; DOC/TDN measurement procedures described.

- 3.2.4 Soil available cations (Ca, Na, K)
  - Extraction with 0.5 M Acetic acid; cations measured using a flame photometer.
  - Data processing by Glanville and collaborators; linked to WP2 and JULES parameterization.

- 3.2.5 Root biomass
  - Total and fine root biomass measured at six sites; 15 cm soil cores; root scanning (WinRhizo) for morphology; dry weight for biomass estimation.
  - In-growth root cores used to assess root growth over a growing season; cores designed and collected by team including Glanville and colleagues.

- 3.2.6 Soil elements - TXRF
  - Total elemental analysis (Al, Fe, Ca, K, Ti, S, …, U, Sn, Ge, I, Br, etc.) by TXRF (Bruker S2 PICOFOX) on 17 sites; samples prepared from 0–15 cm portions and ground to fine powder.
  - Data processing and analysis by Glanville, Chesworth, and Sabine Reinsch; limitations discussed in dedicated file Turf2Surf_WP2_TXRF_Limitations_Glanville.rft.

- Note: TXRF method limitations are documented in a dedicated file; data are linked to a broader goal of integrating plant-soil nutrient dynamics into JULES.

## Dataset structure and data availability

- Data are organized into five CSV files:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Data schema highlights:
  - Column A: Site number; Column B: Habitat; Column C: Habitat description; Column D: Site name; Column E: Ecosystem Component (Plant, Soil, Roots); Column F: if Plant, the species; Columns G and H: Plot and Replicate numbers; Column I: Soil depth interval for Soil and Roots.
  - Missing values are represented as NA; replicates account for non-co-located measurements.
- Purpose of dataset structure: facilitates cross-site, cross-habitat analysis and integration with process models (e.g., JULES).

## Data governance, processing and accessibility

- Principal data responsibility:
  - NPP and related processing: Simon Smart
  - Plant photosynthesis: Lina Mercado and H Harmens
  - Leaf and plant traits: Lina Mercado and Simon Smart
  - Soil and chemical analyses: Helen Glanville and collaborators
  - TXRF and elemental analyses: Glanville, Chesworth, and colleagues
- Data processing and modeling tools:
  - NPP data and processing described in Turf2Surf_WP2_NPP_Smart.rft
  - Photosynthesis modeling scripts and parameter estimates available (GitHub: mdekauwe/FitFarquharModel)
  - Data integration efforts aim to inform JULES parameterization and ecosystem process understanding
- Data sharing and openness:
  - Data are prepared to support collaboration with other research projects and to facilitate model parameterization; explicit public sharing policies are not detailed in this document, but baseline, site-level metadata and dataset structure are documented for reuse.

## Notable considerations and limitations

- TXRF limitations are acknowledged in a dedicated file (Glanville et al.), indicating awareness of method-specific constraints.
- Some measurements are habitat- or site-specific (e.g., woody biomass vs. herbaceous biomass; in-growth root cores), which may affect cross-site comparability and require careful harmonization in analyses.
- Data reflect the 2013–2015 measurement window (with some 2016 references) and are intended for integration with current or future ecological modeling efforts.

## Key takeaways for monitoring framework considerations

- Comprehensive, multi-component dataset: productivity, plant physiology, leaf traits, soil chemistry, root dynamics, and elemental soil composition across a gradient of habitats.
- Strong linkage to modeling: explicit aim to parameterize JULES and to integrate plant-soil nutrient dynamics into ecosystem process frameworks.
- Robust data structure and metadata: standardized data files with site, habitat, species, plot, replication, and depth information, enabling reproducibility and reuse.
- Emphasis on data quality and processing: documented QA/QC, standardized extraction and analysis protocols, and availability of data processing scripts and methodological notes.
- Governance and collaboration potential: data readiness for cross-project collaboration, with clear attribution to responsible researchers and institutions.