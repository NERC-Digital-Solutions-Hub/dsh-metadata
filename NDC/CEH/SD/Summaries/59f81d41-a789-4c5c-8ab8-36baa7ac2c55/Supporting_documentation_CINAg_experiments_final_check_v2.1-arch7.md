# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

- Purpose: Document the CINAg project datasets to optimise farm practices and soil management for improved nitrogen use efficiency and reduced environmental Nr losses, with UK and China collaboration across multiple work packages.

## Spatial scope and locations

- Four UK farm platforms (field-scale experiments):
  - North Wyke (NW) – Devon
  - Harpenden (HA) – Herefordshire
  - Henfaes Farm (HF) – North Wales
  - Easter Bush (EB) – Edinburgh area
- 2016–2017: inorganic fertiliser grass trials and digestate experiments across these four platforms
- 2018: nine UK-wide sites for soil sampling and aboveground biomass measurement (Scotland, Wales, England)
  - Land uses across sites include pristine, cattle grazed, arable, grassland, park grass, soils with varied textures and drainage
- Coordinate and site-type details provided in tables and figures (e.g., site coordinates, soil types, MAT, MAP)

## Data types and key variables

- Experimental data
  - Inorganic fertiliser experiments (grass trials, 2016) and related harvest yields
  - Digestate experiments (winter wheat, 2017) with digestate and inhibitors treatments
  - UK-wide sampling (2018) for land-use comparisons and biomass measurements
- Plant yields and quality
  - Dry matter yields, crude protein, metabolisable energy, fibre fractions, digestibility, total mineral content, D-value
  - For wheat: grain and straw yields, moisture, TGW
- Nitrogen metrics
  - N content in herbage, N offtake, nitrogen use efficiency (NUEc and NUEg)
  - Grain and crop N content via Kjeldahl analysis at EB; lab-specific calculation methods
- Greenhouse gas and ammonia measurements
  - Ammonia (NH3) fluxes via wind tunnels and passive samplers; N2O fluxes via manual and automatic chambers
  - Methodologies for NH3 and N2O sampling, trapping, and flux calculations
- Soil nitrogen metrics (WP1 and WP2)
  - NH4+, NO3-, amino acids, peptides, mineralisable N
  - DOC and TDN; DON
  - Microbial biomass C and N (MBC/MBN); DNA-based measures
- Soil physical and chemical properties
  - Aggregate size distribution; texture (sand, silt, clay)
  - Soil moisture, soil organic matter (LOI)
  - pH and electrical conductivity; base cations (Na, K, Ca, Mg)
  - Total soil C and N; total P
  - POXC (peroxidizable carbon)
  - Citric acid extractable P, acetic acid extractable P, Olsen-P
- Molecular and microbial ecology
  - DNA extractions; qPCR targets for nitrogen cycling genes (nifH, amoA AOB/AOA, nirK/nirS, nosZ I/II, ureC)
  - OTUs and microbial diversity indices (Shannon, richness); 16S and ITS amplicon sequencing data
- Hydrology and soil hydraulics
  - Soil water infiltration (infiltration rate, hydraulic conductivity)
  - Soil water release curves; HYPRO-FIT modeled parameters
- Metadata and QA/QC
  - Protocols, sampling dates, subplots, replication, QA/QC standards, data processing workflows

## Experimental design, sampling, and data collection

- 2016 inorganic fertiliser experiments (grass): three sites (NW, HF, EB) with a complete randomized block design; four fertiliser treatments plus controls; plot sub-division for NH3, N2O, and biomass sampling
- 2017 digestate experiments (winter wheat): complete randomized block design at NW and HF; five treatments (digestate with/without acids and nitrification inhibitors, plus controls); two subplots per plot for harvest and sampling
- 2018 UK-wide sampling: multiple land uses and soil types across nine sites; biomass measurements via grazing exclusion where applicable
- Meteorological and soil data collection
  - Daily rainfall and temperatures at NW, HF; soil moisture sensors (2.5 cm depth); EB measurements with hand probes plus long-term station data
- Protocols emphasize standardized timing within sites, with adjustments for weather and growth, and cross-WP sampling alignment

## Data processing, metrics, and analysis approaches

- Yields and quality
  - Dry matter yields converted to per hectare basis; NIR-based quality analyses
- Nitrogen use efficiency
  - NUEc and NUEg calculated using crop N offtake, control means, and applied N
- Greenhouse gases
  - NH3 fluxes computed from wind-tunnel trap data; N2O fluxes from static chambers (manual and automatic as applicable)
  - Cumulative fluxes derived using area-under-curve methods and Bayesian/MCMC-based approaches for undefined distributions
- Soil and microbial analyses
  - NH4+/NO3- and other N metrics derived from KCl extraction; DOC/TDN measured via analyzers
  - MBC/MBN calculated from DOC/DON differences post microbial kill; aggregate size and texture analyzed by standard lab methods
  - DNA and qPCR data generated for nitrogen-cycling genes; amplicon sequencing processed for OTU/diversity analyses
- Data integration and quality control
  - QA/QC protocols include lab standards, random replicates, and cross-lab validation
  - Data compiled in Excel and integrated into LIMS for final reporting

## GIS-ready layers and mapping considerations

- Potential geospatial data layers to create
  - Farm platform boundaries and field plots (NW, HA, HF, EB)
  - Digestate treatment bands and control plots within wheat/digestate experiments
  - Treatment types, replication, harvest dates, and yield/quality surfaces
  - NH3 wind-tunnel locations, NH3 trap points, and N2O chamber positions
  - Meteorological stations and measurement stations per site
  - UK-wide sampling sites with land-use classifications and soil type
  - Soil property rasters or polygons (pH, EC, texture, SOM, P pools, N metrics)
  - Soil hydraulic data (infiltration points, HYPRO-FIT curves, water release curves)
- Spatial and temporal alignment
  - Multi-resolution data: plot- and field-scale (m–ha) layers nested within country-scale site networks
  - Time series alignment for yield harvests, gas flux campaigns, and soil sampling dates
- Recommended GIS tasks
  - Create georeferenced shapefiles/geoJSON for plots, plots’ fertilizer/digestate treatments, and measurement points
  - Join lab-derived metrics to spatial units (plots, fields, plots-by-site)
  - Visualize temporal trends by site and by treatment, with capacity for interactive maps
  - Overlay with land-use and soil-type rasters to analyze spatial patterns of NUE, N losses, and soil health indicators

## Data sources, access, and references

- Project website: www.rothamsted.ac.uk/international/china/cinag
- Key publications derived from these datasets (examples in document)
  - Assessing the benefits and wider costs of different N fertilisers for grassland agriculture
  - Advanced processing of food waste based digestate for mitigating nitrogen losses in a winter wheat crop
- Appendices and tables provide detailed parameters, dates, and specific treatment rates per site

## Practical takeaways for GIS work

- The dataset offers rich, multi-layer geospatial context: standardized farm-platform geography, plot-level treatments, measurement points, and UK-wide sampling sites
- Visualization opportunities include NUE maps, N-loss hot spots (NH3/N2O), soil-health indicator surfaces, and biomass yield distributions
- Data integration will require harmonizing coordinates, land-use classes, and unit conventions across WP1 and WP2 datasets, with attention to differing resolutions and QA/QC standards
- The materials support development of map-based data products for policymakers, clients, and the public, aligned with the GIS Specialist aim of enabling easy comprehension and exploration of nitrogen agronomy information