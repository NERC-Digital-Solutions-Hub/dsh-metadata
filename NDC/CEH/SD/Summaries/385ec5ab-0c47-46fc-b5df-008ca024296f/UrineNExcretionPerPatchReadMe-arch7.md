# UrineNExcretionPerPatch.csv ReadMe

- Project and provenance
  - Project: Uplands-N2O
  - Grant number: NE/M015351/1
  - Authors: Karina A Marsden; Lucy Lush; Jon A Holmberg; Mick J Whelan; Andrew J King; Rory P Wilson; Alice F Charteris; Laura M Cardenas; Davey L Jones; Dave R Chadwick
  - Usage note: If data are reused, please ensure it is fully cited.

- Purpose and scope
  - Describes a dataset of daily nitrogen excretion associated with urine patches from replicate sheep.
  - Data were filtered to remove zero urination events and two replicate sheep (sheep 1 and 5) due to infrequent urine events.
  - Daily N excretion estimates assume the 10:00–16:00 collection window represents a 24-hour period.

- Data structure and key fields
  - Site: Semi-improved or improved pasture
  - Season: Spring, Summer, or Autumn at the semi-improved site; Autumn at the improved site
  - Sheep_ID: Identifier for the replicate sheep
  - Date: Date of urine collection (dd/mm/yyyy)
  - Vol_ml: Volume of each urine event (milliliters)
  - NContent: Nitrogen concentration in urine (g N per liter)
  - Nexcreted: Total nitrogen excreted per urine event (g N)

- Data processing notes
  - Zero-urination observations were excluded.
  - Two replicates with infrequent events were removed (sheep 1 and 5).
  - Daily excretion calculation normalized to a 24-hour period using the typical collection window (10:00–16:00).

- GIS-relevant guidance
  - Geospatial application: Use Site to assign patches/polygons (semi-improved vs. improved pasture) and join with spatial layers of fields or paddocks.
  - Visualization: Create map-based representations of Nexcreted by site type and season (e.g., choropleth or heatmaps).
  - Temporal analysis: Use Date and Season to explore seasonal patterns of N excretion across patches.
  - data integration: Link with additional GIS layers (land use, grazing management, rainfall) to analyze drivers of spatial variation in N excretion.

- Limitations and considerations for mapping
  - Spatial coordinates are not provided; require linkage to site-level polygons to map locations.
  - Extrapolation assumes the collection window reflects 24-hour excretion, which may introduce uncertainty.
  - Filtering decisions (removal of zero events and certain replicates) may affect representativeness.

- Reuse and citation guidance
  - Provide full citation of the project and authors when reusing the data.