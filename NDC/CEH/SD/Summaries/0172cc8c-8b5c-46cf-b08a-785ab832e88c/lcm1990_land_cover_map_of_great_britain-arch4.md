# Land Cover Map of Great Britain (1990)

- What it is
  - A digital dataset classifying land cover into 25 classes at 25 m resolution, derived from Landsat 5 Thematic Mapper data.
  - First comprehensive, satellite-based, national land-cover map for Great Britain; supports planning, ecology, conservation, forestry, water, urban development, transport, recreation, and mineral extraction.

- Data, methods, and accuracy
  - Method: supervised maximum likelihood classification using Landsat TM data; combines summer and winter imagery to improve accuracy.
  - Accuracy: about 88% for combined-summer/winter classifications; 12% from single-date data; cloud and offshore island gaps noted (0.4% cloud-covered, ~0.1% offshore islands missing).
  - Spatial aspects: ~25 m grid; features around 0.125 ha (two pixels) or larger; registration accuracy ~0.8 pixels (20 m) when aligned to vector field maps; overall accuracy estimated around 80–85% after accounting for definitional and temporal differences.
  - Limitations: misclassification of mixed boundary pixels; differences in class definitions vs. ground truth; time-based changes between surveys; unclassified areas (about 2%) noted.

- Classification scheme (25 target classes + UNCLASSIFIED)
  - A Sea/Estuary; B Inland Water; C Coastal Bare Ground; D Saltmarsh; E Rough Pasture / Dune Grass / Grass Moor; F Pasture / Meadow / Amenity Grass; G Marsh / Rough Grass; H Grass / Shrub Heath; I Shrub Heath; J Bracken; K Deciduous / Mixed Wood; L Coniferous / Evergreen Wood; M Bog (Herbaceous); N Tilled Land (Arable Crops); O Suburban / Rural Development; P Urban Development; Q Inland Bare Ground; UNCLASSIFIED (0).
  - In 17-class outputs, some categories are aggregated (e.g., open shrub heath with moor; shrub/heath groupings).

- Data formats and access
  - Stand-alone datasets: 25 m resolution; or 1 km resolution summary data in 17 key classes.
  - 1 km data presents the proportion (integer percentage) of each 1 km cell comprised of each key class (A–Q); bands correspond to the key classes.
  - Licensing and pricing: three bands—commercial, non-commercial, and research; potential reductions for UK academics; corporate/multi-user licenses available; custom licensing options possible.
  - Availability: data for any area of Great Britain under Licence; contact CEH Wallingford for orders and licensing details.

- Data usage and applications
  - Applicable across agriculture, ecology, conservation, forestry, environmental assessment, water supply planning, urban expansion, transport, telecommunications, recreation, and mineral extraction.
  - Example applications: detecting changing land cover; mapping bracken for health studies; environmental assessments for motorway extensions; planning telecom lines.
  - Data can be linked with other GIS layers and requires consideration of whether to treat land cover as proxy for land use.

- Practical notes for data governance and use
  - Recognize that land cover does not directly determine land use; accuracy depends on dominant cover at imaging time.
  - Ground-truth data are limited; comparisons across studies depend on differing definitions and objectives.
  - Data use guidance and feedback are encouraged via a Data Assessment Report (DAR) form.

- Related updates and resources
  - Land Cover Map 2000 is available; sample 1 km data accessible online; full data downloadable via the Countryside Information System data download site.
  - Appendix 2 provides color mappings for visualization of the 25 classes.

- Additional considerations for data leaders
  - The dataset supports developing a data strategy for large-scale, cross-sector land-cover information with clear licensing, discoverability, and versioning processes.
  - Understanding class definitions and potential need for regional/local masks (e.g., lowland vs. upland distinctions) can aid in consistent application across networks and partner organizations.