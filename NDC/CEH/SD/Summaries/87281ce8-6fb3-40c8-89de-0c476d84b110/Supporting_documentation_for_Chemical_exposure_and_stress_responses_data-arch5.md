# Supporting Document Chemical Exposure and Stress Responses in UK Fish. Pottinger, T. G., Matthiessen, P . (2017)

## Overview
- Study assessing the impact of the chemical milieu downstream of wastewater treatment works (WWTWs) on the stress axis of three-spined sticklebacks (Gasterosteus aculeatus).
- Data collected from multiple sites in north west England, comparing downstream WWTW input vs upstream/no input.
- Indicators measured: whole-body cortisol, cortisol released to water, and whole-body glucose.
- Sampling years: 2011, 2013, 2014; included stressed (confinement) and unstressed (immediately captured) individuals.
- Dataset intended to support analyses of stress axis activity in relation to effluent exposure.

## Sampling regime and collection methods
- Species: three-spined sticklebacks; sites downstream of WWTWs and reference sites.
- Catch method: metal-framed 45 cm D-profile hand net; fish located in vegetation or debris.
- Handling: first ten fish per site killed immediately for unstressed samples; a parallel batch designated as stressed and subjected to confinement before processing.
- Stress protocol: confinement in river water (30–60 minutes, depending on year) to maximize cortisol release; then treated as unstressed or stressed as per batch.
- Collection of cortisol in water: for 2013–2014, cortisol released across gills collected in artificial freshwater to minimize suspended solids.
- Sample preservation: initial fish samples stored at -70 °C; transport in dry shippers; water samples kept on ice, later frozen at -20 °C.

## Processing of fish
- Measurements: weight (mg) and total length (mm); sex determined via ventral examination.
- Tissue processing: fish homogenized in buffer (Tris-HCl, NaCl, EDTA, NaN3); aliquots prepared for cortisol extraction.
- Cortisol extraction: ethyl acetate extraction from homogenate; evaporation and reconstitution for radioimmunoassay (RIA).
- Glucose measurement: enzymatic assay on homogenate supernatant (hexokinase reagent).

## Analytical procedures
- Water samples: inline filtration and Solid Phase Extraction (Sep-Pak C18); blanks and cortisol recovery standards included.
- Cortisol analysis: validated RIA method using specific antibody and radiolabeled cortisol; results expressed as ng/g body weight.
- Quality controls: recovery standards and blanks included with each batch; pre-conditioning of cartridges performed to avoid drying.
- Data capture: cortisol (whole-body and, where applicable, water-borne release) and glucose data recorded; method references provided for reproducibility.

## Data structure and content
- Format: comma-separated values (CSV) with clearly defined columns.
- Key columns (examples):
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
  - CRTW_pg_g_h (cortisol release rate)
- Metadata considerations:
  - Descriptions provided for each column (e.g., sample date, WWTW name, upstream/downstream status, measurement units).
  - Consistent units across years facilitate cross-site comparisons.

## Sampling locations and study design
- Sites include multiple rivers and streams (e.g., Bushburn Brook, Glaze Brook, Pendle Water, R. Mersey, R. Darwen, etc.) with upstream and downstream references to WWTWs and population served data.
- Upstream and downstream comparisons enable assessment of effluent-related stress axis changes.
- Population served data (nomenclature: number of people served by each WWTW) provides context for potential pollutant load.

## Data quality, provenance, and governance
- Provenance: detailed sampling and processing procedures, including handling times, confinement durations, and storage conditions, enabling reproducibility and audit trails.
- Provenance notes: year-specific deviations (e.g., handling times and collection methods differed between 2011 and 2013–2014) are documented, important for interpretation and harmonization.
- Data usage and lineage: dataset has been used in multiple publications evaluating stress responses and wastewater effluent exposure; includes references to foundational methods and validation studies.
- Preservation and storage: physical samples archived at -70 °C (biological samples) and -20 °C (water samples) to maintain integrity for downstream analysis.

## Data governance considerations for reuse
- This dataset is suitable for meta-analyses on fish stress physiology and pollution exposure, provided year-to-year methodological differences are accounted for.
- Citations and data provenance should reference the original sources and methodological papers (Pottinger et al., 2001; 2002; 2013; 2016; Matthiessen et al., 2016) as appropriate.
- Clear documentation of units, sample handling, and QA steps supports data discoverability and reuse within data portals and catalogues.

## Publications and usage
- The dataset has underpinned several publications:
  - Pottinger, G.T., Henrys, P.A., Williams, R.J., Matthiessen, P. (2013). The stress response of three-spined sticklebacks is modified in proportion to effluent exposure downstream of wastewater treatment works. Aquatic Toxicology.
  - Pottinger, G.T., Williams, R.J., Matthiessen, P. (2016). Methods for assessing stress axis activity in wild fish relative to wastewater exposure. General and Comparative Endocrinology.
  - Pottinger, G.T., Matthiessen, P. (2016-2016). Long-term water quality data and interpopulation variation in sticklebacks.
- These studies illustrate the dataset’s relevance for understanding environmental stress, effluent impacts, and methodological comparisons.