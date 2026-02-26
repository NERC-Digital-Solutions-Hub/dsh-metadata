# Supporting Document Chemical Exposure and Stress Responses in UK Fish. Pottinger, T. G., Matthiessen, P . (2017)

## Objective
- Assess whether the chemical milieu downstream of wastewater treatment works (WWTW) affects the stress axis in three-spined sticklebacks.
- Use physiological indicators (cortisol and glucose) to evaluate stress status in fish collected and processed under controlled protocols.

## Sampling regime and collection methods
- Location: three-spined sticklebacks collected downstream of WWTWs and at sites with no identifiable WWTW input in northwest England.
- Timing: sampling conducted in 2011, 2013, and 2014.
- Capture method: nets in areas sheltered from main flow, near banksides or debris.
- Stress vs. unstressed sampling:
  - Unstressed: fish captured and immediately processed.
  - Stressed: a second batch (when possible) kept in river water for about 30–60 minutes to induce a stress response before processing.
- Handling and processing sequence:
  - Fish killed by sedation, weighed, measured, and sexed by gonad inspection.
  - For stressed fish, cortisol was collected from water during confinement using artificial freshwater to minimize solids interference.
  - Samples stored at -70°C or colder prior to processing.
- Control: an aquarium population was sampled in 2011 with comparable procedures.

## Processing of fish
- Measurements: each fish weighed (mg) and total length (mm); sex determined macroscopically.
- Tissue processing: fish homogenised in buffer; aliquots used for cortisol and glucose assays.
- Cortisol extraction: homogenate processed and cortisol measured via cortisol radioimmunoassay (RIA) using a validated antibody and radioligand method.
- Glucose: measured in the homogenate supernatant using a hexokinase-based microplate assay.
  
## Analytical procedures
- Water sampling for cortisol release:
  - Water from confinement period pumped through inline filtration and SPE (Sep-Pak C18 cartridges) for cortisol extraction.
  - Cartridges conditioned with ethyl acetate, methanol, then water; blanks and recovery standards included.
  - Cortisol eluted with ethyl acetate, dried, reconstituted, and 150 µL analyzed by RIA.
- Data normalization: cortisol concentrations expressed per gram body weight; glucose per gram body weight; CRTW (cortisol release to water) normalized to body weight.
- Quality controls: used a validated extraction and assay protocol; included blanks and recovery standards to monitor accuracy.

## Data structure
- Provided as a comma-separated values (CSV) file with columns including:
  - Sample_date, WWTW_name, River, Stressed_or_Unstressed
  - Weight_mg, Length_mm, Condition_factor (K-factor)
  - Sex
  - Whole_body_cortisol_ng_g_bw, Whole_body_glucose_mg_g_bw, CRTW_pg_g_h
- Metadata describes sample handling, processing steps, and calculation methods.

## Sampling locations
- Numerous sites across northwest England with explicit upstream and downstream designations relative to WWTWs and population served (e.g., Bushburn Brook, Glaze Brook, Pendle Water, R. Mersey, etc.).
- Each site includes coordinates, upstream/downstream status, WWTW discharge information, and population served where applicable.

## References
- Foundational methods and context for the sampling, extraction, and assays:
  - Klütgen et al. 1994 (artificial freshwater formulation)
  - Pottinger & Carrick 2001 (stress responsiveness and behavior)
  - Pottinger, Carrick & Yeomans 2002 (three-spined stickleback as environmental sentinel)

## Dataset usage and impact
- The dataset has informed multiple publications, including:
  - Pottinger, G.T., Henrys, P.A., Williams, R.J., Matthiessen, P. (2013) on stress response modifications downstream of effluent exposure (Aquatic Toxicology)
  - Pottinger, G.T., Williams, R.J., Matthiessen, P. (2016) comparing methods for assessing stress axis activity in wild fish relative to wastewater exposure (General and Comparative Endocrinology)
  - Pottinger, G.T., Williams, R. J., Matthiessen, P. (2016) long-term water quality data explaining interpopulation variation in sticklebacks (Environmental Toxicology and Chemistry)
- Demonstrates integration of field sampling, controlled processing, and robust analytical methods to support policy-relevant monitoring of environmental health.