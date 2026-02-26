# Supporting documentation for data resource Eng_Wales_SM_Surficial.csv

## Overview
- Data resource describing dry bulk density, loss on ignition (LOI), and organic carbon content of surficial soils from English and Welsh saltmarshes (2019).
- Part of the C-SIDE project funded by NERC; staff responsible: William Austin; research team across multiple universities.
- 212 surficial soil samples (top 10 cm) from 49 saltmarshes across England and Wales; sampling occurred during Jan 2018–Dec 2019. No repeat sampling planned.

## Data resource details
- Data resource name: Dry bulk density, loss on ignition and organic carbon content of surficial soils from English and Welsh saltmarshes, 2019.
- Locations: Sites across England and Wales; coordinates provided in multiple formats (decimal degrees WGS84, OSGB36 grid references, and corresponding X (Easting) and Y (Northing)).
- Site descriptors: Saltmarsh_Name; Nation (England or Wales); Year of sample collection.
- Spatial fields: Lat_dec_deg, Long_dec_deg, Grid_Reference (OSGB36), X_easting, Y_northing.
- Sampling method: 50 ml syringe used to collect soil from 10 cm depth.
- Depth: 10 cm.
- Variables/parameters observed: Dry_Bulk_Density_g_cm_3; Soil_Texture (Sandy / Not-Sandy / Organic); OC_Perc (organic carbon content, %); LOI_Perc (organic matter content, %).
- Data format: CSV file (Eng_Wales_SM_Surficial.csv) with a data resource description table listing field formats (e.g., text, numeric).

## Methods and calibration
- Laboratory and field procedures: Soil samples collected by syringe into soil, GPS locations recorded; samples frozen at -20°C prior to analysis.
- Soil texture classification: Based on Ford et al., 2019.
- Dry Bulk Density: Calculated from dry mass and sample volume after drying at 60°C for 72 hours.
- LOI: Dried samples milled, combusted at 450°C for 4 hours; mass loss used as organic matter content.
- Organic Carbon: 10 mg milled samples analyzed with Elemental Analyzer after acidification to remove carbonates.
- Calibration and QA: Elemental analyzer calibrated with Acetanilide; repeated analysis using standard (B2178) across runs; QA includes visual checks and independent classifications by four team members.
- Quality control for Citizen Science: GPS coordinates cross-checked against habitat maps; samples visually vetted to match saltmarsh characteristics; independent classification to ensure consistency.

## Data structure and GIS relevance
- Spatial coverage: 49 sites across England and Wales; suitable for mapping saltmarsh carbon stock indicators.
- Coordinate systems: Data provided in WGS84 decimal degrees and OSGB36 grid references, plus X/Y coordinates for flexible GIS workflows; enables reprojection as needed.
- Attributes suitable for maps: Dry bulk density, LOI, OC_Perc, LOI_Perc, Soil_Texture, Depth_cm, sampling year, and location metadata.
- Temporal context: Sampling period spans 2018–2019; dataset represents a snapshot with no planned repeats.

## Data resource contents (data dictionary highlights)
- Saltmarsh_Name (text): Name of the saltmarsh site.
- Nation (text): England or Wales.
- Year (number): Year of sample collection.
- Lat_dec_deg, Long_dec_deg (numbers): Geographic coordinates (WGS84).
- Grid_Reference (text): OSGB36 reference.
- X_easting, Y_northing (numbers): OSGB36 projected coordinates.
- Sampling_Method (text): 50 ml syringe.
- Depth_cm (number): 10 cm.
- Dry_Bulk_Density_g_cm_3 (number): Dry bulk density.
- Soil_Texture (text): Sandy / Not-Sandy / Organic.
- OC_Perc (number): Organic carbon content (%).
- LOI_Perc (number): Organic matter content (%).

## References and methodological sources
- Craft, C.B., Seneca, E.D. and Broome, S.W. (1991): LOI and Kjeldahl digestion methods.
- Dadey, K.A. et al. (1992): Dry-bulk density methodology.
- Ford, H. et al. (2019): Large-scale predictions of salt-marsh carbon stock (habitat and soil-type correlations).
- Kennedy, P. et al. (2005); Nieuwenhuize, J. et al. (1994); Verardo, D.J. et al. (1990): Analytical and calibration references for OC and related measurements.