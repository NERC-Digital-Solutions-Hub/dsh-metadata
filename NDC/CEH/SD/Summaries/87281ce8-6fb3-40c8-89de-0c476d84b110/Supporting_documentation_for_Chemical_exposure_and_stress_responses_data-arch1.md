# Chemical Exposure and Stress Responses in UK Fish

## Objective
- Assess whether the chemical milieu downstream of wastewater treatment works (WWTWs) affects the functioning of the stress axis in three-spined sticklebacks.
- Quantify stress indicators (basal and post-confinement) to evaluate exposure effects.

## Sampling regime and collection methods
- Location: sites downstream of WWTWs and sites with no identifiable WWTW input in northwest England.
- Sampling years: 2011, 2013, 2014.
- Fish capture: metal-framed hand net; fish typically found near banks, vegetation, or debris.
- Unstressed (baseline) samples: first ten fish captured killed immediately after capture.
- Stressed samples:
  - 2011: an additional ten fish per site retained in river water for 30–60 minutes, then killed.
  - 2013–2014: ten additional fish retained in 2.5 L river water for ~30–45 minutes, then transferred to 100 mL artificial freshwater for a further 30 minutes to collect cortisol released across gills; then killed.
- Handling: euthanasia with sedative; samples stored in labeled tubes; water samples processed and stored on ice, then frozen for transport.
- Controls: a CEH aquarium control population was sampled with a similar procedure.

## Processing of fish and analytical procedures
- In-lab measurements:
  - Weigh fish (mg) and measure total length (mm); determine sex by gonad examination.
  - Homogenize tissue; prepare buffer; extract cortisol with ethyl acetate; perform cortisol radioimmunoassay (RIA).
  - Glucose measured in homogenate supernatant using a hexokinase-based assay.
- Water sample processing:
  - Inline filtration, solid-phase extraction (Sep-Pak C18), elution with ethyl acetate, evaporation, reconstitution, and cortisol assay.
- Cortisol metrics:
  - Whole-body cortisol (ng/g bw) and cortisol released to water during confinement (CRTW, pg/g/h), both normalized to body weight.
- Data quality controls:
  - Blank and recovery standards included with each batch.

## Data structure and fields
- Data provided as a comma-separated values (CSV) file with columns:
  - Sample_date
  - WWTW_name
  - River
  - Stressed_or_Unstressed
  - Weight_mg
  - Length_mm
  - Condition_factor (K-factor = 100*weight/length^3)
  - Sex
  - Whole_body_cortisol_ng_g_bw
  - Whole_body_glucose_mg_g_bw
  - CRTW_pg_g_h

## Sampling locations and site descriptions
- Locations include multiple rivers and tributaries with upstream and downstream references relative to specific WWTWs.
- For each site, data include:
  - River name
  - Upstream (us) or downstream (ds) from WWTW
  - WWTW discharge location
  - Population served by the WWTW
- A comprehensive list of sites (and their coordinates/NGR references) is provided in the study, covering various catchments (e.g., Bushburn Brook, Glaze Brook, Maghull Hey Cop Drain, Moss Brook, Netherley Brook, Pendle Water, Pennington Brook, R. Calder, R. Darwen, R. Irk, R. Lostock, R. Mersey, R. Tame, R. Yarrow, Sankey Brook, Sinderland Brook, Tara Carr Gutter, Thistleton Brook, Westleigh Brook, and others).

## Temporal coverage and sampling design
- Three sampling campaigns across three years (2011, 2013, 2014) to capture temporal variability and responses to effluent exposure.
- Parallel collection of unstressed and stressed fish enables assessment of stress axis responsiveness under different environmental conditions.

## Data handling, storage, and availability
- Immediate processing in the field followed by rapid freezing (-70°C storage for initial samples; -20°C storage for some components).
- Water samples processed to minimize interference from suspended solids.
- Data are organized to allow linking of individual fish metrics (size, sex) with stress indicators and sampling context (site, downstream/upstream of WWTW).

## References and prior use
- Methodological foundations and prior validation cited (Klüttgen et al., 1994; Pottinger & Carrick, 2001; Pottinger, Carrick & Yeomans, 2002).
- The dataset has underpinned publications examining how stress axis activity relates to wastewater effluent exposure, including:
  - Pottinger et al. (2013) Aquatic Toxicology
  - Pottinger et al. (2016) General and Comparative Endocrinology
  - Pottinger, Williams & Matthiessen (2016) Environmental Toxicology and Chemistry
  - Pottinger, Henrys, Williams & Matthiessen (2013) Aquatic Toxicology
- Data and methods are designed to support analyses of correlations between effluent exposure, stress physiology, and potential downstream ecological impacts.