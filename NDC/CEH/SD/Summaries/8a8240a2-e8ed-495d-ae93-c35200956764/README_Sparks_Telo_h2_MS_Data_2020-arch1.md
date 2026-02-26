Telomere heritability and parental age at conception effects in a wild avian population

- Overview
  - Long-term study of Seychelles warbler on Cousin Island, monitoring the entire population (~320 adults in 115 territories) since 1985.
  - Telomere data set used was generated from Spurgin et al. (2018) and includes birds captured and blood-sampled between 1995 and 2014.
  - Relative telomere length (RTL) measured by qPCR; DNA integrity and purity checked prior to analysis; samples degraded or failed re-extracted and rechecked.
  - Final cleaned data set comprises 2,664 RTL measurements from 1,318 individuals; data used to assess telomere dynamics, heritability, and parental age effects.

- Nature and units of recorded values
  - RTL: Relative telomere length (unitless metric from qPCR).

- Quality control (QC) and data filtering
  - Within-plate repeatability: ~0.74 for GAPDH and ~0.73 for telomere cq values.
  - Between-plate repeatability (RTL): ~0.68 when samples measured across plates.
  - Storage time: no detectable effect on RTL.
  - Sample inclusion criteria (per Spurgin et al. 2018): DNA concentration ≥ 15 ng/μl; 260/280 ratio 1.8–2.0; 260/230 ratio > 1.8; DNA integrity verified by 1.2% agarose gel; degraded samples re-extracted or excluded.
  - Pre-measurement preparation: samples diluted to 3.3 ng/μl; random assignment to qPCR plates to avoid bias related to age, sex, cohort, or environment.
  - Outlier handling: extreme cq values excluded (telomere cq > 25; GAPDH cq > 26).

- Data structure and key variables (Column descriptions)
  - BirdID: individual identifier
  - Sex: 0 = female, 1 = male
  - AgeY: age at catch (years)
  - AgeClass: developmental stage (e.g., A = adult, CH = chick, FL = fledgling, J = juvenile, etc.)
  - BirthFPID: fieldwork period ID (birth)
  - U_PlateID: qPCR plate ID for RTL measurements
  - RTL: relative telomere length
  - Technician: staff performing qPCR (two levels)
  - Terr: territory during catch
  - FPID: fieldwork period ID for catch
  - mum/dad: parental IDs from pedigree
  - MAC: maternal age at conception (years)
  - PAC: paternal age at conception (years)
  - BrF/BrM: dominant female/male in natal territory

- Experimental design and sampling regime
  - Major breeding season: June–September; minor season: January–March.
  - Birds captured opportunistically during breeding using mist nets to maximize sample coverage across seasons and cohorts.

- Fieldwork and laboratory instrumentation
  - DNA extraction: DNeasy blood and tissue kit (Qiagen) with overnight lysis at 37°C; final elution 80 μl.
  - DNA quality checks: integrity via 1.2% agarose gel; concentration quantified with NanoDrop 8000.
  - DNA handling: samples randomized to plates prior to qPCR; quality thresholds applied before RTL measurement.

- Data provenance and references
  - Sparks et al. 2021 (telomere heritability and parental age at conception effects in a wild avian population) provides sampling framework and QC criteria.
  - Spurgin et al. 2018 (spatio-temporal telomere dynamics) informs RTL measurement and plate-related variance handling.
  - Bebbington et al. 2016 (telomere length and inbreeding effects) contributes methodology for DNA extraction and QC.

- Practical analytics implications
  - Suitable for modeling RTL as a function of parental ages (MAC, PAC), genetic pedigree, and life-history factors.
  - Can incorporate plate as a random effect to account for technical variation; consider random effects for birth period, cohort, and individual identity to capture repeated measures.
  - With a large, longitudinally collected dataset and robust QC, supports estimation of heritability of RTL and assessment of transgenerational effects.