# Mini Disk Infiltrometer

- A device to measure soil unsaturated hydraulic conductivity in the field or lab, enabling data-driven insights into water infiltration, recharge, and soil-water relationships.

## What it is and how it helps with data

- Measures unsaturated hydraulic conductivity of the soil under controlled suction (0.5 to 7 cm).
- Produces data (volume infiltrated over time) that can be analyzed to compute hydraulic conductivity (k) for different suctions.
- Data can be exported to spreadsheet templates for self-serve analysis and visualization.

## Device and core concepts

- Specifications (examples):
  - Total length: 32.7 cm; disk diameter: 3.1 cm; suction regulator tube: 10.2 cm
  - Suction range: 0.5–7 cm; water reservoir: 21.2 cm; Mariotte tube: 28 cm
  - Water required: ~135 mL
- How it works:
  - Upper bubble chamber creates suction; lower chamber infiltrates soil.
  - A porous disk at the bottom prevents air entry and enables measurement on level soil surfaces.
  - As water infiltrates, volumes are recorded at intervals to build a cumulative infiltration versus time dataset.

## Specifications and performance details

- Suction is adjustable to accommodate different soils; typical default is 2 cm, with options for slower or faster infiltration (e.g., 0.5 cm for slow infiltration, 6 cm for very rapid sand infiltration).
- The device can be used on smooth soil surfaces; a fine sand/diatomaceous earth layer can improve contact when needed.
- The infiltrometer is designed for field portability and classroom demonstrations.

## Preparation and setup (Section 4)

- Fill the bubble chamber about three quarters full with non-distilled water (soil water recommended; avoid distilled water to prevent clay dispersion changes).
- Fill the water reservoir after positioning; set the suction offset to zero by adjusting the Mariotte tube end.
- Reassemble the bottom elastomer with the porous disk; ensure no leaks if held vertically.
- Suction rate adjustment: move the suction tube to set the desired rate; use a small amount of vacuum grease if movement is hindered.

### Choosing the suction rate (Section 4.1)

- Default: 2 cm suction for most soils.
- For sandy soils (fast infiltration): use higher suction (up to 6 cm) for better measurement resolution.
- For compact soils (slower infiltration): use lower suction (0.5 cm).
- Adjustments are recommended for advanced users with instrument familiarity.

### Placement (Section 4.2)

- Place on a smooth soil spot; if needed, smooth the surface with a fine layer of silica sand or diatomaceous earth underneath the disk.
- Use a stand and clamp where possible to maintain stable contact during measurement.

## Data collection and analysis (Sections 5, 5.1, 5.2)

- Collecting data (Section 5):
  - Record the starting water volume.
  - At time zero, place the infiltrometer on the soil with solid contact.
  - Record volume at regular intervals; interval length depends on soil type and suction rate (e.g., sand 2–5 seconds, silt loam ~30 seconds, tight clay 30–60 minutes).
  - Ensure at least 15–20 mL infiltrates per measurement for accuracy.
- Spreadsheet Macro (Section 5.1):
  - Decagon provides an Excel macro to compute the slope of cumulative infiltration versus the square root of time.
  - Enter recorded volumes; the sheet automatically computes and visualizes the data, and can be saved as a new file.
- Calculating Infiltration (Section 5.2):
  - Use I = C1 t + C2 sqrt(t); C1 relates to hydraulic conductivity (k = C1 / A) where A depends on soil parameters and equipment geometry.
  - A depends on van Genuchten parameters (n, α), disk radius ro, and suction ho; specific A values for a 2.25 cm disk are provided in Table 2 for 12 soil textures.
  - For a given soil type and suction, compute k using the slope C1 and the corresponding A value.
  - If C1 is negative, data indicate problems (e.g., shallow flow restriction, instrument movement).
  - For soils with n < 1.35, alternate Zhang/Dohnal formulations may yield improved K estimates (Equation 6 provided).
- Additional notes:
  - The tool allows calculation of sorptivity (C2) and uses A to relate geometry to conductivity.
  - The method supports different textures and suction values; Table 2 provides A values for various textures at different suctions.

## Water Repellency Index (Section 6)

- R is determined from sorptivities of 95% ethanol and water.
- Procedure:
  - Fill ethanol measurement with ethanol in reservoir; keep bubble chamber with water; use suction = 2 cm.
  - Record ethanol infiltration data and compute Se from I = Se sqrt(t).
  - Repeat with water to obtain Sw.
  - Repellency index R = 1.95 * Se * Sw.
- Note: Ethanol can damage reservoir markings on older units; use ethanol-only reservoirs if applicable.

## Maintenance, cleaning, and care

- Cleaning: All parts are washable with mild soap and water; stainless disk is dishwasher-safe.
- Suction tube: If difficult to move, apply a small amount of vacuum grease to ease movement.

## Support, warranty, and liability

- Customer support: Email support@decagon.com or sales@decagon.com; phone +1 509-332-5600; hours Monday–Friday, 8 am–5 pm PT.
- Warranty: 1 year on parts and labor; validated on receipt.
- Seller liability: Limited to replacement parts; excludes damages from wear, neglect, misuse, etc.
- Use of the equipment implies acceptance of warranty terms.

## References and further reading

- Foundational references and related readings on soil physics, sorptivity, van Genuchten parameters, and tension infiltrometer methods.