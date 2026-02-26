# Soil temperature profiles from permafrost in subarctic Canada

## Overview
- Dataset of soil temperature profiles measured during summer 2013 and 2014 at multiple sites in subarctic Canada.
- Sites are identified by codes (FFU, BLF, WHF, TPP, TW, MCU, MCB, WTP, WTM, WTS, WTW, BCB, BCS) with brief ecosystem descriptions.
- Temperature measurements span depths from 0–20 cm (shallow) and deeper depths, using site-specific techniques.

## Sites and Sampling Details
- FFU: FireFox Unburnt (unburnt black spruce forest)
- BLF: BlackFox (black spruce forest)
- WHF: WhiteFox (white spruce forest)
- TPP: Teslin Peatland Plateau (peatland plateau near Teslin)
- TW: Teslin Wetland (thawed peatland plateau)
- MCU: Mosquito Creek Unburnt (unburnt black spruce forest)
- MCB: Mosquito Creek Burnt (burnt black spruce forest)
- WTP: White Truck Plateau (peatland plateau near Yellowknife)
- WTM: White Truck Moss (recently thawed peatland plateau with moss)
- WTS: White Truck Sedge (recently thawed peatland plateau with sedge/moss)
- WTW: White Truck Wetland (potentially older collapse feature)
- BCB: Boundary Creek Birch (birch forest)
- BCS: Boundary Creek Spruce (black spruce forest)

## Measurement Methods and Instrumentation
- 0–20 cm: Conventional electronic thermometer inserted in soil.
- Deeper temperatures (for FFU, BLF, WHF, TPP, TW, MCU, MCB, WTP, BCB, BCS): plastic tube sealed at bottom inserted into the post-core hole, filled with antifreeze, capped; a thermistor-equipped cable is lowered into the tube and left at depth to equilibrate; resistance is read and converted to °C. Zero °C corresponds to 7355 ohms; drift calibration established by ice bath for each thermistor.
- Deeper temperatures (for WTM, WTS, WTW): Rototherm probe (1.3 m stainless steel tube, 7 mm sensing tip) with a platinum resistor (100 Ω at 0°C, 4-wire, Class B, IEC 751). Temperature readings obtained with a hand-held digital thermometer.
- For all methods, measurements are taken by inserting a probe and recording resistance or temperature at predefined depths; multiple depths are measured to construct the profile.

## Data Processing and Calibration
- Temperature values derived from resistance readings (for the thermistor-based method) or direct readings (Rototherm probe).
- Calibration/drift: thermistors calibrated in ice bath to establish resistance-to-temperature relationship; drift tracked per thermistor to maintain accuracy.
- Depth-specific measurements require equilibration time before recording stable values.

## Metadata and Documentation Considerations (Data Stewards)
- Key metadata to capture:
  - Site code and corresponding ecosystem description
  - Depths at which temperatures were measured
  - Instrumentation used (thermistor tubing system or Rototherm probe), with model/specifications
  - Calibration details (ice bath drift data, conversion equations, resistance-to-°C constants)
  - Measurement dates (summer 2013 or 2014) and sampling protocol
  - Any data quality notes (e.g., equilibration status, anomalies)

## Data Governance, Sharing, and Stewardship Implications
- Ensure datasets are discoverable with clear site codes and method descriptions.
- Maintain consistent metadata across sites to support interoperability and re-use.
- Document all processing steps (calibration constants, conversion formulas, and any data transformations) for reproducibility.
- Consider creating a uniform data schema to accommodate mixed measurement methods and facilitate portal ingestion.
- Be mindful of provenance and potential method-based biases when combining profiles from different site groups.

## Challenges and Considerations for Data Management
- Heterogeneous measurement approaches across sites (thermistor tube method vs. Rototherm probe) require careful harmonization in metadata and data products.
- Handling legacy or non-interoperable data formats from older measurement approaches.
- Ensuring timely availability and completeness of site-specific metadata to support discovery and reuse.
- Large or complex datasets may require robust storage and clear versioning to support updates and corrections.