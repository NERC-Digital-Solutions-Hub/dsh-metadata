# QGIS Generated Color Map Export File

## Overview
- A discrete color map export used by QGIS that defines 50 land-cover/class categories.
- Each entry lists an ordered index, RGBA color values, an internal class code, and a descriptive label.
- Interpolation method indicated as DISCRETE.
- Categories cover a wide range of urban, agricultural, forest, water, coastal, and other surface types, plus special codes for NODATA and UNCLASSIFIED surfaces.

## Structure and Key Details
- Each line represents a map class with:
  - An ordinal ID (1 through 50)
  - RGBA color values (red, green, blue, alpha)
  - An internal class code (e.g., 111, 112, 121, …, 995)
  - A descriptive label (e.g., Continuous urban fabric, Water bodies, Sea and ocean, etc.)
- Notable groupings include:
  - Urban and infrastructure (e.g., continuous/discontinuous urban fabric, roads, ports, airports)
  - Agricultural and semi-natural (e.g., arable land, irrigated land, vineyards, forests, grasslands)
  - Natural and semi-natural vegetation (e.g., broad-leaved forest, coniferous forest, moors, sclerophyllous vegetation)
  - Water-related (e.g., water bodies, water courses, coastal lagoons, estuaries, sea and ocean)
  - Special categories (NODATA, UNCLASSIFIED LAND SURFACE, UNCLASSIFIED WATER BODIES, UNCLASSIFIED)
- Example entries (illustrative):
  - 1 — RGBA (230, 0, 77, 255) — 111 - Continuous urban fabric
  - 5 — RGBA (230, 204, 204, 255) — 123 - Port areas
  - 23 — RGBA (128, 255, 0, 255) — 311 - Broad-leaved forest
  - 40 — RGBA (0, 204, 242, 255) — 511 - Water courses
  - 50 — RGBA (230, 242, 255, 255) — 995 - UNCLASSIFIED WATER BODIES

## Data Stewardship and Governance Considerations
- Metadata and standardization
  - This file maps 50 classes to specific RGBA colors and internally coded labels; store as part of the dataset’s color schema metadata.
  - Document the mapping between ordinal IDs, internal class codes, and descriptive labels to ensure consistent interpretation across datasets and portals.
- Provenance and transparency
  - Record that the color map is a QGIS-generated, discrete-interval legend used for visualizing land-cover classes.
  - Capture the source/version of the color map for future updates and interoperability.
- Data quality and interoperability
  - Verify that the dataset’s classification scheme matches the color map’s categories and codes.
  - Ensure downstream consumers understand that UNCLASSIFIED and NODATA entries have special meanings and should be treated accordingly in analyses and visualizations.
- Data access, updates, and governance
  - Maintain a versioned copy of this color map; note any changes to class definitions, codes, or colors.
  - Include notes on any embargoed, proprietary, or incomplete classes if applicable to datasets using this map.
- Dissemination and discovery
  - Catalogue the color map alongside the dataset(s) it applies to, linking to full class definitions and any external standards referenced (e.g., CORINE-like nomenclature if applicable).

## Practical Implications for Use
- When visualizing datasets, apply this exact color map to ensure consistent interpretation of land-cover classes.
- Use the internal class codes and descriptions to align visualizations with metadata and data standards.
- For updates, communicate changes in class definitions or colors to data users to avoid misinterpretation of legend changes.