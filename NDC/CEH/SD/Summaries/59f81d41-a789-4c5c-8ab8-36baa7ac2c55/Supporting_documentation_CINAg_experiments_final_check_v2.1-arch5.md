# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

- Aims: Develop improved nitrogen use efficiency (NUE) indicators and holistic soil-health metrics; test on-field N practices and farm platforms; translate findings to Chinese farmers via Science and Technology Backyard programmes.
- Project structure: Four work packages (WP1–WP4) addressing fundamental N cycling, novel N technologies, improved agronomic practices, and predictive capacity with knowledge exchange.
- Scope of datasets: Multi-site field experiments (2016–2018) across four UK farm platforms and nine UK sites, plus related laboratory measurements and analyses.

## 2. Information about the project (data-focused context)

- CINAg project aims to optimise farm practices and soil management to improve agronomic NUE and reduce environmental Nr losses.
- On-farm and cross-UK experiments designed to enable sustainable intensification and real-time soil-health assessment.
- Collaboration spans UK institutions with cross-UK farm platforms and laboratory analyses; data underpinning research that supports knowledge transfer to farmers.

## 3. Experimental platforms, sites and data collection

- Farm platforms (2016–2017): North Wyke (NW, Devon), Harpenden (HA, Herefordshire), Henfaes Farm (HF, North Wales), Easter Bush (EB, Scotland).
- Cross-UK sampling (2018): Nine sites across Scotland, Wales, and England with at least two land uses per site.
- Location and site metadata: Coordinates, soil types, textures, mean annual temperature (MAT), mean annual precipitation (MAP), and farm-field details provided for each platform and site.
- Experimental design summary:
  - 2016: Inorganic fertiliser experiments on grassland across NW, HF, EB; complete randomized block design with four treatments (Urea, Urea + inhibitor, AN, Control) plus P/K/S as per guidelines.
  - 2017: Digestate experiment on winter wheat at NW and HF; complete randomized block with five digestate/treatment plots (Digestate, Digestate + DMPP, Acidified Digestate, Acidified Digestate + DMPP, Control); two subplots per plot for harvest and sampling.
  - 2017: Additional grassland trials at EB and HA.
  - 2018: UK-wide soil sampling; include diverse land uses and soil types; data collection linked to the UGRASS project for context.
- Experimental layout notes: Specific subplot allocations for measurements (NH3, N2O, biomass); plot sizes and spacing varied by site and year; randomization and replication described.

## 4. Meteorological and site data

- On-site weather data: Daily rainfall, daily mean/min/max temperatures at NW, HF; EB used handheld probes and a permanent measurement station (temperature, rainfall, etc.) with 30-minute intervals.
- Soil moisture data: Water-filled pore space (WFPS) calculated from soil bulk density and moisture sensors at HF and NW.
- Long-term meteorological data: Easter Bush measurement station provided site-appropriate climate data.

## 5. Protocols and data processing

- Protocol distinction: Measurements separated by WP1 (fundamental soil/plant metrics) and WP2 (process-based agronomy and emissions).
- Harvests and yields (5.1):
  - Grass trials: three silage cuts; DM yields, crude protein, ME, NDF, ADF, ash, and digestibility metrics; NIR analysis; site-specific harvest methods.
  - Winter wheat: harvest for grain and straw; moisture and N analyses; yield calculations; TGW and DM adjustments.
  - UK-wide biomass assessments (2018): grazing-exclusion biomass estimates; field sampling and drying to determine dry biomass per unit area.
- Nitrogen content and NUE (5.2):
  - Grass N content derived from crude protein (factor 6.25) for 2016 NW/HF; 2017 grain/straw N content via direct analysis; NUEc and NUEg formulas using N applied and N offtake relative to controls.
- Greenhouse gases sampling (5.3):
  - Ammonia (NH3): wind-tunnel systems at NW/HF; acid traps; cumulative NH3 flux calculated from concentration differences and air flow; data processed with R and area-under-curve methods; EB used dispersion modelling for NH3 flux.
  - N2O: Manual and automatic chambers across NW/HF; mixed methodologies (gas chromatography, isotopic analyser) with time-series sampling; flux calculated per chamber method; cumulatives via area-under-curve and Bayesian approaches at EB.
  - Data treatment includes normalization to N applied, per-treatment comparisons, and use of advanced statistical modeling for cumulative fluxes.
- Soil sampling and nitrogen metrics (5.4WP1 and WP2):
  - Topsoil and subsoil cores collected with standardized tools; sampling times aligned with fertiliser events and harvests.
  - Nitrogen metrics: NH4+, NO3-, amino acids, peptides, mineralisable N; DOC/TDN in K2SO4 extracts; DON derived; MBC/MBN (chloroform-fumigation method); aggregate size distribution; soil texture by laser diffraction; soil moisture and SOM (LOI); pH and EC; base cations (Na, K, Ca, Mg) by ammonium acetate extraction; total C and N by elemental analyzers; total P by H2O2/H2SO4 digestion with colorimetric readouts.
  - POXC, various P fractions (CEH Bangor Olsen and citrate-extractable P), and acetic-acid extractable P measured to assess available pools.
  - DNA-based analyses: extraction and qPCR for nitrogen cycling genes (nifH, amoA, nirK, nirS, nosZ, ureC); 16S rRNA and ITS amplicon sequencing for microbial communities; diversity indices (Shannon, richness) and OTU analyses; sequencing performed at CEH Wallingford and other labs with QC steps.
  - Microbial and soil functional data paired with plant measurements for integrated NUE and soil health assessments.
  - Infiltration and water-release curves: Mini-disk Infiltrometer and hyprop methods; HYPRO-FIT modelling with Mualem-Durner frameworks; experiments across multiple land uses.
- Data management and QA/QC:
  - Multi-lab data generation with QA/QC using standards (BS1/BS3) and reference soils; random replicates; calibration curves and method controls; data consolidation in Excel and LIMS; cross-checks by project staff; R-based analyses and Bayesian/MCMC approaches for gas flux data.

## 6. Data management, storage and access

- Data capture and storage: Protocols specify data captured at field sites, laboratory analyses, and digital records in Excel spreadsheets; LIMS usage indicated for data management and reporting.
- Documentation and provenance: Detailed experimental designs, site coordinates, soil types, treatment details, sampling dates, and method references provided to support traceability.
- Access and dissemination:
  - Project webpage hosting information and dataset descriptions.
  - Publications derived from the datasets (two listed articles with DOIs); data-to-publication links indicated.
  - Datasets are associated with the CINAg project and supporting documentation; data reuse is supported through described methods and metadata, with references to primary publications.

## 7. Outputs and key data types

- Plant and crop data: yields (DM), CP, ME, N content, NUEc, NUEg; grain vs. straw yields; TGW.
- Soil and nutrient metrics: NH4+, NO3-, amino acids/peptides, mineralisable N; DOC/TDN/DON; MBC/MBN; aggregate size distribution; texture; SOM; pH and EC; base cations; total C and N; total P; POXC; citrate- and Olsen-extractable P; acetic-acid extractable P.
- Microbial and genetic data: DNA extracts; qPCR gene abundances for nitrogen cycling genes; OTU and diversity indices; fungal ITS data; 16S rRNA gene data.
- Gas emissions: NH3 fluxes (field-based); N2O fluxes (static chambers and automatic chambers); cumulative fluxes with model-based upscaling.
- Hydrology and soil physics: soil infiltration (mL), water retention curves, hydraulic conductivity parameters.
- Metadata: site-level information (coordinates, soil types, MAT, MAP), treatment details, experimental layouts, sampling dates, and measurement units.

## 8. Practical guidance for data stewardship and reuse

- Ensure dataset integrity with comprehensive metadata: include site coordinates, soil type, climate data, planting/harvest dates, treatment codes, and unit conventions.
- Maintain clear data provenance: document measurement methods, instruments, QA/QC procedures, and data processing steps (including equations and statistical models used).
- Standardize data schemas and dictionaries across labs and sites to support interoperability (naming conventions, units, and measurement definitions).
- Archive data in a durable repository with versioning; link to related publications and the project webpage; preserve lab protocols, appendices, and the data dictionary.
- Consider licensing and access terms for downstream users; provide data usage notes and any embargo periods if applicable.
- Ensure data quality through ongoing QA/QC checks, including: blanks/standards in assays, cross-lab verifications, instrument calibration records, and regular validation against reference materials.

## 9. Related publications and resources

- Publications derived from the datasets:
  - Carswell et al., 2018. Assessing the benefits and wider costs of different N fertilisers for grassland agriculture.
  - Sánchez-Rodríguez et al., 2018. Advanced processing of food waste based digestate for mitigating nitrogen losses in a winter wheat crop.
- Project webpage: www.rothamsted.ac.uk/international/china/cinag
- Data and methodology references included throughout the document (Beever et al., Bremmer, Keeney, Loubet et al., etc.) for QA/QC, measurement methods, and modelling approaches.

## 10. Appendices and supplementary material

- Appendices include detailed tables A1–A3 (fertiliser/digestate application rates, harvest dates, and plot designs) and site-specific pre-treatment information.
- Detailed protocol schematics, sampling dates, and data processing instructions are documented to support reproducibility and future data integration.