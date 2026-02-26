# Soil Core Dataset Variables and Descriptions

- Overview
  - A data dictionary for soil core samples capturing treatment status (biochar amendment and wetting) and a suite of soil health indicators measured before and after incubation. Designed to support monitoring, evaluation, and policy decisions around soil management practices.

- Key variables and meanings
  - soilcorenumber: Unique identifier for the soil sample/core.
  - treatmentfullname: Full name of the soil treatment (biochar and wetted).
  - treatmentnamenowet: Full name of the soil treatment (biochar) without the wetting component.
  - shorttreatmentname: Shortened treatment name.
  - biocharamendment: Indicator of whether the sample is un-amended or amended with biochar.
  - temperature: Soil temperature at the time of measurement.
  - pH.water: Soil pH in a water extract at a 1:2.5 ratio.
  - total.C.percent: Total carbon content of the soil (percent).
  - total.N.percent: Total nitrogen content of the soil (percent).
  - CN ratio: Carbon to nitrogen ratio in the soil.
  - extract.nh4-n.mgkg: Extractable ammonium (mg/kg).
  - extract.no3-n.mgkg: Extractable nitrate (mg/kg) after the start of incubation.
  - bulkdens.after.mix.gcm3: Bulk density immediately after mixing (g/cm3).
  - bulkdens.fortydays.after.mix.gcm3: Bulk density 40 days after mixing (g/cm3).
  - WFPS.field.moist.proportion: Water-filled pore space under field-moist conditions (proportion), calculated from gravimetric water content, bulk density, and total porosity.
  - WFPS.after.wetting.proportion: Water-filled pore space immediately after wetting (proportion).

- Units and calculations
  - Temperature: unspecified unit (typically degrees Celsius in soil studies; note to verify).
  - pH.water: pH unitless.
  - Total.C.percent, Total.N.percent, CN ratio: percentage and ratio values.
  - extract.nh4-n.mgkg, extract.no3-n.mgkg: milligrams per kilogram.
  - bulkdens.after.limit: g/cm3.
  - WFPS fields: proportion (0–1).

- Treatment and experimental design context
  - Enables comparisons between biochar-amended and unamended soils, and between wetted versus non-wetted treatments.
  - Captures temporal change in bulk density and nutrient availability, aiding assessment of physical and chemical soil health responses to amendments.

- Data quality, access, and governance considerations for monitoring frameworks
  - Metadata completeness: Ensure all variable definitions, units, and calculation methods are fully specified.
  - Data availability and timeliness: Potential barriers due to data silos or restricted access; need for openness where possible.
  - Dataset standardization: Harmonize units and calculation methods to facilitate cross-site comparisons.
  - Data provenance and quality assurance: Require documentation of QA/QC steps, data cleaning, and versioning.
  - Data transformation needs: Some fields (e.g., WFPS calculations) depend on underlying gravimetric water content, bulk density, and porosity; clear transformation rules are essential.
  - Governance and sharing: Balance between sharing underlying data and any confidentiality or proprietary concerns; ensure responsible data sharing and governance processes are in place.

- Relevance for policy evaluation and decision-making
  - Provides concrete, measurable soil health indicators to evaluate the effectiveness of biochar amendments and moisture management.
  - Supports dashboards, reports, and policy-focused analyses on soil physical, chemical, and nutrient dynamics under different management strategies.