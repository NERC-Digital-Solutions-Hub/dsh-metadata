# Soil Map of the Moor House National Nature Reserve (1963)

- A digitized polygon dataset of soil types for Moor House National Nature Reserve, originally mapped in 1963 by the Soil Survey for the Nature Conservancy and digitized by the Centre for Ecology & Hydrology (CEH Lancaster).
- Source material: Soil Map of the Moor House National Nature Reserve (1963), Westmorland; described in Johnson and Dunham (1963).

## Data structure and provenance

- Columns:
  - SOIL (text): Description of soil type
  - SYMBOL (number): Numeric code for the soil description
- Mapping categories: Listed in the accompanying table (table on page 2 of the document); codes correspond to soil descriptions such as Red Brown Limestone, Peaty Podzol, Peaty Gley, Fell Top Podzol, Brown Earth, Blanket Bog, Valley Bog, Coarse Scree, Soil Complexes, Peaty Gley-Peaty Podzol, Peaty Podzol-Brown Earth, Solifluction Creep, Eroded Blanket Peat, Mixed Bottom Lands, Made Ground, River Tees, and Unsurveyed Area.
- Resolution: 1:10560 (approx. 6 inches to 1 mile), simplified
- Coordinate system: British National Grid
- Projection: OSGB1936 (Transverse Mercator)
- Extent: Great Britain

## Data details and contents

- Contains soil-type polygons digitized from the 1963 map.
- Includes a broad range of soil types and soil complexes (e.g., mineral soils; organic soils like Blanket Bog and Valley Bog; various podzols and gley soils; soil complexes; special categories such as Made Ground and Unsurveyed Area).
- Examples of mapped categories with codes:
  - Red Brown Limestone soils (SYMBOL 5)
  - Peaty Podzol (SYMBOL 43)
  - Peaty Gley (SYMBOL 74)
  - Fell Top Podzol (SYMBOL 53)
  - Brown Earth (SYMBOL 6)
  - Blanket Bog (SYMBOL 2)
  - River Tees (SYMBOL 4)
  - Unsurveyed Area (SYMBOL 68)

## Access, references, and related resources

- Further reading and provenance:
  - Johnson, G.A.L., and Dunham, K.C. (1963). Soil Map of Moor House, The Geology of Moor House, a National Nature Reserve in north-east Westmorland. Monographs of the Nature Conservancy No. 2.
  - Environmental Change Network (for related environmental data context): http://data.ecn.ac.uk/sites/ecnsites.asp?site=T04

## Data quality, provenance, and governance considerations

- Provenance: Based on a 1963 soil map; digitized later by CEH.
- Metadata and standards: Mapping categories and codes are defined, but detailed metadata (quality, accuracy, date of digitization, versioning) should be captured for proper governance.
- Data quality considerations:
  - Old baseline data; potential mismatches with modern standards or newer soil data.
  - Coarse resolution by modern expectations; scale corresponds to 1:10560.
  - Some areas may be marked as UNSURVEYED; these gaps need handling in analyses.
- Potential limitations for reuse:
  - Outdated land conditions may not reflect contemporary soils or land use changes.
  - Requires verification of content and format against current GIS standards.

## Implications for data strategy and use

- Data inventory and discoverability: Documentation of columns, codes, projection, and extent supports metadata completeness and data discovery.
- Data integration: Can be combined with other soil or environmental datasets to support historical analyses, change detection, or landscape-level planning.
- User needs and governance: Useful for researchers and policy colleagues needing historical soil context; ensure clear metadata, lineage, and any updates or reconciliations with current soil data.
- Data stewardship recommendations:
  - Maintain metadata detailing origin, digitization process, and any transformations.
  - Assess alignment with current data standards and consider linking to more recent soil datasets.
  - Clearly document areas of UNSURVEYED or uncertain data and planned remedies or caveats for users.
  - Facilitate data sharing within the wider data community while respecting provenance and limitations.