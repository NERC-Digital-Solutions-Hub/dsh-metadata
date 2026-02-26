# EIDC dataset 2: Caterpillar masses from grass margins and hedgerows under streetlights, Oxfordshire, UK, 2018-2020

## Overview
- Dataset describing caterpillar masses from lit vs unlit transects in hedgerows and grass margins, using a matched-pairs design.
- Fields sampled: two feeding guilds (hedgerow beeting in spring; grass margins sweep netting in winter).
- Lighting treatments: LED, High-Pressure Sodium (HPS), Low-Pressure Sodium (LPS); lit sections illuminated for at least five years prior to sampling.
- Measurements include light intensity (lux) at standardized heights and, for grass margins, spectral data (CCT estimated from spectra).
- Samples were retained and weighed; provisional identifications assigned; two CSV data files plus field-site metadata; data used with previous Street lighting impact studies.

## Study design and field sites
- 26 lit/unlit site pairs, plus one triplet, with identical habitat apart from street lighting (linear habitat strips separated by ≥60 m; median 118 m).
- Sites chosen by overlaying street-light GIS data with satellite imagery and validated via Google Street View and field visits.
- Habitat types: hedgerows and grass margins; sampling locations matched for habitat type and microhabitat features (e.g., hedgerow trees, vegetation height) to minimize confounding factors.
- Site coefficients: paired transects geographically close; hedgerow and grass-margin matching criteria ensured comparability.

## Lighting, illumination, and spectral data
- Lit transects used current regional lighting: LED and HPS (dominant); two LPS transects included.
- Lux measurements taken at five points along each transect; heights: 1.25 m for hedgerows, 0.25 m for grass margins.
- Lit transects remained fully lit throughout the night; sampling occurred 02:00–04:00 to avoid dimming effects.
- Spectral data collected for grass margins using Ocean Optics USB2000+VIS-NIR-ES; CCT values reported (LEDs 2700–4000 K; HPS ~2200 K; LPS ~1800 K).
- Important caveat: lux is a human-vision metric; spectral differences not fully captured by lux alone.

## Caterpillar sampling and data collection
- Hedgerow sampling (spring): beating method at three points along each transect; two beating techniques used (drainpipes or beating tray); sampling at late spring (end of spring) to target spring-flush feeders.
- Grass margins sampling (winter): sweep-net sampling along transects to capture overwintering noctuids on grasses; sampling conducted 21:00–06:30 on mild nights.
- Sampling frequency: grass margins typically four visits; hedgerows two sampling events (late spring 2019 and early 2020); one site dropped due to development.
- Specimens: all caterpillars weighed (grass margins mean 98 mg; hedgerow mean 43 mg); provisional IDs assigned and grouped into 20 hedgerow taxonomic units and 16 grass-margin units; 34 day-flying Lepidoptera included due to potential nocturnal larval activity.
- Data handling: specimens retained at -20°C (except pandemic-related losses in 2020); standardised data collection forms; records double-checked for errors.

## Data structure and files
- Main hedgerow data: Boyes_et_al_2021_hedgerows_mass.csv
- Main grass-margin data: Boyes_et_al_2021_grass_mass.csv
- Field-site metadata: Boyes_et_al_2021_field_sites_data.csv
- Key fields in hedgerow/grасс data include: Visit_ID, Site_ID, Treatment, Sample_number, Provisional_ID, ID2, Caterpillar_mass_mg, DaysSince (grass margins), plus sampling method details.
- Field sites include: Site_Name, Light_Type, Lit_transect coordinates, Unlit_transect coordinates, hedge characteristics, vegetation height, distance between transects, urban-rural context metrics, and various radius-based urbanization proxies (100/250/500 m).
- Data management: standardized Excel-based data entry with dropdowns; data were entered within 24 hours of fieldwork; QA included outlier checks and duplicate data removal.

## Data quality, governance, and limitations
- Matched-pairs design with strict site-matching criteria to minimize confounds; temperature-controlled sampling nights to reduce variability.
- Rigorous QA: identical sampling nights across pairs; cross-checking of identifications; consistent data-entry rules.
- Limitations noted: lux as a proxy for ecological illumination; incomplete spectral data (spectra collected only for grass margins); some sites excluded due to habitat discrepancies; Covid-19 restricted laboratory access affected sample retention in 2020.
- Data linked to established literature on light pollution and moths; data prepared to support analyses of ALAN effects across life stages and guilds.

## Licensing and references
- Data reproduced from and accompanying the Science Advances study on street lighting and insect populations; licensing noted as Creative Commons (CC BY-NC) for the related study materials; data references provided for broader context.

## How this supports data governance for Data Leaders
- Demonstrates end-to-end data handling: field design, standardized collection, instrument calibration, sample preservation, metadata-rich field sheets, and explicit data dictionaries.
- Rich metadata enables cross-site comparability and reproducible analyses (coordinates, lighting type, illuminance, habitat context, sampling method, dates).
- Clear data lineage (link to prior methods study; multiple data products; structured CSV outputs) supports governance of data products and reuse within a wider data ecosystem.
- Addresses data quality by implementing matched-pairs design, QA steps, and explicit caveats, which is essential for governance of complex environmental data.