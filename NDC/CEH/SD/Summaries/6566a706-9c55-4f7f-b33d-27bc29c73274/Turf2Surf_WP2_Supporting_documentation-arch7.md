# Turf2Surf WP2 Supporting documentation for data

- Purpose and scope: Turf2Surf project focusing on coupled nutrient cycling in terrestrial and freshwater ecosystems, linking nitrogen and phosphorus impacts to carbon exchange between land and atmosphere.

- Project team and authors: Bridget Emmett (CEH), Davey Jones (Bangor), Simon Smart (CEH), Lina Mercado (Exeter), Helen Glanville (Bangor), Maria C Blanes (CEH), Harry Harmens (CEH), Sabine Reinsch (CEH); corresponding author Sabine Reinsch; versions dated 01/06/2016, 25/08/2016, 04/11/2016.

- Data focus: WP2 studies nitrogen and phosphorus related impacts on carbon exchange; aims to link plant and soil nutrients to aboveground and belowground processes for incorporation into JULES (a land-surface model).

- Dataset context: Five data files describing plant and soil properties across the Conwy catchment, enabling map-based analyses of spatial patterns in productivity, nutrient pools, and soil chemistry.

- Spatial and governance context
  - Conwy catchment: ~500 km2 in North Wales with a strong climatic gradient (precipitation 500–1064 mm) and diverse habitats.
  - Habitats and stakeholders: blanket bog, moorland, heaths, woodlands, grasslands, lakes, flood plains, estuary areas; engaged stakeholders include water utilities, farmers, foresters, conservation groups, and communities.
  - Map reference: Figure 1 indicates sampling locations across the catchment.

- 1.0 Information about the Conwy catchment
  - Large climatic and topographic gradient; diverse habitats enabling comparative surveys.
  - Main river drainage and estuary dynamics; land-use patterns with agricultural productivity in the east and upland limitations in Snowdonia.
  - Rich baseline data available for broader research aims.

- 2.0 Habitats and sampling sites
  - 23 habitat-site entries with unique site numbers and plots, covering blanket bogs, heaths, coniferwoodlands, broadleaved woodlands, improved and semi-improved grasslands, arable land, and montane sites.
  - Each site lists number of plots and dominant vegetation descriptions (e.g., Nant-y-Brwyn blanket bog, Llyn Serw heaths, Capel Curig valley bog, Ingleborough NNR hay meadow, etc.).
  - Sampling locations chosen to reflect dominant species and habitat variety across the catchment.

- 3.x Data collection and measurements
  - 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
    - Annual NPP measured (2013–2015) for dominant species across four plots per site; winter mowing and protective cages where grazing occurs.
    - Aboveground biomass measured at 10 of 17 sites, with herbaceous biomass in grassland/bog and tree/shrub biomass in woodland; biomass calculations include tree volume, form factor, wood density, and litter components.
    - Aims to relate plant productivity to soil nutrients for integration into JULES.

  - 3.1.2 Plant photosynthesis measures
    - Measures of Asat, Vcmax, and Jmax for dominant species using CIRAS-I or Licor 6400 systems; field and lab protocols across 2013–2016.
    - Data processing via Farquhar-based models; temperature corrections to 25°C; open-source fitting code and references provided.

  - 3.1.3 Leaf traits and plant community traits
    - Leaf N, leaf P, LDMC, SLA, LMA, canopy height, and bryophyte cover measured (2013–2014).
    - LMA determined from 10 leaves per sampling area; leaf area via ImageJ; N and P analyses via standard lab methods.
    - Traits linked to nutrient status for integration into JULES.

  - 3.2.1 General soil measures
    - Intact soil cores collected from 17 habitats (0–1 m depth, multiple depth intervals); SWC, BD, LOI, LOI-C, pH, EC, total C and N measured.
    - QA/QC procedures noted; data processed to quantify soil physical and chemical properties.

  - 3.2.2 Phosphorus
    - Olsen P, Root-P, Complex-P, Enzyme-P, Proton-P fractions measured using colorimetric and extraction methods (Malachite Green, CaCl2 extracts, citrate extracts, enzyme assays).
    - Detailed extraction protocols and calculations described.

  - 3.2.3 Available carbon and nitrogen
    - Soil available C and N measured via 0.5 M K2SO4 extraction; nitrate analyzed by vanadate method; ammonium by salicylate-nitroprusside method.
    - DOC and TDN measured at CEH Bangor using standard protocols with QA considerations.

  - 3.2.4 Soil available cations (Ca, Na, K)
    - 0.5 M acetic acid extraction; cations measured by flame photometry; QA procedures noted.

  - 3.2.5 Root biomass
    - Total and fine root biomass measured at six sites using 15 cm soil cores; roots scanned with WinRhizo; dry weight calculated.
    - In-growth root cores used to estimate root growth; methodology for placement, extraction, and analysis described.

  - 3.2.6 Soil elements – TXRF
    - Total elemental composition (numerous elements) determined by TXRF (S2 PICOFOX); sample preparation and analysis workflow detailed.
    - Limitations discussed in accompanying notes.

- 4.0 Dataset structure
  - Five data files:
    - Turf2Surf_Plant_biomass_data.csv
    - Turf2Surf_Plant_structural_data.csv
    - Turf2Surf_Plant_physiological_data.csv
    - Turf2Surf_Soil_Carbon_data.csv
    - Turf2Surf_Soil_raw data.csv
  - Common schema notes:
    - Column A: Site number (consistent with Table 1 site numbers).
    - Column B: Habitat; Column C: Habitat description; Column D: Site name.
    - Column E: Ecosystem Component (Plant, Soil, Roots). If Plant, Column F lists species; otherwise NA.
    - Columns G–H: Plot number (1–4) and Replicate number (when needed for non-co-located measurements).
    - Column I: Soil depth interval (for Soil and Roots).
  - Data quality notes: Missing values indicated as NA; some datasets restricted by depth, replicates, or outliers.

- Abbreviations and glossary
  - Includes NPP, BD, Jmax, Vcmax, Asat, SLA, LDMC, LMA, SWC, LOI, LOI-C, NO3, NH4, DOC, TDN, Ca, Na, K, TXRF, JULES, etc., with definitions and context.

- GIS relevance and potential use
  - Spatial mapping of sites across the Conwy catchment enables visualization of productivity, nutrient pools, and soil chemistry patterns.
  - Dataset structure supports linking plant and soil measurements to locations for map-based analyses and ecosystem modelling inputs.
  - Rich, multi-depth soil and root data provide opportunities to model spatial variation in belowground processes alongside aboveground metrics.