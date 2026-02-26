# Loch Leven long-term monitoring data

## Purpose and scope
- Long-running data collection from Loch Leven, Scotland, begun in 1968, describing lake chemistry, Secchi depth, and crustacean/zooplankton densities as part of UK-SCAPE WP7 LEVEN.
- Aimed at producing map-based data products and facilitating spatial analyses of lake conditions over time.
- Outputs described, including data processing steps and the CSV storage format for GIS-ready use.

## Sampling design and sites
- Fortnightly sampling regime with two main sites per occasion: Reed Bower (RB) and Sluices/Outflow (L); Harbour (H) is also referenced when describing locations.
- Site identifiers and coordinates (UK National Grid, EPSG:27700):
  - Harbour (H): Easting 312251, Northing 701670
  - Reed Bower (RB5): Easting 313568, Northing 701141
  - Sluices / Outflow (L/Sl8): Easting 317004, Northing 699380
- Sampling access:
  - Reed Bower: boat-based, integrated water-column sample possible.
  - Sluices: boat or shore-based access.
- Occasional constraints (weather, ice, resources) may prevent sampling at one or both sites.

## Measurements and data types
- In situ measurements: conductivity, pH, temperature (and Secchi depth measured at Reed Bower).
- Water samples collected at each site for laboratory analyses:
  - Soluble reactive phosphorus (SRP), total soluble phosphorus (TSP), total phosphorus (TP)
  - Soluble reactive silicate, total diatom silica
  - Chlorophyll a
- Physical and chemical parameters presented as determinands with site-specific columns in the dataset.
- Crustacean and zooplankton dataset:
  - Densities (ind/L) of multiple taxa (e.g., Daphnia, Eudiaptomus, Cyclopidae, Bosmina, Leptodora, Bythotrephes, Chydoridae, Polyphemus pediculus)
  - Two sampling locations (Reed Bower and Sluices)
  - Preservation and counting procedures described; counts converted to densities per litre.

## Data processing and quality assurance
- Data processed with an R import script that:
  - Handles wind force values (e.g., "4-5" uses the first value)
  - Applies median absolute deviation (MAD) filtering to replicate measurements (conductivity, pH, DO, and related temperatures)
  - Converts pH values for MAD calculations (log transformations) and back to pH units
  - Rounds results (pH/DO to 2 dp; conductivity/temperature to 1 dp)
  - Maintains continuity across instrument models (HQ30d vs HQ4300) by using a single column naming convention for this dataset
- Quality assurance:
  - Automated and manual checks for data entry errors and out-of-range values
  - Investigations and corrections of unusual values as needed

## Data format and structure
- Stored as a single CSV file with descriptive column names, including site, determinand, units, and location context.
- Missing data represented as NA.
- Column descriptions (examples):
  - Date, Week_of_Year, Water_Level_cm_Site_H
  - Cloud_cover_Eighths_Site_RB, Wind_Direction_Site_RB, Wind_Force_Beaufort_scale_Site_RB
  - Depth_m_Site_RB, Secchi_m_Site_RB
  - Conductivity_µS/cm_Hach_HQ30d_Site_RB, Temperature_°C_Hach_HQ30d_(cond)_Site_RB
  - DO_mg/L_Hach_HQ30d_Site_RB, DO_%_Hach_HQ30d_Site_RB, pH_Hach_HQ30d_Site_RB
  - TP_ugP/l_Site_RB1, SRP_ugP/l_Site_RB1, TSP_ugP/l_Site_RB1, chla_ug/l_Site_RB1
  - Zooplankton taxa densities (ind/L) for multiple site/taxa combinations
- Column naming and content are designed to support GIS-oriented data joins by site, date, and determinand.

## Geographic and spatial context
- Clear geospatial anchors for map-based analyses via UK National Grid coordinates.
- Site locations enable spatial visualization of environmental gradients and long-term trends across Harbour, Reed Bower, and Sluices.
- Data suitable for creating site-level choropleth maps, time-series overlays, and integration with other GIS layers (e.g., land use, hydrology).

## Applications and considerations for GIS use
- Ideal for visualizing long-term lake water quality and zooplankton dynamics across discrete lake sites.
- Can be combined with other spatial layers (e.g., meteorological data, shoreline changes) to explore drivers of ecological change.
- Mind the sampling gaps due to weather or access when interpreting maps and interpolations; data completeness varies over time.
- Two datasets (water chemistry and crustacean/zooplankton) provide a rich basis for multi-layered GIS analyses and policy-relevant visualizations.

## Methods and references (for GIS data provenance)
- Measurements and nutrient analyses based on standard methods (Murphy & Riley 1962; Wetzel & Likens 2000; Golterman et al. 1978).
- Zooplankton identification and counting procedures follow established taxonomic references (Dussart & Defaye 1995; Einsle 1996; Flößner & Kraus 1986; Harding & Smith 1974; Scourfield & Harding 1966).
- Additional readings available in Hydrobiologia and related Scottish Natural Heritage reports.