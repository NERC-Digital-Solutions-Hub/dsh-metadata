# Supporting information for the dataset: UK Environmental Change Network (ECN) Cairngorm Spider Data 2004-2019 Andrews, C. and Dick, J. Sept. 2021

## Overview
- Supporting documentation for the ECN spider dataset (2004–2019).
- Spiders collected from pitfall traps in three habitats within the Allt a'Mharcaidh catchment, Cairngorms National Park, Scotland.
- All specimens identified by a single expert araneologist to ensure consistency.
- Related data analysis report (Andrews et al., 2020) details methods and temporal trends; protocols available via ECN resources.

## Location and study design
- Location: Allt a'Mharcaidh catchment (57° 6' 28"N, 3° 50' 6"W), Cairngorms National Park, Scotland.
- Elevation: 320–1111 m above sea level; area ~10 km²; includes part of Invereshie and Inchriach NNR.
- Transect focus: west-facing slopes north of the catchment; three habitat types sampled between 460 m and 690 m a.s.l.
- Habitats:
  - I. Woodland transect at 460 m a.s.l. in mature Scots Pine woodland.
  - II. Heath transect at 690 m a.s.l. in dry heath (Calluna-Cladonia) with bare ground patches.
  - III. Bog habitat at 690 m a.s.l. blanket mire (Eriophorum vaginatum and Molinia caerulea).

## Sampling protocol
- Each habitat: 100 m transect with 10 pitfall traps, 10 m apart.
- Trap design: polypropylene pots (75 mm × 105 mm) buried flush with ground, 30 mm depth ethylene glycol; 20 mm² galvanized mesh to deter small vertebrates; 140 mm rain cover with ~30 mm gap to ground.
- Sampling frequency: Fortnightly from April to end of October, start date depends on snow-free conditions.
- Sample processing: Spiders within each habitat collected as a single composite sample; all specimens identified to species and sex by the same araneologist; specimens stored at UKCEH Edinburgh for future research.
- Data products: Long-format CSV providing detailed temporal, spatial, and taxonomic information.

## Data structure and metadata
- Data format: Long-format CSV with fields including:
  - Year (YYYY), Date (DD/MM/YYYY), Month (MMM), Week (2-digit)
  - Habitat (Bog/Heath/Wood), Transect (e.g., T1), Transect age (Old pre-2007 or New post-2007)
  - Taxonomy: Family, Species
  - Counts: Male, Female, Total (male+female)
- Purpose: Enables species- and habitat-level analyses across years, with consistent taxonomy and sampling units.

## Quality control and data considerations
- Transects relocated from 2007 onward; 2007–2008 included overlap where both old and new transects ran simultaneously.
- Datasets labelled to indicate which transect data belong to Old vs. New configurations.
- Sampling periods per year vary (snow and weather can shorten/shift sampling); standardization should use the interval between first and last trapping dates rather than raw sampling effort.
- Traps remain in-place even if sampling dates are missed, allowing calculation of annual trapping effort.

## Data storage and accessibility
- Specimens stored at UKCEH Edinburgh for future research.
- Data and methods are anchored by a dedicated methods page and the 2020 data analysis report; external reference and data provenance are documented.

## Related resources and references
- Andrews, C., Snazell, R., Dick, J. (2020). Temporal trends in spider communities at the UK Environmental Change Network Cairngorm field station, 2007-2019: data analysis report. UK Centre for Ecology & Hydrology.
- Protocols and additional methodological details available via ECN measurements pages and the associated eprint links:
  - http://nora.nerc.ac.uk/id/eprint/529051/
  - http://www.ecn.ac.uk/measurements/terrestrial/i/ia
  - http://nora.nerc.ac.uk/id/eprint/528208

## Governance and stewardship notes for data stewards
- Ensures data standardization by:
  - Consistent sampling design across habitats and years where possible.
  - Uniform taxonomic identification by a single expert.
  - Clear documentation of transect changes and data labeling to support long-term use.
- Metadata completeness and discoverability:
  - Provides a comprehensive data dictionary (column definitions, formats, units implied by field types).
  - Includes provenance, storage location, and related publications for contextual understanding.
- Actionable recommendations:
  - Maintain explicit versioning for dataset over time, particularly around transect relocations (Old vs. New).
  - Retain detailed protocol documentation and links to protocols for reproducibility.
  - Preserve the relationship between the dataset and the accompanying analysis report to aid users in interpreting temporal trends.
  - Ensure updated metadata continues to reflect any future changes in sampling design or storage practices.