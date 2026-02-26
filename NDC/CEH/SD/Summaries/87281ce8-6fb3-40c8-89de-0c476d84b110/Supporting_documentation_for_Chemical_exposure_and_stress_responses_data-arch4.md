# Supporting Document Chemical Exposure and Stress Responses in UK Fish. Pottinger, T. G., Matthiessen, P . (2017)

## Objective and scope
- Assess whether the chemical milieu downstream of wastewater treatment works (WWTWs) influences the stress axis in three-spined sticklebacks (Gasterosteus aculeatus L.).
- Conducted in north west England with sites downstream of WWTWs and sites with no identifiable WWTW input.
- Sampling years: 2011, 2013, 2014 to compare unstressed baseline and stressed (confinement-induced) stress responses.

## Data collected and key variables
- Biological measures:
  - Whole-body cortisol (ng/g body weight)
  - Cortisol released to water during confinement (CRTW; pg/g/h)
  - Whole-body glucose (mg/g bw)
  - Weight (mg)
  - Length (mm)
  - Sex (Male/Female)
  - Condition factor (K = 100*weight/length)
- Experimental status:
  - Unstressed (baseline, immediately after capture)
  - Stressed (after 30–60 minutes confinement; physiological response measured)
- Metadata:
  - Sample date
  - WWTW name
  - River
  - Upstream vs downstream designation
- Processing and storage identifiers linked to each fish sample

## Sampling regime and collection methods
- Fish captured using a metal-framed hand net; typically from bank-side vegetation or debris-associated areas.
- At each site, first ten fish killed immediately for unstressed samples; a second batch designated as stressed underwent a defined confinement period before sampling.
- Confinement specifics:
  - 2011: 30–60 minutes in river water; for cortisol release sampling, artificial freshwater used to minimize solids interference.
  - 2013–2014: 30–45 minutes confinement before transfer to small artificial freshwater volumes for immediate cortisol release sampling.
- Post-confinement, fish killed and preserved for laboratory processing.
- Control samples included from CEH aquarium tanks in 2011 (some fish sampled directly into sedative).

## Laboratory processing and analytical procedures
- Processing:
  - Fish weighed and total length recorded; sex determined via ventral dissection (gonad examination).
  - Tissue homogenates prepared for cortisol and glucose analyses.
- Cortisol extraction and measurement:
  - Homogenate processed with ethyl acetate extraction; cortisol quantified by a validated radioimmunoassay (RIA) using specific antibodies and tritium-labeled cortisol tracer.
  - Quality controls included blanks and recovery standards.
- Water cortisol collection:
  - Water samples passed through inline filters and Sep-Pak C18 cartridges; cortisol extracted with ethyl acetate and reconstituted for RIA.
- Glucose measurements:
  - Plasma homogenate supernatant assayed using a hexokinase-based colorimetric method.
- Storage:
  - Tissue samples stored at -70°C; water samples stored at -20°C prior to processing.

## Data structure and metadata
- Provided as a comma-separated values (CSV) file with clearly defined columns:
  - Sample_date
  - WWTW_name
  - River
  - Stressed_or_Unstressed
  - Weight_mg
  - Length_mm
  - Condition_factor
  - Sex
  - Whole_body_cortisol_ng_g_bw
  - Whole_body_glucose_mg_g_bw
  - CRTW_pg_g_h
- Each row corresponds to an individual fish with associated metadata and analytical results.

## Sampling locations and scale
- Sites include multiple rivers and catchments in the northwest of England (examples: Bushburn Brook, Glaze Brook, Maghull Hey Cop Drain, Moss Brook, Netherley Brook, Pendle Water, Pennington Brook, R. Calder, R. Darwen, R. Mersey, R. Tame, R. Yarrow, Sankey Brook, and others).
- Spatial design includes upstream vs downstream relative to various WWTWs and population served by each WWTW.
- Data captures variability across sites with downstream inputs to rivers from wastewater effluents.

## Usage and publications
- The dataset underpins multiple publications analyzing stress axis activity in relation to effluent exposure downstream of wastewater treatment works.
  - Pottinger, Henrys, Williams, Matthiessen (2013) Aquatic Toxicology
  - Pottinger, Williams, Matthiessen (2016) General and Comparative Endocrinology
  - Pottinger, Williams, Matthiessen (2016) Environmental Toxicology and Chemistry
  - Additional related work on long-term water quality and interpopulation variation (2016)
- Methods and data support cross-study comparisons and longitudinal analyses of stress responsiveness in wild fish populations.