# LANDWISE Detailed Survey Soil Data 2021 Updated

- Purpose and scope
  - Comprehensive dataset of surface and sub-surface hydraulic and hydrological soil properties across the Thames catchment.
  - Aimed at characterising field-scale heterogeneity under different land-based Natural Flood Management (NFM) measures.
  - Supports assessment of how natural land-based measures may reduce flood risk and how soil properties relate to hydrological responses.
  - Part of the LANDWISE project within the Natural Flood Management Research Programme; funded by the Natural Environment Research Council.

- Study design and sampling
  - Seven fields selected from a Broad-scale LANDWISE survey, grouped into three sites by geology: mudstone, chalk, and limestone.
  - Fields span three land-use/management types: permanent grassland, arable on carbonates (chalk/limestone) and limestone, and mixed arable with grass.
  - Replicated sampling across field zones: trafficked (TR), infield (IN), and untrafficked margins (UN).
  - Sampling sites and field IDs include 18_6, 44_1, 26_1, 23_5, 31_3, 27_2, 27_4 with locations provided in the study.
  - Fieldwork conducted April 2021 (Spring) and October 2021 (Autumn) with repeats pre- and post-harvest where applicable.

- Measurements and methods
  - Soil properties (depth up to ~100 cm where practical)
    - Bulk density and inferred porosity by volumetric cores and oven drying.
    - Volumetric soil moisture content (VWC) and soil porosity estimated from bulk density (assuming mineral soil density 2.65 g/cm3).
    - Soil moisture retention (pF 0–2) using an Eijkelkamp Sandbox.
  - Infiltration and hydraulic conductivity
    - Infiltration rate (unsaturated hydraulic conductivity, Kunsat) via Mini Disk Infiltrometer at various suction settings.
    - Saturated hydraulic conductivity (Ksat, Ks) at 25 cm and 45 cm depths using Guelph Permeameter (two-head method preferred; sometimes single-head measurements averaged).
  - Root and soil surface characteristics
    - Soil and vegetation root depth (Auger and tape measure) for each sampling location.
  - Sampling strategy details
    - Measurements conducted along transects with multiple location types and depths; spring measurements focused on initial conditions, autumn measurements after harvest.

- Variables and data structure
  - One dataset file: LANDWISE_detailed_survey_soil_data_2021_updated_v2 (CSV)
  - Contents: 70 columns, 380 rows; field- and location-level identifiers (site, field, location), measurement types, dates, depths, and results.
  - Variables cover: geographic identifiers (OS grid, easting/northing), sampling dates, soil depths, horizon depths, depths for Ksat and Kunosat measurements, VWC at multiple suctions, bulk density, porosity, Kfs in cm/s and m/s, QCs, and notes.
  - Missing values denoted as NA; some measurements flagged for quality issues.

- Quality control and data quality
  - QC process includes cross-checking field and lab entries by different staff to catch typos and inconsistencies.
  - Infiltration QC flags (Infiltration_1_QC_Flag and Infiltration_2_QC_Flag): Good, Invalid (physically implausible), A (unsteady rate), B (<15 ml infiltrated), C (unusually high Ks).
  - Guelph permeameter QC flags (Guelph_Permeameter_QC_Flag): Good, Invalid.
  - Notes indicate whether double-head or averaged single-head Ks measurements were used; preference given to double-head method when valid.
  - Some measurements with QC flags were removed or flagged for further interpretation.

- Fieldwork and instrumentation
  - Soil sampling: Eijkelkamp 07.53.SC sample ring kit with closed ring holder; Edelman and Stony augers.
  - Drying ovens: Heraeus Function Line; balances: Precisa 2200C (lab), Precisa 5000D (sandbox measurements) with calibration checks.
  - Infiltration: Mini Disk Infiltrometers (Decagon Devices).
  - Saturated hydraulic conductivity: Guelph Permeameter (two-head method).
  - Soil moisture retention: Eijkelkamp Sandbox.
  - Analyses and calculations referenced standard methods (e.g., Zhang 1997 for infiltrometer data; Carsel & Parrish 1988 for van Genuchten parameters).

- Geographic and temporal coverage
  - Thames catchment, across three geological contexts: mudstone, carbonate (chalk/limestone), with field sites near the Cotswolds and Oxfordshire.
  - Spring 2021 (April) and Autumn 2021 (October) sampling campaigns; pre-harvest and post-harvest measurements where applicable.

- Related datasets and references
  - Related to LANDWISE Broad-scale survey dataset on soil near-surface properties, vegetation observations, land use and land management in Thames catchment (2018–2021).
  - References for methods and software tools cited (Zhang 1997; Carsel & Parrish 1988; METER Mini Disk Infiltrometer manual; Guelph Permeameter manuals; LANDWISE Supporting Documentation).

- Data accessibility and usage notes for analysts
  - Standardised, field- and lab-derived soil property data suitable for temporal and spatial comparisons of soil hydraulic properties under different land uses and management practices.
  - Data quality flags and notes enable transparent filtering for robust analyses.
  - Useful for evaluating flood risk reduction potential of NFM practices by linking soil properties with infiltration and hydraulic conductivity responses across land-use types and soil textures.