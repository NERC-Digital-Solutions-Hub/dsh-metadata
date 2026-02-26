# Mini Disk Infiltrometer

- Purpose: A portable instrument to measure soil unsaturated hydraulic conductivity in field, lab, or classroom settings.
- Core idea: A tension infiltrometer that uses a controllable suction (0.5 to 7 cm) to infiltrate water into soil from a small disk, enabling calculation of soil hydraulic conductivity.

## Key Specifications and Features

- Physical specs: Total length 32.7 cm; disk diameter 3.1 cm; sintered stainless disk 4.5 cm diameter, 3 mm thick; suction tube 10.2 cm; water reservoir 21.2 cm; Mariotte tube 28 cm; water use ~135 ml.
- Disk and suction: Radius of disk about 2.25 cm; suction range adjustable to tailor measurements for different soils.
- Materials: Includes a bubble chamber and a porous disk to control infiltration; designed for smooth contact with soil surfaces (silica sand or diatomaceous earth can be used to smooth uneven surfaces).

## Data Collection and Processing

- Data collection workflow:
  - Fill the bubble chamber three quarters full with non-distilled water (soil water preferred to preserve ionic balance).
  - Fill the water reservoir, set suction offset, and ensure the disk is securely positioned.
  - Select an appropriate suction rate (default 2 cm; adjust to 0.5–6 cm for challenging soils such as compacted or very rapid infiltration soils).
  - Apply the infiltrometer to a smooth soil surface (use a fine sand layer if needed) and record the starting water volume.
  - Record water volumes at regular time intervals as infiltration proceeds (intervals depend on soil type; e.g., sand 2–5 s; silt loam ~30 s; clay 30–60 min).
  - Ensure at least 15–20 mL infiltrates per measurement for reliable calculations.
- Data processing:
  - Use the provided Excel spreadsheet macro (download from Decagon) to plot cumulative infiltration I versus sqrt(time) and to derive the slope C1.
  - Calculate hydraulic conductivity k = C1 / A, where A depends on soil parameters and the instrument’s geometry (A provided in Table 2 for 2 cm suction across 12 texture classes).
  - For the standard Zhang (1997) approach, fit I = C1 t + C2 sqrt(t); C1 gives k via k = C1 / A.
  - If C1 is negative, identify data quality issues (e.g., shallow flow restrictions, instrument disturbance).
  - For soils with n < 1.35, apply the Dohnal et al. (2010) modification to compute k (alternative equation provided).
- Additional measurement (Water Repellency):
  - Assess soil water repellency using ethanol sorptivity (Se) and water sorptivity (Sw); repellency index R = 1.95 Se Sw.
  - Ethanol measurements require using ethanol in the reservoir; ensure compatibility with reservoir type (polycarbonate reservoirs post-2005 are suitable).

## How to Use the Data and Interpret Outputs

- Outputs include k at specified suctions (e.g., 0.5–6 cm) and corresponding soil parameters (A, n, α, ro, ho) used in calculations.
- The spreadsheet provides an accessible, repeatable method to derive the slope (C1) and thus hydraulic conductivity, supporting comparisons across soils or treatments.
- The method emphasizes unsaturated (tension) infiltration to focus on soil matrix flow and reduce macropore variability.

## Preparation and Placement Nuances

- Water type and ionic balance: Do not use distilled water; soil solution and clays require ionic balance to avoid dispersion or flocculation.
- Suction rate selection: Start with 2 cm; adjust to suit soil type (e.g., slower for compact soils, faster for sandy soils); changes should be done carefully to maintain measurement integrity.
- Surface contact: Ensure solid contact with the soil; use a smooth underlayer if needed for consistent readings.
- Securing the instrument: Use a ring stand and clamp when possible to prevent movement during measurement.

## Maintenance and Support

- Cleaning: All parts are cleanable with mild soap and water; stainless disk is dishwasher-safe.
- Suction tube: If difficult to move, apply a small amount of vacuum grease.
- Support: Decagon provides customer service via email, phone, and fax; warranty is one year for parts and labor.

## Practical Considerations for Data Leaders

- Whole-system view: The device supports field- and lab-based data collection of soil hydraulic properties, enabling cross-site data integration.
- Data quality: Emphasizes standardized preparation, smooth contact, and adequate infiltration volumes to ensure robust k estimates.
- Metadata and reproducibility: The use of an Excel macro ensures consistent data processing; recording soil texture assumptions (via A values) and suction levels is critical for comparability.
- Data gaps and barriers: While the instrument helps quantify unsaturated conductivity, data interpretation depends on correct soil texture parameters and adherence to preparation and measurement protocols; user should account for potential data quality issues (e.g., negative C1) and document measurement conditions.