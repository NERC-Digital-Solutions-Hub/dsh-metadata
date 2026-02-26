# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

## Overview and aims
- The CINAg project seeks to optimise farm practices and soil management to use nitrogen sources more efficiently and reduce Nr losses to the environment, thereby mitigating environmental impacts.
- Key aims:
  - Develop novel indicators of nitrogen use efficiency (NUE) and holistic soil health metrics to guide farming practices.
  - Test and develop on-field experiments and farm platforms for sustainable intensification.
  - Translate developments to Chinese farmers via the Science and Technology Backyard programme.
- Project structured into four work packages:
  - WP1: Improved fundamental understanding of N cycling
  - WP2: Harnessing novel N technologies
  - WP3: Improved agronomic practices
  - WP4: Predictive capacity and knowledge exchange

## Project structure and collaborators
- Multi-site UK research platforms: North Wyke (NW, Devon), Harpenden (HA, Herefordshire), Henfaes Farm (HF, North Wales), Easter Bush (EB, CEH Edinburgh) plus nine UK-wide sampling sites in 2018.
- Core institutions involved include Centre for Ecology & Hydrology (CEH), Rothamsted Research, Bangor University, and associated universities (e.g., University of Córdoba, Edinburgh Napier University).
- Experimental designs include inorganic fertiliser trials (grass trials) and a digestate experiment on winter wheat, plus extensive UK-wide soil and biomass sampling.

## Data types and scope
- Site and experimental metadata
  - Four UK farm platforms with coordinates, soils, climate data (MAT, MAP)
  - Land uses across nine UK sites (e.g., arable, pasture, grazed, etc.)
  - Detailed site characteristics: soil types, textures, mean temperatures, precipitation
- Experimental data
  - Inorganic fertiliser trials (grass): N treatments (urea, urease inhibitor, ammonium-nitrate, controls)
  - Digestate trials (winter wheat): digestate treatments, nitrification inhibitors, acidification, controls
  - UK-wide sampling (2018): biomass and soil measurements across multiple land uses
- Plant and yield measurements
  - Dry matter yields, crude protein, metabolisable energy, fibre fractions, digestibility, total mineral content, grain and straw yields (where applicable)
  - Nitrogen content and uptake (N content, N offtake), nitrogen use efficiency (NUEc, NUEg)
  - Thousand-grain weight and harvest-area calculations
- Soil chemical metrics
  - Nitrogen metrics: NH4+, NO3-, amino acids, peptides, mineralisable N
  - Dissolved organic carbon and nitrogen (DOC, TDN) and DON
  - Microbial biomass C and N (MBC, MBN)
  - Soil texture (sand, silt, clay), soil moisture, SOM, pH, EC
  - Base cations (Na, K, Ca, Mg), total C and N, total P
  - Permanganate oxidisable carbon (POXC)
  - Phosphorus pools: citric acid-extractable P, acetic acid-extractable P, Olsen-P
- Biological and molecular data
  - DNA extraction from soils and qPCR data for nitrogen-cycle related genes (nifH, amoA for AOB/AOA, nirK, nirS, nosZ, ureC)
  - OTUs and microbial diversity indices (Shannon, richness) from 16S rRNA and ITS amplicon sequencing
- Gas emissions
  - Ammonia (NH3) fluxes measured via wind tunnels, passive sorbent samplers, and dissolved trap analyses
  - Nitrous oxide (N2O) fluxes measured with manual and automatic chambers; concentration by GC and isotope analysis where applicable
  - Data processed to yield cumulative emissions and normalized emission metrics
- Physical process data
  - Soil infiltration (Mini Disk Infiltrometer) and hydraulic conductivity
  - Soil water release curves and HYPRO-FIT model outputs
  - Meteorological data from local weather stations and field sensors (rainfall, temperatures, soil temperature, WFPS)

## Data collection, protocols, and processing
- Experimental design and sampling
  - 2016: Inorganic fertiliser grass trials across NW, HF, EB; randomized block designs with multiple subplots per plot for NH3 and N2O measurements
  - 2017: Digestate trials on NW and HF; additional grass trials at EB and HA
  - 2018: UK-wide soil sampling across nine sites with at least two land uses per site
  - Sampling times: WP1 vs WP2 protocols; multiple timepoints (T0, T1, T2 for WP1; digestate monitoring for WP2)
- Yields and plant analyses
  - Harvesting and sub-sampling methods differed by site but aimed at representative measurements
  - Nutrient analyses performed using standard labs and methods; NUE calculations use harvested N content and applied N
- Soil sampling and analyses
  - Topsoil cores (0-15 cm) and deeper sampling (15-30 cm, >30 cm) depending on site
  - Nutrient extractions (NH4+, NO3- via colorimetry; amino acids; mineralisable N via anaerobic incubation)
  - DOC/TDN via analyses of K2SO4 extracts; DON derived
  - MBC/MBN via chloroform fumigation and correction factors
  - Physicochemical analyses: texture by laser diffraction, pH/EC, SOM (LOI), base cations by ammonium acetate extraction, total C and N, total P, POXC, extractable P pools
  - DNA and microbial community analyses: DNA extraction, qPCR, amplicon sequencing (16S rRNA, ITS), OTU/ASV analyses
- Gas measurements and modelling
  - NH3: wind tunnels and passive samplers; concentration measurements and flux calculations; time-series and cumulative emissions
  - N2O: manual and automatic chambers with gas analyses; cumulative flux via area-under-curve and Bayesian approaches
  - Atmospheric dispersion models used for NH3 at certain sites
- Data processing and QA/QC
  - Use of standard reference materials (BS1, BS3) and random replicates for QA
  - Data compiled in Excel and integrated into LIMS; cross-lab QA via multiple institutions
  - Rigorous statistical processing with R (and JAGS for Bayesian inference)
  - Publication-ready datasets linked to project outputs and peer-reviewed publications

## Data governance, storage, and sharing
- Data management through an integrated framework across multiple institutions and sites
- Documentation and metadata embedded in project reports, appendices, and the project webpage
- Data and methods align with established laboratory protocols and standard references (e.g., Mulvaney 1996; Miranda 2001; Keeney 1982; Ohno and Zibilske 1991; Murphy and Riley 1962)
- Outputs include publications and data-derived insights (e.g., NUE indicators, soil health metrics) with clear traceability to experiments and sites
- Project webpage and references provide access points for data descriptions and related publications

## Key challenges and considerations for data stewardship
- Users’ needs may be incomplete or evolving; datasets cover diverse measurements across multiple ecosystems and time scales
- Timely access to data from multiple sites and labs; harmonisation of protocols and units is essential
- Consistency in metadata (site, plot, treatment, sampling dates, methods) across institutions
- Handling large, heterogeneous datasets with varying formats (chemical analyses, sequencing data, gas fluxes, biomass)
- Interoperability across legacy and current databases; need for consistent data standards and repository structures
- Managing bespoke, non-interoperable solutions that may exist for certain legacy datasets

## Data deliverables and impact
- Comprehensive datasets supporting NUE development, soil health indicators, and nitrogen cycling understanding
- Cross-UK collaboration with potential translation to China via the Science and Technology Backyard program
- Datasets underpin publications on fertiliser types, digestate use, and nitrogen losses, contributing to sustainable agronomic practices

## Notable resources and outputs
- Project webpage: www.rothamsted.ac.uk/international/china/cinag
- Publications derived from these datasets (examples provided in the document)
- Appendices with detailed tables and supplementary experimental information (A1–A3), including fertiliser rates, harvest dates, and experimental layouts