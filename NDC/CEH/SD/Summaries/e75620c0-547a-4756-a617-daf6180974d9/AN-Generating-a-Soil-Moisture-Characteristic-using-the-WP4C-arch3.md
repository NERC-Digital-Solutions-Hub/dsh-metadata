# Generating a Soil Moisture Characteristic Using the WP4C

## Overview
- A soil moisture characteristic (moisture release curve) relates soil water potential to water content, describing water storage in soil and water/contaminant transport.
- This protocol specifically generates a wetting (hysteretic) characteristic using the WP4C device.

## What to measure
- For a set of soil samples at varying water contents, measure:
  - Water potential
  - Wet mass (Mw) of each sample and its cup, immediately after potential measurement
  - Dry mass (Md) after drying

## Required preparation and samples
- Use clean stainless steel WP4C sample cups; pre-measure cup mass (Mc).
- Mix soil with water to achieve desired water contents; seal samples between steps.
- If mixing in bulk, large quantities can be used to prepare multiple samples at the same water content.

## Procedure (wetting characteristic)
1. Measure Mc (mass of empty cup).
2. Prepare soil-water mix to achieve the desired water content.
3. Seal the sample with a disposable lid.
4. Repeat steps 1–3 for various water contents.
5. For each sample, measure water potential, then quickly weigh the wet soil and cup (Mw) to minimize moisture loss.
6. Dry each sample (lid off) in an oven at 105°C for at least 16 hours.
7. Cool briefly, then place in a desiccator to prevent moisture uptake; allow cooling.
8. Measure Md (dry soil + cup) after cooling.
9. Calculate water content (g/g) using:
   g/g = (Mw − Md) / ( Md − Mc )
10. Plot the resulting data (e.g., in a spreadsheet) to obtain the moisture release curve.

## Notes and best practices
- A slightly airtight seal (e.g., Parafilm or sealing tape) can improve equilibration.
- Mixing soil in bulk (e.g., ≥15 g) facilitates easier preparation and more consistent results.
- If the target water content range is unknown, start from air-dry and incrementally increase water content in small steps (e.g., 0.05 g/g) until saturation.

## Application notes
- The line in the example is a power-law fit to the data.
- Sample data may include multiple water potentials (MPa) and corresponding water contents (g/g); the example shows a Walla Walla silt loam curve.

## Outputs and interpretation
- The primary output is a plotted soil moisture characteristic (wetting curve), useful for describing soil water storage and predicting water/contaminant movement.
- The moisture content is derived from gravimetric measurements before and after drying, referenced to the soil plus cup.

## Equipment and data source
- Instrument: WP4C Dewpoint PotentiaMeter (Decagon Devices)
- Contact: Decagon Devices, Inc., support@decagon.com