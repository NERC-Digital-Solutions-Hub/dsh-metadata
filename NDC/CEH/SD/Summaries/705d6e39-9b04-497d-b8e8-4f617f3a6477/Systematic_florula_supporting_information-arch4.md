# Supporting information for Pescott, O.L. (2016). A systematic florula of a disturbed urban habitat, Sheffield, England: Plant occupancy data. NERC Environmental Information Data Centre.

## Overview
- Provides the supporting methodology and data structure for the plant occupancy study in a disturbed urban habitat in Sheffield.
- Emphasizes sampling design, field collection of pavement-habitat vascular plants, data fields, and quality control.

## Sampling design and scope
- Target area: urban 1 km2 grid cells within the British National grid that have at least 25% built-up land cover (as per the Land Cover Map 2000).
- Division: each 1 km2 cell subdivided into four 500 x 500 m sub-cells (quadrants).
- Selection: within the Sheffield area, five 1 km2 cells per quadrant were randomly selected; four cells in the NE quadrant near Sheffield that fell into the neighboring city of Rotherham were excluded, leaving 16 cells sampled.
- Within each selected 1 km2 cell: all four 500 x 500 m sub-cells with at least 50% built-up area numbered; a single sub-cell chosen for survey via random selection.
- Survey effort: 16 sub-cells surveyed for 1.5 hours or until every publicly accessible street had been walked on both sides, whichever took longer.

## Field data collection and habitat focus
- Habitat targeted: pavement (sidewalk) habitat; includes plants rooted at edges of paved areas (e.g., walls, kerbs, grass strips, pavement furniture, utilities).
- Boundary garden escapes: plants observed on the pavement-side of boundary walls but rooted in adjacent gardens are recorded as present.
- Temporal window: field surveys conducted in late June to early July across 2012–2014.
- Species identification: all vascular plants recorded; late-flowering species (e.g., Conyza) may be identified to genus if flowering phenology limited precise ID.
- Note on future work: recommends re-surveys accounting for potential phenological shifts due to climate changes.

## Data structure and fields
- RecordedName: species or species aggregate as observed.
- nameAuthor: authority for the scientific name.
- date: observation date (DD/MM/YYYY).
- 1kmLocation: lettered British National grid reference for the sampled 1 km square.
- 1kmQuadrant: which 500 x 500 m sub-cell within the 1 km square was sampled.
- centroidEasting / centroidNorthing: coordinates of the centroid for the sampled sub-cell.
- buffer (m): distance to buffer and square off sampled areas to recreate the survey geometry; ESRI shapefile provided in related materials.
- comment: notes related to species observations (e.g., garden escapes, habitat context).

## Quality control
- All plants identified by the author.
- Specimens that could not be named in the field were keyed using Stace (2010) or vegetative keys (Poland & Clement, 2009).
- In some cases, insufficient material led to genus-level identifications.

## Data provenance and related materials
- Refer to Pescott (in review) Biodiversity Data Journal for additional interpretation and context.
- Supporting references include: Fuller et al. (2002) UK Land Cover Map 2000; Poland & Clement (2009) The Vegetative Key to the British Flora; Smith (2010); Stace (2010) New Flora of the British Isles.

## Implications for data reuse
- Provides a transparent, reproducible sampling framework for urban pavement flora with explicit spatial and temporal scope.
- Metadata includes precise location, sampling units, and data fields to facilitate re-analysis or integration with broader urban biodiversity datasets.
- Limitations include the restricted survey window and the potential for genus-level identifications in late-flowering cases, which should be considered in secondary analyses.