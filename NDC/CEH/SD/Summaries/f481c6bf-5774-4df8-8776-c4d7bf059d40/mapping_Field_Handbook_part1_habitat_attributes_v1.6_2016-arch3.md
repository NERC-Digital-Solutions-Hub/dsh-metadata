# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 1: Habitat Attributes

- Purpose context
  - Every Event, Point, and Area must have a VISIT STATUS to track survey progress, access limitations, and data availability for analysis.
  - Statuses drive workflow: IN PROGRESS as a reminder to complete species data; COMPLETED only when the feature is fully surveyed; REFUSED ACCESS marks inaccessible features.

- Visit Status definitions and uses
  - 0 = unsurveyed
  - 1 = IN PROGRESS
  - 2 = COMPLETED
  - 3 = REFUSED ACCESS
  - COMPLETED should only be assigned when the entire feature is surveyed; otherwise, keep as IN PROGRESS or do not complete.
  - After finishing a square, every feature should be either COMPLETED or REFUSED ACCESS to indicate survey completeness at the square level.
  - Statuses support map-based status indicators and auditing of survey coverage.

- How to search and manage by VISIT STATUS (three main approaches)
  - Find command
    - Select layer: Landscape Points, Landscape Events, or Landscape Areas
    - Select field: VISIT STATUS
    - Enter criterion (0, 1, 2, or 3) via dropdown; typically search for 0 (unsurveyed) or 1 (in progress)
    - Pros/cons: straightforward single-criterion search; cannot search multiple criteria or multiple layers simultaneously
    - Use: features appear in a list; clicking highlights on map; right-click offers “Zoom to feature”
  - Select by Attribute
    - Similar to Find but can highlight multiple features at once and can combine criteria (e.g., 0 or 1)
    - Pros/cons: supports multi-criteria searches; more complex to configure; no automatic list
  - Attribute Table
    - Open via layer → Attributes table; apply selections; SHOW SELECTION to view results
    - Pros/cons: convenient for batch processing of a single criterion; can invert selection to find non-completed features
  - Practical tips
    - For multiple-day or river/road-divided surveys, saving and reloading search terms speeds workflows
    - If keyboard input is tedious, use the unique values option to pick 0, 1, 2, 3
    - To clear highlights, use the clear selection option
  - Operational note
    - Linears in particular can be searched with Select by Attribute to highlight ongoing or incomplete features, aiding focused completion

- Working with Minimum Mapping Units (MMUs)
  - You cannot map areas smaller than MMU; small intrusions at square edges may be left as part of adjoining polygons
  - If you need to split a small portion of a larger polygon before merging, use UPDATE (split/merge in one operation)
  - Selection and editing across MasterMap and Landscape layers
    - Use Copy+ to add areas from one layer to another during selection
    - Use Copy- to remove areas from a selection
    - Freehand drawing can be integrated by adding to the selection rather than re-drawing
  - Practical guidance
    - Combine selections from different layers to manage complex edits without creating MMU-sized features
    - MMU handling is essential to maintain data integrity during updates and merges

- Identifying Ancient (Veteran) Trees (guidance notes)
  - Definition and purpose
    - Ancient/veteran trees are old-looking trees for their species, with accompanying habitat value
    - The terms ancient and veteran are interchangeable in this context
  - Key identifying features
    - Large girth for the species
    - Substantial dead wood in the canopy
    - Major trunk cavities or progressive hollowing
    - Habitat indicators: naturally forming water pools, bark loss, decay holes, crevices, fungal fruiting bodies, epiphytic plants
    - High interdependent wildlife presence, an old appearance, and high aesthetic value
  - Girth considerations
    - Girth (measured at 1.3 m above ground) is the standard metric (DBH: diameter at breast height)
    - Species-specific thresholds exist to indicate potential ancient status; however, girth alone is not definitive
    - The table provided lists species-specific “Max girth” values and thresholds for interpretation (e.g., potentially interesting, valuable, truly ancient), with “notable” as a rule of thumb
  - Practical cautions
    - Species grow differently across conditions; a large girth does not guarantee ancient status
    - Consider multiple indicators (dead wood, cavities, age-related features) alongside girth
  - Context and references
    - Guidance reflects standard veteran-tree assessment practices (example species data and thresholds are provided)

- Implications for monitoring frameworks
  - The VISIT STATUS framework supports data completeness, transparency, and policy-relevant analysis by documenting survey progress and access
  - Multiple search and governance tools (Find, Select by Attribute, Attribute Table) enable rigorous progress tracking and quality control
  - MMU rules and Update workflows ensure spatial data integrity when editing complex polygons
  - Ancient tree guidance adds species- and feature-specific indicators to habitat assessments, informing biodiversity and heritage analyses

- Endnotes and usage reminders
  - The handbook combines practical field procedures with GIS governance to enable robust environmental health measures, policy scrutiny, and informed decision-making
  - The guidance references additional layers, fields, and pages (e.g., Linears page 124) and emphasizes integration into broader monitoring frameworks
  - Ancient trees and veteran-tree guidance illustrate how site-specific biological indicators complement broad habitat attributes in monitoring programs