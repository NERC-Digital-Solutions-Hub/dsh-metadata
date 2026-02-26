# Mini Disk Infiltrometer

- Purpose and scope
  - Tool for measuring soil unsaturated hydraulic conductivity in field or lab settings.
  - Enables evaluation of infiltration rates to inform environmental health monitoring, contaminant transport, groundwater recharge, and ecosystem sustainability.
  - Supports data collection, calibration verification, data handling, and reporting for monitoring frameworks.

- How it works (core concept)
  - Two water-filled chambers: a bubble chamber (upper) to control suction and a lower chamber where water infiltrates into soil.
  - A porous sintered stainless steel disk at the bottom fits the soil surface to enable measurements on relatively level ground.
  - Suction is adjustable from 0.5 to 7 cm; infiltration rate is driven by soil hydraulic properties under tension.
  - Record cumulative infiltration over time to derive hydraulic conductivity.

- Specifications (key metrics)
  - Total length: 32.7 cm; tube diameter: 3.1 cm; disk diameter: 4.5 cm.
  - Suction regulation: 0.5–7 cm; reservoir length: 21.2 cm; mariotte tube length: 28 cm.
  - Water required to operate: 135 mL.
  - Disk material: sintered stainless steel; radius: 2.25 cm.
  - Suitable for field and classroom demonstrations of unsaturated conductivity.

- How it works and data interpretation
  - Infiltration is measured as water leaves the lower chamber and enters soil; volume is logged at set time intervals.
  - Plot cumulative infiltration versus sqrt(time); slope (C1) from this relationship is used to compute hydraulic conductivity (k) with a factor A that depends on soil properties and instrument geometry.
  - The instrument is a tension infiltrometer, so it probes the soil matrix conductivity and reduces influence of macropores under chosen suction.
  - For soils with n < 1.35, alternative equations (Dohnal et al. 2010) may improve k estimates.

- Data collection workflow (operational steps)
  - Preparation ensures bubble chamber is filled and the suction offset is set; avoid using distilled water to prevent ionic shifts in soil.
  - Place the infiltrometer on a smooth soil surface (add fine sand/diatomaceous earth if needed for contact).
  - Record starting water volume, then measure at regular intervals based on soil type and chosen suction rate.
  - Ensure infiltration per measurement is 15–20 mL or more for reliable k calculations.

- Choosing suction rate and placement tips
  - Default suction rate: 2 cm; adjust to 6 cm for rapid sandy soils; 0.5 cm for slow, compact soils.
  - Move the suction tube to set the desired suction; apply a light vacuum grease if movement is stiff.
  - Use a stable stand (ring stand and clamp) to minimize movement and ensure good soil contact.

- Data analysis and tools
  - Decagon provides a spreadsheet macro to compute C1 from the slope of the infiltration vs sqrt(time) data.
  - Steps include entering volumes, generating a sqrt(time) vs infiltration plot, and obtaining C1; k is then calculated as k = C1 / A.
  - A value A is derived from van Genuchten parameters (n, α, ro) and suction, with A values provided for common soil textures (Table 2 in the manual).
  - Negative C1 values indicate data problems (e.g., shallow flow restrictions or movement of the instrument).

- Calculation details and alternative methods
  - Zhang (1997) method used for dry soil infiltration data; k = C1 / A with A dependent on soil parameters and disk geometry.
  - For certain soils (n < 1.35), Dohnal et al. (2010) modification can improve estimates of K (provided equation in the manual).
  - The instrument's suction range (-0.5 to -6 cm in some contexts) and disk radius (ro) are used to compute A.

- Water repellency index (R)
  - Method to assess soil water repellency using sorptivity from ethanol (Se) and water (Sw) sorptivities.
  - Steps: measure ethanol infiltration first, then water infiltration, using the same data collection approach; compute Se and Sw from I = S sqrt(t), then R = 1.95 Se Sw.
  - Note: Ethanol can damage certain reservoir components; use ethanol only with appropriate reservoir types.

- Maintenance and care
  - Cleaning: all parts with mild soap and water; stainless disk can be cleaned with a brush or dishwasher.
  - Suction tube: lubricate movement with vacuum grease if stiff.
  - Regular verification of seal integrity and zero suction offset to ensure accurate readings.

- Support, warranty, and references
  - 1-year warranty on parts and labor; customer support available during business hours.
  - Contact details for support: support@decagon.com, sales@decagon.com, 509-332-5600.
  - References include foundational soil physics literature (e.g., Brady & Weil, Carsel & Parrish, Dane & Topp, Zhang) and related methods for soil sorptivity and hydraulic conductivity estimation.

- Relevance for environmental monitoring programs
  - Provides a field-appropriate method to quantify unsaturated hydraulic conductivity, a critical parameter for evaluating infiltration, contaminant transport, and groundwater recharge.
  - Data produced can feed into monitoring frameworks, with explicit data collection, calculation steps, and transparency about methods.
  - Emphasizes data quality considerations (appropriate suction selection, adequate infiltration per measurement, avoidance of data artifacts) and supports data governance through clear documentation and standardized analysis workflows.