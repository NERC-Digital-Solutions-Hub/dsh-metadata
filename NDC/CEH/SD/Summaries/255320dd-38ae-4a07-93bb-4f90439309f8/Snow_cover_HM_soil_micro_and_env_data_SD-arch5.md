# Supporting documentation for 'Alpine grassland soil microbial and biogeochemical data from a snow manipulation experiment in Hohe Mut, Austria, 2017' deposited in the Environmental Information Data Centre repository

## Overview
- Document describes field experiment at Hohe Mut, Austria (2650 m) with 15 plots (6 m2 each) randomly assigned to snow removal, snow addition, or untreated control (n=5 per treatment).
- Snow manipulation occurred three times (late March–May 2017) and affected soil temperature and moisture.
- Comprehensive biogeochemical, enzymatic, microbial biomass, and molecular data were collected across six sampling points spanning late winter to early summer 2017.
- Data are organized into multiple data files, with raw sequence data deposited at the European Bioinformatics Institute (EBI) and taxonomic tables provided.

## Experimental design and treatments
- Location and plot setup:
  - Summit of Hohe Mut, coordinates provided; plots fenced to prevent disturbance.
- Treatments:
  - Snow removal, snow addition, and untreated control; five replicates per treatment.
- Snow manipulation:
  - Occurred three times between end March and end May 2017.
  - Removal using petrol snow blower or hand; depth reduced to <10 cm on removal plots.
  - Addition plots received evenly added snow; control left undisturbed.

## Sampling strategy and sample handling
- Sampling timeline:
  - Six time points: late winter (28/03/2017), snowmelt (01/06 and 08/06), spring post-snowmelt (12/06 and 18/06), and early summer (08/07).
- Soil sampling:
  - Cores: diameter 2 cm, depth ~7 cm (shallower if soil frozen); five locations per plot, edge avoided.
  - Processing: samples from the same plot pooled and homogenised; vegetation/litter removed.
  - Molecular analyses: five subsamples (~200 mg) taken per plot, preserved in DNA/RNA shield, lysed in the field, stored at -80°C.
  - Biogeochemical/enzyme samples: sieved to <4 mm, stored at 4°C for up to 2 weeks, shipped to Manchester for analysis.

## Biogeochemical and soil properties measurements
- Nutrients and organic matter:
  - NH4+-N and NO3--N via 1 M KCl extraction; DON via water extraction.
  - DON protocol with different extraction volumes; mineralisation potential via 14-day incubation at 25°C.
  - DOC determined from water extracts; TOC measured on dried soil.
  - pH (1:2.5 soil:water); soil water content by gravimetry.
  - Total C and N content by elemental analysis on dried soil.
- General soil parameters:
  - Soil moisture, pH, and total carbon/nitrogen contents documented for each sample.

## Extracellular enzyme assays
- Enzymes measured (potential absolute activities):
  - GLC (β-glucosidase), CBH (cellobiohydrolase), XYL (β-xylosidase), NAG (N-acetylglucosaminidase), PHO (phosphatase), URE (urease), POX (phenol oxidase), PER (peroxidase).
- Method highlights:
  - Colorimetric substrate assays in microplates; absorbance measured and converted to activity using standards.
  - POX and PER measured with L-DOPA; PER subtracted from POX to avoid cross-reactivity.
  - Enzyme activities normalised relative to microbial biomass via division by total PLFA.

## Phospholipid fatty acid (PLFA) analyses
- Purpose: assess microbial biomass and community structure (fungal vs bacterial, Gram+ vs Gram− markers).
- Procedure:
  - PLFAs extracted from freeze-dried soil; analysed by GC.
  - Marker lipids used to indicate fungal (e.g., 18:2w6,9) and bacterial groups (Gram+/- markers).
  - Outputs include total PLFA abundance and community composition ratios.

## DNA extraction and microbial community profiling
- DNA extraction:
  - Performed with ZR soil microbe DNA kit with additional lysis step and filtration enhancements.
- Sequencing targets:
  - 16S rRNA (bacteria) and ITS2 (fungi) amplicons.
- Library preparation:
  - 2-step Illumina PCR with gene-specific primers and Illumina adapters; unique barcodes per sample.
  - Libraries normalised and sequenced on Illumina MiSeq (V3 chemistry).
- Data processing:
  - Quality filtering, dereplication, and ASV generation with DADA2 in R.
  - Taxonomic assignment using Greengenes (16S) and UNITE (ITS).
  - Rarefaction to even depths (16S: 10,083 reads; ITS: 5,349 reads) in phyloseq.
- Data outputs:
  - Snow_cover_HM_seq_tab_16S.csv and Snow_cover_HM_seq_tab_ITS.csv (OTU/ASV tables).
  - Taxonomic assignments in Snow_cover_HM_16S_taxa.csv and Snow_cover_HM_ITS_taxa.csv.
  - Raw sequence data deposited at EBI.

## Data structure and files
- Snow_cover_HM_soil_env_data.csv:
  - Abiotic, PLFA, and soil extracellular enzyme data.
  - Columns include: date, timepoint, season, plot, treatment, snow state, sample identifiers, on/off snow cover, days since melt, soil moisture (swc), pH, TOC in water extracts (TOCwat), NH4, NO3, TIN, TN, ON, NH4inc, NO3inc, urease (urer), NAG (nagr), phosphatase (phor), CBH (cbhr), XYL (xylr), GLC (glcr), PER (perr), POX (poxr), C and N percentages, CN ratio, specific PLFA markers, and others.
- Snow_cover_HM_seq_tab_16S.csv and Snow_cover_HM_seq_tab_ITS.csv:
  - OTU/ASV abundance tables by sample; sample names linked to Snow_cover_HM_soil_env_data.csv.
- Snow_cover_HM_16S_taxa.csv and Snow_cover_HM_ITS_taxa.csv:
  - Taxonomic information for the 16S and ITS sequences.
- Metadata and workflow notes:
  - Raw data deposition details and sequencing methodology references included.

## Data processing pipelines and tools
- R and associated packages:
  - DADA2 for amplicon sequence variant inference; phyloseq for analysis and visualization.
- Reference databases:
  - Greengenes for 16S; UNITE for ITS.
- Normalisation:
  - Rarefaction to fixed depths to account for sequencing depth bias.
- Documentation of methods and references provided to support reproducibility.

## Access, provenance, and references
- Data availability:
  - Soil environment, enzyme, PLFA, and sequencing data organized for deposition in Environmental Information Data Centre; raw sequence data deposited at EBI.
- Provenance:
  - Detailed methodological descriptions enable reproducibility and re-use, including sampling design, laboratory procedures, and data processing steps.
- Key references:
  - Methods and foundational literature for enzyme assays, PLFA analysis, DNA extraction, and Illumina amplicon sequencing pipelines (e.g., DADA2, Phyloseq, Greengenes, UNITE).

## Considerations for data governance and stewardship
- Metadata completeness and consistency:
  - Rich, explicit metadata across sampling times, treatments, and assays to support discovery and reuse.
- Interoperability:
  - Use of standard gene markers and recognized databases for taxonomic assignment; clear linking between environmental data and sequencing data via sample identifiers.
- Data quality and traceability:
  - Clear documentation of sample handling, preservation, and storage conditions; details of extraction, incubation, and assay conditions; QC steps in sequencing and data processing.
- Licensing and access:
  - Repository deposition with accessible data structures; sequence data pending deposition at EBI ensures traceability and reuse while enabling broader dissemination.