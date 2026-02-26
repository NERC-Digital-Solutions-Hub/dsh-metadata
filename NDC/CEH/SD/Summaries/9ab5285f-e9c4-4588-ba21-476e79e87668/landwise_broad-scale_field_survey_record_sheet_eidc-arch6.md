# LANDWISE Broad-scale Field Survey - Record Sheet

## Overview
- A field data collection form designed to capture comprehensive, field-level information for broad-scale land surveys.
- Supports recording of site identifiers, field/plot details, land use and management, soil/geology classifications, drainage, and surface conditions.
- Intended to enable data aggregation, comparison across sites, and downstream analysis for insights on land management, soil, and hydrology.
- Includes sections for current management practices by land type, as well as observations and sampling location information.

## Data capture structure
- Records are organized by fields and plots with standard metadata (site name, field name, field/plot information, field number, date).
- Uses a mix of tick boxes and free-text fields to capture both structured and descriptive data.
- Contains two broad “General” sections: one focused on metadata and land-use/management inputs, and a second focused on surface observations and sampling location details.
- Includes both qualitative observations (descriptions of surface form, condition, erosion features) and categorical data (land use type, soil/geology class, management practices).

## Key data fields by section

- General metadata
  - Site name, Field name, Field/plot information, Date, Field no., Any unrepresentative field areas?, Last ploughed?
  - Land use and management indicators (e.g., arable with/without grass, permanent grassland, woodland)
  - Soil and geology classification (LANDWISE Soil and Geology Class)
  - Grazing history details (weeks grazing/year, last grazed, managed vs unmanaged)
  - Tillage type (conventional, minimum, none), Controlled Traffic, Tramline width/spacing
  - Tree species, Age, Path management

- Current management practices (by land type)
  - Arable, Woodland, Grassland: field drainage, buffer strips/zones, other practices
  - Grassland specifics: grass species, livestock type, stocking density (heads/ha), stock in/out wintering, mob/paddock grazing
  - Cropping and rotation details: crop types/rotation, cover crops, herbal leys
  - Management style: organic vs conventional, organic amendments, other

- Land use history and environmental context
  - Land use history, Flooding history, Waterlogged duration (>1 week/year), Water/sediment runoff, other comments

- Ground conditions and sampling observations
  - Surface form (flat/gentle/steep/undulating) and related descriptors (furrowed/mounded, etc.)
  - Surface condition (slaked/unslaked/etc.), slope shape, ponding or runoff indicators
  - Erosion features, tramline effects, poached ground, other surface observations
  - Sampling location information (add info)

## Data quality and structure considerations
- Combination of structured (tick-box) and unstructured (free-text) fields supports rich descriptive data but may require careful cleaning and standardization for aggregation.
- Repeated sections and overlapping fields (e.g., General data and surface observations) provide both metadata and detailed field condition data, enabling multilayer analyses.
- Consistency across fields (e.g., units, coding for land-use categories, soil/geology classes) is important for reliable cross-site comparisons.

## Potential data products and uses (Data Support perspective)
- Dashboards and pivot-table summaries of land use types, management practices, and drainage features by site or region.
- Maps and spatial analyses linking soil/geology class with drainage status, flood history, and surface conditions.
- Time-series or change-detection capabilities when multiple surveys exist over time (e.g., last ploughed, flooding history, management shifts).
- Self-service insights for field managers: recommended practices based on observed drainage, surface form, erosion, and land-use history.
- Data synthesis to inform policy or advisory work for local councils or private organizations, aligning field observations with management recommendations.

## Notes for effective reuse
- Ensure consistent coding for land use categories, soil/geology classes, and management practices.
- Maintain standardized date formats and field identifiers to enable reliable merging with other datasets.
- Consider augmenting with geospatial coordinates or map references for precise location-based analyses.
- QA steps should address potential ambiguities in free-text fields (e.g., wildlife or crop descriptors) and reconcile any conflicting observations.