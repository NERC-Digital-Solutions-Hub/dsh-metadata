# DATASET: Stable water isotopes in Western Siberian inland waters

## Overview
- Part of the JPI/NERC SIWA project: Climate impact on the carbon emission and export from Siberian inland waters.
- Provides stable water isotope data (δ2H and δ18O) for rivers, lakes, soils across Western Siberian inland waters to inform understanding of hydrological processes and carbon dynamics in permafrost regions.

## Authors and collaborations
- A multi-institutional collaboration across the UK, France, Russia, and Sweden:
  - University of Aberdeen (UK) – Northern Rivers Institute, isotope analysis coordination.
  - Géosciences Environnement Toulouse (France) – sampling planning and logistics.
  - N. Laverov Federal Center for Integrated Arctic Research, Russian Academy of Science (Russia) – sampling coordination.
  - Tomsk State University (Russia) – sampling logistics and river/soil sampling in permafrost regions.
  - Umeå University (Sweden) – lake and river sampling planning.
- Roles span project planning, field sampling, isotope analysis, data curation, and archiving.

## Data generation responsibilities
- Northern Rivers Institute, U Aberdeen (Soulsby as PI; Tetzlaff as Co-I):
  - Planned sampling campaigns; coordinated stable water isotope analyses; compiled results into a database.
- GET Toulouse:
  - Planned sampling campaigns; coordinated logistics with TSU and UU.
- TSU Biogeochemistry/Geography (Kirpotin as PI):
  - Planned sampling; coordinated logistics with other partners.
  - Specific sampling assignments: Manasypov (large rivers/large areas), Lim (thaw ponds/suprapermafrost flow), Krickov (small rivers north–south gradient), Vorobyev (Ob river time series), Kolesnichenko (Tomsk region river), Loiko (soil pore waters north of permafrost), Serikova (lake sampling 2016).
- Umeå University (UU):
  - Planned sampling campaigns; contributed to lake/river sampling.
- Acknowledgements note additional team members for laboratory analysis.

## Sample collection and study design
- Sample types and collection:
  - River: grab samples from mid-channel when possible (from bridge or bank) at ~0.5 m depth in flowing water.
  - Lakes: collected from a boat at ~0.5 m depth; thermokarst lakes very shallow (0.5–1.0 m); for small lakes (<1000 m²) depth ~0.25 m.
  - Inundated areas: grab samples from boat.
  - Soil: ceramic cup suction lysimeters at 20–50 cm depths (typically ~10 cm above permafrost), filtered in the field (0.45 μm) and processed per Raudina et al. 2017.
- Sampling details documented with sample descriptions for rivers, lakes, floods, and soils; aims to cover large-scale permafrost zone to northern latitude gradients.

## Analysis and quality control
- Measurement: Los Gatos DLT-100 laser isotope analyser.
- Instrument precision: δ2H ±0.4 ‰; δ18O ±0.1 ‰.
- Isotope ratios reported in δ notation relative to Vienna Standard Mean Ocean Water (VSMOW).

## Data storage and provenance
- Storage: samples kept in the dark at 4–6 °C; shipped to University of Aberdeen for analysis; post-analysis archived in UoA facilities.
- Traceability: archived by analysis date and sample ID to enable easy re-tracing of samples.

## Metadata and data structure
- File: SIWA_stable_water_isotope_data.txt
- Encoding: UTF-16LE with Byte Order Mark (BOM)
- Structure: tabular; each row is a unique sample; columns describe attributes.
- Key data fields (with purpose and units):
  - T_ID: internal sample ID (text)
  - sample_ID: alternative sample ID (text)
  - lat_N: northern latitude (decimal degrees, WGS 84)
  - long_E: eastern longitude (decimal degrees, WGS 84)
  - sample_type: inland water type (lake, river, soil, flood)
  - sample_description: detailed English/Russian description
  - name_engl: English name of water body
  - sampling_date: date of collection (dd/mm/yyyy)
  - analysis_date: date of analysis (dd/mm/yyyy)
  - d2H: Deuterium isotope ratio (‰)
  - d18O: Oxygen-18 isotope ratio (‰)

## Relevance for monitoring frameworks
- Provides standardized, traceable isotope data across multiple water bodies and permafrost zones, enabling hydrological source tracking and carbon export analyses critical for environmental health monitoring.
- Demonstrates robust data governance and collaboration across institutions, including:
  - clearly defined roles and responsibilities
  - rigorous on-site sampling protocols and filtration steps
  - high-quality analytical methods with quantified precision
  - comprehensive metadata and a clear data schema to support data discovery, reuse, and integration into dashboards and policy evaluation.
- Addresses common monitoring challenges by outlining:
  - data collection across large geographic scales and diverse environments
  - metadata completeness and dataset provenance
  - data storage, traceability, and potential barriers to data sharing (noting that public sharing of underlying datasets can be a barrier in general, while this record emphasizes structured metadata and archiving to support governance).