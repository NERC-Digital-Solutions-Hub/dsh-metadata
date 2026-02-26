# Supporting information for Pescott, O.L. (2016). A systematic florula of a disturbed urban habitat, Sheffield, England: Plant occupancy data. NERC Environmental Information Data Centre. http://doi.org/10.5285/705d6e39-9b04-497d-b8e84f617f3a6477

## Overview
- Provides supporting details for the plant occupancy data associated with a study of urban pavement habitats in Sheffield.
- Defines sampling design, field methods, data structure, and quality control to enable reuse and integration within larger biodiversity datasets.
- Covers temporal scope (2012–2014), focus on late June–early July surveys, and guidance on future resampling considerations.

## Sampling design and scope
- Target area: 1 km2 grid cells of the British National grid with at least 25% built-up land cover in the Sheffield region.
- Spatial framework: grid cells divided into four quadrants (NE, SE, SW, NW) centered on specified coordinates.
- Selection: random sampling within quadrants to choose 5 cells per quadrant; after exclusion, 16 urban 1 km2 cells were surveyed.
- Within each selected 1 km2 cell:
  - Four 500 x 500 m sub-cells with at least 50% built-up area; one sub-cell selected randomly for survey.
  - Final survey comprised 16 sub-cells across the selected 1 km2 cells.
- Field method: surveys conducted for up to 1.5 hours or until every publicly accessible street had been walked on both sides, whichever took longer.
- Habitat focus: plants recorded only if they occurred in pavement (sidewalk) habitat, including edges of paved areas, walls, grass strips, kerbstones, pavement furniture, utility installations, etc.
- Garden escapes: plants growing on pavement side of a boundary wall but rooted in a garden are recorded as “Garden escapes; surviving.”
- Temporal window: cross-sectional snapshots collected from 2012-06-23 to 2014-07-11; surveys constrained to late June and early July each year.

## Field methods and identifications
- All vascular plant species observed in the pavement habitat were recorded.
- Identification approach:
  - Field-identified by the author.
  - Specimens not identifiable in the field were keyed using Stace (2010) or vegetative keys (Poland & Clement, 2009).
  - In rare cases with insufficient material, records were assigned to genus level.

## Data structure and metadata
- Core fields and descriptions:
  - recordedName: species or aggregate as observed in the field.
  - nameAuthor: authority for the recorded name.
  - date: observation date (DD/MM/YYYY).
  - 1kmLocation: 1 km square reference.
  - 1kmQuadrant: quadrant within the 1 km square (NE, SE, SW, NW).
  - centroidEasting / centroidNorthing: centroid coordinates for the sampled sub-cell.
  - buffer (m): distance used to recreate the sampled area geometry (in metres).
  - comment: notes on observations or interpretation (e.g., presence on pavement, garden escapes).
- Data availability: ESRI Shapefile of sampling areas referenced via the report; additional metadata and data structure details provided in the supporting information.

## Quality control and provenance
- Taxonomic verification: conducted by the study author; uncertain identifications corroborated with standard flora references (Stace 2010; Poland & Clement 2009).
- Documentation: dataset includes field-derived observations with accompanying metadata to support reproducibility and re-use.
- Note on identifications: late-flowering taxa (e.g., Conyza spp.) may be identified to genus level when flowering material was insufficient for species-level determination.

## Temporal and phenological considerations
- Survey period fixed to late June–early July across all years to mitigate detectability bias due to phenology.
- Recommendation for future surveys: consider phenological shifts and potentially adjust survey timing; multiple visits outside the original window could improve species detectability.

## Limitations and considerations for reuse
- Cross-sectional snapshot limits inference about temporal dynamics; suitable for comparative assessments across time only if resampling schedule is maintained.
- Pavement habitat focus excludes plants outside the pavement microhabitat, which may be relevant for broader urban flora studies.
- Data interpretation should account for potential identification to genus for certain taxa and the single-season sampling window.

## Data use and sharing
- The supporting information complements the Biodiversity Data Journal manuscript (Pescott, In review) and should be cited accordingly.
- Users should refer to the original references for methodology and taxonomic keys used in identifications.
- Links to related data and references provided for context and interoperability with other urban flora datasets (e.g., UK Land Cover Map 2000, flora keys, and regional biodiversity resources).

## References (as cited in the supporting information)
- Fuller RM, Smith GM, Sanderson JM, Hill RA, Thomson AG (2002) The UK Land Cover Map 2000: Construction of a Parcel-Based Vector Map from Satellite Images.
- Pescott, O.L. (2016) A systematic florula of a disturbed urban habitat, Sheffield, England. Biodiversity Data Journal. In review.
- Poland J, Clement EJ (2009) The Vegetative Key to the British Flora. John Poland & BSBI.
- Smith H (2010) Value for birds of the green corridors associated with Rivers Don and Rother and their tributaries in the Sheffield Area.
- Stace C (2010) New Flora of the British Isles. 3rd Ed. Cambridge University Press.