# QGIS Generated Color Map Export File

## Overview
- A QGIS color map export for a land cover classification, using discrete interpolation.
- Associates each class with a specific RGBA color and a descriptive label (including an internal numeric code).

## Structure and Contents
- Each line defines one class: class identifier, red, green, blue, alpha, then the label with a numeric code (e.g., 111, 112, 121, …).
- Interpolation is discrete, suitable for categorical land-cover visualization.
- The catalog covers a wide range of land cover types plus special entries for data handling.

- Example categories included:
  - Urban and transportation: continuous urban fabric (111), discontinuous urban fabric (112), industrial or commercial units (121), road and rail networks (122), port areas (123), airports (124).
  - Resource extraction and waste: mineral extraction sites (131), dump sites (132), construction sites (133).
  - Green spaces and recreation: green urban areas (141), sport and leisure facilities (142).
  - Agriculture and farmland: non-irrigated arable land (211), irrigated land (212), rice fields (213), vineyards (221), fruit trees and berry plantations (222), olive groves (223), pastures (231), annual crops with permanent crops (241), complex cultivation patterns (242), agriculture with significant natural vegetation (243), agro-forestry areas (244).
  - Forests and natural vegetation: broad-leaved forest (311), coniferous forest (312), mixed forest (313), natural grasslands (321), moors and heathland (322), sclerophyllous vegetation (323), transitional woodland-shrub (324).
  - Other land covers: beaches-dunes-sands (331), bare rocks (332), sparsely vegetated areas (333), burnt areas (334), glaciers and perpetual snow (335).
  - Wetlands and water: inland marshes (411), peat bogs (412), salt marshes (421), salines (422), intertidal flats (423), water courses (511), water bodies (512), coastal lagoons (521), estuaries (522), sea and ocean (523).
  - Special and unclassified: NODATA (48) labelled 999, UNCLASSIFIED LAND SURFACE (49), UNCLASSIFIED WATER BODIES (50), and a final UNCLASSIFIED entry (990).

- Each line’s color is given as an RGBA value (red, green, blue, alpha) in 0–255.

## Special entries
- 48 - NODATA (color 255,255,255,255; label code 999)
- 49 - UNCLASSIFIED LAND SURFACE (color 255,255,255,255; label code 990)
- 50 - UNCLASSIFIED WATER BODIES (color 230,242,255,255; label code 995)
- Final UNCLASSIFIED entry (color 255,255,255,255,255; label code 990)

## Usage and Considerations for Analysts
- Useful for visualizing and communicating land cover classifications by mapping discrete class IDs to human-readable labels.
- Enables reproducible color schemes when documenting GIS workflows and reports.
- Should be used in conjunction with corresponding raster data that uses the defined class IDs; ensure alignment between raster values and these color/label mappings.
- Helps with metadata and dataset discoverability by clearly enumerating class meanings and colors.