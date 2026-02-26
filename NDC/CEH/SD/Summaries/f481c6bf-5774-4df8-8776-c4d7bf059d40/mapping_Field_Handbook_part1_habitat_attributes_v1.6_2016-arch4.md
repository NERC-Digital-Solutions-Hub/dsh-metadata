# Glastir Monitoring & Evaluation Programme Mapping Field Handbook Part 1: Habitat attributes

## Visit status: purpose and meanings
- Each Event, Point, and Area includes a VISIT STATUS field to indicate survey progress and access restrictions.
- Status values:
  - 0: unsurveyed
  - 1: IN PROGRESS
  - 2: COMPLETED
  - 3: REFUSED ACCESS
- REFUSED ACCESS marks areas you cannot survey; IN PROGRESS acts as a reminder to return and complete species assignments; COMPLETED should only be used when the feature is fully mapped.
- Completed status helps ensure the whole square is surveyed; every feature should be either COMPLETED or REFUSED ACCESS when a square is finished.
- Status presence will influence layer coloring and searchability; the system provides several ways to search by VISIT STATUS across Landscape Points, Events, and Areas.

## Tools and methods to search and manage VISIT STATUS
- FIND command (binocular icon):
  - Choose the relevant layer and VISIT STATUS field; search by the numeric value (0, 1, 2, 3).
  - Features matching appear in a list; selecting a feature flashes it on the map; right-click for “Zoom to feature.”
  - The Find window can stay open during edits; changes to VISIT STATUS remove items from the list automatically.
- SELECT BY ATTRIBUTE:
  - Similar to Find but highlights all matching features on the map; can search for multiple criteria (e.g., 0 and 1) simultaneously, but does not produce a list.
  - Build queries by selecting layer, field, and criteria; apply to see highlighted features.
- ATTRIBUTE TABLE:
  - Opens a table of features; you can show and select items from the table, applying criteria there.
  - Useful for working through a list, though typically limited to one criterion at a time.
- Practical tips:
  - Save frequently used search terms for quick re-use, especially when surveying different sub-areas divided by rivers or roads.
  - Use the “use unique values” option to quickly access 0, 1, 2, 3 in dropdowns.

## Dealing with MMUs (Minimum Mapping Units) and editing
- No mapping for features smaller than MMU; occasionally you must handle partial overlaps carefully.
- If a small corner of a larger area intrudes into your square, include it in the adjoining polygon; if it’s the end of a long linear feature, leave it.
- To split/merge polygons without losing data:
  - Use UPDATE to split/merge in one operation, preserving field data.
  - You can copy selections from Mastermap or other layers and add to selections (Copy +); similarly remove with Copy -.
  - You can combine freehand drawing with layer-derived selections to manage complex edits.

## Identifying Ancient and Veteran Trees
- Definition: Ancient vs. veteran trees are trees that look old relative to others of the same species; terms are interchangeable in this guidance.
- Key indicators beyond age:
  - Very large girth for the species
  - Large amounts of dead wood in the canopy
  - Major trunk cavities or hollowing; signs of hollowness
  - Epiphytic plants, fungi, decay features, bark loss
  - Evidence of long-term management (pollarding, historic form) or cultural/historic value
  - Health and structural stability indicators and the tree’s prominent landscape position
- Girth and measurement:
  - Measure DBH (diameter at breast height) typically at 1.3 meters above ground.
  - Girth thresholds are species-specific; tables provide minimum girth values and categorizations (potentially interesting, valuable, truly ancient).
  - Girth alone is not definitive: growth conditions, management (e.g., pollarding), and look/age indicators must also be considered.
- Practical guidance:
  - Use girth as a guideline, not sole criteria; assess overall old-looking characteristics.
  - Acknowledge that some species and forms may not fit neatly into thresholds (especially pollarded or damaged trees).
  - Species-specific guidance exists to help categorize trees and determine their conservation value.

## Practical field data governance notes
- VISIT STATUS directly supports Data Leaders’ aims by enabling clear tracking of survey progress, access limitations, and completion status across the dataset.
- The combination of status fields and multiple search tools supports efficient data curation, quality checks, and timely updates, aligning with needs for an interoperable, user-responsive data system.
- Inclusion of ancient/veteran tree criteria and species-specific girth guidance enhances data richness for biodiversity, heritage, and landscape history analyses, while maintaining caution about over-reliance on single metrics.