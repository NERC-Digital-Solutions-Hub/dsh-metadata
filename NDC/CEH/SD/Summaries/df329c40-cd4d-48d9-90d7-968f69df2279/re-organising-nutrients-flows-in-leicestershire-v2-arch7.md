# Nutrient flows and stocks in the organic waste system of Leicestershire and Leicester City: A Material Flow Analysis (MFA)

- Purpose: Map and quantify how nutrients (nitrogen and phosphorus) are embedded in regional organic waste streams (green waste, food waste, slurry/manure, wastewater) to identify key sources, sinks, and opportunities for improved resource, economic, and environmental performance.

- Scope and region: Leicestershire County and Leicester City (UK); focus on wastes generated within the region; time basis uses 2019 data as the most recent pre-COVID year.

- Data formats and outputs: Sankey diagrams and an accompanying spreadsheet; nutrient contents (N, P) reported in tonnes per year; visualisations prepared with SankeyMATIC via an Excel-based data model.

- Methodological approach: Material Flow Analysis (MFA) combining raw waste quantities, processing/disposal options, outputs from processing, and nutrient contents; complemented by mass balance modelling of processing units (PUs).

- Data sources and data types:
  - Waste Data Interrogator (Environment Agency) 2019: waste received/removed, origin by Waste Planning Authority, European Waste Catalogue classifications; used to determine processing destinations with some necessary assumptions.
  - Green waste, food production/processing waste: EA-derived streams with county and city-specific destination rules; coded to determine within-region vs outside-region processing.
  - Food consumption waste: Household waste estimated from per-household tonnes and household counts; non-household waste inferred from WRAP-based estimates.
  - Slurry and manure: Defra dataset on manure volumes by livestock type and land use.
  - Wastewater: Severn Trent data (2022) adjusted to an annual average of 125 million tonnes/year; includes sludge streams and AD processes; additional septic tank sludge considered.
  - Other notes: Aimed at within-region flows; some cross-border or transfer-only streams required assumptions; run-offs and certain data gaps acknowledged.

- Stakeholder engagement:
  - First workshop (5 July 2022): identified nutrient sources, key actors, desired outcomes, opportunities, bottlenecks; helped produce a qualitative map (Figure 1.1).
  - Second workshop (Feb 2021) and follow-ups: refined technical, economic, environmental, and regulatory issues; validated data gaps and potential options for Leicestershire.
  - Result: A systematic diagram of nutrient stocks and flows to support subsequent quantitative MFA modelling (Figure 1.2).

- Key focus streams and processing units (PUs) considered in the MFA:
  - Green waste: composting, landfill, mechanical processing; in/out-of-county treatment considered with coded destinations.
  - Food production/processing waste: anaerobic digestion (AD), composting, land spreading, mechanical processing, disposal; various in-county and out-of-county destinations.
  - Food consumption waste: household and non-household fractions with assigned destinations (landfill, incineration, AD) based on regional practices.
  - Slurry and manure: on-farm application and limited off-farm destinations; nutrient contents sourced from Defra data.
  - Wastewater: municipal treatment (primary/secondary) feeding into AD and sludge management; septic tank sludge included.

- Visualisation and outputs:
  - Sankey diagrams produced to illustrate flows of raw waste streams and outputs from processing units, including N and P contents for raw streams and processed outputs (and sludges/effluents).
  - Figures cover:
    - Overall MFA system (Figure 1.5)
    - Green waste subsystem for city and county (Figures 1.6a–1.6b)
    - Food waste subsystem for city and county (Figures 1.7a–1.7b)
    - Slurry and manure subsystem (Figure 1.8)
    - Wastewater subsystem (Figure 1.9)
  - A distribution map of N and P across sources and sinks (Figure 1.10); note: N losses to N2 from wastewater treatment were excluded.

- Mass balances of waste processing units (Section 2):
  - Presents mass balance diagrams for primary PUs: anaerobic digestion (food waste and sewage sludge), composting, incineration (food waste, sewage sludge, green waste), and wastewater treatment.
  - Focus on nutrient recovery; energy flows are not depicted.
  - Data sources for PU balances include UK/Western European literature and reports (cited in Section 2 and Table 2.1).

- Limitations and caveats:
  - Data limitations: incomplete data for some streams; potential double-counting for transfer streams; some EA codes imprecise requiring assumptions.
  - PU parameters drawn from diverse literature; results reflect representative point values rather than full ranges.
  - Scope limitations: run-offs, import/export of nutrients, and chemical fertilizer inputs not included; other nutrient flows (non-waste streams) not yet integrated.
  - Future work suggested: broaden data to include additional nutrient flows and improve data resolution and standardisation.

- Practical implications for GIS and map-based data products:
  - The MFA framework provides spatially explicit mappings of nutrient stocks and flows within a defined region, suitable for map-based visualisations and scenario analysis.
  - Data sources indicate potential GIS layers for origin/destination at Waste Planning Authority levels, processing unit classifications, and nutrient concentrations by stream type.
  - The Sankey-based outputs can be paired with geospatial data to reveal spatial distribution of key flows, bottlenecks, and opportunities for nutrient circularity interventions at local scales.