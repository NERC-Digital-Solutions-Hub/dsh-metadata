# Generating a Soil Moisture Characteristic Using the WP4C

- Purpose: A moisture release curve (soil moisture characteristic) links soil water potential to water content, describing soil water storage, plant water availability, and predicting water/contaminant transport. The procedure described generates the wetting (wetting) characteristic, noting hysteresis where wetting paths yield higher water content at a given potential than drying paths.

## What is generated
- Wetting moisture characteristic by measuring water potential and water content across a range of moisture contents.
- Data suitable for plotting a moisture release curve in a spreadsheet (and can be fit with a power-law model as indicated).

## Key concepts
- Hysteresis: samples reaching a given water potential by wetting have higher or lower water content than those reached by drying.
- Wetting characteristic: procedure focuses on wetting, not drying.

## Equipment and materials
- WP4C sample cups (stainless steel) and disposable lids.
- Soil mixed with water to achieve target water contents.
- WP4C dewpoint potentiometer for measuring water potential.
- Oven capable of maintaining 105°C for drying.
- Desiccator for cooling and moisture control after drying.

## Procedure (concise steps)
1. Measure the mass of a clean WP4C sample cup (Mc).
2. Mix soil with water to achieve the desired water content.
3. Seal the sample with a disposable lid.
4. Repeat steps 1–3 for multiple water contents; preparing in bulk can supply many samples of the same content.
5. Equilibrate as needed (at least 16 hours).
6. Measure the water potential of each sample, then immediately weigh the wet soil and cup (Mw) to minimize moisture loss.
7. Dry each sample in a drying oven at 105°C for at least 16 hours, then place in a desiccator to cool.
8. When cool, measure the mass of the dry soil and cup (Md).
9. Calculate water content (w, in g/g) with:
   w/g/g = (Mw − Md) / (Md − Mc)
10. Plot the resulting data in a spreadsheet (as shown in Figure 1).

## Notes and practical tips
- Sealing: a more airtight seal (e.g., Parafilm or sealing tape around the lid) can improve equilibration.
- Mixing: larger initial mixing (15 g or more) leads to more reliable and consistent results.
- Range selection: if the desired water content range is unknown, start with an air-dry sample and incrementally increase water content by about 0.05 g/g or less until saturation.

## Data interpretation and presentation
- The data can be plotted to produce the soil moisture characteristic curve.
- The application note indicates a power-law fit line may be applied to the data.
- Figure 1 shows an example moisture release curve for Walla Walla silt loam using the WP4C, illustrating the relationship between water potential and water content.

## Output and reporting
- A wetting moisture characteristic curve that describes how soil water content varies with water potential for the tested samples.
- Documentation should include the measurement sequence, calculated w values, and any fits or models applied to the data.

## Reference and contact
- Decagon Devices, Inc. contact: support@decagon.com