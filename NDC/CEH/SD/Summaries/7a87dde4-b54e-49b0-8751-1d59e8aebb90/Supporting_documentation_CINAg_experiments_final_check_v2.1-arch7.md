# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

## Overview and aims
- Collaborative project (CINAg) to optimise farm practices and soil management for better nitrogen use and reduced environmental Nr losses.
- Objectives include developing indicators of nitrogen use efficiency (NUE), integrating real-time soil metrics, testing on-field practices and farm platforms, and translating developments to Chinese farmers via a Science and Technology Backyard programme.
- Project structure comprises four work packages: WP1 fundamental N cycling, WP2 novel N technologies, WP3 improved agronomic practices, WP4 predictive capacity and knowledge exchange.

## Geographic coverage and locations

### Four UK farm platforms (experimental hubs)
- North Wyke (NW) – Devon, Rothamsted and CEH involvement; grass trials and winter wheat trials conducted; inorganic fertiliser and digestate experiments over 2016–2017.
- Harpenden (HA) – Herefordshire, Rothamsted involvement; grass trials, part of 2017 activities (plant in 2017).
- Henfaes Farm (HF) – North Wales, Bangor University; grass trials (2016) and digestate/digestate-related treatments (2017).
- Easter Bush (EB) – Near Edinburgh, CEH (Edinburgh/Bangor collaboration); grass trial platform with multiple fertiliser treatments (2016) and broader sampling in 2017.

- Site details: coordinates and plots are provided in the project tables; soil types vary by site (Cambisols and Luvisols, etc.), with site-specific mean annual temperature and precipitation data.

### UK-wide sampling sites (2018)
- Nine sites across Scotland, Wales, and England with at least two land uses per site (e.g., pristine, cattle-grazed, arable rotations, park grass, glimmung/cultivation mixtures, dunes, etc.).
- Land-use diversity captured to support cross-UK soil-plant-N dynamics and aboveground biomass measurements.
- Sites include Parsonage Down, Silwood, Harpenden, Wymondham, Plynlimon, Abergwyngregyn, Newborough, Easter Bush, and Kirkton.

## Data collected and variables

### Experimental design and scope
- 2016: Inorganic fertiliser experiments on grassland at NW, HF, EB (three treatments plus controls) with complete randomized block design; total N applied around 240 kg N/ha.
- 2016–2017:  Digestate experiment on winter wheat at NW and HF; additional grassland trials at EB and HA in 2017.
- 2017: Digestate treatments include digestate alone, acidified digestate, digestate with nitrification inhibitor (DMPP), and combinations; control plots included.
- 2018: UK-wide soil sampling and aboveground biomass measurements across nine sites.

### Measured outputs and metrics (WP1 and WP2 emphasis)
- Yields and biomass: dry matter yields, grass quality metrics (crude protein, metabolisable energy, fibre components, digestibility, etc.) and grain/straw for wheat; harvest methods varied by site.
- Nitrogen metrics: herbage N content, N offtake, nitrogen use efficiency (NUEc, NUEg); total N in harvested crops; N application rates and uptake calculations.
- Soil nitrogen metrics (Nr): ammonium, nitrate, amino acids, peptides, mineralisable N; DOC and TDN, DON; soil moisture and SOM; pH and EC; base cations (Na, K, Ca, Mg); total soil C and N; total P; POXC; P fractions (CEH Bangor/Olsen/Acid extracts); DNA and nitrogen-cycling genes (nifH, amoA, nirK, nirS, nosZ, ureC); microbial diversity and OTUs.
- Microbial community analyses: amplicon sequencing (16S rRNA for bacteria/archaea; ITS for fungi); diversity indices (Shannon, Richness); qPCR for nitrogen-cycling genes; data processing with standard pipelines (GreenGenes, UNITE, DADA2).
- Gas emissions: ammonia (NH3) and nitrous oxide (N2O) flux measurements using wind tunnels, static manual and automatic chambers; flux calculations and cumulation over measurement periods; Bayesian approaches for N2O flux upscaling.
- Soil physical and chemical properties: texture (sand, silt, clay); aggregate size distribution; soil moisture; loss-on-ignition for SOM; pH (and CaCl2 pH) and EC; extractable base cations; total C and N; total P; POXC; citric/acetic-extractable P and Olsen-P.
- Infiltration and water retention: soil water infiltration measurements and HYPRO-model-based water retention curves; hydraulic conductivity parameters.
- Spatial and data-processing aspects: soil cores collected at specific depths (0–15 cm and 15–30 cm); sampling schedules aligned with WP1/WP2; QA/QC with standards and replicates; outliers and data integrity checks.

## Protocols, data processing, and QA

- Distinct sampling protocols for WP1 (soil-centric, pre- and post-treatment sampling schedules) and WP2 (treatment-specific sampling post-application, frequent early sampling).
- Standardized harvest and analysis procedures across sites, with site-specific adaptations due to weather and crop growth.
- Analyses performed with established laboratory methods (e.g., colorimetric assays for NH4+, NO3-; NIR for forage quality; Kjeldahl for total N; dry matter and grain assays).
- Molecular analyses (DNA extraction, qPCR, amplicon sequencing) with strict quality controls, including positive/negative controls, standard curves, and rarefaction criteria.
- Data processing tools include R (lm, cumtrapz), JAGS for Bayesian N2O flux inference, and standard LIMS for chemistry data; outputs compiled in Excel or LIMS.
- Documentation and data provenance: comprehensive appendix tables (A1–A3), site-specific harvest dates, fertiliser rates, and sampling schedules; project webpage and published datasets available.

## Project structure and outputs

- WP1: Deeper understanding of N cycling and soil health indicators.
- WP2: Harnessing novel N technologies (e.g., digestate processing, inhibitors).
- WP3: Improving agronomic practices based on NUE indicators and real-time metrics.
- WP4: Predictive capacity and knowledge exchange, including translation to farmers in China via established programmes.
- Data products are designed to support GIS mapping of field experiments, soil properties, land uses, and emission hotspots; includes cross-site comparisons and multi-resolution data (plot-level to site-level).

## Practical GIS considerations and references

- Geographic scope includes fixed farm platform coordinates and multiple land-use sites across the UK; time-series data for 2016–2018 enables spatial-temporal mapping of N dynamics.
- Data types suitable for GIS: site boundaries and coordinates, plot layouts, land-use classifications, soil property rasters (pH, texture, SOM, C and N), NUE metrics, NH3/N2O flux footprints, and biomass/yield distributions.
- Related outputs include methodological papers and datasets available via the project webpage: www.rothamsted.ac.uk/international/china/cinag, plus published articles in Archives of Agronomy and Soil Science and Frontiers in Sustainable Food Systems.