# Supporting documentation for data

## Overview
- Describes the Clocaenog field site, an automated manipulation experiment to project climate-change effects on upland moorland habitats over decades.
- Site uses automated roof technology powered by solar and wind; established in 1998; located in Clocaenog Forest, North East Wales (specific coordinates provided).
- Experimental design includes replicated drought and warming treatments to study ecosystem responses.

## Measurements and protocols (fortnightly data collection)
- Rainfall (mm)
  - Measured at ground level with a storage rain gauge (12.7 cm funnel); samples accumulated over two weeks (occasionally 3–4 weeks during holidays).
  - Preferred over AWS data when hourly data are not required due to robustness against logger power issues.
- Plot-level rain throughfall (mm)
  - Collected bi-weekly using a 16.8 cm diameter funnel and 3000 mL bottle per plot.
  - Data require adjustment to be comparable with site rainfall; use throughfall percent change applied to site rainfall to obtain plot-specific rainfall.
  - If data are lost or compromised (e.g., funnel/bottle issues), mark as NA for the affected plot.
- Water table depth (cm)
  - Measured bi-weekly using water-permeable tubes extending to bedrock; recordings taken with a head torch and tape.
  - Maximum detectable depths specified per plot (differing by plot).
- Soil respiration (mg CO2-C m⁻² h⁻¹)
  - Measured fortnightly with three opaque soil collars per plot (20 cm diameter) installed 5–10 cm deep; past vegetation disturbance minimized.
  - Post-2014, measurement uses an infrared gas analyser (EGM-4) linked to an SRC-1 chamber; 120-second sampling time.
  - Data processing: raw measurements converted to mg CO2-C m⁻² h⁻¹; for g CO2 m⁻² h⁻¹ readings, multiply by 0.272727 and then by 1000.
  - Three measurements per plot averaged; unrealistically high values removed from plot average.
  - Note: in summer 2013, installation of larger collars for automated measurements caused localized drier conditions that may bias results.
- Soil temperature (°C)
  - Measured near soil respiration chambers with a digital thermometer; measurements averaged per plot.
- Soil moisture (vol%)
  - Measured near respiration chambers with a Theta Probe (ML3, Delta-T); averaged per plot.
- Photosynthetic active radiation (PAR; µmol m⁻² s⁻¹)
  - Measured alongside soil respiration data; supported by plot-level micro-meteorological data and AWS data; hand-held device measurements encouraged only if site data are unavailable from preferred sources.
- Data recording and processing
  - Field data sheets; raw data transcribed to Excel; units standardized and calculations documented (e.g., conversion factors, averaging rules).
  - Emphasis on combining plot-level measurements with site- and micro-meteorological context for robust interpretation.

## Data handling, quality, and metadata
- Data lineage includes supporting documentation for the data series and a separate file detailing non-continuous measurements and methods.
- When time-series data are incomplete or compromised, clearly note gaps (NA) and rationale.
- Metadata limitations noted, including the need to supplement with originator-provided information when necessary.
- Documentation highlights the importance of context (treatment regime, collars, and instrumentation changes) for interpreting measurements and trends.

## Site-specific considerations and challenges
- Relevance of micro-meteorological and AWS data to interpret soil respiration and related variables; caution advised against relying solely on hand-held measurements.
- Throughfall adjustments require careful calculation to ensure comparability with site rainfall data, particularly during periods of data loss or equipment issues.
- Changes to instrumentation (e.g., larger soil collars in 2013) can introduce microhabitat changes (e.g., drier surrounding soil) potentially biasing measurements.
- Some measurements (e.g., water table depth) have plot-specific maximum detectable limits, influencing data interpretation across plots.

## Context and environment
- Moorland habitat dominated by Calluna vulgaris (heather), with Vaccinium myrtillus and Empetrum nigrum also present.
- The document provides a detailed methodological foundation for consistent data collection, processing, and interpretation to support environmental health monitoring and policy-relevant analysis.