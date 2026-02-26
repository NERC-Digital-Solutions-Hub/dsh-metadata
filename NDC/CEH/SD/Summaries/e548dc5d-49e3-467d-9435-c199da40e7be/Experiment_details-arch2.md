# pigAMRgenecounts.csv

## Overview
- Data are quantitative PCR (qPCR) readouts of antimicrobial resistance gene (AMRG) assays with associated metadata.
- Reported as mean gene copy numbers per microlitre of DNA extract.
- Samples from a single British commercial pig unit: faecal and environmental (sow housing, growing houses, slurry tanks, and surrounding land).
- Two study arms: "main study" (Oct 19, 2016 – Apr 5, 2017) and "depopulation (depop) study" (Jun 19 – Nov 13, 2017); data generated Aug 1, 2017 – May 1, 2018.
- Purpose: monitor AMR gene dynamics in response to antimicrobial administration and management practices, including partial depopulation.
- Missing values are random and do not bias analysis.

## Experimental design and sampling regime
- Timepoints correspond to a full production cycle on a 600-sow farrow-to-finish unit.
- Treatments in the study period included rapid antimicrobial exposure: acidified water for 2 weeks, in-feed chlortetracycline, followed by tylosin in-feed.
- Sampling framework:
  - Weaner piglets: weekly faecal samples from three pen replicates during weaning, growing, and finishing phases.
  - Sow barn: weekly samples to establish background resistance levels (no routine in-feed antimicrobials).
  - Slurry tanks: pooled representations of on-farm AMR levels.
- Main study: 329 faecal and environmental samples; Depop study: 45 samples.
- Some samples missing due to absence of material or access; treated as random.

## Sample collection, storage and processing
- Sample types and collection protocols:
  - Farrowing crate: faecal and piglet faecal samples; immediate freezing at -20°C.
  - Sow barn: faecal material from unbedded areas; immediate freezing at -20°C.
  - Slurry: collection from slats and slurry lagoons; immediate freezing at -20°C.
  - Weaning/growing/finishing pens: piglet faeces; immediate freezing at -20°C.
- On-farm storage at -20°C; transport on dry ice to laboratory; storage at -80°C prior to processing.
- Detailed, equipment-specific sampling procedures provided for each site (sterile containers, gloves, labeling, and handling steps).

## Quality control and sample handling
- Use only PCR-grade reagents and dedicated clean spaces; avoid cross-contamination with strict handling rules (e.g., separate coats/gloves, no shared consumables with amplified DNA).
- Thaw on wet ice before processing; use fresh tips and filter tips; avoid handling near PCR machines.
- Record sample weights and ensure traceability; acknowledge random missingness where applicable.

## DNA extraction
- Method: PowerSoil DNA Isolation Kit (MoBio) with detailed stepwise protocol.
- Key workflow elements:
  - Mechanical lysis with PowerBead tubes and high-speed vortexing for thorough homogenization and lysis.
  - Inhibitor removal steps (Solution C2 and C3) to remove humic substances and contaminants.
  - Binding of DNA to silica membranes, sequential washing (Solution C5), and final elution with Solution C6.
  - Multiple load steps to maximize DNA recovery; careful handling to avoid pellet carryover.
- Final DNA eluate stored appropriately for downstream quantification.

## DNA quantification and storage
- Eluted DNA divided into five aliquots (20 µL each) for tracking and contamination control.
- Quantified using NanoDrop:
  - Record DNA concentration (ng/µL) and 260/280 and 260/230 purity ratios.
  - Abnormal absorbance shapes documented.
- One aliquot marked to indicate opening outside sterile conditions; all remaining aliquots stored at -80°C.

## qPCR methodology
- Instrument: Agilent Mx3005p; absolute quantification using standard curves.
- Standards: dilution series of cloned target plasmids (10^7 to 10^1 copies/µL); runs include negative controls in triplicate.
- Reagents: Agilent Brilliant III Ultra Fast Mastermix.
- Reaction setup (20 µL total) includes master mix, optimized concentrations of probes and primers, and DNA template.
- Controls: no-template control in triplicate to monitor contamination.
- Cycling program: 95°C denaturation; 40 cycles of 95°C and 60°C annealing/extension.
- Target genes and primers/probes include tetB, ermA, ermB, dfrA1, tetQ, and 16S rRNA, with respective fragment sizes noted.
- Primers/probes tabulated with sequences and product sizes referenced in the study.

## Processing of data generated from qPCR runs
- Data processing tool: MxPro software (associated with the Agilent instrument) to interpolate unknown sample copy numbers from the standard curve.
- Post-run processing: export triplicate data to Microsoft Excel; align with sample metadata.
- Reported data: mean gene copy numbers per microlitre of DNA extract.
- Optional standardization: normalize by sample % dry matter (%DM) or by 16S copy numbers to facilitate cross-sample comparisons.

## Details of data structure
- Dataset: pigAMRgenecounts.csv with 24 columns:
  - Column 1: Shortened sample identifier (S/N)
  - Column 2: Sample description (e.g., faeces, soil)
  - Column 3: Full sample identifier (Sample ID)
  - Column 4: Category of pigs (e.g., sow, piglet)
  - Column 5: Date of sampling
  - Column 6: Sampling site (e.g., sow barn, growing pen)
  - Column 7: DNA box ID
  - Column 8: DNA concentration (ng/µL)
  - Column 9: Sample wet weight (WW, g)
  - Column 10: Sample dry weight (DW, g)
  - Column 11: Percentage dry matter (%DM)
  - Column 12: Distance from sow barn (environmental transects)
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
  - Column 23: Pen ID (sow barn, slurry tank, pen numbers)
  - Column 24: Antibiotic used (none, mixed, acidified water, acid.chlortet, chlortet, tylosin)
- Reference: PowerSoil DNA Isolation Kit protocol and methodology cited for reproducibility.

## Relevance for environmental monitoring and policy evaluation
- Provides standardized, traceable AMR gene abundance data across multiple farm environments and production stages.
- Facilitates longitudinal monitoring of AMRG dynamics in response to antimicrobial administration and management changes, including depopulation events.
- Supports data integration with other environmental datasets by offering standardized metadata (sampling site, pig category, weight metrics, DM, etc.) and normalization options (e.g., %DM, 16S normalization).
- Emphasizes data quality assurance, documentation of protocols, and reproducible data processing pathways aligned with monitoring objectives.