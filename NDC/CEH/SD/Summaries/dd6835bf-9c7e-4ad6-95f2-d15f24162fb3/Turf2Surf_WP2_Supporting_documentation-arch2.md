# Turf2Surf WP2 Supporting documentation for data

- The Turf2Surf project investigates coupled nutrient cycling in terrestrial and freshwater ecosystems and its links to water quality, carbon sequestration and biodiversity. WP2 specifically examined nitrogen and phosphorus impacts on carbon exchange between land and atmosphere.

## Project scope and contributors

- Project team includes: Bridget Emmett, Davey Jones, Simon Smart, Lina Mercado, Helen Glanville, Maria C Blanes, Harry Harmens, Sabine Reinsch.
- Authors: Sabine Reinsch (corresponding author), Helen Glanville, Simon Smart.
- Version dates: 01/06/2016; 25/08/2016; 04/11/2016.

## Study area and context

- Location: Conwy catchment, North Wales (~500 km2).
- Features: diverse landscapes enabling comparative survey; broad climatic gradient (precipitation from ~500 mm to >1000 mm across the catchment); range of habitats including blanket bog, moorland, woodlands, grasslands, lakes, flood plains and estuary.
- Stakeholders: water industries, shell fisheries, farmers/foresters, tourism, conservation groups and local communities.
- Aim: develop a holistic understanding of how pressures affect natural resources and their benefits.

## Habitats and sampling sites

- 17 soil habitats sampled across the Conwy catchment (sites 1–10, 14–21), with diverse habitats listed (e.g., blanket bog, acid grassland, conifer woodland, broadleaved woodland, upland oakwood, hay meadow, improved grassland, arable).
- For each habitat: multiple plots (most 1–4 plots per habitat) representing dominant species; detailed site descriptions provided (dominant species and habitat type when possible).

## Key measurements and data processing

- 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
  - NPP measured annually (2013–2015) for all dominant species at all sites; four plots per site representing main species.
  - Winter regrowth protected with cages where grazing occurs; standing biomass measured at 10 of 17 sites (3–9 replicates per habitat); methods differ for grassy/bog habitats vs. woodland.
  - Biomass calculations combine herbaceous biomass in quadrats and tree/shrub biomass from cores, volume formulas and wood density; leaf biomass added via litter fall.
  - Purpose: link plant production with soil nutrients and integrate outputs into JULES model (data processing by Simon Smart).

- 3.1.2 Plant photosynthesis measures
  - Parameters measured: Asat, Vcmax, Jmax (at 25°C) for dominant species.
  - Field measurements used CIRAS-I with CO2 equipment; CO2 curve measurements (50–2000 ppm) with Licor at 20–25°C.
  - Data processing uses Farquhar-based models; temperature corrections applied (Bernacchi et al., Medlyn et al.).
  - Outputs intended for integration into JULES; processing scripts available (GitHub link provided).

- 3.1.3 Leaf traits and plant community traits
  - Traits measured: leaf N and P (%), leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover.
  - LMA derived from leaf area and dry weight; SLA is inverse of LMA.
  - N and P analyzed with standard lab methods; data contribute to plant–soil nutrient linkage in JULES.

- 3.2 Soils and related measures
  - 3.2.1 General soil measures
    - Intact soil cores collected to 1 m (n=3 per habitat, across 17 habitats).
    - Analyses included soil water content (SWC), bulk density (BD), loss-on-ignition (LOI and LOI-C), pH, EC, total C and N.
    - SWC and BD calculated from moisture and core data; LOI estimates organic matter; LOI-C expressed as LOI adjusted to carbon content; total C and N measured by thermal oxidation.

  - 3.2.2 Phosphorus (P)
    - Olsen P (0.5 soil with NaHCO3 extraction) via malachite green colorimetry.
    - Root-P: 0.01 M CaCl2 extraction followed by colorimetric analysis.
    - Complex-P: 10 mM citrate extraction; malachite green analysis.
    - Enzyme-P: phosphatase and phytase activities measured with enzyme extracts and colorimetric P assay.
    - Proton-P: 1 M HCl extraction to assess recalcitrant inorganic P; colorimetric P analysis.

  - 3.2.3 Available carbon and nitrogen
    - Soil available C and N measured with 0.5 M K2SO4 extraction; analyses include NO3 (nitrate) and NH4 (ammonium) by colorimetric methods.
    - DOC and TDN measured at CEH Bangor using thermal oxidation and IR detection; QA/QC procedures described.

  - 3.2.4 Soil available cations (Ca, Na, K)
    - 0.5 M acetic acid extraction; cations determined by flame photometry; unit conversions and QA/QC implied.

  - 3.2.5 Root biomass
    - Total and fine root biomass measured at six sites using 15 cm soil cores; roots scanned with WinRhizo to quantify length, diameter, branching; dried to determine biomass.
    - In-growth cores deployed to measure root growth across seasons; cores retrieved and analyzed similarly.

  - 3.2.6 Soil elements – TXRF
    - Total element analysis (Al, Fe, Ca, K, Ti, S, etc.) by TXRF for all 17 sites; sample prep includes grinding and suspension plating on silicon discs.
    - Analyses performed by TXRF facility; limitations discussed in a dedicated file.

## Dataset structure and contents

- Five data files provided:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Column schema highlights:
  - Site number (unique identifier), Habitat and detailed Habitat description, Site name.
  - Ecosystem component: Plant, Soil, or Roots.
  - For Plant: species information; for Soil/Roots: NA.
  - Plot number (1–4) and Replicate number (for aligning outputs to plots).
  - Soil depth interval indicated for Soil and Roots components.
- Data gaps are indicated as NA.
- Purpose: standardized, queryable dataset to support environmental monitoring and policy evaluation, with outputs suitable for archival and portal submission.

## Data management and use

- Data verification, quality assurance, cleaning and transformation are undertaken using established methods from the project’s monitoring framework.
- Outputs are designed for clear presentation (reports, maps, charts) and for storage/upload to appropriate data portals.
- The WP2 dataset aims to enable broader access and reuse, supporting combined analyses with other data sources to increase dataset value and facilitate broader scrutiny and policy assessment.