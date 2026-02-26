# Harmonia axyridis invasion: UK distribution data 2004-2016

## Overview
- Dataset of Harlequin ladybird (Harmonia axyridis) observations in the UK from 2004–2016 (three records from 2003).
- Aggregates records from multiple sources, mainly online recording via the Harlequin Ladybird Survey, UK Ladybird Survey, and the iRecord Ladybird app; plus contributions from coleopterists and a data call for the latest atlas.
- Includes abundance, life stage, and colour form information when available; used for monitoring and informing policy decisions.

## Collection/generation/transformation methods
- Records collated from diverse sources and stored in an Oracle database; records are not altered, apart from standardised exports for this dataset.
- Quality checks applied during collection; standardised data exports are described in accompanying sections.

## Nature and units of recorded values
- Each record is a sighting of one or more individuals; abundance, life stage, and colour form available only for some records.
- Abundance can be a single figure, a range, or qualitative descriptors (e.g., a couple, a few).
- Location provided as grid references (OSGB, OSI, or MGRS) and as latitude/longitude; both 1km and 10km grid references included where available.
- Dates: STARTDATE and ENDDATE (full dates when provided; otherwise month/year or year only).
- Recorder: recorder identifier refers to the recorder name, not necessarily an individual person; one recorder ID can refer to multiple individuals.
- Data schema includes fields for precise geography (GRIDREF, PRECISION, VC, LATITUDE/LONGITUDE, GR_1KM/GR_10KM, etc.) and attributes (ABUNDANCE, FORM_ABUNDANCE, FORM, STAGE_ABUNDANCE, STAGE, RECORDER).

## Quality control
- Validation checks ensure grid references map to land, dates are valid, and records are verified.
- Verification conducted by a team of Coccinellidae experts; verification via photographs or specimens, or assumed correct if the recorder is a known expert.

## Details of data structure
- Key fields include: STARTDATE, ENDDATE, GRIDREF, PRECISION, VC (vice county), LATITUDE/LONGITUDE, GR_1KM, LATITUDE_1KM, LONGITUDE_1KM, GR_10KM, LATITUDE_10KM, LONGITUDE_10KM, ABUNDANCE, FORM_ABUNDANCE, FORM, STAGE_ABUNDANCE, STAGE, RECORDER.
- Grid reference systems vary by region (OSGB for Britain, OSI for Ireland, truncated MGRS for Channel Islands); precision and grid layers (1km, 10km) are explicitly stored.
- Recorder identifiers standardized as surname–initials; one ID may cover multiple individuals, and individuals may have multiple IDs.

## Recording bias
- Citizen-science-based data likely biased toward urban areas.
- Temporal spikes may occur during periods of intensive media activity surrounding the survey.
- Spatial and temporal biases are acknowledged as factors affecting representativeness.

## Relevance for environmental health monitoring (archetype perspective)
- Demonstrates a robust approach to building an environmental health monitoring dataset: multi-source data integration, rigorous quality control, and clear metadata (locations, dates, abundances, life stages, forms).
- Highlights the importance of standardized data structures and non-alteration of raw records, with transparent export-standardisation processes.
- Illustrates challenges common to monitoring frameworks: data gaps, access and timeliness issues, data governance considerations (e.g., provenance, recorder identification), and the need to communicate complex findings clearly.
- Emphasizes handling of spatial-temporal metadata (grid systems, precision, vice counties) to support reproducible analyses and policy-relevant monitoring outputs.