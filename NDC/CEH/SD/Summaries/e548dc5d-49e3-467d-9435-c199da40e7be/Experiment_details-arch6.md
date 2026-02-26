# Overview of data

- What the dataset is
  - pigAMRgenecounts.csv containing quantitative PCR (qPCR) readouts of antimicrobial resistance gene (AMRG) assays plus associated metadata.
  - Values represent mean gene copy numbers per microlitre of DNA extract from samples.

- Source and scope
  - Collected from a single British commercial pig unit.
  - Sample types: faecal (sow housing barn, pig growing houses) and environmental (slurry tanks); slurry samples also collected from surrounding land.
  - Two studies: the main study (Oct 2016–Apr 2017) and a depopulation study (Jun–Nov 2017).
  - Data generated between Aug 2017–May 2018.
  - Aim: monitor AMR gene dynamics in response to antimicrobial administration and farm management practices, including partial depopulation.

- Data completeness
  - Some missing values due to absence of material or access issues.
  - Missing data assumed to be random and not informative for analysis.

- Experimental design highlights
  - Weaner piglets received acidified water for 2 weeks, then chlortetracycline in feed, then tylosin in-feed during growing/finishing.
  - Three pen replicates tracked weekly faecal samples; sow barn samples for background AMR; slurry tank samples for pooled farm representation.
  - Main study: 329 faecal/environmental samples; Depop study: 45 additional samples.
  - Notable gaps: specific dates with no samples due to material absence or access problems; missing data treated as random.

- Sample collection, storage and processing overview
  - Protocols defined for:
    - Farrowing crate
    - Sow barn
    - Slurry
    - Weaning/growing/finishing pens
  - On-site storage at -20°C, transport on dry ice, lab storage at -80°C.

- Quality control and handling
  - Avoid contamination: use PCR-grade reagents, work in a microbiological cabinet, dedicated lab wear, separate PPE for different steps.
  - Thawing and handling guidelines to minimize contamination and degrade risk.
  - Specific faecal handling steps include homogenization, drying to determine % dry matter, and sample storage.

- DNA extraction
  - Performed with PowerSoil DNA Isolation Kit (MoBio), including:
    - Detailed lysis/mixing steps with PowerBead tubes and Solution C1–C6 reagents.
    - Inhibitor removal steps (C2 and C3) to improve DNA purity.
    - Silica spin filter binding, washes (C5), and final elution (C6).
  - Final DNA stored at -80°C.

- DNA quantification and storage
  - DNA eluted into five 20 µL aliquots; concentration and purity assessed with NanoDrop (A260/280 and A260/230 recorded).
  - One aliquot designated for analysis; remaining aliquots stored at -80°C.

- qPCR methodology
  - Absolute quantification using standard curves (cloned plasmids; 10^7 to 10^1 copies/µL); triplicates for all samples and controls.
  - Reaction setup includes master mix, primers, probes, and reference dye; no-template controls in triplicate.
  - Cycling program and fluorescent detection configured for absolute quantification.
  - Target AMRGs and 16S rRNA gene included:
    - tetB, ermA, ermB, dfrA1, tetQ, 16S.
  - Primer/probe sequences and amplicon sizes provided for each target.

- Data processing and normalization
  - qPCR data processed with MxPro software to extrapolate copy numbers from standard curves.
  - Data imported into Excel; triplicate results combined into mean copy numbers per µL DNA extract.
  - Standardization options noted: normalize by sample % dry matter (%DM) or by 16S copy number for cross-sample comparability.

- Dataset structure and variables
  - One CSV file: pigAMRgenecounts.csv with 24 columns:
    1) Short sample identifier (S/N)
    2) Sample description (faeces, soil)
    3) Full sample identifier (Sample ID)
    4) Category of pigs (sow, piglet)
    5) Date of sampling
    6) Sampling site (sow barn, growing pen)
    7) DNA box ID
    8) DNA concentration (ng/µL)
    9) Sample wet weight (WW, g)
    10) Sample dry weight (DW, g)
    11) Percentage dry matter (%DM)
    12) Distance from sow barn (environmental transect)
    13) tetB copies/µL
    14) ermA copies/µL
    15) ermB copies/µL
    16) dfrA1 copies/µL
    17) tetQ copies/µL
    18) 16S copies/µL
    19) Experiment type (main or depopulation)
    20) Sample type (faeces, soil or slurry)
    21) Pig type (sows, mixed, piglets or enviro)
    22) Pig age (sows, mixed, farrowing, weaning, growing, finishing or enviro)
    23) Pen ID (sow barn, slurry tank, farrowing pen IDs, pen 1–3 or enviro)
    24) Antibiotic used (none, mixed, acidified water, acid.chlortet, chlortet, tylosin)

- Reference framework
  - Methodology aligns with PowerSoil DNA Isolation Kit protocol; data suitable for integration with antibiotic usage records and environmental metadata for downstream analyses.