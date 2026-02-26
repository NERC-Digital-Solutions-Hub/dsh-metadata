# Supporting Document
Chemical Exposure and Stress Responses in UK Fish. Pottinger, T. G., Matthiessen, P . (2017)

## Purpose and scope
- Evaluate whether the chemical milieu downstream of wastewater treatment works (WWTWs) affects the stress axis in three-spined sticklebacks (Gasterosteus aculeatus L.).
- Measure stress indicators: whole-body cortisol, cortisol released to water, and whole-body glucose.
- Compare stressed (after confinement) versus unstressed (immediately after capture) individuals.
- Conducted across multiple years to assess exposure effects.

## Sampling regime and field methods
- Locations: sites downstream of WWTWs and sites with no identifiable WWTW input in northwest England.
- Years: 2011, 2013, 2014.
- Fish collection: metal-framed hand nets; fish often found in vegetation or debris near banks.
- Stress manipulation:
  - Unstressed: immediate processing after capture.
  - Stressed: first batch retained in river water for 30–60 minutes, then killed for processing.
  - In 2011: additional batch retained in river water; in 2013–2014: second batch retained in 2.5 L river water then moved to artificial freshwater for cortisol release sampling.
- Sampling sequence: capture → sedation and disposal for unstressed samples; confinement period for stressed samples → transfer to sedative and processing.
- Sample handling: fish weighed and measured; sex determined biologically; samples stored at -70°C (fish tissue and certain water samples) or on ice/cool boxes prior to storage.

## Laboratory processing and assays
- Tissue processing: homogenisation of fish for cortisol and glucose analysis.
- Cortisol analysis: extraction from homogenate with ethyl acetate, followed by a cortisol radioimmunoassay (RIA) using specific antibodies and radioligand.
- Glucose analysis: microplate assay using hexokinase method.
- Water sample processing: inline filtration, solid-phase extraction (Sep-Pak C18 cartridge), cortisol elution with ethyl acetate, drying, reconstitution, and RIA.
- Quality controls: inclusion of blank samples and recovery standards (artificial freshwater with known cortisol concentration) with each batch.

## Data structure and variables
- Data provided as comma-separated values (CSV) with the following columns:
  - Sample_date: date of fish capture.
  - WWTW_name: upstream wastewater treatment works name.
  - River: river name sampled.
  - Stressed_or_Unstressed: stressed (after confinement) or control (unstressed) status.
  - Weight_mg: fish weight (mg).
  - Length_mm: total length (mm).
  - Condition_factor: K-factor = (100 × weight) / length.
  - Sex: Male (M) or Female (F).
  - Whole_body_cortisol_ng_g_bw: cortisol concentration in whole-body tissue (ng/g bw).
  - Whole_body_glucose_mg_g_bw: glucose concentration in whole-body tissue (mg/g bw).
  - CRTW_pg_g_h: cortisol released to water during confinement (pg/g/h), normalized to body weight.

## Sampling locations and context
- Provides a comprehensive list of sites with:
  - NGR coordinates for site locations.
  - Upstream (us) vs downstream (ds) status relative to WWTW inputs.
  - Specific WWTW discharge locations and population served by each WWTW.
- Examples of sites include Bushburn Brook, Glaze Brook, Maghull Hey Cop Drain, Moss Brook, Netherley Brook, Pendle Water, Pennington Brook, R. Calder, R. Darwen, R. Irk, R. Mersey, and others.
- Data structure includes both site coordinates and administrative context (WWTW names and population served).

## Quality control, storage, and handling
- Fish samples stored at -70°C prior to processing.
- Water and tissue samples transported on ice or stored at appropriate temperatures (ice for short-term handling; -20°C for storage).
- After processing, data are prepared for statistical analyses and cross-study comparisons.

## References and usage
- Foundational methods and prior validation include:
  - Klüttgen et al. (1994) on artificial freshwater for culture.
  - Pottinger & Carrick (2001) on stress responsiveness and cortisol measurement.
  - Pottinger, Carrick & Yeomans (2002) on stress indicators in sticklebacks.
- This dataset has been used in publications examining how stress axis activity in wild fish relates to wastewater effluent exposure:
  - Pottinger et al. (2013) Aquatic Toxicology.
  - Pottinger et al. (2016) General and Comparative Endocrinology.
  - Pottinger et al. (2016) Environmental Toxicology and Chemistry.
- The data support GIS-enabled visualization and spatial analyses of exposure and stress responses across multiple sites downstream of WWTWs.