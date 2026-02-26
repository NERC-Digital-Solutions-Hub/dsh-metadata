# WildCrickets01-BasicTraits Description of content

- This dataset provides basic information on each adult tagged cricket in the population for a defined set of traits.

## Field definitions

- Year: Year when the cricket was alive.
- Tag: Two-character code identifying the cricket in video recordings; read from a plastic tag on the pronotum.
- Sex: Male (M) or Female (F).
- Emerged: Date when the cricket emerged as an adult (may be empty if unknown).
- Tagged: Date when the cricket was caught and tagged.
- Dead: Date of death or, if death is not recorded, the last observation date.
- ThoraxWidth: Width of the thorax, measured from an above-view picture.
- BodyMass: Mass of the cricket at the date of tagging.
- Monitored: Number of days the individual has been under observation.

## Data quality and governance considerations

- Some fields may be missing (e.g., Emerged), so handle missing values appropriately.
- Ensure consistent date formats across all time fields (Tagged, Emerged, Dead).
- Document measurement methods (e.g., ThoraxWidth from images) and units for reproducibility.
- Maintain unique Tag identifiers and link records to video data or source observations.
- Track data provenance and any transformations (e.g., image-based measurements) for auditability.
- Establish update and curation workflows to keep records current (e.g., new death date, additional tagging events).

## Data stewardship implications

- Include metadata describing data collection context, measurement procedures, and data quality checks.
- Define access and sharing policies, especially regarding longitudinal observations and any derived metrics.
- Provide clear data discovery aids (datasets, fields, units) to ensure usability by researchers and other data users.

## Potential uses

- Longitudinal analyses of growth, survival, and life-history traits.
- Investigations of relationships between emergence timing, body size, and mortality.
- Cross-referencing with video records via Tag identifiers for richer behavioral studies.