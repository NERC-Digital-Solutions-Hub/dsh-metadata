# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Purpose and scope
- Establishes a geographically comprehensive field-mapping framework for Countryside Survey CS2007.
- Aims to report change over time for Broad Habitats (BH) and Priority Habitats (PH), including upland unenclosed habitats.
- Supports country- and UK-level reporting with a digital, time-series data model and cross-square/year change analysis.

## Data model and classification
- Two-tier habitat framework: Broad Habitats (BH) and Priority Habitats (PH); PH nests into BH and may be recorded anew in 2007.
- Outputs include polygons (areas), lines (linear features), and points (discrete features); explicit rules for when to split, merge, or mosaic habitats.
- Detailed woodland and non-woody classifications:
  - Vegetation Key informs BH/PH allocation (composition, canopy indicators).
  - Woodland Types Key aids in classifying woody vegetation (e.g., Belt of trees, Clump of trees, Woodland/Forest).
- Metadata elements cover buffers, veteran trees, and other contextual attributes.

## Data capture system and governance
- CS Surveyor: ArcMap-based extension for field data capture, editing, and management.
- End-to-end data governance: logging edits, tracking change (REAL vs ERROR), audit trails, and ensuring consistency across squares and time.
- Change provenance: reason-for-change fields; mandatory documentation of alterations; Save Session workflow to ensure data integrity.

## Data structure and themes
- Data organized around landscapes with landscape feature editing tools:
  - Areas (polygons): assign BH/PH, edit attributes, determine change, manage components, apply baselines.
  - Lines (linear features): manage events (fences, hedges), modify shape, copy attributes, record margins.
  - Points (discrete features): record individual trees, ponds, buildings, buffers, and components.
- Thematic domains for attributes include Inland Physiography, Inland Water, Agriculture/Natural Vegetation Use, Forestry (including Forestry Features and Forestry Use), Structures, Recreation, and Coastal features where applicable.

## Methodology and mapping rules
- Minimum mapping unit (MMU) of 1/25 hectare (400 m2); polygons below this size are not mapped unless representing a discrete habitat unit.
- Habitat composition within polygons described via components; mosaics allowed with percentage covers summing to 100%.
- Change assessment:
  - REAL change: genuine habitat/attribute change since previous survey.
  - ERROR: correction of earlier misclassification.
- Post-survey GIS masks delimit PH/BH extents (upland vs lowland) for PH reporting and extent estimates.

## Pond and freshwater mapping
- Every square requires pond identification and basic attributes; one survey pond per square for detailed condition assessment.
- Preselected pond lists used when available; random selection if needed.
- Dedicated pond definitions, boundaries, and delineation guidance to ensure consistent pond identification across surveys.
- Pond data are central to the Inland Water theme with a pond mapping sheet and sampling workflow.

## Field keys and woodland attributes
- Vegetation Key drives primary BH/PH allocation; includes species composition and canopy indicators.
- Woodland Types Key supports classification into types (e.g., Belt of trees, Clump of trees, Woodland/Forest).
- Additional attributes cover buffer zones and veteran trees (up to 10 per square; max 2 per species).

## Data quality, provenance, and governance
- Emphasizes extent and change accuracy over pinpoint spatial precision; correct attribution and extents are prioritized.
- Encourages integration of multiple data sources (CS1990, CS1998, CS2000) to support PH allocations and refine habitat details.
- Preserves data provenance through reason-for-change fields, component-level editing, and strict merge/split rules.
- Mandatory documentation of reasons for change; Save Session workflows to maintain traceability.

## Veteran trees and species data
- Records up to 10 veteran trees per square (max 2 per species) with detailed attributes (buffer zones, metrics, epiphytic species).
- Tree and shrub data captured within Forestry theme; includes modal DBH and species-specific attributes.

## Practical guidance and support
- Extensive operational detail for using ArcMap/CS Surveyor, including interfaces, toolbars, editing workflows, and error handling.
- Support channels (helpdesk and wiki) provided for field issues and methodology updates.

## Implications for Data Leaders (data strategy and governance)
- Delivers a single digital, time-series data model enabling cross-square and cross-year habitat change analysis and reporting.
- Emphasizes data discoverability, reusability, and collaboration across networks through standardized keys, attributes, and governance rules.
- Requires ongoing coordination to apply GIS masks, reconcile old datasets with new classifications, and maintain PH/BH delineations over time and geography.
- Highlights robust data quality processes, change tracking, and clear metadata to support policy and biodiversity monitoring.

## Key challenges for data leadership
- Managing data gaps and granularity limitations in unenclosed upland habitats; ensuring consistent PH allocations post-survey.
- Coordinating data across partners and networks to maintain consistent classifications and data sharing practices.
- Balancing detailed biological attribute recording with field workload and MMU constraints; keeping methodology/tools up to date with user feedback.

## Endnotes and appendices (processing and implementation)
- Appendix coverage includes pond surveying, random-number tables, field assessment references (FABs), and tools for point/linear/polygon edits.
- Pond recording sheets and CS2007 pond mapping procedures are detailed, including selection of survey ponds and recording formats.
- Additional references to CS2000/CS1990 datasets and earlier field-handling methods provided for continuity and provenance.