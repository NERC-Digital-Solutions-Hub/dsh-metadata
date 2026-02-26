# DATA HEADER information for Standing_dead_wood_carbon_stock.csv

## Purpose and scope
- Records the carbon stock of standing dead wood.
- Associated with ESPA (Programme) and P4GES (Project); data usage requires acknowledgment to Laboratoire des Radio Isotopes, Université d'Antananarivo for derived products.

## Data provenance and references
- Programme: ESPA http://www.espa.ac.uk/
- Project: P4GES https://www.p4ges.org
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Acknowledgement required for products derived from these data.

## Variables and units
- site_ID: P4GES site code; Type = Text String.
- DBH: diameter of dead wood trunk at 130 cm height; Type = Numeric; Unit = Centimeter.
- Diam_base: diameter at 30 cm height; Type = Numeric; Unit = Centimeter.
- Diam_top: estimated diameter at the top of the trunk; Type = Numeric; Unit = Centimeter.
- Height: height of the standing dead wood; Type = Numeric; Unit = Meter.
- Volume: volume calculated; Type = Numeric; Unit = cubic metre (m^3). Calculation uses height and diameters (see Calculation method).
- Category: wood density category; Type = Categorical; Units = S (sound), I (intermediate), R (rotten).
- Density: wood density; Type = Numeric; Unit unspecified.
- Carbon_stock: carbon stock of standing dead wood; Type = Numeric; Unit = milligrams per hectare (Mg.ha-1).

## Calculation method
- Volume computed as Volume = 1/3 * π * H * (r1^2 + r2^2 + r1*r2), where:
  - H = total height
  - r1 = diameter at the base
  - r2 = diameter at the top
- Note: The specification uses radii notation but defines r1 and r2 in terms of diameters.

## Data quality and notes
- Notes indicate “means no data available” for missing values.
- Data fields include several measurements at different heights and a derived volume; potential mismatches between units (e.g., radius vs diameter) should be checked during analysis.
- Some fields (e.g., Density) have unspecified units.

## Usage considerations for analysis
- Useful for estimating standing dead-wood carbon stock across sites; volume and carbon_stock can support site-level Carbon stocks and comparisons by category.
- Consider standardising units and validating the volume formula inputs (base and top diameters vs radii) to ensure consistency.
- Pay attention to potential missing data indicated by the Notes.

## Access and reuse
- Data provenance and DOIs provided; proper acknowledgment required for derived products.
- Metadata available in the header; further dataset access details may be required for full replication and discovery.