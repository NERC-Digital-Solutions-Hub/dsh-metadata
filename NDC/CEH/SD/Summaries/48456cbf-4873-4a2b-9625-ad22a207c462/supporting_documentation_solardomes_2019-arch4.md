# Ozone exposure experiment in solardomes, North Wales, UK (2019)

## Overview
- Rural site in North Wales, UK, part of Bangor University farm; near the sea.
- Eight hemi-spherical solardomes used in 2019; ozone added via a computer-controlled system (LabView) following a weekly profile; ozone applied at night and during the day.
- Three of the solardomes were heated by 7°C above ambient to mimic tropical/subtropical conditions; plant biomass and physiology data available only for these three heated domes.
- Experiment involved four replicate pots per species/cultivar; exposure lengths varied by species due to growing-season differences.
- Treatments (all heated) target different ozone levels: Low (peak ~35 ppb), Medium (peak ~80 ppb), High (peak ~115 ppb).
- Endpoints: biomass/yield for all species/cultivars; ad-hoc stomatal conductance measurements, soil moisture, chlorophyll content index during exposure.

## Experimental design and data collection
- plant material: four replicate pots per species/cultivar grown from seed.
- Exposure setup: continuous hourly sampling of ozone and meteorology in the solardomes.
- Measurements: ad-hoc stomatal conductance, soil moisture, chlorophyll content index during exposure; biomass/yield measured at end.
- Start and end times per species differ (e.g., several beans and sweet potato measurements span 13/06/2019 to 01/10/2019 or 10/10/2019 for some cultivars).

## Treatments and equipment
- Low ozone, heated: target peak ~35 ppb, ambient temperature +7°C
- Medium ozone, heated: target peak ~80 ppb, ambient temperature +7°C
- High ozone, heated: target peak ~115 ppb, ambient temperature +7°C
- Instruments: LabView-controlled ozone/meterology loggers; AP4 porometer for stomatal conductance; Delta-T theta probe for soil moisture; CCM-200 for chlorophyll content.

## Data resources and structure
- Biomass_and_Yield_2019.csv: 11 columns, 63 rows; includes metrics such as pod/bean counts and weights per pot; sweet potato tuber yield (when applicable).
- Ozone_and_meteorology_2019.csv: 11 columns, 10,008 rows; hourly ozone (ppb) and meteorological variables (Light, Temperature, RH, etc.); includes DO3SE model inputs (air pressure, wind speed, precipitation as dummy values).
- Plant_Physiology_2019.csv: 12 columns, 692 rows; plant physiology data (only available for sweet potato); blank cells indicate missing readings.
- Data files include detailed column definitions and units, with blank cells indicating missing data.
- Some periods lacked logging due to computer power/technical faults; gaps were filled per a documented gap-filling protocol.

## Quality control and calibration
- Data logged automatically with quality checks for range plausibility; gap filling applied where needed.
- Ozone analysers calibrated by an external lab; porometer and CCM-200 calibrated/calibration steps followed per manufacturer guidance.
- Consistency checks and plausibility checks performed on QA; outliers identified and reviewed.

## Gap filling and data processing (gap filling protocol)
- Maintain original and a filled/corrected copy of data; record all modifications.
- Gaps of up to 5 consecutive hours: fill with the average of the preceding and following values.
- Larger gaps: consult lab book; fill using values from the same time on the previous/next day; adjust as necessary to preserve data patterns.
- If the ozone system was not running, fill with a dummy value of 5 ppb.
- Anomalous values (e.g., negative ozone) corrected to plausible values using surrounding data.
- All changes documented in separate worksheets/files.

## Data provenance and governance
- Data collection and logging were automated with periodic QA and calibration records.
- Gap filling and data amendments are versioned and documented to preserve traceability.
- Summary and supplementary information reference the CEH Solardomes ozone field-release facility website for facility context.

## Considerations for reuse and data leaders
- Data are suitable for model inputs (e.g., DO3SE) requiring hourly ozone and meteorology data, with note on constant wind speed and dummy precipitation values.
- Plant physiology data are limited to sweet potato; broader cross-species comparisons are constrained by data availability.
- Documentation covers data structure, measurement methods, QA, calibration, and gap-filling procedures, supporting reproducibility and data integrity.
- Licensing and access details are not specified within the provided document; cross-reference the facility website for additional context and access pathways.