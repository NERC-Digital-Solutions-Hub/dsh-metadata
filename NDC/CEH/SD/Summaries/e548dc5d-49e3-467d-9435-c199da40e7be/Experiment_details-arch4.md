# pigAMRgenecounts.csv

## Purpose and scope
- Provides quantitative PCR (qPCR) readouts of antimicrobial resistance gene (AMRG) assays with metadata.
- Reports mean gene copy numbers per microlitre of DNA extract for each sample.
- Aims to monitor AMR gene dynamics on a single British commercial pig unit in response to antimicrobial use and management practices, including a partial depopulation event.
- Data generated between 2017 and 2018, corresponding to two study phases: the main study ( Oct 2016–Apr 2017 ) and the depopulation study (Jun–Nov 2017).

## Data sources and study design
- Sample types: faecal (sow housing, growing houses) and environmental (slurry tanks, broader farm environment).
- Studies:
  - Main study: 329 samples across a full production cycle from a 600-sow farrow-to-finish unit.
  - Depopulation (depop) study: 45 additional samples to track AMR dynamics after partial depopulation.
- Sampling design includes weekly faecal samples from three piglet pens, sow barn background samples, and pooled slurry samples.
- Missing values exist due to absence of material or access issues; treated as random and not informative for analysis.

## Data collection, handling, and storage
- Collection protocols detailed for:
  - Farrowing crate, sow barn, slurry, and weaning/growing/finishing pens.
- On-farm storage at -20°C; transport on dry ice; storage at -80°C in the lab.
- Quality control and contamination prevention procedures, including dedicated PPE, controlled lab environment, and avoidance of PCR contamination.

## Laboratory methods
- DNA extraction: PowerSoil DNA Isolation Kit (MoBio).
  - Describes sample homogenization, lysis, inhibitor removal, and DNA elution steps.
  - Emphasizes handling to maximize DNA yield and purity; includes multiple loading steps and ethanol washes.
- DNA quantification: NanoDrop measurements (concentration, 260/280, 260/230) and storage recommendations.
- qPCR: Absolute quantification using standard curves with cloned plasmids (10^7 to 10^1 copies/µL); reactions run in triplicate with appropriate negative controls.
  - Primer/probe sets for target genes (tetB, ermA, ermB, dfrA1, tetQ) and 16S as a reference.
  - Cycle program: standardizing 95°C denaturation and 60°C annealing/extension parameters; data collection during amplification.
- Standards and controls: triplicate reactions for each sample; no-template controls in triplicate.

## Data processing and normalization
- qPCR results processed using MxPro software to interpolate gene copy numbers from standard curves.
- Data imported into Excel; metadata aligned with sample records.
- Reported metric: mean copies per microliter of DNA extract; potential standardization options include normalization to percent dry matter (%DM) or 16S copy number.

## Dataset structure and contents
- File: pigAMRgenecounts.csv
- 24 columns with the following schema:
  - Column 1: Shortened sample identifier (S/N)
  - Column 2: Sample description (e.g., faeces, soil)
  - Column 3: Full sample identifier (Sample ID)
  - Column 4: Category of pigs (e.g., sow, piglet)
  - Column 5: Date of sampling
  - Column 6: Sampling site (e.g., sow barn, growing pen)
  - Column 7: DNA box ID
  - Column 8: DNA concentration
  - Column 9: Sample wet weight (WW)
  - Column 10: Sample dry weight (DW)
  - Column 11: Percentage dry matter (%DM)
  - Column 12: Distance from sow barn (environmental samples)
  - Column 13: tetB copies/µL
  - Column 14: ermA copies/µL
  - Column 15: ermB copies/µL
  - Column 16: dfrA1 copies/µL
  - Column 17: tetQ copies/µL
  - Column 18: 16S copies/µL
  - Column 19: Experiment type (main or depopulation)
  - Column 20: Sample type (faeces, soil, slurry)
  - Column 21: Pig type (sows, mixed, piglets, enviro)
  - Column 22: Pig age (sows, mixed, farrowing, weaning, growing, finishing, enviro)
  - Column 23: Pen ID (sow barn, slurry tank, pen IDs, or enviro)
  - Column 24: Antibiotic used (none, acidified water, chlortet, tylosin, etc.)
- Foundation: data linked to PowerSoil DNA extraction protocol and qPCR assays; standard references cited for methodological context.

## Data provenance, access, and references
- Data generated under a defined experimental framework with explicit authorship and roles.
- Protocols based on published references and the PowerSoil DNA Isolation Kit (2014) guidelines.
- Dataset shared with EIDC; methodological details and references included for reproducibility.

## Limitations and considerations for use
- Missing data present but assumed random; may require imputation or sensitivity analyses.
- Normalization options (e.g., %DM or 16S) available to account for sample variability.
- Study context is a single farm unit; cross-site generalizability should be assessed when integrating with other datasets.