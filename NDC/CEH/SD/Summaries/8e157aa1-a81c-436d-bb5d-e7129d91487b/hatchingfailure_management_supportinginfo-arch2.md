# Supporting documentation for the dataset ' Avian hatching failure and management interventions in published studies of wild and captive populations '

- Overview
  - The dataset compiles hatching failure rates, threat status, and management interventions for 244 bird species across 233 published studies.
  - Originally created to support a meta-analysis comparing hatching failure between threatened and non-threatened species under different management levels.
  - Free to reuse with acknowledgment of the dataset DOI; citation of the associated Marshall et al. (2023) Biological Reviews paper is appreciated.

- Data scope and aims
  - Focuses on wild and captive birds (excluding domesticated poultry or birds bred intensively for the pet trade) and excludes studies with in-ovo injections or eggshell manipulation not aligning with the defined criteria.
  - Aims to enable cross-study synthesis of hatching failure and to assess how threat status and management influence hatch outcomes.

- Collection and sources
  - Three main collection streams:
    - Web of Science Core Collection search (16 Feb 2020) with a broad query on hatching metrics and English language.
    - Datasets from previous comparative analyses, checked for eligibility and data eligibility/verification.
    - Additional studies identified via February 2019–September 2020 Google Dataset Search, Google Scholar alerts, and related literature.
  - Records screened to remove duplicates and ineligible studies; pre-2004 studies not captured in prior analyses were typically excluded.

- Inclusion criteria
  - Peer-reviewed articles or online theses/dissertations; excludes predatory journals.
  - Accessible via publisher sites or institutional libraries.
  - Species are wild or captive birds (not domesticated poultry/gamebirds or intensively bred for sale as pets).
  - No in-ovo injections or egg component manipulations (except control handling).
  - Clear definition of hatching failure relative to eggs present at incubation end, excluding losses due to predation, desertion, accidents, extreme weather, or unknown factors.
  - Sufficient information to calculate hatching failure/success; minimum sample size of 10 eggs.
  - Availability of total eggs and/or hatched/unhatched counts or proportions.

- Data extraction and processing
  - Each record undergoes qualitative and quantitative extraction from text, tables, figures, and supplements.
  - WebPlotDigitizer used to extract data from figures when necessary.
  - When exact numbers were unavailable, derived estimates were created from available study details (e.g., nest counts, clutch sizes).
  - Efforts to verify data sources via original publications; records with insufficient information labeled as NA.
  - Population records may be split by species and population when multiple data points exist within a single study.

- Geographic and threat status details
  - Study locations converted to decimal degrees using Google Maps; central points used for ranges.
  - Threat status recorded for current IUCN Red List and the status at the time of the study; if subspecies lacked regional status, the parent species status used.
  - Only species recognized by BirdLife International and listed on IUCN Red List were included; subspecies status handled as described.

- Population type and management interventions
  - Population types classified as:
    - Captive: adults and eggs managed and reared in captivity.
    - Wild: adults in the wild with no management interventions.
    - Wild managed: wild adults with management interventions (e.g., predator control, nestboxes, supplementary feeding) or egg manipulations.
  - Management interventions classifications:
    - Often incomplete reporting; many records unable to confirm specific interventions.
    - Assumptions used:
      - All captive populations assumed supplementary fed unless stated otherwise; no artificial nests unless stated.
      - Non-captive populations assumed to have no management unless stated.
      - If any part of a population had an intervention and subpopulation data could not be separated, the intervention was attributed to the whole population.

- Hatching failure proportion extraction and calculations
  - Primary outcome: proportion of hatching failure across the population (eggs present at incubation end that failed to hatch, excluding certain losses).
  - For 286 of 483 records (59.2%), the sample size was directly available; otherwise, estimated.
  - Estimation methods included using the product of hatched nests and mean clutch size, or borrowing mean clutch sizes from external sources when not provided.
  - Caveats highlighted:
    - Some eggs labeled as abandoned/deserted may bias calculations.
    - Some nests reported only the number of eggs hatched or survived in “successful” nests, potentially excluding clutches that failed entirely.

- Terminology and standardization
  - Noted the terminology used across studies: hatching success, hatching failure, hatchability, and other terms.
  - Definitions were homogenized to standardize interpretation; 51 distinct definitions of hatching success and 12 of hatchability were identified in the dataset after processing.

- Data structure and variables
  - Table 1 (described): details the variables and units, including:
    - Publication year, study name, title, journal, and notes.
    - Geographic coordinates (latitude/longitude).
    - Population type (captive, wild, wild managed) and incubation type (natural/artificial).
    - Presence of nestboxes/burrows and supplementary feeding.
    - Clutch size data (BoW, NZBO, av. clutch size, etc.), nest/clutch counts, eggs counted.
    - Outcome data: total eggs, hatched/unhatched counts, Proportion, and standard errors/SDs.
    - Definitions used for hatching success/failure and any calculations/estimations performed.
  - The dataset integrates multiple sources and provides standardized effect sizes (including multiple effect sizes per study where applicable).

- Quality control
  - Data extraction performed by A. F. M.; around 10% of records cross-checked by P. B.
  - Potential outliers identified and examined for errors.

- Usage, access, and citations
  - Dataset is available for reuse with DOI acknowledgement.
  - Primary publication documenting the dataset is Marshall et al. 2023 (Systematic review of avian hatching failure and implications for conservation, Biological Reviews).
  - Original dataset methods and supplementary materials are open access and outlined to aid reproducibility.

- Relevance to environmental monitoring
  - Standardized, cross-study data on hatching failure and management interventions support monitoring of environmental health and conservation policy outcomes.
  - Enables comparisons across wild, wild managed, and captive contexts and across management regimes.
  - Facilitates integrating hatching outcomes with other environmental datasets (e.g., threat status, habitat conditions) for policy performance assessment and broader biodiversity monitoring.

- Limitations and caveats
  - Exclusion of predatory journals and some older records may limit historical coverage.
  - Incomplete reporting of management interventions and occasional misclassification risks.
  - Reliance on estimates when data are incomplete introduces uncertainty.

- References (selected)
  - Marshall AF, Balloux F, Hemmings N, Brekke P. 2023. Systematic review of avian hatching failure and implications for conservation. Biological Reviews. 98(3): 807-832. DOI: 10.1111/brv.12931.
  - Supporting methodological and data sources from Briskie & Mackintosh (2004), Spottiswoode & Møller (2004), Heber & Briskie (2010), Møller et al. (2010), Reding (2015), Johnsen (2019), and others cited in the dataset.