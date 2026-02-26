# Windermere Fish Abundance 1940-2012

## Overview
- Long-term dataset on fish abundance in Windermere (Cumbria, Great Britain) covering 1940–2012.
- Species tracked: Arctic charr (Salvelinus alpinus), Pike (Esox lucius), Perch (Perca fluviatilis), Roach (Rutilus rutilus); plus total fish abundance via hydroacoustics.
- Data origins: initial collection by the Freshwater Biological Association (FBA); from 1989/1990 onwards by CEH and its predecessor IFE. Hydroacoustics data collected by CEH/IFE since 1990.
- Geographical scope: Windermere North and South Basins; annual averages available.

## Data Structure and Contents
- Data file: Windermere_fish_1940_2012.csv (CSV, 24 KB).
- Columns include:
  - YEAR: year of measurement.
  - SITE: Windermere North basin or Windermere South basin.
  - DETERMINAND: fish species (and total fish via hydroacoustics).
  - ANNUAL_AVERAGE: yearly mean value.
  - UNITOFMEASUREMENT: CPUE (catch per unit effort) for species data; fish ha-1 for hydroacoustics.
- Measurements are presented as CPUE per year per species per basin.
- Determinands covered: Esox lucius (Pike), Perca fluviatilis (Perch), Rutilus rutilus (Roach), Salvelinus alpinus (Arctic charr), and Total fish (hydroacoustics).

## Data Collection and Methods
- Pike
  - Sampling: standardized gill-netting in north and south basins since 1982.
  - Net specifics: 64 mm bar mesh, 40 m x 3 m, deployed Oct–Dec at ~4–5 m depth across 10 sites per basin.
  - Sampling cadence: weekly pattern (Mon–Wed catch processing; Fri lift); systematic site rotation.
  - Effort: ~240 net days annually since 1990.
  - Output: CPUE by numbers (annual average per basin, per year).
- Perch
  - Sampling: standardized trapping from 1943–present; ~300 traps historically; design changes over time.
  - Output: CPUE by numbers per year (1982–2012); high annual variability limited confidence limits.
- Roach
  - Sampling: bottom-set survey gill nets at 15 inshore sites; years: 1995, 2000, 2005, 2012.
  - Nets: varying lengths and bar mesh sizes across years (adjusted designs noted).
  - Output: CPUE for small and large roach per basin per year.
- Arctic charr
  - Sampling: gill nets in the north basin from 1940–2012; spawning grounds detailed; nets ~28 m x 1.8 m with 32 mm mesh.
  - Output: CPUE for spawning Arctic charr in November each year; measurements include length; fish released after processing.
- Hydroacoustics (Total fish abundance)
  - Sampling: day- and night-time hydroacoustic surveys monthly from 1990 onward.
  - Equipment evolution: early single-beam 70 kHz system; since 2002, split-beam 200 kHz system with calibration between systems.
  - Output: night-time abundance of all detectable fish (whole water column); day-time abundance of large fish (>~200 mm) in upper 20 m.
  - Statistics: yearly means with 95% CIs from monthly data; two-operator quality checks.
- Metadata and site details
  - Location: Windermere lake; coordinates provided (OS grid references and lat/long).
  - Determinants and measurement units standardized to CPUE (or CPUE-derived units for hydroacoustics).

## Data Processing, Quality Control, and Provenance
- Specimen measurement and ageing
  - Pike: morphometrics (fork length, weight) and sexing; ageing via opercular bone; birth date assumed 1 April.
  - Arctic charr: species identification and measurement; released alive except for incidental mortalities.
- Ageing and calibration references
  - Ageing methods and references cited for pike (Frost & Kipling, 1959; Le Cren, 1959/2001) and arctic char methods.
- Quality control
  - Repeated measurements checked by multiple individuals (three individuals for QC; two for hydroacoustics QC in some steps).
  - Hydroacoustic calibration steps and inter-system calibration documented (Baroudy & Elliott 1993; Winfield et al. 2006).
- Data lineage and publications
  - The dataset underpins related publications (e.g., Baroudy & Elliott 1993; Winfield et al. 2006; Winfield et al. 2008) that relate population trends to eutrophication, climate change, and prey abundance.

## Dataset Access, Standards, and Provenance
- Access and format
  - Data downloadable as Windermere_fish_1940_2012.csv; designed for integration with other datasets via common CPUE metrics.
- Stewardship and custodians
  - Originally collected by FBA; later maintained by CEH/IFE and associated CEH publications.
- Data coverage and gaps
  - Comprehensive time series for Arctic charr (1940–2012) in the north basin; pike and perch datasets span multiple decades with standardized methods from the 1980s–2012; roach data available for a subset of years (1995, 2000, 2005, 2012); hydroacoustics available from 1990–2012 with monthly frequencies.

## Implications for Data Strategy and Management (Data Leaders)
- Data integration and harmonization
  - Multiple sampling methods across species require careful normalization to enable cross-species and cross-method analyses (CPUE as a common metric; hydroacoustics CPUE interpreted as fish per hectare).
- Metadata completeness and discoverability
  - Clear documentation of basins, time periods, sampling regimes, mesh sizes, and equipment is essential for re-use and reproducibility.
- Data quality and provenance
  - Rigorous QC procedures (multi-person checks, calibration records, ageing references) support reliability and auditability of trends.
- Data governance and stewardship
  - Longitudinal stewardship across institutions (FBA → CEH/IFE) highlights the need for formal data provenance tracking, versioning, and cross-institution data-sharing agreements.
- Usability and governance outcomes
  - This dataset enables time-series analysis of fish populations and ecosystem responses (e.g., eutrophication, climate effects) and supports stakeholder needs for policy-relevant biodiversity and fisheries insights.
- Potential challenges to plan for
  - Methodological changes over time (trap designs, net specifications, hydroacoustic technology) requiring careful methodological notes.
  - Gaps in roach data and the focus on spawning-period CPUE for Arctic charr; interpretive caution for trend analyses across all species.
  - Ensuring ongoing accessibility and updates to align with new data products and downstream analytics.