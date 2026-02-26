# NAIIONAL WOODLANDS CLASSIFICAIIDN 1971 HANDBOOK OF FIELD METHODS

## Overview
- A comprehensive field protocol for surveying woodlands to classify and describe habitats, vegetation, soils, and management history.
- Data products are intended to be map-based and suitable for GIS-style analysis and public/policy-facing visualization.
- Emphasizes data quality, end-user needs, and iterative refinement through feedback.

## Data Collection Framework for GIS-Focused Outputs
- Prepare an operational plan to minimize travel and align with access permissions; coordinate with regional staff.
- Obtain site access permission from landowners when required; maintain good public relations to avoid reputational risk.
- Each site is documented with a site-level description and habitat data, plus 16 plots per site, each producing multiple data layers.
- Data are captured on standardized forms and later digitized/punched; a “Code No” field exists for office data handling.

## Sampling Design and Location of Points
- Sites are located using 1" Ordnance Survey maps and site maps; 16 sampling points per site are pre-marked on the map.
- Accuracy target: locate each ground point within a 20 m radius on the ground.
- Location method:
  - Identify the next sampling point on the map (can be non-sequential).
  - Find a ground control point (e.g., road intersection) near the target point.
  - Orient the map and compass; measure a bearing to the point, adjust for magnetic variation.
  - Pace out ground distance; use predetermined paces for ground placement, with caution on slopes (>20% adjustments discouraged).
  - Mark ground to center the point with fixed corner markers; maintain consistent pace and direction to avoid bias.

## Data Collected per Site and per Plot
- Each site yields four data sets per plot (16 plots per site total) and two soil samples per plot:
  - (a) Ground flora: presence/absence in five nested quadrats (2x2 m up to 14.14x14.14 m) with % cover estimates; collect bryophytes comprehensively from vascular-plant search zones; herbarium specimens for verification.
  - (b) Trees, saplings, and shrubs: measure stems >5 cm DBH for trees; record saplings and shrubs in diagonally opposite quarters; capture species, diameter, and height metrics; mark dead or coppiced stems; measure tallest tree height with a provided instrument.
  - (c) Plot description and habitats: code-based attribute presence/absence for habitat features; provide a detailed slope/aspect profile and a ground-profile sketch.
  - (d) Soil data: small pit and auger boreings to sample top 10–15 cm plus composite topsoil; limited suite of measurements to support large-scale data handling.

## Ground Flora and Vegetation Data (GIS-Relevant Details)
- Quadrats are laid out outward from a center point; species are recorded for each quadrat size with nomenclature consistent with herbarium references.
- Bryophytes are collected but not tabulated by successive quadrat size; a full vascular-plant inventory is compiled with a separate bryophyte collection.
- After recording presence, perform a cover/abundance estimate for the full plot (14.14 m square), including litter, wood, rock, water, bare ground, and bryophytes; enter into code and cover/abundance fields.

## Tree Regeneration and Size Metrics (GIS-Relevant)
- Trees (>5 cm DBH) and saplings/shrubs are mapped by plot quarters; multi-stemmed trees are recorded as individual stems with dead/live status.
- Largest tree height per plot is recorded; use standard height tools supplied in field kit.
- Distinct categorization for coppice conditions, stumps, and signs of prior management, via standardized management attributes.

## Plot Description, Habitats, and Sketches
- Plot-level habitat attributes are captured with defined codes; a ground-profile sketch accompanies the form to illustrate major topographic and habitat features.
- Aspect and slope are measured with instrument-specified methods; a short ground-profile sketch is drawn for interpretation and GIS layering.

## Site Description and Habitats (Site-Level GIS Layer)
- A separate but related form documents site-scale habitats, marginal land use, boundary types, and surrounding land cover.
- Attributes cover site context (e.g., margins, glades, streams, ponds, roads) and help define landscape-scale GIS layers.
- The site form supports cross-linking plot-level data to broader site characteristics.

## Soil Data: Rationale, Types, and Interpretation (Important for GIS Attribute Tables)
- Due to scale, only a limited set of physical/chemical soil measurements are collected on-site:
  - pH, loss on ignition, and a simplified mechanical analysis (sand/silt/clay) with retained sub-samples for future analyses.
- Soil profiles are interpreted using horizon-based attributes (Ao, Ai, A2, B1, B2, C) and horizon boundaries:
  - Horizon identification and depth (from-to) with emphasis on reducing cumulative error.
  - Horizon-specific attributes: organic layers, leached layers, weathered mineral layers, underlying material, color, texture, structure, moisture, and rock fragments.
  - Podzolic, brown earth/brown forest, podzols, and calcareous soils are recognized as major woodland soil types; the plan acknowledges transitional and mosaic patterns.
- The soil description is designed to be compatible with numerical/descriptor-based analysis for large datasets (e.g., 1648 plots).

## Data Packaging, Documentation, and QA
- After completion, all data sheets are checked for missing items and consistency; equipment and samples are accounted for and packed for transport.
- Site-level and plot-level forms are prepared in parallel; site and plot codes are cross-checked for logical consistency.
- Herbarium specimens are prepared to enable later verification; a formal specimen policy ensures consistency across teams.

## Equipment and Data Management Considerations for GIS Integration
- Field equipment supports standardized data capture: center pole and right-angle gauge for plot layout, distance strings, compasses, tapes, diameter measurement tools, auger, mattock, trowel, and field forms.
- Data fields are highly codified (Code No, Plot No, Recorder, Date, Slope, Aspect, etc.) to facilitate data punching and GIS-ready import.
- The forms and associated appendices define how to translate field observations into structured, queryable GIS attributes (vegetation types, soil horizons, hydrology, habitats, boundary types, marginal land uses, etc.).

## Summary of End-State Outputs for GIS
- A site-level habitat map with boundary types and marginal land-use layers.
- A 16-plot dataset per site containing:
  - Ground flora presence/absence and percent cover across nested quadrats.
  - Tree regeneration metrics, DBH, height, and dead/live status.
  - Plot-level habitat and slope/aspect attributes with a ground-profile sketch.
  - Soil horizon data and limited chemical measurements (pH, LOI, texture) with horizon interpretation.
- A soil-profile-coded dataset aligned to horizon definitions (Ao, Al, A2, B1, B2, C) for each plot.
- Herbarium/specimen documentation linked to taxa identified in field forms.
- A structured, code-based dataset designed for GIS ingestion and subsequent spatial analyses, with site-to-plot linkage and robust metadata (dates, recorder initials, equipment, etc.).