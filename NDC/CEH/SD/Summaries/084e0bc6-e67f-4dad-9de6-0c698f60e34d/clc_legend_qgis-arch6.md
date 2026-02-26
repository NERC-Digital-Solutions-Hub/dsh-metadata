# QGIS Generated Color Map Export File

## Overview
- A discrete color map export for QGIS that links land-cover class codes to specific RGBA colors and descriptive labels.
- Designed to be used as a styling reference to enable consistent, self-serve visualization of classified spatial data.

## Key Class Mappings
- Code 111: Continuous urban fabric — Color (230, 0, 77, 255)
- Code 112: Discontinuous urban fabric — Color (255, 0, 0, 255)
- Code 121: Industrial or commercial units — Color (204, 77, 242, 255)
- Code 122: Road and rail networks and associated land — Color (204, 0, 0, 255)
- Code 123: Port areas — Color (230, 204, 204, 255)
- Code 124: Airports — Color (230, 204, 230, 255)
- Code 131: Mineral extraction sites — Color (166, 0, 204, 255)
- Code 132: Dump sites — Color (166, 77, 0, 255)
- Code 133: Construction sites — Color (255, 77, 255, 255)
- Code 141: Green urban areas — Color (255, 166, 255, 255)
- Code 142: Sport and leisure facilities — Color (255, 230, 255, 255)
- Code 211: Non-irrigated arable land — Color (255, 255, 168, 255)
- Code 212: Permanently irrigated land — Color (255, 255, 0, 255)
- Code 213: Rice fields — Color (230, 230, 0, 255)
- Code 221: Vineyards — Color (230, 128, 0, 255)
- Code 222: Fruit trees and berry plantations — Color (242, 166, 77, 255)
- Code 223: Olive groves — Color (230, 166, 0, 255)
- Code 231: Pastures — Color (230, 230, 77, 255)
- Code 241: Annual crops associated with permanent crops — Color (255, 230, 166, 255)
- Code 242: Complex cultivation patterns — Color (255, 230, 77, 255)
- Code 243: Land principally occupied by agriculture with significant areas of natural vegetation — Color (230, 204, 77, 255)
- Code 244: Agro-forestry areas — Color (242, 204, 166, 255)
- Code 311: Broad-leaved forest — Color (128, 255, 0, 255)
- Code 312: Coniferous forest — Color (0, 166, 0, 255)
- Code 313: Mixed forest — Color (77, 255, 0, 255)
- Code 321: Natural grasslands — Color (204, 242, 77, 255)
- Code 322: Moors and heathland — Color (166, 255, 128, 255)
- Code 323: Sclerophyllous vegetation — Color (166, 230, 77, 255)
- Code 324: Transitional woodland-shrub — Color (166, 242, 0, 255)
- Code 331: Beaches - dunes - sands — Color (230, 230, 230, 255)
- Code 332: Bare rocks — Color (204, 204, 204, 255)
- Code 333: Sparsely vegetated areas — Color (204, 255, 204, 255)
- Code 334: Burnt areas — Color (0, 0, 0, 255)
- Code 335: Glaciers and perpetual snow — Color (166, 230, 204, 255)
- Code 411: Inland marshes — Color (166, 166, 255, 255)
- Code 412: Peat bogs — Color (77, 77, 255, 255)
- Code 421: Salt marshes — Color (204, 204, 255, 255)
- Code 422: Salines — Color (230, 230, 255, 255)
- Code 423: Intertidal flats — Color (166, 166, 230, 255)
- Code 511: Water courses — Color (0, 204, 242, 255)
- Code 512: Water bodies — Color (128, 242, 230, 255)
- Code 521: Coastal lagoons — Color (0, 255, 166, 255)
- Code 522: Estuaries — Color (166, 255, 230, 255)
- Code 523: Sea and ocean — Color (230, 242, 255, 255)
- Code 999: NODATA — Color (255, 255, 255, 255)
- Code 990: UNCLASSIFIED LAND SURFACE — Color (255, 255, 255, 255)
- Code 995: UNCLASSIFIED WATER BODIES — Color (230, 242, 255, 255)
- Code 990 (duplicate): UNCLASSIFIED — Color (255, 255, 255, 255)

## Format Details
- Interpolation: DISCRETE
- Each line maps a class code to a specific RGBA color and a human-readable label.
- Includes special classes for NODATA and UNCLASSIFIED categories.

## How It Supports Data Work
- Provides ready-to-use styling for land-cover classification in GIS, enabling quick visualization for stakeholder communication.
- Facilitates consistent interpretation across maps, dashboards, and reports.
- Aids data QA by ensuring colors align with defined classes during data integration and product development.

## Practical Considerations
- Ensure compatibility: class codes (e.g., 111, 112, 121, ..., 999, 990, 995) align with your dataset’s coding schema.
- Be mindful of UNCLASSIFIED/NODATA classes; map them appropriately in analyses to avoid misinterpretation.
- This file is best used as a QGIS style/export reference to support end-user data exploration and presentation.

## Next Steps for Data Support
- Import as a style into QGIS or apply as a color ramp for a categorized raster/vector layer.
- Validate that your data’s class codes match the mapped codes and adjust if necessary.
- Integrate with dashboards or reports to enable end users to explore data via consistent color semantics.