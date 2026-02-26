# PRECIPITATION CHEMISTRY Version 1.1 (supplier contact details updated July 2005)

## Aim and context
- Measures the chemical composition of precipitation and dry deposition (bulk deposition) at ECN sites using a continuously open gauge.
- Provides data to support understanding of atmospheric deposition impacts on ecosystems and to enable mapping and spatial analysis of deposition patterns.
- Data linkages exist with the UK Precipitation Composition Monitoring Networks (UKPCMN) for broader spatial context.

## Data collected and core measurements
- Bulk deposition collects both dry and wet deposition; results are treated as bulk deposition due to costs of separating components.
- Analytes and related measurements (weekly):
  - Volume of precipitation
  - pH and conductivity (on unfiltered water)
  - Alkalinity (as mg L-1)
  - Ions: Na+, K+, Ca2+, Mg2+, Fe2+, Al3+, NH4+-N, Cl-, NO3--N, SO4--S, PO4-3-P
- Units and precision are specified for each parameter (e.g., Na+, Cl-, NO3--N in mg L-1; conductivity in µS cm-1; pH scale).

## Sampling procedure and timing
- Sampling follows a standardized weekly protocol (Appendix I), with bottle changes coordinated to a regular day/time (standard: Wednesdays at 0900 GMT when possible).
- Sample handling includes cleaning and transferring protocols to minimize contamination; volume determined by weighing bottle contents.
- Volume flux calculations may use data from a nearby automatic weather station or standard raingauge to improve accuracy.

## Site and location metadata
- Each ECN site has:
  - A unique Site Identification Code (e.g., T05)
  - A Core Measurement Code (e.g., PC)
  - A Location Code (e.g., 01)
  - A Sampling Date/Time (GMT)
- Sampling stations are positioned to minimize contamination (upwind of sources; away from tracks, buildings, trees; approximately 1.75 m above ground; near soil solution samplers when feasible).
- Collectors are bolted to a base or secured with guy-ropes; care taken to avoid obstruction to other instruments.

## Lab analysis and data handling
- Initial water handling and pH/conductivity measured on unfiltered samples; after filtration, ion concentrations are determined.
- Labels uniquely identify samples: ECN Measurement Code, Site ID, Location Code, Sampling Date; field disturbance codes (insects, dust, bird droppings, etc.) are recorded.
- The recording form and additional notes ensure traceability from field collection to database entry.

## Data formats, transfer and access
- Data formats and required variables for each sampling location are defined in the ECNCCU Data Transfer documentation (restricted access on the Site Managers' extranet).
- Data transfer and archival practices are specified; contact ECNCCU for access if needed.

## Quality assurance and references
- QA procedures align with those used in related acid deposition networks (e.g., Acid Deposition Monitoring Network).
- Procedures cover potential errors from sampling, handling, and analysis; references include standard works on UK precipitation networks and related methods.

## Appendices (sampling specifics and equipment)
- Appendix I: Routine sample collection – step-by-step field procedures, contamination prevention, and handling of funnels, bottles, and filters.
- Appendix II: Equipment details – composition of the complete collector assembly, spare parts, recommended funnel sizes (usually 152 mm), and supplier information.

## Practical GIS considerations
- Data model implications: use Site Identification Code, Core Measurement Code, Location Code, and Sampling Date/Time as primary keys to link samples to spatial data.
- Spatial integration: link sample records to site coordinates and deployment metadata to create deposition maps and temporal trend analyses.
- Data quality and provenance: maintain field disturbance codes, labeling conventions, and QA notes to support data cleaning and audit trails in GIS workflows.
- Data harmonization: standard units, precision, and recording conventions enable consistent cross-site comparisons and integration with other national networks.