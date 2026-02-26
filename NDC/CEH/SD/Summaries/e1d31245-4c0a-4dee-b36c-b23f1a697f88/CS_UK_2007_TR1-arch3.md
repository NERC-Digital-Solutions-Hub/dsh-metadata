# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Purpose and scope
- Provides methodology for mapping and monitoring habitat types and landscape features to inform policy and decision-making.
- Focuses on Broad Habitats (BH) and Priority Habitats (PH) with a digital, time-series approach.
- Aims to integrate multiple themes (forestry, agriculture/natural vegetation, boundaries/structures/physiography) and support policy-relevant insight.

## Data model and mapping units
- Surveys cover 1 km square units; data captured as polygons (areas), lines (linear features), and points (point features) in GIS.
- Minimum Mapping Unit (MMU) is 1/25 hectare (400 m2); smaller areas generally not mapped as separate units.
- For each habitat type, primary and secondary attributes are recorded; supports reporting of extent and change.
- Post-survey GIS masks constrain PH/BH ranges by upland/lowland; nesting PHs within BHs where applicable.

## Broad Habitats and Priority Habitats (BHs and PHs)
- BHs cover major ecosystem types with woody vs non-woody classifications; PHs are finer-scale habitats nested within BHs.
- BH examples include woodland types, boundaries/linear features, arable lands, various grasslands, wetlands, aquatic/linear features, urban and coastal elements.
- PHs are mapped where possible; some rare or scattered PHs supported by prior data; national extents constrained by data availability.

## Keys: Vegetation Key and Woodland Types/Features Key
- Vegetation Key: assigns polygon-level BH/PH attributes based on species composition and vegetation cover; guides attribute decisions.
- Woodland Types/Features Key: classifies woody vegetation by canopy-based categories and woody features (e.g., belts, lines, clumps, hedges); supports mosaics within polygons and guides attribute application.

## The digital mapping system: CS Surveyor and ArcMap
- CS Surveyor is a custom ArcMap extension enabling field capture of habitats/features with predefined attribute schemas.
- Workflow constraints:
  - Editing requires map scale ≤ 1:5000; emphasis on accurate habitat extent rather than exact positional accuracy.
  - Change recording is mandatory when editing areas/lines/points.
- Editing capabilities cover areas, lines, and points with comprehensive attribute management and governance requirements.

## Field survey methods and change management
- Change mapping distinguishes genuine ecological change from data corrections (REAL vs ERROR changes).
- Reconciliation of older CS1990/CS1998 data with CS2007 data for unenclosed habitats; newer baseline data for enclosed habitats.
- A decision framework determines if a change is real, an error, or a new baseline/subdivision.

## Pond and water body mapping
- All ponds in each square identified and recorded on Pond Mapping Recording Sheets.
- A survey pond is selected for in-depth condition assessment; some ponds from CS2000 may be used where applicable.
- Ponds defined as standing water 25 m2 to 2 ha, typically water-covered for at least 4 months/year; special handling for temporary ponds and connected water bodies.
- Post-mapping, freshwater surveyors conduct detailed pond condition assessments.

## Points and woody features (WOODY) methodology
- Points capture landscape elements smaller than 20x20 m (trees, scrub, ponds, etc.).
- Veteran trees: up to 10 per square (max 2 per species) with detailed attributes.
- Buffer zones, species data, DBH, and proportion documented; features mapped as points or areas depending on size/context.

## Woody Linear Features (WLFs) and margins
- WLFs include hedges, lines of trees, belts, scrub, fences/walls, and other woody linear elements.
- Distinguishes natural-shaped lines from managed hedges; gaps >20 m mapped as separate sections or individual trees.
- Large-width lines (>5 m) may be belts or broader linear features; margins and event attributes recorded.

## Ecological classifications and attribute structure
- Primary attributes structured within themes (Inland Physiography, Inland Water, Coastal Features, Forestry, Agriculture/Natural Vegetation, etc.).
- Habitats/features have mandatory and optional attributes focused on presence/absence, proportion, canopy cover, species, and habitat indicators.

## Wales expansion and time-series considerations
- CS2007 adds 60 new squares in Wales to enable country-level habitat reporting.
- Methods designed to maintain consistent time-series for policy-relevant comparisons over time.

## Data quality, sharing, and governance
- Outputs are designed for open sharing with governance to support policy monitoring and environmental health assessment.
- Emphasis on metadata quality, data management, and governance to ensure datasets meet standards and are up-to-date and properly stored.

## Practical workflow notes for practitioners
- Plan surveys to capture BH/PH extents, change status, and habitat attributes per square.
- Use Vegetation Key and Woodland Types/Features Key for accurate classification.
- Map digitally with CS Surveyor; follow MMU and editing constraints.
- Record comprehensive attributes for areas, lines, and points (species, cover, structural attributes).
- Identify survey ponds and complete pond mapping; select a pond for detailed assessment.
- Maintain rigorous change logs, distinguishing REAL changes from ERRORS, and update baselines as needed.
- Ensure data openness and reuse with appropriate metadata and governance.