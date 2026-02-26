# Supporting document for
# 'Nitrous oxide emissions and associated microbial diversity, soil biochemical properties and crop growth and yield from a field trial of winter barley with the addition of microplastics, Abergwyngregyn, UK, 2020-2021'

## Overview
- Field trial (Sept 2020 – July 2021) to assess the effects of conventional versus biodegradable microplastics on N2O emissions, soil biochemical properties, microbial diversity, crop growth, and yield in winter barley.
- Location: Henfaes Research Centre, Abergwyngregyn, North Wales.
- Experimental design: randomised block with three treatments (conventional microplastic, biodegradable microplastic, control) and four replicates per treatment.

## Experimental design and treatments
- Treatments and replication: conventional microplastic, biodegradable microplastic, and control; n = 4 replicates per treatment.
- Plot arrangement: randomised block design (see layout figure in the document).

## Data collection: in-field and laboratory measurements
- In-field measurements (in situ):
  - Nitrous oxide flux using a mobile gas chromatograph system.
  - Soil moisture (Acclima sensors) and ambient meteorological data (rainfall, air temperature).
- Laboratory measurements:
  - Soil properties: pH and electrical conductivity (EC); ammonium (NH4+) and nitrate (NO3−) contents.
  - Crop data: growth measurements (SPAD chlorophyll, plant height), crop harvest, and yield metrics.
  - Microbial data: 16S rRNA gene sequencing (Illumina MiSeq) to derive Amplicon Sequence Variant (ASV) counts and taxonomic assignments.
- Data processing tools:
  - N2O flux: Peak490Win10Canabis → Flux.NET → Excel → CSV; cumulative flux via trapezoidal integration.
  - Ammonium/nitrate: microplate method analyzed with Gen5; concentrations from calibration curves.
  - Microbial data: Python processing and QIIME v1.3.1 to generate ASV count table and taxa table.

## Data resource layout (10 files)
- crop_harvest.csv: contains date, treatment, plot, and harvest-related measurements.
- crop_yield.csv: contains metrics including stem count, grain per ear, ear weight, straw weight, grain weight.
- n2o_cumulative.csv: date, time, chamber, treatment, and cumulative N2O flux (mg N2O-N m−2).
- n2o_flux.csv: date, time, chamber, treatment, and flux values (μg N2O-N m−2 h−1).
- soil_n.csv: date, treatment, plot, nitrate and ammonium contents (kg NO3–N ha−1 and kg NH4–N ha−1).
- soilph_ec.csv: date, time, treatment, soil pH and EC (μS cm−1).
- weather.csv: date, time, air temperature (°C), and rainfall (mm).
- wfps.csv: date, time, treatment, plot, and water-filled pore space (%).
- asv_count_table.csv: ASV counts by treatment/replication across 2796 ASVs.
- taxa_table.csv: taxonomic assignments (Domain to Species) for ASVs, with some blanks where resolution was not available in SILVA v138.

## Sampling regime and analysis methods
- N2O flux:
  - Frequency: 8 measurements per 24-hour period using the automated GC system.
  - Data processing: raw peaks converted to flux values; cumulative flux calculated.
- Soil moisture and meteorology:
  - Soil moisture: every 30 minutes.
  - Air temperature and rainfall: every 30 minutes (weather station data used).
- Soil chemistry:
  - pH and EC: every 30 minutes initially, then weekly (reduced to fortnightly after 28/05/2021).
  - NH4+ and NO3−: every 30 minutes (weekly to fortnightly reductions after 28/05/2021).
- Plant data:
  - Leaf chlorophyll (SPAD) and plant height: every 30 minutes initially, then weekly/fortnightly reductions.
  - Crop harvest: at end of trial from designated middle-plot areas.
- Microbial community:
  - Sampling: soil 0–10 cm, stored at −80°C, then processed for 16S sequencing.
  - Analysis: ASV counting and taxonomic assignment via QIIME and Illumina MiSeq data.
- Data management:
  - All measurements linked to plots, treatments, and dates; data stored as CSVs for deposition.

## Data management, quality and accessibility
- Data processing pipelines use established tools (Flux.NET for N2O, Gen5 for chemistry, QIIME for microbiology) to ensure standardised outputs.
- Data files are prepared for deposit in the EIDC data portal to enable access to underlying datasets and facilitate reuse.
- The study aligns with environmental monitoring aims by providing standardized, reproducible data on emissions, soil health, microbial communities, crop performance, and microplastic treatment effects.

## Important dates and material details (highlights)
- Table 1 (key activities): dates for microplastic applications, barley sowing, greenhouse gas chamber setup, fertilizer applications, gas chamber extensions, sampling schedules, and harvest-related events.
- Table 2 (microplastics): conventional PE microplastics (40–48 μm, 100 kg/ha) and biodegradable PHBV microplastics (1–15 μm, 100 kg/ha); both applied to the top 0–10 cm soil layer.
- Table 3 (sampling regime): outlines frequency and methods for N2O flux, soil properties, leaf measurements, microbial sampling, and crop harvest.

## References
- Marsden et al., 2018: N2O emissions in grasslands (method context for N2O flux assessment).
- Miranda et al., 2001; Mulvaney, 1996: methods for nitrate/nitrite detection and soil inorganic N analysis.