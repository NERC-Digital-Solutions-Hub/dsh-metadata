# Mini Disk Infiltrometer

- Purpose: Portable instrument for measuring unsaturated hydraulic conductivity of soils in the field, lab, or classroom. The manual covers setup, calibration verification, sample preparation, operation, data collection, analysis, and maintenance.

## What it measures and why it matters for environmental monitoring
- Measures unsaturated hydraulic conductivity (how quickly water infiltrates soil under tension), informing infiltration, groundwater recharge, contaminant transport, and ecosystem sustainability.
- Uses a tension infiltrometer approach with an adjustable suction (0.5 to 7 cm) to assess soil matrix flow and reduce macropore effects.
- Data support assessments of soil water movement under varying matric potentials, aiding policy and management decisions.

## Instrument specifications (highlights)
- Total length: 32.7 cm; disk diameter: 3.1 cm; sintered stainless disk: 4.5 cm diameter, 3 mm thick.
- Suction regulation: 0.5 to 7 cm; water reservoir: 21.2 cm; Mariotte tube: 28 cm.
- Water requirement: 135 ml to operate.
- Disk radius: 2.25 cm; suitable for measuring infiltration on relatively level soil surfaces.

## How it works (principle)
- Both chambers filled with water; the top chamber controls suction via the bubble chamber, the lower chamber infiltrates water into the soil.
- Water infiltration rate is recorded as the water level in the lower chamber drops; data are plotted as cumulative infiltration versus time (and versus the square root of time) to derive hydraulic properties.
- Infiltration measurements are influenced by soil pore structure; tension infiltration emphasizes the soil matrix and reduces macropore variability.

## Preparation and setup
- Fill the bubble chamber to three-quarters full with non-distilled water (soil water contains salts and clays).
- Fill the reservoir after configuring suction; adjust Mariotte tube position to maintain zero suction offset during bubbling (re-set to 6 mm if displaced).
- Ensure the porous disk is properly seated and there are no leaks when held vertically.

### Choosing the suction rate
- Default recommended suction: 2 cm for most soils.
- Faster infiltration soils (e.g., sandy soils) may benefit from higher suction (up to 6 cm).
- Slower, compact soils may require lower suction (as low as 0.5 cm).
- Adjustments are for advanced users; use vacuum grease to ease movement of the suction tube if needed.

### Placement
- Use a smooth soil surface; if needed, apply a thin layer of fine silica sand or diatomaceous earth under the disk to ensure good contact.
- A ring stand and clamp can help hold the infiltrometer in place.

## Collecting data (how to run measurements)
- Record starting water volume.
- Place instrument on the soil at time zero with solid contact.
- Record volume at regular time intervals; interval choice depends on soil type and suction.
  - Examples: sand every 2–5 seconds; silt loam every 30 seconds; dense clay every 30–60 minutes.
- Ensure infiltrated water per measurement is at least 15–20 mL for accuracy.

## Data analysis using the spreadsheet macro
- Download and use the Microsoft Excel macro from Decagon to compute the slope of cumulative infiltration versus square root of time.
- Steps outline:
  - Enter recorded volumes; the macro auto-calculates sqrt(time) and infiltration values and updates the graph.
  - Save the resulting data as a new spreadsheet.

## Calculating infiltration and hydraulic conductivity
- Infiltration model (Zhang, 1997) used for infiltration into dry soils:
  - I = C1 t + C2 sqrt(t), where C1 relates to hydraulic conductivity, and C2 is soil sorptivity.
  - Hydraulic conductivity k = C1 / A, where A depends on van Genuchten parameters, disk radius, suction, and soil properties.
- A and K calculations require van Genuchten parameters (n, α) for the soil texture class (from Carsel and Parrish, 1988) and the disk radius (ro = 2.25 cm) and suction ho (0.5–6 cm).
- Table 2 provides A values for 12 soil texture classes at various suction values.
- If data yield a negative C1, it indicates data issues (often due to shallow flow restrictions or movement during measurement); re-check measurements.
- For soils with n < 1.35, use the Dohnal et al. (2010) modification to estimate K:
  - K = [C1 (α ro)^(0.6)] / [11.65 (n^0.82 − 1) exp(34.65 (n − 1.19) α ho)]
- Example result: illustrated calculation shows how to convert C1 to k using A from Table 2.

## Water repellency index (R)
- Measures soil water repellency via sorptivity differences between ethanol and water.
- Procedure:
  - Use ethanol for ethanol sorptivity (I = Se sqrt(t)) and water for water sorptivity (I = Sw sqrt(t)).
  - Sorptivities Se and Sw are computed from linear fits of I versus sqrt(t).
  - Repellency index R = 1.95 * Se * Sw.
- Ethanol is used only with polycarbonate reservoirs (post-2005); avoid spills that can damage the reservoir numbering.

## Maintenance and care
- Cleaning: use mild soap and water; stainless disk can be brushed or dishwasher-cleaned.
- Suction tube: if stiff, apply a small amount of vacuum grease to ease movement.

## References and additional reading
- Key methodological references include Zhang (1997), Dohnal et al. (2010), and related soil physics literature.
- Additional guidance on tension infiltrometry and related analysis is provided in Dane and Topp (2002) and other cited sources.

## Support, warranty, and liability
- Warranty: 1 year on parts and labor.
- Seller liability limited to replacement parts; excludes damages from wear, neglect, misuse, or improper use.
- Customer support available Monday–Friday, 8 am–5 pm Pacific time; contact via email, phone, or fax.