# Land Cover Map of Great Britain (1990)

- What it is
  - A digital dataset classifying land cover into 25 classes at 25 m resolution, derived from Landsat 5 Thematic Mapper imagery.
  - Represents the first comprehensive, satellite-derived digital map of Britain's land cover and the first national land-cover map created from satellite data.
  - Used for planning, ecology, conservation, forestry, environmental assessment, water resources, urban growth, transport, telecommunications, recreation, and mineral extraction.

- Data content
  - 25 target land-cover classes (sea, inland water, bare ground, arable land, pastures/meadows, moor/grasslands, woodlands, bogs, urban/suburban development, etc.).
  - Includes an UNCLASSIFIED category (about 2% of Britain) for areas not fitted to the 25 target classes.
  - Stand-alone data products available at 25 m resolution and 1 km summary data (17 key classes).

- Classification system and usage
  - Two levels: 25 target classes (full detail) and 17 key classes (1 km data) for broader applications.
  - 25 classes are described in detail; 1 km data provides the proportion of each 1 km cell occupied by each key class.
  - The 25 classes are labeled, with a corresponding 1–to–25 mapping; the 1 km product uses A–Q as the 17 key classes.

- Methodology
  - Supervised maximum likelihood classification of Landsat TM data.
  - Uses a combination of summer and winter imagery to improve accuracy over single-date analyses.
  - Accuracy assessments acknowledge differences in class definitions and reference data; comparisons show inherent uncertainties in translating continuous landscapes into discrete classes.

- Spatial resolution, registration, and map accuracy
  - 25 m grid; features clearly resolved down to about 1 ha; finer patterns exist within larger features (e.g., roads, shelter belts).
  - Registration to 1 km vector field maps typical displacement around 0.8 pixels (~20 m); most squares required little or no shift.
  - Accuracy: ground-truth data are often unavailable or vary by methodology; overall correspondence with ground data typically 67–82%, depending on whether boundary pixels are included.
  - A realistic overall accuracy estimate is around 80–85% when accounting for class-definition differences and temporal changes (e.g., pasture ploughed or renewed between dates).

- Data access, licensing, and pricing
  - Stand-alone data available by area with licensing options ranging from single-user to corporate multi-user licenses.
  - Pricing bands: commercial, non-commercial, and research use (lower price for research); UK academics may receive further reductions.
  - Data available at 25 m resolution (full 25-class product) and 1 km resolution (17 key classes); custom aggregations or tailored datasets can be produced.
  - Licensing and data requests managed via CEH Wallingford; contact details provided.

- How to use this class description and caveats
  - Class descriptions are designed to be ecologically meaningful and consistently detectable across Britain.
  - Subclasses may be re-aggregated in GIS for specific objectives; some distinctions (e.g., grassland management) may be difficult to map consistently at this scale.
  - Land cover is not the same as land use; accuracy depends on dominant cover at imaging time and interpretations should consider potential temporal changes and generalization effects.
  - A Data Assessment Report (DAR) is provided to gather feedback and help users improve analyses.

- Applications and examples
  - Detecting changing land cover, landscape management, and environmental assessments.
  - Health-related studies (e.g., mapping bracken for tick-related research).
  - Planning for motorway extensions, telecommunication lines, forestry, and urban development monitoring.

- Appendix highlights
  - Appendix 2 provides the color mapping (RGB values) for each LCM1990 subclass, plus notes on how to interpret and display the data.

- Availability of related data
  - Mention of Land Cover Map 2000 being available, with additional information and download options via the Countryside Information System.