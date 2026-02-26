# Mini Disk Infiltrometer

- A portable instrument for measuring soil unsaturated hydraulic conductivity (infiltration through soil) in field, lab, and classroom settings.
- Assists in understanding water movement, contaminant transport, and recharge dynamics by providing data on how quickly water infiltrates different soils under controlled suction.

## Key Specifications and Features

- Overall size: compact; designed for in-field use with minimal water carried.
- Suction range: adjustable from 0.5 to 7 cm of suction.
- Disk: sintered stainless steel, 4.5 cm diameter; small disk radius (2.25 cm) for localized contact.
- Water reservoir: ~135 ml required to operate.
- Dimensions: total length 32.7 cm; tube diameter 3.1 cm.
- Additional components: bubble (upper) chamber controls suction; Mariotte tube ensures suction stability; lower chamber collects infiltrating water.

## How It Works (Concept)

- Both chambers are filled with water; suction is generated in the upper/bubble chamber.
- Water in the lower chamber infiltrates into soil at a rate determined by the chosen suction and soil properties.
- The disk’s small size and tension (unsaturated) infiltration emphasize soil matrix flow and reduce macropore effects.
- Data are collected as volume infiltrated over time and analyzed to derive hydraulic conductivity.

## Preparation and Setup

- Fill the bubble chamber to about three-quarters full with non-distilled soil water (to preserve ionic balance).
- Fill the water reservoir after setting suction to zero offset; reinstall the bottom elastomer and disk securely.
- Ensure no leaks when vertical.
- Suction rate adjustments:
  - Typical: 2 cm suction for most soils.
  - Faster infiltration (sandy soils): up to 6 cm.
  - Slower infiltration (compact soils): around 0.5 cm.
- Placement: use a smooth soil surface; if needed, add a fine layer of silica sand/diatomaceous earth for good contact; clamp/ring stand recommended.

## Data Collection Protocol

- Record starting water volume.
- Place infiltrometer in full contact with soil at time zero.
- Record infiltrated volume at regular intervals (intervals depend on soil and chosen suction; e.g., sand 2–5 s, silt loam ~30 s, clay 30–60 min).
- Ensure each measurement infiltrates at least 15–20 mL for accurate hydraulic conductivity calculation.

## Data Analysis and Processing

- 5.1 Use the Spreadsheet Macro
  - Decagon provides an Excel spreadsheet to compute the slope of cumulative infiltration versus sqrt(time).
  - Download and input recorded volumes; it automatically updates the sqrt(time) and infiltration columns; save as a new spreadsheet.

- 5.2 Calculate Infiltration
  - Infiltration data are modeled with I = C1 t + C2 sqrt(t) (Zhang 1997; good for infiltrations into dry soils).
  - Hydraulic conductivity k is computed as k = C1 / A, where A depends on soil properties (van Genuchten parameters), disk radius, and suction.
  - A is calculated via equations using van Genuchten parameters (n and α), disk radius ro, and suction ho. The Mini Disk Infiltrometer uses a 2.25 cm radius disk and suction of -0.5 to -6 cm.
  - Van Genuchten parameters for 12 soil textures are provided; A values tabulated for each texture class and suction level.
  - Example: for a silt loam at 2 cm suction, A ≈ 7.93; if C1 = 0.0028 cm/s, then k ≈ 3.5 × 10^-4 cm/s.
  - If data yield a negative C1, it indicates data issues (e.g., shallow flow barriers or instrument disturbance) and should be re-evaluated.
  - For soils with n < 1.35, use the Dohnal et al. modification to Zhang’s equation for better estimates:
    K = [C1 (α ro)^{0.6}] / [11.65 (n^{0.82} − 1) exp(34.65 (n − 1.19) α ho)]
  - Notes on data quality and interpretation are provided in the documentation (Dane & Topp, 2002; related literature).

- 6 Water Repellency Index
  - Measures soil water repellency via sorptivity using 95% ethanol and water.
  - Procedure: fill reservoir with ethanol for ethanol sorptivity; with water for water sorptivity; compute slope Se and Sw from I = S sqrt(t).
  - Repellency index R = 1.95 Se Sw.
  - Cautions: ethanol can damage reservoirs; use only specified polycarbonate reservoirs (post-2005).

## Maintenance and Cleaning

- Cleaning: mild soap and water; stainless disk is dishwasher-safe.
- Suction tube: if stiff, apply a small amount of vacuum grease to facilitate movement.

## Support, Warranty, and Liability

- Customer support: email support@decagon.com or sales@decagon.com; phone 509-332-5600; hours M–F 8 am–5 pm Pacific.
- Warranty: 1 year on parts and labor; automatically validated upon receipt.
- Seller’s liability: limited to replacement parts; excludes damages from wear, misuse, accident, or improper use; no implied warranties beyond stated terms.

## Practical Considerations for Analysts

- Data quality and scale: ensure proper sampling at suitable scales and avoid red herrings by validating data integrity (e.g., check for negative C1 values).
- Data integration: use the spreadsheet macro to streamline analysis and maintain traceability between raw data, processed results, and underlying equations.
- Parameter dependencies: understanding van Genuchten parameters and soil texture classification is essential to select the correct A value and compute accurate k.
- Handling macropores: the tensioned infiltration suppresses macropore flow, yielding soil-matrix hydrau­lic conductivity that is more spatially consistent but may differ from saturated conductivity.
- Field-to-lab translation: the compact design supports field measurements, but careful surface contact and soil preparation are critical for reliable results.

References and additional reading are provided for deeper theory and method context.