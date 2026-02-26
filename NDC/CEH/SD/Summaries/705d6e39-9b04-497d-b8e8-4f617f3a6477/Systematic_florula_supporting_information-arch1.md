# Supporting information for Pescott, O.L. (2016). A systematic florula of a disturbed urban habitat, Sheffield, England: Plant occupancy data

- Study design
  - Target area: urban 1 km2 grid cells within the British National grid (OSGB 1936, EPSG 27700) that have at least 25% built-up land cover (from the Land Cover Map 2000).
  - Spatial framework: grid cells divided into four quadrants (north-east, south-east, south-west, north-west) centered at Lat 53.378493, Long -1.430239.
  - Sampling process: within each quadrant, identify urban 1 km2 cells; randomly select five cells per quadrant. Excluded four NE cells that fell in the adjacent city of Rotherham, yielding 16 sampled cells in total.
  - Within-cell sampling: each sampled 1 km2 cell contains four 500 x 500 m sub-cells with at least 50% built-up area; one sub-cell per 1 km2 is randomly chosen for survey.
  - Field survey: in each of the 16 selected 500 x 500 m sub-cells, survey conducted for 1.5 hours or until every publicly accessible street had been walked on both sides (whichever is longer).
  - Habitat focus: plants recorded only if they occur in pavement (sidewalk) habitats, including edges of paved areas, walls, grass strips, kerbstones, pavement furniture, and utility installations. Occurrences on pavement-adjacent boundaries (e.g., garden-adjacent walls) were recorded as present in the focal habitat; garden-escape occurrences are noted in the comments.
  - Temporal scope: surveys conducted as a late June to early July cross-sectional snapshot across three years (2012–2014). Late-flowering species may be identified only to genus level due to phenology and resource constraints.
  - Scope of data: includes all vascular plant species found in the target pavement habitat.

- Data structure and fields
  - recordedName: species or species aggregate as observed.
  - nameAuthor: authority for the name, when applicable.
  - date: survey date (DD/MM/YYYY).
  - 1kmLocation: 1 km square reference (lettered British National grid reference) for the sampled area.
  - 1kmQuadrant: quadrant within the 1 km square (NE, SE, SW, NW).
  - centroidEasting / centroidNorthing: coordinates of the centroid of the sampled 500 x 500 m sub-cell.
  - buffer (m): distance to recreate the sampled area footprint (in meters); an ESRI Shapefile of these areas is available via Pescott (In review).
  - comment: notes relating to species occurrence observations (e.g., pavement-only, boundary cases, etc.).

- Quality control and identification
  - All plants were identified by the author in the field.
  - Specimens that could not be named in the field were identified using standard references: Flora for Britain and Ireland (Stace 2010) or vegetative keys (Poland and Clement 2009).
  - In cases with insufficient material for confident identification, specimens were recorded to genus level.

- Additional information and references
  - See the main Biodiversity Data Journal article by Pescott (2016) for full interpretation and context.
  - Related references include Fuller et al. (2002) on the UK Land Cover Map 2000; Poland and Clement (2009) The Vegetative Key to the British Flora; Stace (2010) New Flora of the British Isles; Smith (2010) value of green corridors; among others.