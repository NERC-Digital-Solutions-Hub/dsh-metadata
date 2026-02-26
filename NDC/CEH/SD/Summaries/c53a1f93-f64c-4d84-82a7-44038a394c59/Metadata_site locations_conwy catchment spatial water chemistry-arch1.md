# Site_Cod Northin

- This document is a gazetteer-style listing of river/stream sampling sites identified by CC codes, with associated site names and spatial coordinates (Easting and g values, likely representing the British National Grid X and Y coordinates). Some sites have multiple sub-sites (denoted by 1/2/3) and a few entries have missing coordinate values.

## What the data contains

- For each entry: CC code, site name (often Afon or local feature), Easting, and g (northing) coordinates.
- Some entries include cross-references or additional identifiers (e.g., EA numbers such as EA25009/EA25010) linking to external datasets.
- Several sites are split into multiple sub-sites (e.g., CC66 Nant Genneth, CC14 Nant y Brwyn, CC55 Nant y Foel, CC95 Nant y Groes, CC61 Nant y Rhiw-felen, CC85 Pen-y-Clogwyn, etc.).
- A subset of entries shows missing coordinate data (e.g., CC16 Llyn Conwy) or inconsistent formatting in the sub-site entries.

## Geographic scope

- Focused on the Conwy region and surrounding catchments in North Wales, with numerous Afon (river) names such as Afon Cadnant, Afon Ddu, Afon Nug, Afon Oernant, Afon Machno, Afon Lledr, and Conwy-related locations (Betws-y-Coed area, Conwy Harbour, Conwy Morfa).
- Easting values range roughly from 271,000 to 289,100; g (northing) values range roughly from 344,000 to 378,000, indicating a Welsh National Grid coordinate framework.

## Data structure and notable patterns

- Regular entries: CC code, site name, Easting, g.
- Multi-part entries: Certain CC codes list several sub-parts (1/2/3), implying multiple sampling points within a single site area.
- Some entries include descriptive or alternative identifiers (e.g., “Pont ar Gonwy,” “Pont Eidda Stream,” “Trib of …”) indicating tributaries or specific stream features.
- Some data points reference external identifiers (EA25009/EA25010), enabling cross-linking to agency datasets.
- A few entries have missing coordinates, notably CC16 for Llyn Conwy, hindering immediate spatial placement.

## How this data can be used by analysts

- Spatial mapping and network analysis of river/stream sites across the Conwy catchment.
- Correlation and modelling efforts by linking site coordinates with environmental variables (flow, water quality, habitats) and with external datasets via EA references.
- Baseline cataloging for monitoring programs, enabling selection of sites at appropriate scales and ensuring coverage across major tributaries and confluences.
- Cross-dataset integration, once coordinate systems and missing values are reconciled, to support predictive modelling or impact assessment.

## Data quality considerations and cautions

- Missing coordinates at certain CC codes (e.g., CC16 Llyn Conwy) require imputation or source verification.
- Inconsistent formatting for multi-part entries (e.g., CC66, CC14, CC55, CC95, CC61, CC85, CC12, CC62/CC63/CC68/CC93/CC78/CC17/CC84/CC80/CC81/CC76/CC82/CC83/CC8) may need cleaning before analysis.
- Ensure consistent interpretation of the “g” value (likely northing) and confirm the coordinate reference system (presumed OSGB36 / British National Grid) before spatial analyses.
- Some entries tie to external EA codes; verify mapping and refresh links as datasets evolve.

## Example entries (highlights)

- Master Site Aber Las (CC51) — Easting 277900, g 344500.
- Afon Ddu Lower (CC11) and Afon Ddu Upper (CC10) — coordinates provided for each.
- Conwy Harbour (CC15) and Conwy Morfa (CC1) — coordinates available, supporting coastal confluence context.
- Dolgarrog bridge (CC4) and Rowen Stream (CC78) as representative stream-crossing and tributary sites.
- Tributaries/tribs: Trib of Ceunant y Garnedd (CC80), Trib of Hafod-llian (CC81), Trib of Nant Peris (CC76), Trib of Oernant (CC82), Trib of Wybrnant (CC83).
- Cross-referenced locations: Pont ar Gonwy (CC12) and Pont Eidda Stream (CC62/CC63) indicating specific river crossing points.
- Nant-focused clusters with multiple sub-sites: Nant Genneth (CC66), Nant y Brwyn (CC14/CC18), Nant y Foel (CC55), Nant y Groes (CC95), Nant y Rhiw-felen (CC61).