# Woodland Indicators: analysis of field survey

- A field handbook for National Woodland Survey (2002) detailing methods to survey woodlands, collect data, and prepare map-based data products for GIS analysis.
- Focuses on standardized data collection, data quality, and reproducible spatial datasets across multiple plots and site descriptions.

## Scope and aims for GIS-focused work

- Create map-based data products that enable understanding and exploration of woodland features.
- Produce integrated datasets suitable for GIS visualizations and spatial analysis.
- Emphasize careful data cleaning, transformation, and verification, with documentation to support map-based interpretation.

## Planning, permissions, and logistics

- Field teams receive site/location maps, plot maps, and equipment lists; access permissions must be obtained from landowners.
- Use letters of introduction and provide landowners with copies of 1971 and 2002 results to facilitate permissions.
- Be aware of potential landscape changes since 1971 (e.g., motorways) and record changes or restricted plots accordingly.
- Safety emphasis: stay alive; plan for changing land use and access limitations; GPS use is discouraged due to potential relocation bias.

## Plot design and sampling framework

- Each site contains 16 random sampling points (plots) within a defined area; 4 datasets per plot plus one soil sample.
- The primary plot is a 14.14 x 14.14 m (200 m2) area with nested 2 x 2 m, 4 x 4 m, and larger quadrats for vegetation recording.
- Ground-truthing relies on map-based relocation rather than GPS to preserve consistency with 1971 mappings.
- A site-wide description/habitat form accompanies the 16 plots to characterize the whole site.

## Data collection per plot (datasets and recording approach)

- Vegetation plot: Ground flora
  - Record presence/absence of species in five quadrats (2 x 2 m to 14.14 x 14.14 m); identify major bryophytes; estimate % cover for the full plot to nearest 5%.
  - Use a spiral outward search from the plot center; record species in Q columns; note “Other species” as needed.
  - Distinguish ground flora from canopy; do not record bryophytes on tree bases or rocks beyond common soil habitats.
- Trees, saplings, and shrubs
  - Trees: species and DBH > 5 cm; record each stem; note dead stems with a D marker.
  - Saplings: height >130 cm but <5 cm DBH; recorded only in diagonally opposite quarters (1 NE and 3 SW).
  - Shrubs: recorded in diagonally opposite quarters; same data as trees (species, DBH if applicable).
  - Measure height of the largest tree per plot using a clinometer, hypsometer, or calibrated method; ensure horizontal distance is measured on a level contour.
- Plot description and habitats
  - Capture presence/absence of defined attributes to characterize site conditions; use defined area-based rules for features like ponds, glades, etc.; comments field for additional context.
- Soil sampling
  - Obtain a composite soil sample from the plot center (top 15 cm); label bags with site and plot identifiers; double-label to avoid mix-ups.
  - If sampling is difficult, supplement from within 1 m distance and document any deviations.
  - Bags stored in site-specific boxes and returned to the lab promptly.

## Data management, forms, and quality checks

- Four data forms per plot plus one soil sample; plus a site description form for the whole site.
  - Vegetation plot (ground flora)
  - Site description and habitats
  - Trees, saplings and shrubs
  - Plot description and habitats
- Ensure consistency between plot forms and the site form; check for logical omissions and verify site-wide coverage.
- Data entry codes are standardized (e.g., site code, plot code, and attribute codes) to enable combined site/plot analysis in GIS.
- Location relocation relies on map scale and compass-based methods rather than GPS to avoid bias.
- Complete documentation in the field supports future GIS integration and re-surveys.

## Appendices, codes, and supplementary materials

- Appendix I & II: lists of bryophytes (common across pilot woodland sites and Great Britain) for ground flora identification.
- Appendix III: tree, sapling, and shrub data structures and data recording templates.
- Appendix IV: site description and habitat attribute definitions; coding schemes; guidance on plotting and data entry, including open-ended attributes and margins.
- Appendix V: field equipment list and per-site data collection requirements.
- Appendix VI: soil laboratory protocols (pH, moisture loss on ignition, sample preparation, and calculation methods).

## Practical considerations for data products and GIS use

- The survey yields per-site and per-plot datasets that can be layered in GIS with site boundaries, plot centers, and habitat attributes.
- Vegetation, tree, and soil data provide multi-resolution inputs (plot-level and site-level) suitable for change detection, habitat mapping, and bryophyte/ground flora distribution analyses.
- The emphasis on standardized methods, rigorous relocation procedures, and detailed metadata supports reproducible, map-ready data products and long-term archives.