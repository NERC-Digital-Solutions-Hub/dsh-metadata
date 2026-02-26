# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

## Aim and scope
- Presents supporting documentation for the CINAg project, which aims to optimise farm practices and soil management to improve nitrogen use efficiency (NUE) and reduce environmental nitrogen losses.
- Objectives include developing novel NUE indicators, testing in field experiments and farm platforms, and translating findings to Chinese farmers via the Science and Technology Backyard programme.
- Structured into work packages: WP1 (N cycling), WP2 (novel N technologies), WP3 (agronomic practices), WP4 (predictive capacity and knowledge exchange).

## Spatial scope and locations
- Four UK farm platforms for field experiments:
  - North Wyke (NW) – Devon
  - Harpenden (HA) – Herefordshire
  - Henfaes Farm (HF) – North Wales
  - Easter Bush (EB) – Edinburgh area
- 2018 UK-wide soil and biomass sampling across nine sites in Scotland, Wales, and England with diverse land uses (e.g., pristine, cattle-grazed, arable wheat, park grass, grazed margins, dunes).
- Site details include coordinates, soil types, textures, mean annual temperature (MAT), and mean annual precipitation (MAP).
- Figures and tables referenced for locations and site characteristics (e.g., coordinates, soil types, MAT/MAP).

## Datasets and key variables
- Experimental designs and measurements across multiple data themes:
  - Yields and biomass production (dry matter yields, quality metrics such as crude protein, metabolisable energy, fibre fractions, etc.).
  - Grass N content and N offtake; nitrogen use efficiency (NUEc, NUEg).
  - Greenhouse gas measurements: ammonia (NH3) emissions and nitrous oxide (N2O) emissions.
  - Soil nitrogen metrics: NH4+, NO3−, amino acids, peptides, mineralisable N; soil dissolved organic C and total dissolved N (DOC and TDN).
  - Soil microbial measurements: microbial biomass C and N (MBC/MBN); DNA targets (nifH, amoA, nirK, nirS, nosZ, ureC) and microbial diversity indices (OTUs, Shannon index).
  - Physical/chemical soil properties: aggregate size distribution, soil texture (sand/silt/clay), soil moisture, soil organic matter, pH, electrical conductivity (EC), base cations (Na, K, Ca, Mg), total C and N, total P; POXC and various P fractions (CEH Bangor, Olsen-P, acetic acid extractable P, citric acid extractable P).
  - Soil hydrology: soil water infiltration and soil water release curves (HYPRO/Durner models).
  - Plant/biomass sampling protocols and land-use sampling schemes from UK-wide sites.
- Data management and formats:
  - Data collected under WP1 and WP2 protocols; sampling dates and plots aligned within sites.
  - Appendices with detailed fertilizer application rates, plot layouts, harvest dates, and site-specific protocols.
  - Data compiled in Excel; QA/QC via standards, replicates, and cross-lab checks; some analyses use LIMS, and specialized software for N2O/NH3 flux analyses and sequencing pipelines.

## Experimental design and timelines
- 2016 inorganic fertilizer experiments (grass trials) conducted across NW, HF, EB with a three-cut silage system and total N around 240 kg N ha−1; treatments include urea, urea with inhibitor, ammonium-nitrate, and controls.
- 2016–2017 digestate experiment (winter wheat) at NW and HF with randomized block design; treatments include digestate alone, digestate with nitrification inhibitor, acidified digestate, and combinations; target N application rate ~190 kg N ha−1 as digestate.
- 2017 additional grass trials at EB and HA.
- 2018 UK-wide soil sampling across nine sites to capture diverse land uses and soil types and to measure aboveground biomass.

## Protocols and data processing
- Clear separation of protocols for WP1 (fundamental NUE metrics) and WP2 (novel technologies); sampling dates and methods may vary by site but plots are sampled on the same day within a site.
- Yields and biomass:
  - Harvest and sampling procedures varied by site; dry matter yields and quality measures (CP, ME, fibre fractions, D value) assessed by NIR or standard lab methods.
  - NUE calculations use grain/grass yield and N content relative to N applied, with control plots as baselines.
- Nitrogen content and N use efficiency:
  - N content estimated from protein where needed; N offtake computed from yield and N content; NUEc and NUEg derived from Nt, Nc, and Napplied.
- Greenhouse gases:
  - NH3 measured with wind tunnels and passive samplers; fluxes calculated from concentration differences and air flow; cumulative NH3 emissions integrated via area-under-curve methods.
  - N2O measured with static chambers (manual and automatic) and isotopic analyses; fluxes calculated from concentration changes and chamber geometry; cumulative fluxes estimated with Bayesian approaches and lognormal distributions; MCMC (JAGS) used for parameter estimation.
- Soil sampling and analyses (WP1 and WP2):
  - Topsoil cores (0–15 cm) and deeper samples collected with standard corers; NH4+/NO3− extraction and colorimetric analyses; mineral N pools quantified; DOC/TDN measured from sulfate extracts; DON inferred.
  - Soil physical/chemical properties measured across multiple subtopics (POXC, P fractions, DNA, OTUs, MBC/MBN, infiltration, water retention curves, etc.).
  - QA/QC includes laboratory standards, blanks, replication, and cross-lab checks; data processed in LIMS and Excel.
- Molecular analyses:
  - DNA extraction from soil; qPCR for nitrogen-cycling genes; amplicon sequencing for bacterial 16S and fungal ITS; diversity indices computed (Shannon, richness); taxonomic assignments via GreenGenes and UNITE databases.
- Data integration and accessibility:
  - Project webpage and related publications for data access and derived datasets.
  - Appendices provide granular methodological details for reproducibility and GIS-ready metadata.

## GIS-ready outputs and potential products
- Geolocated site coordinates and land-use context across multiple UK sites enable mapping of:
  - Spatial patterns of NUE indicators and N losses (NH3, N2O) across sites and treatments.
  - Spatial distribution of soil properties (N metrics, POXC, P fractions, C/N, pH, texture) and microbial indicators.
  - Land-use classifications and contemporaneous biomass/yield maps.
  - Temporal dynamics by linking flux measurements and soil/biomass data to sampling dates.
- Possible map layers and analyses for GIS specialists:
  - Plot-level treatment maps and harvest-yield surfaces.
  - Soil property rasters derived from point samples and interpolation.
  - NH3/N2O flux hotspots over fertilizer events, with dispersion-model or inverse-dispersion insights (FIDES-based approaches).
  - Cross-site comparisons of NUE and N-loss factors aligned with climate and soil typologies.

## Metadata, access, and references
- Project webpage: www.rothamsted.ac.uk/international/china/cinag
- Publications arising from the datasets:
  - Carswell et al., 2018 – assessing benefits and costs of different N fertilizers for grassland agriculture.
  - Sánchez-Rodríguez et al., 2018 – processing of digestate for mitigating N losses in winter wheat.
- Appendices (A1–A3) and figures provide granular data on plot layouts, fertilizer rates, and harvest dates, supporting reproducibility and GIS data tagging.

## Key takeaways for GIS specialists
- The CINAg documentation provides rich geolocated, multi-temporal, multi-proxy data across four primary UK farm platforms and nine additional sites, suitable for map-based data products and spatial analyses of NUE and nitrogen losses.
- Data encompass agronomic yields, soil chemical/physical properties, microbial gene abundances, and greenhouse gas fluxes, enabling integrated spatial dashboards and decision-support tools.
- Standardized protocols, QA/QC, and cross-institution collaboration support harmonized metadata, facilitating GIS integration and cross-site comparisons.