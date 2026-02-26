# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

- Purpose and scope
  - Describes the CINAg project data collection, experiments, protocols, and processing to optimise farm practices and soil management for nitrogen use efficiency (NUE) and to reduce environmental Nr losses.
  - Aims to develop real-time, holistic soil health indicators and test them in field experiments; results are intended for translation to Chinese farmers via established outreach programs.

- Project structure and objectives
  - Four work packages (WP):
    - WP1: Improved fundamental understanding of N cycling
    - WP2: Harnessing novel N technologies
    - WP3: Improved agronomic practices
    - WP4: Predictive capacity and knowledge exchange
  - Key deliverables: data products and indicators to inform farm practices and soil management decisions.

- Geographic scope and site structure
  - Four main farm platforms in the UK:
    - North Wyke (NW), Harpenden (HA), Henfaes Farm (HF), Easter Bush (EB)
    - Each site has specific coordinates, soil types, textures, and climate profiles (Table 1 and Table 2 summaries).
  - Cross-UK atmospheric/soil sampling in 2018 at nine sites with at least two land uses each (Scotland, Wales, England):
    - Parsonage Down, Silwood, Harpenden, Wymondham, Plynlimon, Abergwyngregyn, Newborough, Easter Bush, Kirkton (Table 3 cross-referenced with Fig. 2).

- Data types and spatial-temporal coverage
  - Meteorological data and soil moisture (live measurements at multiple sites; WFPS calculations; daily rainfall and temperature at NW, HF; long-term station data at EB).
  - Experimental data across two major campaigns:
    - 2016: Inorganic fertiliser experiments on grassland (NW, HF, EB)
      - Treatments: Control, Urea (U), Urea + urease inhibitor (IU), Ammonium nitrate (AN)
      - Uniform P, K, S inputs per guidelines; 3 subplots per plot for NH3, soil sampling/N2O, and biomass yields
    - 2017: Digestate experiments on winter wheat (NW, HF) plus additional grassland trials at EB and HA
      - Treatments: Digestate, Digestate + DMPP (nitrification inhibitor), Acidified digestate, Acidified digestate + DMPP, Control
      - Target N: ~190 kg N/ha via digestate; plots subdivided for harvest and sampling
  - 2018 UK-wide sampling across multiple land uses (nine sites) with aboveground biomass measurements
  - Rich suite of soil and biogeochemical measurements (see below) and molecular analyses

- Measured variables and data layers (GIS-ready attributes)
  - Yields and biomass
    - Dry matter yields (t/ha), forage quality metrics (crude protein, ME, NDF, ADF, ash, etc.), metabolisable energy, digestibility
  - Nitrogen metrics
    - Grass/wheat N content, N offtake (kg N/ha), NUEc and NUEg calculations
  - Greenhouse gases
    - Ammonia emissions (NH3-N m-2 d-1), nitrous oxide (N2O-N m-2 h-1); flux measurements via wind tunnels, static/manual and automatic chambers; cumulative emissions
  - Soil nitrogen metrics (WP1 and WP2)
    - NH4+, NO3-, amino acids, peptides, mineralisable N
    - DOC and TDN; DON (calculated)
  - Soil physical and chemical properties
    - Aggregate size distribution; texture (sand, silt, clay); soil moisture, SOM
    - pH, EC; base cations (Na, K, Ca, Mg)
    - Total C and N; total phosphorus (P)
    - Permanganate oxidisable C (POXC)
    - P fractions: citric acid extractable P, acetic acid extractable P, Olsen-P
  - Soil microbial and molecular data
    - DNA extractions; nitrogen-cycling genes (nifH, amoA, nirK, nirS, nosZ, ureC); 16S rRNA and ITS amplicon sequencing; OTUs and diversity indices
  - Hydrology and soil physics
    - Soil water infiltration (infiltrometer), water release curves (HYPRO/Hyprop data) and related hydraulic parameters
  - Sampling framework and dates
    - WP1 vs WP2 sampling timelines; multi-year sampling at NW, HF, EB; 2018 sampling across sites with predefined dates (Tables 4–5 and related figures)

- Experimental design and treatments (GIS-relevant context)
  - Inorganic fertiliser grass trials (2016)
    - Randomised block design (NW, HF; EB with four controls and four replicates per treatment)
    - Treatments: U, IU, AN, Control; subplots for NH3, soil/N2O, biomass
  - Digestate trials (2017)
    - Complete randomised block design at NW and HF; five replicates per treatment
    - Treatments: Digestate, Digestate + DMPP, Acidified digestate, Acidified digestate + DMPP, Control
    - Harvest and sampling subplots defined; target N rate around 190 kg N/ha
  - UK-wide sampling (2018)
    - Sites chosen for diverse land uses and soil types; data enriched by UGRASS project sites

- Protocols, data processing and analysis
  - Sampling protocols separated by WP1 vs WP2; same-day sampling within a site; harvest season aligned with management guidance
  - Yields and quality: standardized sampling, drying and NIR-based analyses; site-specific harvesting methods
  - NUE and N content calculations: back-calculation from crude protein to total N (factor 6.25); NUE equations for crop and grain
  - Ammonia and N2O fluxes
    - NH3: wind tunnels, acid traps, ambient/background separation, area-under-curve integrations
    - N2O: manual and automatic chambers; isotopic analyses; Bayesian modelling approach to cumulative fluxes
  - Soil analyses (WP1 and WP2)
    - NH4+, NO3- via colorimetry; amino acids/peptides via OPA-MET; mineralisable N via anaerobic incubation
    - DOC/TDN via analyzers; MBC/MBN via chloroform fumigation; aggregates, texture via laser diffraction; SOM via LOI
    - pH, EC, base cations via standard extractions; total C/N by elemental analyzer or LECO systems
    - POXC, P extracts (CEH) and Olsen-P; DNA extractions and qPCR; amplicon sequencing and diversity metrics
  - Hydrology
    - Infiltration with Mini Disk Infiltrometer; HYPRO-FIT modelling for hydraulic parameters; water retention via HYPROP and WP4
  - Data management and QA/QC
    - Laboratory standards, replicates, blanks, reference soils, and cross-lab QA/QC procedures; R and JAGS used for statistical analysis; data compiled in Excel/LIMS

- Data availability and outputs
  - Project webpage: www.rothamsted.ac.uk/international/china/cinag
  - Publications derived from these datasets (examples cited)
  - Appendices include detailed site-specific tables, fertiliser rates, dates, and additional methodological detail

- Practical considerations for GIS specialists
  - Rich geolocated, plot-level, and sub-plot data across multiple years and sites enable multi-layer map visualisations (treatments, yields, soil properties, GHG flux hotspots, microbial gene distributions)
  - Temporal stacking across 2016–2018 supports time-series mapping of NUE indicators, soil health metrics, and gas emissions
  - Diverse data types require harmonised coordinate systems, consistent plot-level georeferencing, and careful handling of differing plot layouts across sites
  - Data standards and QA procedures support reliable integration with other soil, climate, and land-use datasets

- References and further reading
  - Key methodological references for gas flux calculations, soil analyses, and molecular assays are provided alongside project outputs and related publications

- Notes on provenance and collaborations
  - Core contributors include multiple UK-based institutions (CEH, Rothamsted, Bangor University, etc.) with new addresses noted for collaborators in Spain and Edinburgh Napier University
  - The dataset supports cross-disciplinary insights into N cycling, soil health, agronomic practices, and environmental impact mitigation