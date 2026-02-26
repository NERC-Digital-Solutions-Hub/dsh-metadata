# Overview

- A dataset compiling results from the in-stream N-cycling component of the PRINCe project, led by Queen Mary University of London.
- Field campaigns conducted in winter (Feb 2018) and summer (Jul 2018) to measure in situ nitrogen transformations, porewater chemistry, and microbial gene abundance/transcripts.
- Study sites: 12 rivers with permeable beds in the Hampshire Avon catchment, Kent, and Essex; geologies include Chalk and Sand.
- Methods combined chemical measurements, isotope tracing (15N), porewater sampling via a push-pull technique, sediment cores, and molecular analyses (RNA and DNA) to assess nitrogen cycling processes and microbial communities.
- Data are organized with identifying information, measured variables (chemical, physical, and molecular), and metadata; raw amplicon sequencing data are available under an embargo until publication.

## Field sampling design and procedures

- Permeable-bed river sites; two depths (5 cm and 10 cm) across three unvegetated sediment patches per patch, using 15 probes per sediment patch.
- Porewater sampling sequence per probe:
  - Measure O2 and pH in porewater.
  - Preserve porewater for Iron(II) and gas analyses.
  - Filter and freeze for nutrient and chloride analyses.
- Nitrogen transformation rates measured with 15N-labeled ammonium or nitrate injections (25 mL tracer, ~300 µM, 98% 15N; ~150 mg/L KCl).
- Each push-pull experiment includes 4 time points (immediate and three subsequent) over up to 60 minutes.
- For each sediment patch, a single 2 cm core collected and subsampled at 5 and 10 cm depths for molecular analyses; core positioned at least 20 cm from a probe and cryopreserved in liquid N2.

## Data structure and identifying information

- Sample tracking fields:
  - Sample_ID (unique sample identifier)
  - SiteCode (river site identifier)
  - SiteName (river name)
  - Lat/Long (sampling coordinates, decimal degrees)
  - Geology (sub-catchment geology: Chalk or Sand)
  - Season (Winter or Summer)
  - Treatment_15A_15N (substrate injected during push-pull; 15A-labelled ammonium or 15N-labelled nitrite)
  - Depth (sampling depth in cm)
  - Core (unique core identifier per site/season)
- Data organization supports linking chemical measurements, porewater chemistry, and molecular data to specific site-seasons-depths-patches.

## Measurements, units, and methodologies (highlights)

- Nitrogen transformation rates:
  - R_NO3: mean rate of 15N-NO3 production (µmol N L-1 h-1), determined by linear regression of 15NO3- over time.
  - R_N2: mean rate of 15N-N2 gas production (µmol N L-1 h-1), from 15N-nitrite injections.
  - nitrification_efficiency: percentage based on R_NO3 and R_N2.
- Porewater chemistry and physico-chemical parameters:
  - temp: river water temperature (°C, measured with Hach meter)
  - pH: porewater pH
  - O2: dissolved oxygen in porewater (µM; with calibration and contamination correction)
  - NO2, NO3: nitrite, nitrate concentrations in porewater (µM)
  - NO3.NO2: NOx (nitrate + nitrite) concentrations (µM)
  - NH3: ammonium (µM)
  - PO4: soluble reactive phosphorus (µM)
- Molecular biology datasets (gene/transcript abundances per sediment mass):
  - RNA_Comammox_amoA, RNA_Anammox_hzo, RNA_nirS_C1, RNA_nosZ_C1 (transcripts per g dry weight)
  - DNA_AOA_amoA, DNA_AOB_amoA, DNA_Bac_16S, DNA_Anammox_hzo, DNA_Anammox_hzsA, DNA_nirK_C1/C2/C3, DNA_nirS_C1/C2, DNA_nosZ_C1/C2, DNA_Nitrospira_nxrB, DNA_Thaum_ureC (gene copies per g dry weight)
  - Primers and methodologies cited for each target; details provided for qPCR and RT-qPCR workflows.
- Sequencing data:
  - NCBI_BioProject_accession (embargoed: raw amplicon sequence data for archaeal/bacterial 16S, hzo, nirK_C3, nirS_C1, nosZ_C1, AOA_amoA, AOB_amoA, comammox_amoA, Nitrospira_nxrB)
  - DNA extracted with PowerSoil kit; libraries prepared with NexteraXT and sequenced on Illumina MiSeq (4 runs)
- Quality and calibration notes:
  - O2 contamination estimate in measurements (~10 µM) subtracted from data
  - Detection limits and precision stated for each chemical measurement (e.g., NO2, NO3, NH3, PO4)
  - Calibration against standards and reference materials described for each assay

## Data access and embargo

- Raw amplicon sequence data are deposited under a NCBI BioProject accession.
- Data are embargoed and will be released upon publication of manuscripts using these data.

## Use cases and considerations for data support

- Enables end users to self-serve: combine chemical, porewater, and molecular data to explore nitrogen cycling processes across sites, seasons, and depths.
- Supports dashboard/report development to visualize rates, nitrification efficiency, and microbial functional gene/transcript abundances.
- Requires careful data cleaning and merging due to multi-modal data (chemical measurements, porewater probes, isotope-tracer results, and molecular datasets) and embargoed sequencing data.
- Quality assurance considerations available in methodology notes (calibrations, LODs, precision, and contamination corrections) to inform data curation and downstream analyses.