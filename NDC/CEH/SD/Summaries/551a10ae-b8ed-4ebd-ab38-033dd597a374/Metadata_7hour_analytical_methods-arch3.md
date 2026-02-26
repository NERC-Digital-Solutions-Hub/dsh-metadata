# Analytical Data Metadata for Water Quality Monitoring (2007-2009)

- Purpose and scope
  - Comprehensive dataset detailing dissolved and total measurements for a wide range of elements and compounds in water.
  - Includes detailed metadata for each analyte, such as form, determinand, units, detection/quantitation parameters, sampling windows, locations, methods, and data qualifiers.
  - Reflects both laboratory analyses and field-derived metrics (e.g., area-weighted stream flow, rainfall, and runoff).

- Key data elements
  - Analyte name, chemical form, determinand, units, lower quantitation data (LQDC), quoted value, start and end dates.
  - Location of analysis, analytical method and QC data qualifier, data qualifier codes, filtration method, preservation method, and associated SOP references.
  - Additional notes or comments fields where applicable (e.g., method specifics, equipment, or procedures).

- Temporal and spatial coverage
  - Time span: 6-Mar-2007 to 27-Jan-2009 (with some end dates extending to 27-Jan-09 or specific sites).
  - Locations include Lancaster, Wallingford, Bangor, and field sites; several entries indicate field analysis or combined hydrological calculations.
  - Includes derived field metrics (area-weighted stream flow, area-weighted rainfall, hourly water fluxes, stream flow in cumecs, and time-based conversions).

- Data quality, QC, and accreditation
  - Analytical method QC codes indicate QA measures such as participation in interlaboratory proficiency testing (Aquacheck LGC) and ISO 17025 accreditation status (some methods accredited, others not).
  - Data qualifier codes explain data integrity: 10 Raw data; 11 data at or below detection limit; 12 unusual patterns requiring caution.
  - SOPs referenced (e.g., SOP 3504, SOP 3149, SOP 3115b) and method descriptions emphasize standardized procedures and QA practices.

- Metadata standards and data governance
  - Consistent, richly described metadata across analytes (form, units, LQDC, data qualifiers, preservation, filtration, and analytical method).
  - Highlights the importance of metadata completeness for comparability and transparency, including data provenance (location, method, date, and QC context).
  - Notes on data sharing: publicly sharing underlying data can be a barrier; underscores need for data governance, openness, and standardized data management at source.

- Data transformation and sampling timing
  - Sampling times link to both water samples (stream) and precipitation samples, with a volume-weighted time base to align with hydrological timing.
  - Hydrological conversions provided: converting stream flow from cumecs to mm/15min and back, using catchment areas.
  - Precipitation sampling intervals defined as 7-hour blocks; autosampler changes (7 PM–2 AM, then 12 Noon from 2007-05-01) to better align samples with rainfall/runoff intervals.
  - For first eight weeks, potential timing misalignment due to autosampler unloading; later adjustments standardized sampling boundary.

- Practical implications for monitoring framework authors
  - Emphasizes the necessity of rich, machine-readable metadata to support data integration across sites and over time.
  - Demonstrates how derived metrics (area-weighted runoff, rainfall, hourly fluxes) rely on transparent methods and timing rules.
  - Illustrates challenges in data governance: data silos, access barriers, and the need for standardized QA/QC and data-sharing policies.
  - Highlights the value of ISO 17025 accreditation and interlaboratory comparisons for establishing confidence in monitoring results.

- Notable challenges illustrated
  - Data gaps and incomplete metadata for certain analytes or entries (e.g., some LQDC or method details missing or not uniformly documented).
  - Potential data silos across sites and varying data-sharing permissions.
  - The balance between making data openly available and maintaining governance and quality controls.
  - Alignment of sampling times with precipitation events and runoff, and handling of timing uncertainties in early sampling periods.