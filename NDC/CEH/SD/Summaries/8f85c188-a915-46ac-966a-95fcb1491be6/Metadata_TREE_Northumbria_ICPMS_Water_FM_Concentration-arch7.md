# TREE_Northumbria_ICPMS_Water_FM_Concentration

## Overview
- Dataset of ICP-MS-derived water concentrations from Northumbria (UKCEH).
- Captures sample identifiers, sampling site, date, preparation notes, and multiple element concentrations (all in mg/L).
- Some concentration values may include a “less than” marker indicating censored/detection-limit values.

## Data Structure
- Metadata fields:
  - CEH_Sample_Identifier
  - CEH_Sample_Description
  - Site
  - Sampling_Date
  - Notes
- Concentration fields (elements): Al_mg_l, As_mg_l, B_mg_l, Ba_mg_l, Be_mg_l, Ca_mg_l, Cd_mg_l, Ce_mg_l, Co_mg_l, Cr_mg_l, Cs_mg_l, Cu_mg_l, Fe_mg_l, K_mg_l, La_mg_l, Li_mg_l, Mg_mg_l, Mn_mg_l, Mo_mg_l, Na_mg_l, Ni_mg_l, Pb_mg_l, Pr_mg_l, Rb_mg_l, Sb_mg_l, Se_mg_l, Si_mg_l, Sn_mg_l, Sr_mg_l, Ti_mg_l, U_mg_l, V_mg_l, W_mg_l, Zn_mg_l.
- Units for all concentration fields: mg/L.
- Explanations accompany each field (e.g., "Concentration of X in milligram per litre"). Some fields include special notation (e.g., < marker indicating a "<" value for concentrations or detection limits).

## Key Fields and Descriptions
- Sample metadata:
  - CEH_Sample_Identifier: UKCEH sample code identifier.
  - CEH_Sample_Description: UKCEH sample description.
  - Site: Sampling site name.
  - Sampling_Date: Date sample was collected.
  - Notes: Preparation notes or additional context.
- Concentration measurements:
  - For each element (Al, As, B, Ba, Be, Ca, Cd, Ce, Co, Cr, Cs, Cu, Fe, K, La, Li, Mg, Mn, Mo, Na, Ni, Pb, Pr, Rb, Sb, Se, Si, Sn, Sr, Ti, U, V, W, Zn): concentration value in mg/L, with accompanying explanation.
  - Some values may be prefixed by a "<" marker indicating a concentration below a detection limit.

## GIS-Specific Considerations
- map-ready attributes: concentration fields can be joined to a site-based GIS layer (points) or aggregated to polygons (e.g., catchments) for visualization.
- Date field enables time-enabled mapping to show concentration changes over sampling events.
- Ensure consistent join keys: CEH_Sample_Identifier and Site align with your GIS dataset.
- Handling "<" values: decide whether to treat as censored data (e.g., substitute with detection limit, use interval analysis, or flag as below-detection in maps).
- Data integration: dataset may be combined with other GIS layers (siting accuracy, hydrography, basin boundaries) to derive spatial patterns.

## Data Quality and Curation
- Data may originate from multiple sources; maintain consistent units (mg/L) and handling of detection-limit markers.
- Missing data and “n/a” items require careful treatment when producing maps or analyses.
- Large, multi-parameter dataset requires chunking or batching for processing and packaging into GIS workflows.

## Potential Map Products and Workflows
- Per-element concentration maps showing sample site locations colored by concentration level.
- Time-lapse maps or dashboards displaying concentration changes across Sampling_Date.
- Multi-parameter visualizations (e.g., stacked or facet maps) to compare elements across sites.
- Link site points to metadata (Site, Notes, Sample Description) for contextual storytelling in policy or public-facing maps.

## Practical Notes for Use
- Verify coordinate availability or join with site geolocation data for accurate spatial representation.
- Confirm and document handling of < values before visualizing (e.g., substitution rules or uncertainty annotations).
- Prepare data into manageable GIS layers (e.g., separate per-element layers or a single multi-attribute layer) to support varied audience needs.