# Laboratory soil incubation respiration rates from permafrost in subarctic Canada

- Objective: quantify gas production rates (CO2 and CH4) with depth in soil cores from subarctic Canada under both oxic and anoxic conditions, at 5 and 15°C.
- Scope: samples from three soil cores per site, four depths per core (A–D, A is shallowest). Sites include FFU (FireFox Unburnt), FFB (FireFox Burnt), BLF (BlackFox), WHF (WhiteFox), TPP (Teslin Peatland Plateau), and TW (Teslin Wetland).
- Permafrost context: active layer and permafrost represented; TW layers labeled as permafrost in data, with peatland formed after permafrost thaw.

## Data and variables

- Spatial and site identifiers:
  - Site codes: FFU, FFB, BLF, WHF, TPP, TW.
  - Depth codes: A, B, C, D (A = shallowest; D = deepest).
  - Depth interval in centimeters (soil_depth_interval_cm).
  - Permafrost status (Permafrost column).
- Sample structure:
  - Three replicates per site (3 replicates shown in the 'replicate' column).
  - Four depths per core (A–D) across each site.
- Measured outputs:
  - CO2 production rates (mg C per day per g dry soil) from aerobic incubations.
  - CH4 production rates (mg C per day per g dry soil) from anaerobic incubations.
  - Time-based measurements: time1 and time2 CO2 (and CH4) concentrations used to compute production rates.
  - Carbon and nitrogen content: % dry mass for C and N.
- Experimental conditions:
  - Aerobic vs. anaerobic incubation.
  - Temperatures: 5°C and 15°C.
  - Moisture maintained at water-holding capacity; additional water added for anaerobic treatments.
- Equipment and processing:
  - CO2 measured with EGM-4 Infrared Gas Analyser; CH4 with DP-IR Detecto Pak.
  - Dilution corrections applied to CO2/CH4 concentrations.
  - Production rate calculations assume linear increase between time1 and time2.

## Methods and workflow (highlights)

- Sample preparation:
  - Soil mixed, top vegetation and large roots removed; mineral soil sieved to remove pebbles as needed.
- Incubation setup:
  - Aerobic: soil in plastic pots placed in 0.5 L glass jars; CO2 measured at two time points.
  - Anaerobic: jars flushed with N2; headspace sampled after incubation for CO2 and CH4 analysis.
- Data handling:
  - Concentrations corrected for jar volume via dilution corrections.
  - Rates expressed as mg C per day per gram of dry soil.
  - C and N content reported as percentage of dry mass.

## GIS-relevant data characteristics and integration considerations

- Data granularity:
  - Depth-resolved measurements (A–D) across multiple sites, enabling depth-profile mapping of respiration.
- Metadata to link spatially:
  - Site codes aligned with geographic coordinates; permafrost status annotated per depth.
  - Depth intervals (cm) and soil_layer designations (A–D) provide consistent vertical axes for 2D/3D maps.
- Derived variables for mapping:
  - Respiration_CO2_rate (mg C day−1 g dry soil) by site/depth.
  - Respiration_CH4_rate (mg C day−1 g dry soil) by site/depth (from anaerobic data).
  - Permafrost_flag per depth (yes/no) with special note for TW labeling.
  - %C and %N as baseline soil composition attributes to enrich soil property layers.
- Potential visualization approaches:
  - Choropleth or graduated symbol maps of CO2/CH4 production by site, with depth as an additional facet (e.g., small multiples by depth).
  - 3D cross-sections or vertical profiles showing gas production versus depth for each site.
  - Layered maps combining permafrost status, peatland/wetland context, and gas production rates.
- Data quality and preparation needs:
  - Ensure replicates are aggregated or summarized appropriately (mean/median) for map displays.
  - Handle TW permafrost labeling consistently to avoid misclassification in per-depth layers.
  - Confirm unit consistency (mg C day−1 g dry soil) across all records before integration.

## Use considerations and limitations

- Variability and assumptions:
  - Three replicates per site; may require aggregation for stable map representations.
  - Linear rate assumption between time1 and time2; real-world nonlinearity not captured.
- Contextual notes:
  - Permafrost status varies by site/depth; some peatland contexts involve permafrost dynamics (TW note).
  - Data reflect laboratory incubations, not in-situ fluxes; suitable for comparative visualization and modeling inputs rather than direct emission inventories.

## Applications for GIS specialists

- Create map-based data products to explore spatial and vertical patterns in soil respiration across subarctic sites.
- Combine with permafrost and peatland/wetland layers to examine relationships between permafrost status and gas production.
- Integrate C and N content as contextual soil properties to enrich interpretability of spatial visualizations.