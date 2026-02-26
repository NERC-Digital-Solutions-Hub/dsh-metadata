# Telomere heritability and parental age at conception effects in a wild avian population

## Overview
- Describes how relative telomere length (RTL) data for the Seychelles warbler are collected, quality-checked, transformed, and structured for long-term ecological analysis.
- Aims to enable standardized RTL-based assessments of environmental and heritable effects across individuals and generations, suitable for monitoring environmental health indicators over time.

## Data collection and generation
- Population and monitoring: Seychelles warbler on Cousin Island (~320 adults in 115 territories) monitored intensively since 1985.
- Sampling window: major breeding season (June–September); some birds also bred in the minor season (Jan–Mar).
- Blood collection: since 1990, ~25 μl blood stored in absolute ethanol for RTL assays.
- RTL data source: RTL dataset derived from Spurgin et al. (2018), with birds caught and blood-sampled between 1995–2014 when data were most complete.
- RTL measurement method: quantitative PCR (qPCR) used to estimate RTL; DNA integrity and 260/280 ratios checked prior to qPCR; degraded samples re-extracted or excluded.

## Measurements and units
- Primary variable: relative telomere length (RTL).

## Quality control and data cleaning
- Reproducibility: within-plate repeatability ~0.74 for GAPDH and ~0.73 for telomere cq values; between-plate repeatability for RTL ~0.68.
- Sample filtering: initial cleaned dataset included 2,664 samples from 1,318 individuals after applying criteria.
  - Exclusion criteria: telomere cq ≥ 25; GAPDH cq ≤ 21 or ≥ 26 or cq replicate difference ≥ 0.5; RTL values < 3.
- DNA quality criteria (prior to inclusion): DNA concentration ≥ 15 ng/μl (mean of three measurements); 260/280 between 1.8–2.0; 260/230 > 1.8; visual confirmation of DNA integrity via agarose gel.
- DNA preparation: samples diluted to 3.3 ng/μl before RTL measurement.
- Controlling for bias: random assignment of samples to qPCR plates to avoid systematic bias by age, sex, cohort, or environment; outliers (extremely large cq values) excluded.
- Statistical treatment: plate identity included as a random effect to account for plate variance.

## Data structure and metadata
- Key columns include:
  - BirdID (individual identifier)
  - Sex (0=female, 1=male)
  - AgeY (age in years at capture)
  - AgeClass (e.g., A=adult, CH=chick, FL=fledgling, J=juvenile, OFL=old fledgling, SA=subadult)
  - BirthFPID (birth fieldwork period ID)
  - U_PlateID (qPCR plate ID)
  - RTL (relative telomere length)
  - Technician (person performing qPCR)
  - Terr (territory)
  - FPID (fieldwork period ID when captured)
  - mum/dad (parental IDs from pedigree)
  - MAC/PAC (maternal/paternal age at conception)
  - BrF/BrM (dominant female/male in natal territory)

## Experimental design and fieldwork
- Field protocol: major breeding season dominates trapping; many birds captured using mist nets.
- Longitudinal scope: data span multiple years with repeated measures possible across samples and plates.

## Fieldwork and laboratory instrumentation
- DNA extraction: DNeasy Blood & Tissue Kit with overnight lysis at 37°C; final eluate 80 μl.
- DNA QC: integrity checked by 1.2% agarose gel; concentration quantified with NanoDrop 8000.
- Telomere measurement prep: samples randomly allocated to qPCR plates to mitigate systematic bias.

## Data handling, integration, and availability
- Data derive from established long-term studies and prior publications (e.g., Sparks et al. 2021; Spurgin et al. 2018; Bebbington et al. 2016), with explicit QC and data-cleaning steps to ensure comparability across years and individuals.
- The standardised data structure and QC framework facilitate integration with other environmental, demographic, or genetic datasets for monitoring environmental health and policy-relevant outcomes.

## Notes on relevance for environmental monitoring
- Provides a robust RTL dataset with transparent QC, enabling analyses of environmental influences, parental age effects, and heritability in wild populations.
- The standardized, well-documented data pipeline supports reproducibility and reuse in environmental health assessments and multisource data integration.