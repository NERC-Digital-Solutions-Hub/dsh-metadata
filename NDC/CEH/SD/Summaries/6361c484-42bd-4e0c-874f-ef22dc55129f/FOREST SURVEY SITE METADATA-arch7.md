# Forest Planting and Harvest Records

- Dataset comprises numerous spatial records (identified by codes like A1, A2, A7, B3, C17, D32, etc.) with map coordinates (Easting/Northing) and detailed planting histories.
- Each record tracks a site’s planting events, including species, soil type, and harvest history, enabling GIS-based analysis of forestry activities over time.

## Spatial and Temporal Coverage

- Spatial data are provided as Easting/Northing coordinates (likely OSGB-style grid) for many forest plot locations.
- Temporal range covers early 20th century planting (e.g., 1930s–1940s) through at least 1990s (e.g., Year felled up to 1995–1997 in multiple records).
- Harvest status varies: some records indicate standing crops (not yet felled), others show felled years, and many include second planting events.

## Data Model and Key Fields

- Core fields per record:
  - Location: Easting, Northing
  - First planting: year; species
  - Soil type: e.g., Gley (PG), Podzol (PIP), Bog, Brown earth
  - Year felled: year or term like Standing crop
  - Year of second planting and Second planting species
  - Start date and End date fields (multiple entries per site; often split into Day/Month/Year components or numeric placeholders)
- Data entries show repeated patterns (A1, A2, …, B3, C17, D32, E44, etc.) with variations in planting cycles and harvest status.
- Some fields contain NA or unclear date components, indicating incomplete data or placeholder values.

## Species and Soil Type Distribution

- Predominant species: Sitka spruce appears most frequently.
- Other species present: Western hemlock, Norway spruce, Japanese larch, Scots pine, Lodgepole pine, Douglas fir, Noble fir, and others.
- Soil types frequently appearing: Gley (PG/SWG), Podzol (PIP/IIP), Bog, Brown earth.
- Some plots show changes in species across second plantings (e.g., second planting species different from first).

## Planting History Patterns

- Many sites have a defined first planting year and species, followed by a possible second planting year and different species in some cases.
- Harvest indicators vary: some sites are recorded as standing crops (not yet felled), others show felled years (e.g., 1988–1995 range), and some have updated second plantings after felling.
- Several sites include explicit second-planting events in the mid-to-late 1990s, suggesting cycling planting regimes.

## GIS Preparation and Use

- Suitable for creating a GIS layer of forest plots with:
  - Point features using Easting/Northing coordinates
  - Attributes for planting history (first/second planting years and species), harvest status, soil type, and start/end dates
- Potential analyses:
  - Temporal visualization (timeline of planting and harvest)
  - Species distribution mapping
  - Soil-type associations with planting cycles
  - Age calculations (e.g., Year felled minus First planting year) where data is complete
- Data normalization steps:
  - Standardize soil type nomenclature (e.g., consolidate Podzol/IIP vs PIP variations)
  - Resolve ambiguous Start/End date entries (convert to consistent date fields)
  - Handle NA values and document data gaps

## Data Quality, Gaps, and Considerations

- Incomplete data: numerous records have missing second planting years or NA values for some fields.
- Date fields sometimes contain non-standard values (e.g., single numbers for Start date or End date) requiring interpretation or cleaning.
- Some records report ongoing or standing crops, while others reflect historical harvests; careful handling is needed to avoid misinterpretation in temporal analyses.

## Practical Guidance for GIS Workflows

- Import as a point layer with the coordinates; ensure the coordinate reference system matches OSGB or the dataset’s native grid.
- Create derived fields to enhance analysis:
  - Age at felled (Year felled - First planting year) when both are available
  - Second-planting interval (Year of second planting - First planting year)
  - Categorical encoding for harvest status (Standing crop vs Felled)
- Build a time-enabled layer to visualize changes over time (planting and harvest events).
- Standardize and harmonize:
  - Soil type labels
  - Species names (e.g., Sitka spruce vs Sitka Spruce)
  - Date formats across Start/End fields
- Validate spatial clustering and cross-check with adjacent plots to detect potential coordinate misplacements.

Note: This dataset appears tailored for GIS-based exploration of forestry planting histories, emphasizing spatial context, temporal dynamics, and multi-species/a multi-planting lifecycle analysis.