# hydroscape_lakedistrict_core_metadata.csv

## Overview
- Metadata file describing lake core samples from the Hydroscape Lake District.
- Captures core-site location, sampling context, measurement indicators, core length/type, dating status, and internal identifiers.
- Designed to support environmental health monitoring and palaeolimnological interpretation to inform policy and decision-making.

## Key variables and fields
- Waterbody Identification number (WBID)
- Hydroscape region name
- Lake Name
- Core site designation (deep, littoral, intermediate)
- OSGB36_Easting and OSGB36_Northing coordinates
- Water_depth_at_core_site (m) – measured from boat with handheld echo sounder; littoral depth verified with Secchi depth
- Secchi_disc_depth (m) – mean of three measurements, taken at deepest lake position
- Core_length_and_type (m) – core length; corer type (Tapper, Big Ben, Livingstone, Renberg)
- Date_core_collected – fieldwork and core collection date (dd/mm/yyyy)
- UCL_Code – internal UCL bag/database code
- UCL_Sample_ID – internal Amphora code for entire sample core
- 210_Pb-dated_Y_N_for_Hydroscape – whether core dated by 210Pb (Yes/No)

## Measurement methods and data provenance
- Water depth: measured by hand-held echo sounder; littoral depth cross-checked with Secchi disc depth resting on sediment.
- Secchi depth: 20 cm disc lowered until not visible; three measurements averaged.
- Core types and references: includes Tapper, Big Ben, Livingstone, Renberg corers with cited literature for operation.
- Date collection and internal coding: field dates and unique sample identifiers are recorded for traceability.

## Data quality, metadata, and governance considerations
- Metadata completeness is essential for assessing suitability of data for monitoring and synthesis.
- Public sharing of underlying datasets can be a barrier; governance should address openness while protecting sensitive data.
- Data provenance requires clarity: originator details, method standardization, and potential need for metadata augmentation.
- Coordinate system (OSGB36) should be consistently applied for spatial analyses.
- Quality assurance steps implied (calibration, transformation, and documentation of methods) to ensure data are fit for purpose in dashboards and reports.

## Relevance for monitoring frameworks
- Provides geolocated core samples and associated measurements that can be used to infer historical environmental conditions and lake health proxies.
- Enables gap-filling in long-term environmental monitoring by supplying palaeolimnological context.
- Supports evaluation of policy interventions over time through comparability of core-derived indicators.

## Usage considerations and recommendations
- When integrating into a monitoring framework, ensure metadata completeness and data governance alignment (open data where appropriate, with clear data provenance).
- For analysis, verify consistency of depth measurements, Secchi protocols, and core-dating status across cores.
- Engage with originators or data custodians if additional metadata are needed (e.g., detailed QA steps, additional sample metadata).

## Limitations and caveats
- Some cores may not be 210Pb-dated, limiting certain chronological interpretations.
- Metadata notes specify measurement protocols; deviations or historical changes in methods should be documented for accurate interpretation.