# Vegetation work

- A multi-component ecological data collection protocol covering vegetation, soil, microbial, and faunal aspects to support ecosystem assessments.
- Aims aligned with data stewardship: generate usable, well-documented datasets that meet standards and can be discovered and reused.

## Datasets and data types

- Vegetation metrics:
  - Species cover estimates from four 50 cm × 50 cm quadrats per site.
  - Species richness; grasses and forbs cover summed across quadrats.
  - Biomass per quadrat: clipped at soil surface, dried at 80°C for 24 h, weighed; summed to site level (g biomass m^-2).
  - Diversity metrics: Shannon's index.
  - Community weighted mean (CWM) trait values derived from species traits databases.
  - Trait categories include longevity, plant height, specific leaf area, root architecture, rooting depth, and mycorrhizal (VAM) affinity; trait values sourced from LEDA and PlantATT databases.
- Greenhouse gas fluxes:
  - CO2: net ecosystem exchange, photosynthesis, and respiration using four 25 cm collars with transparent chambers and an infrared gas analyser; measurements with two-minute trials, repeated with dark measurements; concurrent soil moisture, temperature, and PAR (in triplicate).
  - Calculations convert chamber data to CO2 flux (mg m^-2 h^-1) with time-based flux formulas.
  - CH4, CO2, and N2O: gas samples collected via reflective-chamber method; analyzed with a gas chromatograph; flux calculations parallel to CO2 method.
- Soil and physical properties:
  - Six soil cores per site (4 cm width) to 10 cm depth; samples sieved to remove stones/roots; subsamples allocated for PLFA and DNA; remaining soil stored for analysis.
  - Bulk density: from two cores, 0–5 cm and 5–10 cm, dried and weighed.
  - pH: soil-water slurry (1:1), measured with pH meter.
  - Volumetric moisture content: fresh weights dried to determine moisture fraction.
- Molecular and biochemical analyses:
  - PLFA lipids: Bligh and Dyer extraction with phase separation; neutral, glycolipid, and phospholipid fractions isolated; internal standards added; GC analysis of fatty acids (e.g., C14:0, C16:0, C18:2(n-6), etc.); PLFA concentrations calculated in nmol g^-1 dry soil; most fatty acids identified as bacterial biomarkers.
  - DNA sequencing: soil DNA extracted (MOBIO Powersoil kit); 16S (bacteria) and 18S (eukaryotes) amplicons prepared with dual-indexed primers; libraries pooled and sequenced on Illumina MiSeq (V3, 600 cycles); data processed to cluster OTUs at 97% similarity; results reported as OTU relative abundances per sample.
- Soil fauna and nematodes:
  - Soil fauna: cores collected with appropriate corers; three subsamples per plot; use of Berlese-Tullgren funnels to extract microarthropods and annelids; large earthworms hand-sorted; extracts preserved in 75% ethanol; nematode samples stored cold.
  - Nematodes: wet extraction through sieving and gravity-based collection over ~24 h; samples cold-stored for later identification and enumeration.
- Trait values (context for CWM):
  - Longevity (ordinal 1–5), plant height, specific leaf area, root architecture (seven levels), rooting depth (three levels), VAM affinity (three levels); sources include LEDA traitbase and PlantATT.

## Data collection methods and workflows

- Vegetation data collected by standardized quadrat sampling and visual cover estimation; biomass harvested, dried, and weighed; data used to derive richness, cover, biomass, and functional trait summaries.
- GHG flux measurements employed standardized chamber and IRGA protocols with environmental covariates captured alongside fluxes.
- Soil sampling and subsampling approach designed to support multi-omics (PLFA, DNA) plus physical-chemical analyses; samples stored under strict temperature controls (-20°C for DNA/PLFA subsamples; 5°C for remaining soil) to preserve integrity.
- Laboratory workflows documented in detail (lipid extraction, lipid class separation, GC analysis; DNA extraction and sequencing; sequencing data processing; PLFA calculations; nematode extraction).
- Data processing steps include computational calculations for CWM, diversity indices, and gas flux conversions; OTU clustering at 97% similarity; trait integration using external trait databases.

## Metadata, standards, and provenance

- Trait values and species information tied to established databases (LEDA, PlantATT) with explicit trait definitions.
- Instrumentation identified (e.g., EGM-4 IRGA; Agilent 7890B GC; MiSeq with V3 chemistry) to support calibration and reproducibility.
- Data outputs include:
  - Vegetation metrics (cover, richness, biomass, Shannon diversity, CWM).
  - Gas fluxes (CO2, CH4, N2O) with environmental covariates.
  - Soil properties (bulk density, pH, moisture content) and sample metadata (site, plot, quadrat, date).
  - Molecular data (OTU tables, relative abundances) and sequencing reads.
  - PLFA profiles and fatty acid concentrations.
  - Nematode and microfauna counts/identifications.
- Documentation supports traceability from field collection to final data products, with clear sequencing and extraction protocols.

## Data management, sharing, and accessibility

- Datasets are uploaded to relevant portals and catalogued as part of data holdings, with ongoing updates and change tracking.
- Data creators may need coaching or follow-up to obtain timely data; emphasis on QA, cleaning, and transformation prior to sharing.
- Sharing limitations are acknowledged (disclosure risks, proprietary concerns, embargoes); systems are in place to manage these constraints while enabling discoverability.
- Documentation accompanies datasets to support reuse, including method details, unit conventions, and trait synthesis.

## Trait values and references

- Trait values drawn from established trait databases:
  - Longevity, rooting depth, root architecture, VAM affinity, etc. drawn from LEDA and PlantATT sources.
  - Other trait metrics (plant height, specific leaf area) sourced from PlantATT or equivalent trait references.
- Foundational ecological references underpin calculations:
  - Shannon (1963) for diversity calculation.
  - Díaz et al. (2007) and Grime et al. (2007) for trait-based approaches.
  - Kleyer et al. (2008) LEDA Traitbase for life-history attributes.

## Data governance implications and challenges

- Aligning data collection with user needs requires documenting dataset scope, variables, units, and methodological nuances to support reuse.
- Ensuring timely data delivery from multiple contributors and harmonizing data across diverse systems and formats is critical.
- Metadata completeness, standardization of formats, and interoperability across omics, physiological, and ecological data pose ongoing challenges.
- Large multi-omics and high-volume sequencing data demand robust storage, cataloguing, and versioning strategies.
- Versioning and embargo policies should be explicit to balance openness with data-provider considerations.