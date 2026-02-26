# Generating a Soil Moisture Characteristic Using the WP4C

## Overview
- A soil moisture characteristic (moisture release curve) links water potential to water content, describing soil water storage, plant water availability, and potential transport of water and contaminants.
- The document outlines a wetting-characteristic procedure to generate this curve using the WP4C device.

## Relevance for GIS Specialists
- The resulting curve informs spatial modeling of soil moisture and hydrological processes, aiding map-based analyses of water availability and transport across landscapes.
- Can be used to calibrate hydrological models and to compare soil moisture properties across soil types and regions when integrated with GIS data layers.

## Procedure (summary)
- Prepare clean WP4C sample cups and mix soil with water to a range of water contents.
- Seal samples and allow equilibration (wetting characteristic; samples should equilibrate at least 16 hours if possible).
- Measure water potential for each sample, then quickly weigh the wet soil plus cup.
- Dry samples in an oven at 105°C for at least 16 hours, then cool and weigh to determine dry mass.
- Calculate water content (g/g) using: (Mw - Md) / (Md - Mc).
- Plot the resulting data (water content vs. water potential) to form the moisture release curve (often shown as a power-law fit).
- If the water-content range is unknown, start with air-dry soil and increase content in small increments until saturation.

## Notes and Practical Considerations
- A somewhat airtight seal between the lid and cup improves equilibration.
- Mixing in larger quantities (15 g or more) beforehand enhances reliability and consistency.
- When the desired range is unknown, begin at air-dry and incrementally increase moisture content until saturation.
- Data are typically plotted in a spreadsheet; the presented example shows a moisture release curve for a specific soil (Walla Walla silt loam).

## Output and Interpretation
- The result is a soil moisture characteristic that can be used to estimate soil water storage, plant-available water, and hydraulic behavior for GIS-based analyses and spatial decision-making.

## Equipment and Source
- WP4C Dewpoint PotentiaMeter (Decagon Devices, Inc.).