# Supporting Document Chemical Exposure and Stress Responses in UK Fish. Pottinger, T. G., Matthiessen, P . (2017)

## Aim and scope
- Assess whether the chemical milieu downstream of wastewater treatment works (WWTWs) affects the stress axis in three-spined sticklebacks.
- Compare unstressed (baseline) and stressed indices: whole-body cortisol, cortisol released to water, and whole-body glucose.
- Data collected across multiple sites in north-west England during 2011, 2013, and 2014.

## Sampling regime
- Sites include downstream of WWTWs and reference sites with no identifiable WWTW input.
- Fish captured with a metal-framed hand net; focus on emergent vegetation and sheltered areas.
- Sampling years: 2011, 2013, 2014; at each site, first ten fish killed immediately for unstressed samples; a second batch designated as stressed (retained in water for 30–60 minutes in 2011; 30–45 minutes in 2013–2014) before death.
- Post-confinement, fish processed similarly to unstressed individuals.
- For cortisol collection during confinement, artificial freshwater used to minimize interference from suspended solids.

## Processing and analytical procedures
- In the lab, for each fish: weigh (mg), measure total length (mm), determine sex by gonad inspection.
- Tissue processing: homogenate prepared in buffer; a 250 μL aliquot processed for cortisol extraction.
- Cortisol analysis: cortisol extracted with ethyl acetate, then measured by cortisol radioimmunoassay (RIA) using a validated method with a tritiated cortisol tracer.
- Water cortisol: water samples filtered inline, cortisol extracted via Sep-Pak C18 cartridges, blanks and recovery standards included; eluted with ethyl acetate, dried, reconstituted, and assayed by RIA.
- Glucose: whole-body glucose measured in homogenate using a microplate assay (hexokinase reagent).
- Sample storage: fish samples stored at -70°C prior to processing; water samples stored on ice then at -20°C after return to the laboratory.

## Data structure and variables
- Data format: comma-separated values (CSV).
- Key columns:
  - Sample_date: date of capture
  - WWTW_name: upstream wastewater treatment works name
  - River: river sampled
  - Stressed_or_Unstressed: stressed after confinement or control
  - Weight_mg: fish weight
  - Length_mm: total length
  - Condition_factor: K-factor (100*weight/length)
  - Sex: M or F
  - Whole_body_cortisol_ng_g_bw: cortisol concentration in whole-body homogenate (ng/g bw)
  - Whole_body_glucose_mg_g_bw: glucose concentration in whole-body homogenate (mg/g bw)
  - CRTW_pg_g_h: cortisol released to water during confinement (pg/g/h), normalised to body weight

## Sampling locations and site context
- Sites include Bushburn Brook, Glaze Brook, Maghull Hey Cop Drain, Moss Brook, Netherley Brook, Pendle Water, Pennington Brook, R. Calder, R. Darwen, R. Irk, R. Lostock, R. Mersey, R. Tame, R. Yarrow, Sankey Brook, Sinderland Brook, and others.
- For each site: upstream location, downstream WWTW discharge location, and population served by the WWTW (where provided).
- Upstream vs downstream designation captured (us/ds) and WWTW discharge relationships noted.

## Data handling and quality controls
- Use of blanks and a recovery standard with each batch of ten water samples to ensure extraction accuracy.
- Well-documented protocols for sample collection, storage, extraction, and assay to support reproducibility.
- References underlying methods include Klüttgen et al. (1994) for artificial freshwater and Pottinger & Carrick (2001, 2002) for cortisol and stress-response methodologies.

## Data usage and publications
- The dataset underpins multiple publications:
  - Pottinger, G.T., Henrys, P.A., Williams, R.J., Matthiessen, P. (2013). The stress response of three-spined sticklebacks is modified in proportion to effluent exposure downstream of wastewater treatment works. Aquatic Toxicology, 126, 382-392.
  - Pottinger, G.T., Williams, R.J., Matthiessen, P. (2016). A comparison of two methods for the assessment of stress axis activity in wild fish in relation to wastewater effluent exposure. General and Comparative Endocrinology, 230-231, 29-37.
  - Pottinger, G.T., Williams, R.J., Matthiessen, P. (2016). Long-term water quality data explain interpopulation variation in responsiveness to stress in sticklebacks at both wastewater effluent-contaminated and uncontaminated sites. Environmental Toxicology and Chemistry, 35, 3014-3022.
- Data are suitable for self-service analysis of stress biomarkers across spatial (site-to-site) and temporal (years) dimensions, enabling examination of effluent exposure effects on the fish stress axis.