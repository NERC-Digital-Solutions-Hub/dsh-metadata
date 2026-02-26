# Metadata for data associated with dataset 'Measurements of carbon cycling processes in tropical forest soils varying in soil abiotic and biotic properties' (13C_Peru_fluxes.csv, 13C_Peru_soils.csv and 13C_PLFA_incorporation.csv)

- Study context
  - Ten sites along a tropical elevation gradient on the east flank of the Peruvian Andes (210 to 3400 m asl) with continuous forest cover.
  - Climate variables: annual temperatures 26-8 C; precipitation 1700-3200 mm yr-1; cloud-forest zone at 1500-3400 m asl.
  - Organic soil layer sampled from 5 sub-plots per site within 1 ha plots; samples stored at 4 C for 6 weeks before experiments.

- Dataset scope and metadata schema
  - Data associated with measurements of carbon cycling processes, including three CSV datasets: 13C_Peru_fluxes.csv, 13C_Peru_soils.csv, and 13C_PLFA_incorporation.csv.
  - Variables include: Elevation, Replicate, pH, TotC, TotN, Cnratio, BulkDensity, various PLFA metrics (FPLFA, BPLFA, GP, GN, F:B, GP:Gn), substrate information (Substrate, SubsName), respiration metrics (ActualFlux, Basal24/48/168, Subs24/48/168, Prime24/168), 13C-plfa and 13C-PLFA measurements (BPLFA13C, FPLFA13C, GP13C, GN13C, Unspec13C, TotPLFA13C), and derived metrics (PLFA_RESPC, 13CPLFA_PC).
  - Units and descriptions are provided for each variable (e.g., Elevation in metres above sea level; TotC and TotN in percent; BulkDensity in g cm-3; ActualFlux in CO2-C µg g-1 soil dw day-1; 13C labels in ng or µg per g soil dw; δ13C corrections for PLFA; etc.).

- Field sampling and experimental design
  - At each site, soils were collected from the organic layer within 1 ha plots; samples homogenized and characterized for abiotic properties.
  - Soils incubated with four 13C-labelled substrates (xylose, glycine, vanillin, hemicellulose) plus a control, at 75% of maximum water holding capacity, for 7 days at 20 C in the dark.
  - Substrates included both soluble and non-soluble forms; 100% 13C-labelled substrates mixed with 12C substrates to create ~10 at% labelled solutions.
  - Headspace sampling at 24, 48, and 168 hours; end-of-incubation analyses include PLFA biomarkers and δ13C measurements.

- Measurements and analytical methods
  - CO2 flux: measured by GC with a flame ionization detector; fluxes converted to CO2-C µg g-1 soil dw day-1; non-linearity addressed by fitting exponential curves.
  - Isotope analyses: δ13C of CO2 via IRMS after pre-concentration; calibration and blanks with quality-control standards; precision ≥ ±0.2‰.
  - PLFA analysis: extraction from soils, GC-MS identification, and internal standard quantification; biomarkers used to distinguish fungal (SP/ECM), Gram-positive, and Gram-negative bacteria; calculate total PLFA and relative ratios (F:B, GP:GN).
  - 13C-PLFA: δ13C values computed for individual PLFAs after correcting for methylation; percent substrate-derived C calculated for PLFAs; actual incorporation into PLFAs derived by combining abundance with isotope enrichment.
  - Calculations and metrics: enrichment expressed as δ13C; substrate-derived CO2 calculated via a mixing model; primed carbon determined as difference between treated and control respirations minus substrate-derived respiration; microbial carbon-use efficiency (CUE) calculated as 13C assimilated into PLFAs relative to 13C respired.
  - Data handling: exponential respiration curves used to derive fluxes; δ13C corrections account for derivatization and molecule-specific adjustments.

- Data processing, quality control, and provenance
  - Calibration against certified standards; daily instrument calibration for δ13C; blanks and reference standards included in batches.
  - Corrections applied for methanolysis δ13C when computing PLFA δ13C and substrate incorporation.
  - Documentation includes detailed description of each variable, units, and meanings to support reproducibility and reuse.

- Data governance, storage, and sharing guidance for Data Stewards
  - Ensure complete, consistent metadata with explicit units and descriptions for all variables; align field names across datasets (fluxes, soils, PLFA).
  - Maintain provenance: link datasets to the Maximum Prime study (Whitaker et al., 2014) and include full references to original methods and calibration procedures.
  - Data quality checks: verify any anomalous or misaligned metadata entries (e.g., noted in Prime24/Prime168 mappings) and correct inconsistencies before sharing.
  - Access and versioning: store datasets with clear versioning, assign persistent identifiers, and provide documentation that explains data processing steps and any transformations.
  - Sharing considerations: prepare data for upload to relevant data portals and catalogues; include explicit privacy-free, open-access-friendly licensing and usage terms.

- Challenges and considerations for data stewardship
  - Incomplete understanding of user needs may hinder dataset discoverability and reuse; provide user-focused metadata and usage notes.
  - Timely acquisition of data from field sites and standardization across multiple elevations and substrates.
  - Heterogeneous data formats and legacy databases; ensure interoperability through standardized units and controlled vocabularies.
  - Managing large, multi-component datasets (fluxes, soils, PLFAs, isotopes) with complex relationships; maintain clear relational links between datasets and their metadata.

- References and provenance
  - Core study framework and related analyses derive from Whitaker et al., 2014 (Maximum Prime: Microbe-substrate interactions control tropical forest soil carbon release) and associated literature cited in the metadata and methods.