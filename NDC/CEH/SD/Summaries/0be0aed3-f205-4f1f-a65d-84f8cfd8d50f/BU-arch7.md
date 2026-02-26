# RABBITS AND DEER

- Purpose: Monitor broad changes in rabbit and deer populations (Oryctolagus cuniculus; red deer Cervus elaphus; roe deer Capreolus capreolus) using an index based on dropping counts to infer relative abundance and detect trends over time (e.g., post-myxomatosis dynamics).
- GIS relevance: Data are collected along predefined transects and organized into sampling locations and sections, suitable for spatial mapping, layering with habitat types, and temporal analysis.

## Spatial design and data structures

- Transect framework:
  - Use the existing ECN butterfly transect (IB) extended to 2 km; add a second transect to cover major habitat types not encountered on the butterfly transect.
  - Transects divided into sections (up to 15) based on discrete habitat types or management differences; transect length recorded per section.
- Geographic identifiers:
  - Sampling locations identified by Site Identification Code, Core Measurement Code, and Location Code; each ECN Site assigns codes for replicates.
  - Data are linked to ECN Site metadata and may be transferred via ECNCCU documentation.

## Sampling schedule and field methods

- Timing: Late March and late September each year.
- Method: Count rabbit and deer droppings along transects after clearing a 1 m strip two weeks prior; counts are recorded for each transect section.
- Habitat and segmentation: Each transect (and the second transect) is subdivided; the habitat type for each section is described and recorded.
- Data granularity: Separate records maintained for each section of each transect; zero counts are important for longitudinal comparisons.
- Species differentiation: Ensure accurate distinction between droppings of rabbits, deer, and any sheep present.

## Data collection and field methods (GIS workflow)

- Recording and documentation:
  - Two recording forms: one for droppings and one for lengths and habitat types; the habitat form is used in the first year and when habitat changes occur.
- Consistency: Transect sections are numbered sequentially across both transects to remain unique within an ECN site.

## Data schema and recording conventions

- Core schema (first four identifying fields required for every sample/recording):
  - Site Identification Code (e.g., T05)
  - Core Measurement Code (e.g., PC for a specific core measurement)
  - Location Code (e.g., 01)
  - Sampling Date/time (including time if sampling is more frequent than daily)
- Core measurement: vertebrates – rabbits and deer (BU Protocol)
  - Fields per sampling location/section: Number of rabbit droppings, Number of deer droppings
  - Spatial attributes: Transect section length; Habitat description (units as character code)
  - Recording dates: Date droppings cleared; Date droppings recorded (sampling date)
- Data capture details:
  - Separate records for each transect section and for each transect
  - Reporting precision: Dropping counts with specified recording precision (e.g., 0.1)

## Recording forms and workflow

- Form 1: Droppings counts by transect section
- Form 2: Lengths and habitat types by transect section
- Use: First year of survey or after habitat changes; number of transect sections depends on habitat pattern at each site

## Data integration, sharing, and standards

- Data transfer and formats: Refer to accompanying Data Transfer documentation for ECN dataset formats; available on the restricted access Site Managers' extranet.
- Access and contact: ecnccu@ceh.ac.uk for access to documentation and datasets.

## Practical GIS considerations

- Data layers to create:
  - ECN Site polygons (sites), transect lines, and transect section polygons/segments with attributes.
- Key attributes to maintain:
  - Site ID, Location Code, Transect ID, Section Number, Section Length, Habitat Description, Droppings counts (rabbit and deer), Dates cleared and recorded.
- Quality and consistency:
  - Maintain unique section identifiers across both transects within each ECN site.
  - Track habitat changes and ensure forms are updated accordingly.