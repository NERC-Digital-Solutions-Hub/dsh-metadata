# Turf2Surf WP2 Supporting documentation for data

- The Turf2Surf project focuses on coupled nutrient cycling in terrestrial and freshwater ecosystems and its links to water quality, carbon sequestration and biodiversity.
- WP2 studies nitrogen and phosphorus related impacts on carbon exchange between land and atmosphere.
- Data are intended to support standardized monitoring, enabling cross-site comparisons and integration into models (notably JULES).

## Project, authors and versioning

- Project members: Bridget Emmett (CEH), Davey Jones (Bangor University), Simon Smart (CEH), Lina Mercado (Exeter University), Helen Glanville (Bangor University), Maria C Blanes (CEH), Harry Harmens (CEH), Sabine Reinsch (CEH).
- Authors: Sabine Reinsch (corresponding author), Helen Glanville, Simon Smart.
- Version dates: 01/06/2016; 25/08/2016; 04/11/2016.
- Data management aim: verify, quality assure, clean and transform data; store datasets and upload to appropriate portals; present outputs as clear formats; enable data to be reused beyond single outputs.

## 1.0 Information about the Conwy catchment

- Location and size: Conwy catchment in North Wales, ~500 km2; main river drains 380 km2 to tidal limit; estuary drains ~200 km2.
- Climate and topography: strong gradient from 500 mm/year to over 1000 mm/year; Snowdonia mountains up to 1064 m; varied soils from neutral to acidic.
- Habitats: blanket bog, montane/moorland, conifer woodlands, grasslands, lakes/reservoirs, flood plains, salt marsh.
- Stakeholders: water industries, shell fisheries, farmers/foresters, tourism, conservation groups, local communities.
- Objective: study ecological, biogeochemical and hydrological processes from gene to landscape scale; assess how pressures affect natural resources and benefits.

## 2.0 Habitats and sampling sites

- Table 1 lists habitats with unique site numbers, number of plots, location names, and dominant species (samples span 17 sites with multiple plots per site).
- Example site descriptions include Nant-y-Brwyn (blanket bog), Llyn Serw (blanket bog with varying age), Capel Curig (valley bog and acid grassland), Glasgwm (conifer woodland), Red Kite Woods (lowland mixed broadleaf), Ingleborough NNR (limestone grassland and hay meadow), Conwy arable, various pasture and woodland types, and montane habitats with bryophyte communities.
- Sampling design includes multiple plots per habitat to capture community and soil variation.

## 3.0 Equipment, protocols and data processing

- Overarching goal: link plant and soil nutrients to aboveground and belowground ecosystem processes for incorporation into JULES; standardized data capture and processing.
- 3.1 Aboveground components
  - 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
    - Annual NPP measured for dominant species at all sites (2013–2015); four plots per site represent main species.
    - Winter vegetation clipping with grazing-exclusion cages where applicable; biomass dried and weighed; standing biomass estimated for grasses/bogs and woodland via tree cores and leaf biomass integration.
    - Data processing linked to Turf2Surf WP2 aims to connect plant/soil nutrients to ecosystem processes; NPP data processed by Simon Smart; detailed methodology in Turf2Surf_WP2_NPP_Smart.rft.
  - 3.1.2 Plant photosynthesis measures
    - Parameters: Asat, Vcmax, Jmax (measured at 20–25°C; CO2 curves from 50–2000 ppm; light 1500 μmol m-2 s-1).
    - Field and lab protocols using CIRAS-I, LICOR systems; data analysis via fits to Farquhar model; temperature corrections using Bernacchi et al. and Medlyn et al.; scripts available from mdekauwe repository.
    - Data processing and analysis by MC Blanes and H Harmens; Vcmax/Jmax calculations by L Mercado.
  - 3.1.3 Leaf traits and plant community traits
    - Measurements: leaf N and P (%), leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover.
    - Leaf traits linked to photosynthesis studies; LMA derived from scanned leaves, with leaf area via ImageJ; chemical analyses via Vario and SEAL for N and P.
    - Data processing to support JULES parameterization; handled by MC Blanes and Simon Smart.
- 3.2 Soil components
  - 3.2.1 General soil measures
    - Intact soil cores collected (n=3 per habitat) to 1 m depth across 17 habitats; samples divided into depth intervals (0–15, 15–30, ..., 90+).
    - Measurements: soil water content (SWC), bulk density (BD), loss-on-ignition (LOI and LOI-C), pH, electrical conductivity (EC), total C and N (via elemental analyzer).
    - QA/QC and processing team listed; data linked to WP2 aims and JULES integration.
  - 3.2.2 Phosphorus
    - Olsen P, Root-P, Complex-P, Enzyme-P, and Proton-P fractions measured using standard colorimetric assays (Malachite Green) and extraction methods (Olsen P; 0.01 M CaCl2 for Root-P; citrate extractable P; enzyme-assisted P; 1 M HCl for recalcitrant P).
    - Detailed procedural steps for extractions, reagent preparation, plate loading, and absorbance measurement at 630 nm.
  - 3.2.3 Available carbon and nitrogen
    - Soil available C and N measured via 0.5 M K2SO4 extraction; DOC and TDN analyzed (DOC by Thermalox with NDIR; TDN via similar approach with NH4-N along with lysine/creatinine adjustments).
    - Nitrate (NO3) analyzed by vanadate method; Ammonium (NH4) analyzed by salicylate-nitroprusside/hypochlorite method.
  - 3.2.4 Soil available cations (Ca, Na, K)
    - 0.5 M acetic acid extraction; cations measured by flame photometry (Sherwood 410).
  - 3.2.5 Root biomass
    - Total and fine root biomass measured at six sites via 15 cm soil cores; roots scanned with WinRhizo for structural metrics; roots dried and weighed.
    - In-growth root cores implemented to assess root growth over a growing season; roots processed similarly.
  - 3.2.6 Soil elements – TXRF
    - Total elemental analysis (Al, Fe, Ca, K, Ti, S, Ba, Mn, P, Sr, Zr, Cl, V, Rb, Zn, Cr, Nd, La, Cu, Y, Ni, Pb, Ga, Nb, Th, Co, Sc, As, Cs, U, Sn, Ge, I, Br, Sb, Se, Cd, Hg) via TXRF (Bruker S2 PICOFOX).
    - Sample prep includes grinding, suspension with TritonX, deposition on discs, and TXRF analysis; limitations discussed in Turf2Surf_WP2_TXRF_Limitations_Glanville.rft.
- Data collection and processing teams are listed for each dataset, with QA steps embedded in procedures.

## 4.0 Dataset structure

- The data are organized into five data files:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Common data schema:
  - Column A: Site number (referenced from Table 1)
  - Column B: Habitat
  - Column C: Habitat description (detailed)
  - Column D: Site name
  - Column E: Ecosystem Component (Plant, Soil, Roots)
  - Column F (if Plant): Specific plant species; otherwise NA
  - Columns G and H: Plot number and Replicate number (Plot 1–4; replicates used when outputs were not co-located with plots)
  - Column I: Soil depth interval for Soil and Roots components
- Missing values are indicated as NA where data are unavailable due to depth restrictions, limited replicates, or outliers.
- Overall aim: provide a consistent, machine-readable dataset to support environmental monitoring and model integration (e.g., JULES) with clear traceability to sampling sites and habitats.

## Notes on purpose and use

- Data are designed to support monitoring of environmental health and policy performance over time by providing standardized, high-quality measurements of plant productivity, photosynthesis, leaf and soil traits, soil nutrient pools, and root dynamics.
- The five data files enable cross-cutting analyses of plant and soil processes, with explicit linkages to JULES model parameters and Turf2Surf WP2 objectives.
- The documentation emphasizes data provenance, standardized methodologies, and the potential for data reuse beyond the original project outputs.