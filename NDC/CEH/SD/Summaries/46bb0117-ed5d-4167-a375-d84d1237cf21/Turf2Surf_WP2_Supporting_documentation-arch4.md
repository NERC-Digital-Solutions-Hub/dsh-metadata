# Turf2Surf WP2 Supporting documentation for data

## Overview
- The Turf2Surf project investigates coupled nutrient cycling in terrestrial and freshwater ecosystems and links nitrogen and phosphorus impacts to carbon exchange between land and atmosphere.
- WP2 focuses on nitrogen and phosphorus related impacts on carbon exchange.
- Data gathered 2013–2015 from the Conwy catchment, with multiple collaborators and authors led by Sabine Reinsch et al.
- Version history: 01/06/2016; 25/08/2016; 04/11/2016.

## Study area: Conwy catchment
- Location: North Wales, ~500 km2 catchment with a wide range of landscapes.
- Drainage: Main river (~380 km2 to tidal limit) plus 200 km2 to the estuary.
- Climate gradient: 500 mm to >1064 mm annual precipitation; diverse topography (Snowdonia to lowlands).
- Habitats: Blanket bog, moorland, conifer plantations, grasslands, lakes, flood plains, salt marshes.
- Stakeholders: Water companies, shell fisheries, farmers/foresters, tourism, conservation groups, local communities.
- Data goal: Build a holistic understanding of pressures on natural resources and their benefits, with baseline data available for broader research.

## 1.0 Habitats and sampling sites
- 17 habitats sampled across Conwy catchment (table lists site numbers, plots, locations, and dominant species).
- Sites include blanket bogs, heath on blanket bog, valley bog, conifer woodland, lowland woodlands, oakwood, montane flora, improved grasslands, arable land, and other habitat types.
- Sampling design includes 4 plots per site for most data; site-specific replication varied by habitat.

## 3.0 Equipment, protocols and data processing
- Responsible data collection and processing teams are named for each measurement area.

### 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
- Annual NPP measured for dominant species at all sites (2013–2015) using summer/winter sampling and protective cages in growth seasons.
- Aboveground biomass measured at 10 of 17 sites (3–9 replicates per habitat); methods differ by habitat (grassland/bog vs. woodland/shrubland).
- For grasses/bogs: harvest and 1 cm height, dry and weigh; for woodland: tree cores from random plots; biomass per m2 calculated with area-specific formulas.
- WP2 linkage: NPP data prepared to inform JULES model parameters; detailed methodology described in Turf2Surf_WP2_NPP_Smart.rft.

### 3.1.2 Plant photosynthesis measures
- Parameters measured: Vcmax (max carboxylation at 25°C), Jmax (electron transport at 25°C), Asat (photosynthetic rate at saturating light).
- Field measurements (2013–2014) with CIRAS-I, leaf chambers; 2014–2016 using LICOR 6400 for CO2 response curves.
- Data processing uses A-Ci curves fitted to Farquhar model; temperature corrections to 25°C.
- Scripts and workflow available (GitHub link provided). Data processing and calculations by L. Mercado, CEH Bangor, and others.

### 3.1.3 Leaf traits and plant community traits
- Traits measured: leaf N (%), leaf P (%), leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover.
- LMA derived from scanned leaves; SLA = 1/LMA. N and P measured via standard lab methods; images analyzed with ImageJ.
- Data used to inform JULES parameterization as part of Turf2Surf.

### 3.2.1 General soil measures
- Soil cores collected spring 2014 from 17 habitats (depths 0–1 m, multiple depth intervals).
- Measured: soil water content (SWC), bulk density (BD), loss-on-ignition (LOI) and LOI-C, pH, electrical conductivity (EC), total C (C_tot) and total N (N_tot).
- QA/QC and multi-site compositional data processing described; core processing methods detailed.

### 3.2.2 Phosphorus
- Olsen P (extractable inorganic P via 0.5 M NaHCO3, pH 8.5) measured by malachite green colorimetric method.
- Root-P (0.01 M CaCl2 extraction) and Complex-P (10 mM citrate extractable P) measured similarly.
- Enzyme-P (phosphatase and phytase activity) assessed with enzyme extracts and colorimetric malachite green assay.
- Proton-P (1 M HCl extraction) used to estimate recalcitrant inorganic P; colorimetry as above.
- Data indicate multiple fractions to capture diverse P pools and bioavailability.

### 3.2.3 Available carbon and nitrogen
- Available C and N measured via 0.5 M K2SO4 extraction from 17 habitats; subsequent analyses include DOC and TDN.
- Nitrate (NO3) and ammonium (NH4) analyzed using standard colorimetric methods (vanadate/Miranda for NO3; salicylate-nitroprusside/hypochlorite for NH4).
- DOC/TDN quantified at CEH Bangor using established oxidation and detection protocols.

### 3.2.4 Soil available cations (Ca, Na, K)
- Extracted with 0.5 M acetic acid; cations measured by flame photometry.
- Site coverage matches other soil analyses; data support nutrient status interpretation and modeling inputs.

### 3.2.5 Root biomass
- Total and fine root biomass measured at 6 sites using 15 cm soil cores; roots cleaned, scanned (WinRhizo) for morphometrics; dried and weighed.
- In-growth root cores used to assess root growth over growing season; described methodology for installation, retrieval, and analysis.
- Data accompany aboveground biomass for integrated root–shoot carbon assessments.

### 3.2.6 Soil elements – TXRF
- Total elemental analysis (Al, Fe, Ca, K, Ti, S, Ba, Mn, P, Sr, Zr, Cl, V, Rb, Zn, Cr, Nd, La, Cu, Y, Ni, Pb, Ga, Nb, Th, Co, Sc, As, Cs, U, Sn, Ge, I, Br, Sb, Se, Cd, Hg) across 17 sites via TXRF (Bruker S2 Picofox).
- Sample preparation includes drying, grinding, suspension, and silicon disc deposition; QA/QC noted with internal standards.
- Data processing and limitations documented; intended to support nutrient cycling and soil–plant interaction analyses for JULES.

## 4. Dataset structure
- Datasets comprise five CSV files:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Common schema across files:
  - Column A: Site number (matching Table 1)
  - Column B: Habitat
  - Column C: Habitat description
  - Column D: Site name
  - Column E: Ecosystem component (Plant, Soil, Roots)
  - Column F: If Plant, the species; otherwise NA
  - Columns G–H: Plot number and Replicate number
  - Column I: Soil depth interval for Soil and Roots components
- Missing values indicated as NA due to depth restrictions, limited replicates, or outliers.
- Purpose: Facilitate cross-domain analyses (plant and soil) and integration into the Turf2Surf data system and JULES modeling.

## Data governance and usage notes
- Data responsibilities are specified per data type (NPP, photosynthesis, leaf traits, soils, roots, TXRF) to ensure traceability.
- The dataset is designed to support broader research collaborations by providing consistent baseline data across diverse habitats and depths.
- Linkages to the JULES model are explicit, aiming to incorporate measured plant and soil parameters into ecosystem process simulations.