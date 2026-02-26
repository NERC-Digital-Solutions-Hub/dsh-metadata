# Overview

- A dataset compiling in-stream nitrogen (N) cycling measurements from the PRINCe project, funded by NERC and led by Prof. Mark Trimmer (Queen Mary University of London).
- Data collected in 2018 across two field campaigns (winter February 2018 and summer July 2018) in 12 permeable-bed rivers in the Hampshire Avon catchment, Kent, and Essex.
- Aimed to quantify in situ rates of nitrogen transformations, porewater chemistry, and microbial gene/transcript abundances.

## Scope and aims

- Measure in situ rates of nitrogen transformations and associated porewater chemistry.
- Assess microbial community activity via transcripts and gene abundances related to nitrogen cycling.
- Perform standardized measurements to support environmental health monitoring and policy evaluation over time.

## Study design and sampling

- Rivers with permeable beds (sand or chalk geology) sampled at multiple patches.
- Field methods used push-pull technique with 15 stainless steel probes installed at two depths (7 at 5 cm, 8 at 10 cm) across three unvegetated sediment patches per site.
- For each probe: porewater O2 and pH measured in situ; porewater preserved for Fe(II) or gas analysis; an additional porewater sample filtered for later nutrient and chloride analysis.
- For nitrogen transformation rates, 15N-labeled ammonium or nitrate injected into riverbed/porewater with tracer concentration ~300 µM (98 atom % 15N); 25 mL tracer per experiment; four time points including immediately after injection; total duration ≤ 60 minutes.
- At each patch: a 2 cm sediment core collected pre-push-pull and subsampled at 5 and 10 cm depths for molecular analyses; cores positioned ≥20 cm from probes to minimize surface water intrusion; subsamples cryopreserved in liquid N2.

## Measurements and data types

- Nitrogen transformation rates:
  - R_NO3: mean rate of 15N-NO3 production (µmol N L^-1 h^-1)
  - R_N2: mean rate of 15N-N2 gas production (µmol N L^-1 h^-1)
  - nitrification_efficiency: percentage calculated from R_NO3 and R_N2
- Physicochemical porewater parameters:
  - temp: river water temperature (°C)
  - pH: porewater pH
  - O2: dissolved oxygen in porewater (µM)
  - NO2, NO3: concentrations (µM); NO3.NO2 (NOx), NOx calculated from NO3 and NO2
  - NH3: ammonium concentration (µM)
  - PO4: soluble reactive phosphorus (µM)
- Molecular biology data (gene and transcript abundances):
  - RNA targets: Comammox amoA, Anammox hzo, nirS (clade I), nosZ (clade I)
  - DNA targets: AOA amoA, AOB amoA, Bac 16S, Anammox hzo, Anammox hzsA, nirK (clades I-III), nirS (clades I-II), nosZ (clades I-II), Nitrospira nxrB, Thaumarchaeota ureC
  - Units: transcripts or gene copies per g dry weight sediment
  - Methodologies include RNA/DNA extraction, qPCR or RT-qPCR, and absolute quantification against internal standards or reference materials
- Sequence data:
  - NCBI BioProject accession for raw amplicon data (archaeal/bacterial 16S, hzo, nirK_C3, nirS_C1, nosZ_C1, AOA_amoA, AOB_amoA, comammox_amoA, Nitrospira_nxrB)
  - Data embargoed and released upon manuscript publication; sequencing performed on Illumina MiSeq after standard extraction and amplification procedures

## Metadata, identifiers, and data structure

- Identifying information collected for each sample:
  - Sample_ID, SiteCode, SiteName, Lat, Long
  - Geology (Chalk or Sand), Season (Summer or Winter), Depth (cm), Core identifier
- Measurements have defined units and documented methodologies, including references to established literature for rate calculations and instrument calibrations.

## Analytical methods and data processing

- Rates derived from linear regression of accumulated 15N-labeled species over time.
- Nitrification efficiency calculated as (R_NO3 / (R_NO3 + R_N2)) × 100.
- Porewater chemistry measured using calibrated meters and auto-analyzers with standard calibration and detection limits documented (e.g., O2, NO2, NOx, NO3, NH3, PO4).
- Molecular data generated via standardized extraction and amplification protocols; quantification performed with qPCR/RT-qPCR against calibration curves.
- DNA/RNA sequence data prepared using established kits and sequencing workflows with embargo status until publication.

## Data access, sharing, and embargo

- Raw sequence data deposited under a NCBI BioProject accession.
- Data are currently embargoed and will be released upon publication of manuscripts using these data.
- Prepared outputs (datasets, reports, maps) are intended to be stored and uploaded to appropriate data portals to enable broader access and reuse.

## Quality assurance and standardization

- Adheres to established methodologies for push-pull measurements and 15N tracers (as described in Lansdown et al., 2014).
- In-field measurements include calibration and control steps for O2, pH, and temperature sensors; detection limits and precision are documented for all chemical analyses.
- Core sampling distance and handling procedures designed to minimize cross-contamination and porewater intrusion.

## Geographical and site context

- Study conducted across 12 rivers with permeable beds in the Hampshire Avon catchment, Kent, and Essex.
- Geological substrate categories include Chalk and Sand, enabling assessment of geology-influenced N cycling.

## Relevance for environmental monitoring

- Provides standardized, multi-dimensional data (chemical fluxes, porewater chemistry, microbial functional genes and transcripts) suitable for longitudinal environmental health assessments and policy performance evaluations.
- Data integration potential with other datasets to enhance the value and enable broader, cross-site analyses.
- Emphasis on data accessibility and transparency, with a pathway to share underlying datasets and metadata through appropriate portals.