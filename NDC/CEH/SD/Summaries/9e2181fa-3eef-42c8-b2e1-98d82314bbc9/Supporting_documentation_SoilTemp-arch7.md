# Soil temperature profiles from permafrost in subarctic Canada

## Overview
- Dataset of soil temperature profiles measured in subarctic Canada during the summers of 2013 and 2014.
- Measurements cover shallow (0–20 cm) and deeper soil depths using different methods depending on site.
- Sites span diverse forest and peatland environments, identified by codes (see below).

## Sites and codes
- FFU - FireFox Unburnt: unburnt black spruce forest
- BLF - BlackFox: black spruce forest
- WHF - WhiteFox: white spruce forest
- TPP - Teslin Peatland Plateau: peatland plateau near Teslin
- TW - Teslin Wetland: thawed peatland plateau
- MCU - Mosquito Creek Unburnt: unburnt black spruce forest
- MCB - Mosquito Creek Burnt: burnt black spruce forest
- WTP - White Truck Plateau: peatland plateau near Yellowknife
- WTM - White Truck Moss: thawed peatland plateau with moss
- WTS - White Truck Sedge: thawed peatland plateau with sedge/moss
- WTW - White Truck Wetland: older thaw feature (thawed peatland plateau)
- BCB - Boundary Creek Birch: birch forest
- BCS - Boundary Creek Spruce: black spruce forest

## Measurement methods and depths
- Shallow (0–20 cm): measured with a conventional electronic thermometer inserted directly into the soil.
- Deeper depths (for FFU, BLF, WHF, TPP, TW, MCU, MCB, WTP, BCB, BCS):
  - Plastic tube method: sealed bottom in the soil core hole, hole filled with soil, tube filled with antifreeze, capped at the top.
  - Thermal sensing: thermistor lowered via a cable inserted into the tube; equilibrates to a depth, then reading recorded with a multimeter.
  - Temperature values are derived from resistance readings; 0°C corresponds to 7355 ohms; prior drift calibrated via ice bath.
- Deeper depths (for WTM, WTS, WTW):
  - Rototherm probe: 1.3 m stainless steel tube; sensing tip 7 mm; platinum resistor (100 Ω at 0°C, 4-wire, Class B, IEC 751); measurement with handheld digital thermometer.
  - Tolerances: ±0.3°C.

## Data processing and calibration
- Readings stabilized (equilibrated) at each depth before recording.
- Resistance values converted to Celsius using established calibration relationships.
- Calibration details include ice-bath calibration for thermistors and Rototherm specifications for the platinum sensor.

## Data characteristics and considerations for GIS
- Depth coverage: 0–20 cm plus variable deeper depths depending on site, using two distinct measurement approaches.
- Data units: Celsius.
- Method heterogeneity: two primary deep-measuring approaches (thermistor-in-tube with antifreeze vs Rototherm probe) that may affect cross-site comparability.
- Rich site metadata embedded in codes (ecosystem type and disturbance status), enabling contextual mapping of temperature profiles.

## Temporal scope
- Summer measurements conducted in 2013 and 2014 across all sites.

## Practical implications for map-based data products
- When visualizing, include depth as a key dimension (e.g., depth layers or profiles) and annotate method used per site.
- Consider harmonization or documentation to account for method-related differences in deeper soil temperatures.
- Incorporate calibrations and uncertainty (e.g., Rototherm tolerance, thermistor drift) into metadata and uncertainty visualization.
- Use site codes to link to habitat types and disturbance regimes for richer spatial analyses.