# Fish abundance, habitat, water quality, flow and climate in English Rivers from 1975-2017.

- Purpose and scope
  - Provides extracted chemical statistics for chemical determinand locations nearest to NFPD fish sites in England.
  - Statistics are calculated for the antecedent period immediately prior to the biota (fish) survey date, set to 12 months for fish.

- Data provenance and authorship
  - Authors: Rachel Ainsworth (University of Hull) and Virginie Keller (UK CEH).
  - Funding: NERC Chempop grant NE/S000100/2.
  - Geographic focus: England; data collection period around 2021–2022; publication in 2024 (data citation available).

- Data content and file structure
  - Main file: Region_FISHWIMSStats_DET.csv (per region), containing wims statistics for each fish sample for chemical determinand (DET_Label).
  - Variables: 18 core variables per region, plus 41 chemicals referenced in supporting documentation.
  - Key fields include:
    - Fish_SiteID, Fish_SurveyDate
    - W1_SMPT_REF (chemical determinand sampling point)
    - Water quality statistics with three LOQ handling options (LOQ1, LOQ2, LOQ3) for min, max, median, mean, and standard deviation
    - WQ_Count, WQ_COUNT_L_LOQ, WQ_COUNT_G_LOQ
  - DET metadata: DET_CODE, DET_DESC, DET_Label, Max_Concentration (values above max discarded)

- Data linkage and metadata
  - Fish_SiteID links to Fish_SiteID in fish Datatable, Hydrology, and chemical determinand files.
  - The dataset uses Environment Agency water quality data from the Water Quality Archive (Beta). Some determinand data excluded due to licensing.
  - Public access: environment.data.gov.uk/water-quality/view/landing
  - Citation: Ainsworth et al. (2024), DOI provided; dataset hosted by NERC EDS Environmental Information Data Centre.

- Methods and data processing
  - Site matching: ArcGIS Near Table Generator to identify the nearest three chemical determinand sites for each fish site; additional criteria applied (sufficient sampling, river/order compatibility, temporal overlap within a 2-year allowance, geographic distance).
  - Data extraction: EA Water Quality data portal for the selected chemical determinands (41 chemicals) for the defined antecedent period.
  - Statistical calculations: min, max, median, mean, standard deviation, plus:
    - Total number of samples
    - Number of samples below LOQ
    - Number of samples above LOQ
  - Processing rules for LOQ:
    - Three options to handle values below LOQ: treat as LOQ, 0, or LOQ/2
  - Thresholds and curation:
    - Metals: maximum threshold concentration of 10 mg/L; values above threshold discarded
  - Software: ArcGIS (10.7+ or Pro); Python 3 with math, pandas, numpy, itertools, datetime, dateutil, os, time, shutil

- Quality assurance and personnel
  - QA: Subset chemical matching checked by Monika Jurgens.
  - Involved personnel: Monika Jurgens, Rachel Ainsworth, Virginie Keller, Nuria BachellerJareno.

- Data governance, access, and limitations
  - Licensing: Data derived from Environment Agency Water Quality Archive; some data restricted by licensing.
  - Data sharing: Publicly accessible through the EA data portal; non-public data omitted due to licensing restrictions.
  - Limitations: Not all water quality determinands are included; some sensitive sites omitted; LOQ handling introduces methodological variance; Max_Concentration thresholds may affect rare high values.

- Practical notes for data leaders
  - Clear provenance and cross-linking via Fish_SiteID enables integration with other regional datasets.
  - Explicit LOQ handling options should be standardized across analyses to ensure comparability.
  - Licensing and data sensitivity considerations are critical for cross-sector data integrations; maintain awareness of restricted data and cite the EA Water Quality Archive as data source.
  - The DET metadata (CODE, DESC, LABEL, Max_Concentration) supports consistent interpretation across chemicals and facilitates reuse in other CHEMPOP-related projects.