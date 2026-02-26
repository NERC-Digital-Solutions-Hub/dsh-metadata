# MicroCT 3D scans from Passer sparrows - house ( Passer domesticus) , Spanish ( Passer hispaniolensis) , and Italian ( Passer italiae) sparrows and F1 hybrids generated during a crossing experiment at the University of Oslo, Norway in 2014/2015.

## Aim and scope
- Provide a morphometric dataset of skulls from three sparrow taxa and their F1 hybrids for analyses of shape and size.
- Enable comparison across species and hybrids, using 3D landmarks and Procrustes-based shape analysis.

## Data collection and generation
- Samples originate from the Natural History Museum of Oslo under a material transfer agreement.
- Scanned with a high-resolution X-ray Waygate Technologies v|tome|x M 240kV CT system (26 μA) at the Hounsfield Facility, University of Nottingham, UK.
- Skulls rotated on a polystyrene mount; projections produced, yielding ring artefacts mainly on the braincase dorsal area. Artefacts were not significantly detrimental to data quality.
- Initial outputs included .TIF images and 3D reconstructions; .VOL files rendered for visualization and analysis in Avizo 9.1.0.
- For geometric morphometrics, 20 landmarks in 3D were digitized three times per individual in Avizo; the mean coordinates were used for analysis.
- Landmark placement was limited to the right side (sagittal plane) to avoid shape redundancy, leveraging presumed bilateral symmetry.

## Data processing and analysis
- Landmark coordinates were organized in a 3D array in R and aligned using Partial Generalized Procrustes Analysis (GPA) via the gpapgen() function in geomorph.
- Procrustes steps:
  - Translate to a common centroid
  - Scale so centroid size = 1.0
  - Rotate to minimize Procrustes distance
- After alignment, shape is defined as geometric information excluding scale, location, and rotation; size is captured by centroid size (the square root of the sum of squared landmark distances from the centroid).
- All configurations are analyzed in tangent space after superimposition.

## Data structure and formats
- Primary data are STL files (stereolithography) describing triangulated 3D skull surfaces with recorded landmark coordinates.
- Each STL file represents a single individual.
- Data also include generated 3D landmark coordinates (averaged across three replicate digitizations) used for subsequent morphometric analyses.

## Metadata and identifiers
- Metadata linked to each STL file includes species, sex, and location of capture.
- Filenames encode identity; examples include:
  - 2019-1.stl (Species = P. domesticus × P. hispaniolensis; Sex = M; Location = badajoz, Spain)
  - HYB-10.stl (Hybrid, stem indicates cross lineage; Location = badajoz, Spain)
  - HTE-01.stl / HTE-09.stl (P. domesticus; Location = oslo, Norway)
  - MAS_60.stl / MAS-66.stl / etc. (P. italianiae; Location = puglia, Italy)
- The metadata table provides consistent fields: Species, Sex, Location; filenames correspond to individual STL files.

## Quality control
- Average landmark coordinates were inspected for placement errors and corrected where needed to ensure consistency across specimens.

## Potential uses and limitations
- Analysts can investigate:
  - Morphological differences in skull shape and size across species and hybrids
  - Allometric patterns and shape variation related to sex or geographic origin
  - Procrustes-based analyses to quantify shape differences and perform multivariate testing
- Limitations and considerations:
  - Ring artefacts were present but deemed not to meaningfully affect analyses
  - Data are limited to right-side landmarks and a predefined 20-landmark configuration
  - Uneven sample distribution across taxa and locations may influence comparative analyses

## References
- Gower, JC (1975) Generalized Procrustes analysis, Psychometrika, 40, 33-51.
- Baken, E., Collyer, ML., Kaliontzopoulou, A., & Adams, DC (2021) geomorph v.4.0 and gmShiny: Enhanced analytics and a new graphical interface for a comprehensive morphometric experience, Methods in Ecology & Evolution, 12, 2355-2363.