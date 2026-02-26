# Mini Disk Infiltrometer

## Overview
- Portable field instrument for measuring soil unsaturated hydraulic conductivity.
- Compact design suitable for field, lab, and classroom demonstrations.
- Generates data that can feed GIS-based analyses of infiltration, groundwater recharge, and contaminant transport.

## What it measures
- Unsaturated hydraulic conductivity of soils under controlled suction (0.5 to 7 cm).
- Measures soil matrix flow by restricting macropore flow through tension (suction) control.

## Key data outputs
- Infiltration data: cumulative infiltration versus time and versus square root of time.
- Hydraulic conductivity (k) calculated from data using C1 and A parameters.
- A values linked to soil texture via van Genuchten parameters; provides k at a given suction.
- Optional: water vs ethanol sorptivity used to compute a Water Repellency Index (R).

## Specifications (highlights)
- Total length: 32.7 cm; disk diameter: 4.5 cm; disk radius for calculations: 2.25 cm.
- Suction range: 0.5–7 cm; water reservoir: ~135 mL; Mariotte tube: ~28 cm.
- Suitable for field and lab use; works with standard Excel-based analysis macros.

## How it works
- Upper bubble chamber creates suction; water-filled lower chamber infiltrates soil at a rate set by suction.
- A porous sintered stainless steel disk beneath the soil surface prevents air leakage and concentrates infiltration through the soil matrix.
- As water infiltrates, record volume at defined intervals to build infiltration vs. time data.
- Data are plotted and analyzed to derive hydraulic properties.

## Preparation
- Fill bubble chamber to three-quarters full with non-distilled water (soil water preferred to maintain ionic balance).
- Fill reservoir, set zero suction offset, and ensure the disk is firmly seated.
- Check for leaks and adjust suction tube to the desired suction mark.

## Choosing the suction rate
- Default suction is 2 cm; adjust to 0.5–6 cm for challenging soils (e.g., sandy or compacted soils).
- Higher suction speeds are helpful for rapid infiltration soils; use caution and advanced understanding when deviating from 2 cm.

## Placement
- Place on a smooth soil surface; if needed, compact a thin layer of fine sand/diatomaceous earth beneath the disk to improve contact.
- Use a ring stand and clamp when available to hold the instrument steady.

## Collecting Data
- Record starting water volume; place instrument at time zero and ensure solid soil contact.
- Take readings at intervals appropriate for the soil and suction rate (e.g., seconds for sands, minutes for clays).
- Ensure each measurement infiltrates at least 15–20 mL to support accurate analysis.

## Data analysis with the Spreadsheet Macro
- Use Decagon’s Excel macro to compute the slope of cumulative infiltration versus sqrt(time).
- Steps:
  - Enter recorded volumes; whole data set can be extended as needed.
  - The macro updates the sqrt(time) and infiltration relationships and graphs.
  - Save the results as a new spreadsheet for record-keeping.

## Calculate Infiltration
- Infiltration data can be analyzed with the Zhang (1997) method for dry soils:
  - I = C1 t + C2 sqrt(t)
  - Hydraulic conductivity k = C1 / A
- A is calculated from van Genuchten parameters, disk radius, and suction; equations provided for different soil textures.
- For soils with n < 1.35, Dohnal et al. (2010) modification may improve estimates (K = [C1 (α r0)^0.6] / [11.65 (n^0.82 − 1) exp(34.65(n − 1.19) α ho)]).
- The device typically uses a 2 cm suction with a 2.25 cm disk; Table 2 lists A values for 12 soil texture classes and various suction values.

## Water Repellency Index
- Measures sorptivity for 95% ethanol and water to compute repellency index R = 1.95 Se Sw.
- Steps: fill reservoir with ethanol for ethanol sorptivity and with water for water sorptivity; use same time intervals and macro to compute slopes.
- Note: Ethanol can damage certain reservoir types; only polycarbonate reservoirs (post-2005) are recommended for ethanol.

## Maintenance and cleaning
- Clean all parts with mild soap and water; stainless disk is dishwasher-safe.
- Lubricate the suction tube with a small amount of vacuum grease if it sticks.

## Notes and references
- Negative C1 values indicate data issues (e.g., shallow flow restrictions or instrument movement).
- Detailed methodology and context available in referenced literature (Dane & Topp 2002; Zhang 1997; Dohnal et al. 2010).

## Relevance to GIS Specialists: Data Integration and Applications
- Outputs provide spatially explicit soil hydraulic properties (k at specific suctions, sorptivity), usable in GIS for infiltration modeling, groundwater recharge estimation, and contaminant transport mapping.
- Data workflow-friendly: volumes, times, infiltration rates, and derived k values can be exported to CSV/Excel and imported into GIS attribute tables for site-based analysis.
- Enables creation of infiltration maps across landscapes by combining field measurements with soil texture classifications and texture-specific A values.
- Important considerations for GIS data quality and standardization:
  - Ensure consistent suction rates, sampling protocols, and documentation of soil surface conditions.
  - Avoid distilled water to preserve soil ionic balance and avoid altering soil dispersion.
  - Maintain data integrity by flagging anomalous results (e.g., negative C1) and noting measurement conditions.