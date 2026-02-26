# Errata for dataset http://doi.org/10.5285/1fb2cda3-cb49-414f-ad844a2f88ecce15

## What happened
- The dataset titled “Historic grassland survey data with contemporary spatial habitat data for semi-natural grasslands across England” has been withdrawn.
- It has been superseded by a new version titled “Historic grassland survey data with contemporary spatial habitat data for semi-natural grasslands across England v2.”

## Why the withdrawal
- Concerns raised by one author (Richard Pywell) about the high resolution of quadrat locations.
- High-resolution data could enable pinpointing exact land sites, potentially upsetting landowners.
- The dataset also contained information about the loss of important grassland habitats.

## What changed in v2
- Location precision reduced to 10km grid reference resolution (coarser spatial detail).

## Implications for analysts
- Analyses relying on precise quadrat locations will need to be adapted to the coarser 10km resolution.
- Potential impact on findings related to exact land parcel-level habitat loss.
- Need to update workflows, code, and reproducibility materials to reflect the new spatial granularity.

## Data governance and privacy considerations
- Demonstrates emphasis on protecting landowner privacy and sensitivities around habitat loss data.
- Aligns with responsible data sharing practices at larger scales or aggregated levels.

## Practical guidance for users
- Use the v2 dataset for any future work and reference the updated spatial resolution.
- Update metadata and documentation to reflect the 10km grid reference resolution.
- Reassess any decision-support or policy implications that depended on high-resolution land-area pinpointing.