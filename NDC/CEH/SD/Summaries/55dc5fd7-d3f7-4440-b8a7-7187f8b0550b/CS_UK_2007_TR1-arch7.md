# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Purpose and scope
  - Field mapping methodology for Countryside Survey CS2007, focusing on habitats and landscape features on a digital GIS map.
  - Emphasizes mapping habitat extent and change (BH/PH) to support time-series biodiversity reporting at country and UK scales.
  - Data are captured in CS Surveyor (ArcMap extension) with editing of Areas (polygons), Lines (linear features), and Points (point features).

- Key feature: Woody Linear Features (WLFs) – attributes and coding
  - Unnatural shape / line of stumps – Yes/No
  - Height, base canopy height categories (Height of base of canopy)
    - Categories include: <1m, 1-2m, 2-3m, >3m, 3-4m, 4-6m, >6m
  - Base height note: Height of base of canopy
  - Species composition – Mixed species; >50% hawthorn; >50% other
  - Evidence of management – 1 = no recent management; newly planted; cutting (<3 yrs); laying or coppicing (<5 yrs); both preceding
  - Line of stumps – Yes/No
  - Vertical gappiness – % breaks from canopy to ground; categories: <10%, 10-<25%, 25-<50%, 50-<75%
  - Margin Left / Margin Right – categories include not present and width ranges (e.g., <2m, 2m-<4m, 4m-<6m, 6m-<12m, 12m-20m)
  - Staked trees – Yes/No
  - Tree protectors – Yes/No
  - Note: If base height >2m, check trimmed or cut woody species to maintain desired shape; natural shape should be recorded if appropriate
  - The section includes illustrated examples and consistent code schemes to classify WLFs across photographs

- Line editing workflow (CS Surveyor)
  - Create New Line – within square, minimum scale 1:5000; minimum length 5.0 m; cannot cross itself; lines cannot extend outside the survey square; new line starts with an Unsurveyed/Missing Data event
  - Modify Line – edit line shape by moving vertices; end vertices of shared boundaries are edited via Shared Node Modify; must avoid creating self-intersections
  - Shared Nodes – modify node positions to move adjoining lines; lines move with node; caution to prevent new intersections
  - Cut Line – digitize a cut polygon along the line; show length removed vs remaining; edits must result in valid line length
  - Reshape Line – use a reshape line to alter an existing line; must intersect at beginning and end; can be performed after editing
  - Reshape following a copied line – follow a copied follow line to reshape the target line; requires intersection with the target and the copied boundary
  - Copy Tool – import external polygon shapes (e.g., OS Mastermap) to refine the cut line edit sketch; can combine features into the edit sketch
  - Delete Line – delete only when all events have a valid Reason for Change; scale must be 1:5000 or less; single-line deletions
  - Checking and managing line visits – use Select By Attributes to identify unvisited lines (VISIT_STATUS = 0); blue highlighting for unvisited lines
  - Loops and data integrity – loops in the dataset may contain corrupted event data; apply a defined procedure to mark as Deleted Feature, set Visit Status to Completed, and recreate the line as needed

- General rules for mapping lines and areas
  - MMU (minimum mappable unit) is 1/25 ha; smaller patches are not mappable unless part of a larger unit
  - For each habitat type, record multiple component attributes (e.g., trees, shrubs) and ensure two to four species per polygon/component when possible
  - Spatial accuracy is secondary to accurate habitat extent; maintain consistency across 1km squares for time-series analyses
  - mosaics and patch descriptions – use explicit component-level descriptions with percent covers that sum to 100%
  - Ponds – identify every pond within a square; select one survey pond for detailed condition assessment; ponds mapped with dedicated protocol

- Pond mapping protocol and attributes
  - Record every pond in the square on the CS2007 Pond Mapping Recording Sheet
  - One survey pond per square selected for condition assessment; selection uses preselected lists or randomization if needed
  - Ponds defined as standing water from 25 m2 to 2 ha, typically present for at least four months
  - Attributes to capture for each pond include polygon ID, area, presence of water, reason for loss/creation, and notes
  - Post-mapping, survey ponds are handed to freshwater surveyors for condition assessment
  - The form supports tracking ponds from CS2000 and documenting changes (loss reasons, creation reasons)

- Points and Woody Linear Features (Points and Lines)
  - Points include trees and standing water features; each point may have multiple components
  - Points editing requires scale ≤ 1:5000
  - Woody Linear Features (WLFs) – attributes as described above; lines support events (e.g., fence types, hedge management)
  - Line events have minimum length requirements and carry event-specific attributes

- Non-specific and other habitat attributes
  - Record primary attributes such as bare ground, signs of drainage, and non-native species where relevant
  - Orchards are to be recorded as Priority Habitats (PHs) and can be part of curtilages or recorded separately

- Data structure and practice notes for GIS practitioners
  - Emphasize accurate extent and change of habitat rather than pin-point spatial precision
  - Adhere to MMU guidelines and ensure habitat types change triggers creation of new polygons
  - Maintain consistency across all survey squares to support time-series analysis and UK-wide reporting
  - Use predefined keys, templates, and codes to standardize data capture across surveyors
  - Documentation and references (FABs, CS2000 notes) are available to assist interpretation when needed

- Appendix references and context
  - The handbook includes detailed appendices and examples for WLFs, veteran trees, and loops, as well as historical CS2000 field assessment practices
  - The CS2007 framework integrates with prior CS1990/CS2000 practices to support evolving habitat classification and attribute schemas

- Practical guidance for GIS teams
  - Follow the CS Surveyor workflow to ensure data integrity and time-series compatibility
  - Validate editing operations with end-of-session saves; ensure reasons for change are properly recorded
  - Maintain consistent attribute templates and coding schemes to enable UK-wide biodiversity reporting and historical comparisons