# WP1 - Physico-chemical characterization of anaerobic digestate and biomass ash derived from UK bioenergy production (anaerobic digestion and thermal transformation)

- Overview
  - AVAnD project ran from January 2015 for 3 years; collected bioenergy waste streams (digestates and biomass ashes) from UK sites (and ashes from Spain) for research.
  - WP1 focuses on physico-chemical characterization and formulation of waste blends; data used primarily for batches 1 and 2, but the dataset includes all batches to cover WP1’s scope.
  - Samples processed following ISO/DIS 14820-2 and BS EN 15002:2006; minimum subsample size 0.5 kg; analyses sometimes outsourced to accredited external laboratories.

- Materials and sampling
  - Anaerobic digestates: collected from multiple industrial-scale UK plants at several time points (batches 1–8 spanning 2015–2018); from batch 3 onwards, inclusion limited to selected digestates for WP1-related work.
  - Biomass ashes: sourced from Spain and the UK (six ash types total: fly and bottom ashes across sources); samples 10–20 kg each; fresh subsamples air-dried, milled, and sieved to 1 mm; dried samples processed at 105°C when needed.
  - Fresh vs dried preparation noted; some analyses relied on external laboratories for specific nitrogen and phosphorus forms.

- Batches and sources
  - Digestates: batches 1–8 with varied feedstock compositions (e.g., source-segregated food waste, maize silage, vegetables waste, anaerobically treated waste).
  - Ashes: multiple sources and types; detailed source codes and batch timing provided (e.g., ABaF, ABaB, ASe, ALuF, ALuB, Aspa, etc.).
  - For WP1, data from batches 1 and 2 are the primary dataset; all batches included to ensure comprehensive characterization across waste streams.

- Methods and analyses
  - Standard analytical methods summarized in TABLE 3; modifications described where applicable.
  - In-house measurements complemented by external laboratory results for select parameters (notably nitrogen and phosphorus forms in some batches).
  - Key measurement suite includes pH, electrical conductivity (EC), total carbon (TC), total nitrogen (TN), carbon-to-nitrogen ratio (C/N), dry matter (DM), loss on ignition (LOI), nitrates and ammonium species (NO3-, NH4+, NO3-N, NH4-N), and a broad suite of water-soluble and aqua regia soluble elements.

- Data structure and variables (GIS-friendly framing)
  - material_type: Digestate or Ash
  - batch_id: numeric (1–8)
  - source_code: codes like DB1, DB2, DB3, DB4/D1, Dba/D2, DTa, ABaF, ABaB, ASe, ALuF, ALuB, Aspa, etc.
  - sampling_date: date of collection
  - location: country/region (UK, Spain) and plant_id if available
  - feedstock_composition: description of feedstock (e.g., source-segregated food waste, maize silage, vegetables waste)
  - sample_mass: kg per digestate sample or ash batch
  - DM: dry matter (%)
  - pH: pH units
  - EC: electrical conductivity (mS/cm)
  - TC: total carbon (g/kg)
  - TN: total nitrogen (g/kg)
  - C_N: carbon-to-nitrogen ratio (TC/TN)
  - NO3-, NH4+, NO3-N, NH4-N: nitrogen species (g/kg or as noted)
  - WSCa, WSMg, WSK, WSNa, WSCu, WSFe, WSMn, WSNi, WSPb, WSZn: water-soluble extractable elements (various units)
  - ARCa, ARMg, ARK, ARNa, ARP, ARS, ARAl, ARCd, ARCo, ARCr, ARCu, ARFe, ARMn, ARNi, ARPb, ARZn: aqua regia extractable elements (various units)
  - methods_reference: methodology notes (e.g., BS EN 13137, ISO/DIS 13395)
  - data_quality_flags: BDL (below detection), blanks (not measured), replicates (analytical)
  - notes: dry-basis normalization assumed unless stated otherwise; some data are “in-house” only

- Data quality, provenance, and notes
  - Some datasets include external laboratory results (notably Available N & P for batch 2).
  - Replicates are analytical; blanks indicate missing measurements or differing replicate counts.
  - All results expressed on a dry basis unless specified.
  - The dataset documents method origins, with a catalog of referenced standards (ISO, BS EN, DIN) and equipment mappings.

- GIS use and potential applications
  - Spatial distribution: map AD plants and ash sources across the UK (plus Spain for ash), linked to batch dates and feedstock types.
  - Thematic maps: visualize spatial variation in key physico-chemical properties (e.g., TN, TC, C/N, nutrient contents) by site and batch.
  - Data fusion: combine dataset with plant-level attributes (location, feedstock mix) to support formulation of waste blends and to assess suitability for policy or industry use.
  - Temporal analysis: track changes over batches and relate to processing conditions or feedstock changes.
  - Inform policy/communication: produce map-based summaries for stakeholders (policy colleagues, clients, public) showing nutrient potential, contaminant profiles, and processing contexts.

- Limitations and considerations for mapping
  - Geospatial details are limited to plant locations and country-level sources; precise coordinates are not provided in the description.
  - Some analyses depend on external lab results; ensure metadata includes provenance when integrating.
  - Only batches 1–2 are the primary WP1 focus for characterization, though all batches are included for comprehensive WP1 coverage.

- References and standards
  - ISO/DIS 14820-2; BS EN 15002:2006; BS EN 16168:2012; BS EN 13137:2001; BS EN 13037:2011; BS EN 14346:2006; BS EN 15169:2007; ISO/DIS 13395; BS ISO 15958; DIN EN ISO 15681-2; BS EN 13652; BS EN 13657, among others.
  - Documentation notes indicate data points and the relationship to TABLE 1, TABLE 2, and TABLE 3 for sample origin, composition, and analytical methods.