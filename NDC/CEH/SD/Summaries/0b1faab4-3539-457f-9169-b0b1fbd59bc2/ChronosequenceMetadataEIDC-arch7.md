# Soil biochemical measurements from saltmarshes of different ages on the Essex coast, UK 2011

## Overview
- Dataset describing soil biochemical properties across a chronosequence of saltmarshes on the Essex coast, UK.
- Focuses on natural salt marshes, restored salt marshes, breached sites, and fields on former salt marsh.
- Designed for GIS-ready analysis of spatial and temporal patterns in soil chemistry and composition.

## Spatial and temporal scope
- Chronosequence spanning 16 to 114 years since restoration/breach of tidal flow.
- Sampling locations include:
  - Restored and accidentally breached salt marshes with grid references and ages to 2011 (16–114 years).
  - Natural salt marsh sites with grid references.
  - Fields on former salt marsh with grid references.
- Sampling dates:
  - October 2011 (salt marshes).
  - July 2010 (Tollesbury field samples).
  - April 2017 (Barrow Hill, Wallasea Island, Brandy Hole fields/natural sites).
- No planned repeat sampling.

## Sampling design and methods
- Field sampling:
  - Salt marshes: 4 sampling locations per marsh; randomly selected away from edges.
  - Fields on former marsh: 2–6 locations per site.
  - At each location, 3 soil cores (4 cm diameter, 30 cm length).
- Laboratory analyses (per core):
  - Bulk density, moisture content, pH, electrical conductivity (EC).
  - Organic matter content via loss on ignition (LOI) at 375°C.
  - Available ammonium (NH4+) and total oxidised nitrogen (NO3−) by 1M KCl extraction; colorimetric analysis.
  - Total soil carbon (C) and nitrogen (N) by combustion.
  - Below-ground biomass to 30 cm depth estimated from root material after washing and drying.
- Moisture content determined by weight loss after drying at 105°C.

## Data structure and formats
- Primary CSV datasets:
  - Saltmarsh_Chronosequence_data_2011.csv
  - Saltmarsh_Chronosequence_data_2010_2017.csv
- Data quality and provenance:
  - Data checked for outliers; no repeat sampling planned.
  - Calibration procedures aligned with CEH Bangor practices; equipment calibrated accordingly.
- Header and field descriptions provided to support GIS use:
  - SiteName, SiteCode, BulkDensity (g cm−3), MoistureContent (%), pH, Conductivity (mS cm−1), NO3-N (TON mg N g−1), NH4-N (mg N g−1), OrganicMatter (% LOI), BelowGround (kg m−2 to 30 cm), Carbon (%), Nitrogen (%).
  - Notes indicate missing data where samples were lost or not analysed; blank cells indicate missing data.

## Site details (spatial and contextual)
- Restored and breached salt marsh sites (with grid references and age since breach to 2011):
  - Tollesbury, Orplands, NortheyMR, Barrow Hill, Ferry Lane (B), Wallasea Island, Northey Island, North Fambridge, Brandy Hole (ages 16–114 years; varied breach years and grid refs).
- Natural salt marsh sites (with grid references):
  - Tollesbury Natural, Orplands Natural, Northey Natural, Barrow Hill Natural, Ferry Lane (B) Natural, Wallasea Island Natural, North Fambridge Natural, Brandy Hole Natural.
- Fields on former salt marsh (with grid references):
  - Barrow Hill Field, Wallasea Island Field, Brandy Hole Field, Tollesbury Field.
- Grid references are provided as Easting/Northing coordinates to enable GIS mapping.

## Data quality, standards, and references
- Quality control:
  - Data checked for outliers; notes indicate missing data due to sample loss or non-analysis.
- Calibration and methods references:
  - Laboratory practices aligned with CEH Bangor.
  - References: Avery & Bascombe (1974) for EC and pH procedures; Ball (1964) for LOI as a measure of organic matter/organic carbon.

## Key uses for GIS Specialists
- GIS-ready variables suitable for spatial analyses and visualization:
  - Soil physical and chemical properties by site and depth (0–30 cm).
  - Spatial relationships between natural, restored, breached marshes, and former marsh fields.
  - Temporal dimension via the 16–114 year chronosequence anchored to grid-referenced sites.
- Supports map-based data products showing spatial gradients, site comparisons, and changes over time.