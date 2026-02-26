# Supporting documentation for 'Alpine grassland soil microbial and biogeochemical data from a snow manipulation experiment in Hohe Mut, Austria, 2017' deposited in the Environmental Information Data Centre repository

## Purpose and scope
- Documents field experiment design, data collection, analyses, and data structure for alpine grassland soil microbial and biogeochemical data.
- Facilitates data discovery, reuse, and integration across abiotic, microbial biomass, enzyme activity, and sequencing datasets.

## Field experiment design
- Location: Hohe Mut summit, 2650 m, near Obergurgl, Austria (coordinates provided).
- Plots: 15 plots (~6 m² each) randomly assigned to three snow manipulation treatments: snow removal, snow addition, and untreated control (n = 5 replicates per treatment).
- Setup: Plots fenced to prevent trampling; HOBO sensors to monitor soil moisture and temperature.
- Snow manipulation: Three interventions between late March and late May 2017; removal via snow blower or shovels, addition by even distribution; ground/vegetation protection ensured during manipulation.

## Sampling and data collection
- Soil sampling timeline: six time points spanning late winter to early summer 2017 (late winter 28/03; snowmelt 01/06 and 08/06; spring 12/06 and 18/06; summer 08/07).
- Sampling protocol: five soil cores per plot (diameter 2 cm, depth ~7 cm; shallower where soil was frozen), pooled per plot, vegetation removed; five subsamples (~200 mg) for molecular analyses.
- Preservation: DNA preserved in DNA/RNA Shield and field-lysed; samples stored at -80°C. Soil for enzyme and biogeochemical analyses sieved (4 mm) and stored at 4°C for up to two weeks before laboratory analyses.

## Biogeochemical and soil properties measured
- Plant-available inorganic N and DON: NH4+-N and NO3--N extracted with 1 M KCl; DON extracted with ultrapure water.
- Mineralisation potential: 14-day incubation at 25°C to measure NH4+-N and NO3--N release.
- Dissolved organic carbon (DOC): water extraction and TOC measurement.
- Physicochemical properties: soil pH (1:2.5 soil:water), soil water content (gravimetric), total C and N (105°C dried soil; elemental analysis).

## Microbial functional assays (extracellular enzyme activities)
- Enzymes measured (eight total): GLC (β-glucosidase), CBH (cellobiohydrolase), XYL (β-xylosidase), NAG (N-acetylglucosaminidase), PHO (phosphatase), URE (urease), POX (phenol oxidase), PER (peroxidase).
- Relevance: indicators of lignocellulose degradation, nitrogen cycling, phosphorus cycling, and polyphenol degradation.
- Methods: high-throughput photometric assays with substrate-specific colorimetric readouts; corrections for soil/substrate color; units in nmol product g⁻¹ soil h⁻¹ or similar; PER and POX measured with L-DOPA substrate with time-point corrections; URE via ammonium production.
- Normalisation: enzyme activities expressed relative to microbial biomass using phospholipid fatty acid (PLFA) data.

## Microbial biomass and community composition (PLFA)
- PLFA analyses used to quantify total microbial biomass and to differentiate fungal vs bacterial and Gram-positive vs Gram-negative bacteria.
- Biomarkers: defined FA markers (e.g., 18:2w6,9 for fungi; 16:1w9 and others for Gram-negative; a-15:0, i-15:0, etc., for Gram-positive; additional non-specific markers).
- Outcome: total PLFA abundance and ratio metrics (fungal:bacterial, Gram-positive:Gram-negative).

## DNA extraction and sequencing (microbial community profiling)
- DNA extraction: Zymo Research kit with enhanced lysis step and additional purification steps; samples thawed and processed to maximize DNA recovery.
- Targeted communities: bacteria (16S rRNA gene) and fungi (ITS2 region).
- Two-step Illumina PCR protocol:
  - Step 1: gene-specific primers with Illumina adapters.
  - Step 2: Illumina tag primers with unique sample barcodes for multiplexing.
- Library preparation: standard normalisation, pooling, concentration, and sequencing on an Illumina MiSeq (V3 chemistry).
- Bioinformatics:
  - Quality control and ASV calling with DADA2 in R.
  - 16S: trimmed to 250 bp (forward) and 220 bp (reverse); ITS2: trimmed to 270 bp (forward) and 220 bp (reverse).
  - Filtering: maxN = 0; maxEE = 1,1; primer removal; chimera removal.
  - Taxonomy: 16S with Greengenes v13.8; ITS with UNITE v7.2.
  - Output: ASV tables (bacterial 16S, fungal ITS) and corresponding taxonomic assignments.
- Sequencing depth: after filtering, 5,726,754 bacterial and 3,077,751 fungal sequences used; rarefied to depths of 10,083 (16S) and 5,349 (ITS) to account for uneven sampling.

## Data structure and files
- Env data file: Snow_cover_HM_soil_env_data.csv
  - Contains: date, timepoint, season, plot, treatment, snow status, sample identifiers, environmental measurements (swc, pH, TOC in water, NH4, NO3, TIN, TN, ON, NH4inc, NO3inc, ure, nagr, phor, cbhr, xylr, glcr, perr, poxr), and C/N metrics.
  - Columns are aligned to support cross-linking with molecular and enzyme data via sample16S and ITS sample identifiers.
- Sequencing data files:
  - Snow_cover_HM_seq_tab_16S.csv (bacterial OTU/ASV abundances)
  - Snow_cover_HM_seq_tab_ITS.csv (fungal OTU/ASV abundances)
  - Snow_cover_HM_16S_taxa.csv (16S taxa information)
  - Snow_cover_HM_ITS_taxa.csv (ITS taxa information)
- Raw data deposition: raw sequences are deposited at the European Bioinformatics Institute (EBI).
- Cross-linking keys: sample16S and ITSsample identifiers in the env file match corresponding columns in the sequence tables to enable integrated analyses.

## Data quality, access, and provenance
- Explicit documentation of sampling design, processing steps, and analytical methods supports reproducibility and auditability.
- Data processing pipelines and software references (e.g., DADA2 in R, Greengenes, UNITE) are provided to enable re-analysis.
- Open data approach: raw sequences deposited in EBI; metadata and processed tables organized to enable reuse and cross-study comparisons.
- Metadata richness includes sampling dates, treatments, snow cover status, and a comprehensive suite of biogeochemical and microbial measurements, facilitating multi-omic and time-series analyses.

## Potential use and considerations for data leaders
- Holistic view of data systems: integrates abiotic soil properties, microbial biomass, enzyme activities, and community composition across a temporal snow manipulation experiment.
- Enables cross-disciplinary analyses (ecology, biogeochemistry, microbiology) and supports development of data-driven policies or climate-related soil studies.
- Highlights data governance needs: consistent sample naming, clear cross-file links, explicit metadata schemas, and accessible deposition for long-term stewardship.
- Addresses common data challenges such as data fragmentation, need for standardization of metadata, and ensuring discoverability across platforms and partner networks.