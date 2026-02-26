# Solute concentrations in water samples from clearfelled and standing Sitka spruce forest ecosystems, Kershope Forest

## Overview
- Historical dataset (1981–1987 for drainage water; earlier standing periods) from Kershope Forest, Cumbria, England.
- Aimed at assessing how clearfelling Sitka spruce plantations affects nutrient fluxes and soil fertility, informing forest management and environmental monitoring.

## Dataset contents and structure
- Drainsker.csv
  - Solute data from drainage water of six plots (Block 1) across six main drains.
  - Variables include discharge (m3 s-1), pH, suspended solids, and concentrations of K, Ca, Mg, Fe, Na, Al, PO4-P, NO3-N, NH4-N, Cl, SO4-S, and total organic carbon (TOC).
  - Contains sampling occasion codes and a note that '-1' indicates no sample.
- Soilsker.csv
  - Solute data from soil water samples collected via soil solution samplers and lysimeters across horizons (L, O, E, B) and sample types (needle trays, etc.).
  - Includes pH, K, Ca, Mg, Fe, Na, Al, PO4-P, NO3-N, NH4-N, Cl, SO4-S, TOC, with volume and sample codes.
- Kershope_sampling_points.csv
  - Metadata for sampling locations: plot, block, felled status, drain spacing/depth, and geographic coordinates (Easting/Northing).
  - Details on which sampling points correspond to drains, stemflow, rainfall, throughfall, Knapp throughflow, Lysimeters, and needles.
- Additional context
  - References and file-level notes describe the sampling equipment, sampling cadence (mostly weekly), and the sampling hierarchy (drains, soils, rainfall, stemflow, throughfall, etc.).

## Sampling design and methods
- Experimental setup
  - Six plots within Block 1 of a long-running drainage experiment on peaty gley soil.
  - Three plots remained standing; three were felled in 1983 (timing varies by plot).
  - Drains from all plots collected and analyzed; each plot had a main exit drain.
- Sampling scope and cadence
  - Drainage water: weekly samples from 1981–1987; discharge measured at sampling via a V-notch weir.
  - Other ecosystem components: soil solution samplers, lysimeters, rainfall collectors, stemflow, throughfall, and needle trays sampled at regular intervals (fortnightly to weekly, with some historical notes on sampling reliability for certain throughflow methods).
- Analytical methods (chemical analysis)
  - Ion concentrations: potassium and sodium by flame photometry; calcium, magnesium, iron, and aluminum by atomic absorption spectrophotometry; phosphate by molybdenum blue; ammonium by indophenol blue; nitrate and chloride by ion chromatography or alternative spectrophotometric methods (with cross-method comparability checks).
  - Carbon and solids: suspended solids (TSS) and total organic carbon (TOC) by standard methods.
- Site and vegetation context
  - Sitka spruce plantation established in 1948 on upland grassland; felled plots investigated to understand nutrient release and soil process changes.
  - Soils described as Cambic stagnohumic gleys on peaty material.

## Geographic and temporal coverage
- Location: Kershope Forest, Cumbria, England.
- Site characteristics: peat-rich, gley soils; gentle slopes (1–5 degrees); altitude around 225 m.
- Time frame
  - Drainage water sampling: 1981–1987.
  - Pre- and post-felling comparisons: sampling began two years before final felled status and continued through successive stages of standing and felled forest systems.

## Data quality, metadata, and accessibility
- Rich metadata describing plots, drains, sampling points, horizons, and sample codes to support traceability and reuse.
- Some data quality notes
  - Throughflow data acknowledged as not fully reliable due to sampling equipment problems.
  - Historical methods changed over time; cross-checks were performed to ensure comparability (e.g., concurrent use of old and new analytical methods for three months).
- Data structure supports monitoring framework needs
  - Clear mapping between sampling points, plot treatments, and chemical measurements.
  - Datasets include explicit codes for missing samples (e.g., -1) and detailed field definitions to aid data governance and reproducibility.

## Related literature and context
- Key publications tied to the data
  - Changes in solute chemistry of drainage waters following clearfelling (Forestry, 1987).
  - The effect of clearfelling on solute concentrations in drainage water (Journal of Hydrology, 1990).
  - Foundational methodological references for chemical analyses (Allen, 1989; Rowland, 1983) and soil/peatland hydrology (Knapp, 1973; Avery, 1980; Pyatt et al., 1985).
- These works provide interpretation of nutrient flux changes, soil fertility implications, and broader context for conifer harvesting impacts on surface water acidity.

## Monitoring framework relevance
- Demonstrates an integrated, multi-component water chemistry monitoring approach linked to forest management actions (standing vs felled plots).
- Highlights data governance considerations for monitoring programs
  - Comprehensive metadata for sampling points, plots, and drains.
  - Documentation of analytical methods and cross-method validation.
  - Clear data dictionaries and sample-coding schemes to ensure data interoperability.
- Illustrates challenges often faced in monitoring frameworks
  - Longitudinal data collection across changing management regimes.
  - Ensuring data accessibility and consistency when methods evolve.
  - Handling incomplete or unreliable components of the measurement suite (e.g., Knapp throughflow data).