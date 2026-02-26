# Generating a Soil Moisture Characteristic Using the WP4C

- Purpose
  - Produce a soil moisture characteristic (moisture release curve) that relates water potential to water content.
  - Helps describe soil water storage, plant-available water, and predict water and contaminant transport.
  - This protocol describes the wetting (wetting characteristic) curve and notes hysteresis with drying curves.

- What is measured
  - Water potential and water content for soil samples at a range of water contents.
  - Results are plotted (water content, g/g vs. water potential, MPa) and can be fit with a power-law model.

- Equipment and samples
  - WP4C dewpoint potentiometer and stainless steel sample cups.
  - Soil samples prepared to controlled water contents; use airtight sealing to minimize evaporation.
  - Example reference: Walla Walla silt loam curve.

- Procedure (condensed steps)
  - Measure the mass of a clean WP4C sample cup (Mc).
  - Prepare soil-water mixtures to obtain the desired water contents.
  - Seal samples with disposable lids; repeat for multiple water contents.
  - For each sample: measure water potential, then quickly weigh the wet soil plus cup (Mw) to minimize moisture loss.
  - Dry samples in a oven at 105°C for at least 16 hours; cool in a desiccator; weigh dry soil plus cup (Md).
  - Calculate water content (g/g) with:
    - w/g = (Mw − Md) / (Md − Mc)
  - Plot the data in a spreadsheet to generate the moisture characteristic.

- Key considerations and tips
  - Equilibration is improved with a near-airtight seal (e.g., Parafilm or tape around lid).
  - Mixing soil in bulk (e.g., 15 g or more) before aliquoting improves reliability and consistency.
  - If the water-content range is unknown, start from air-dry and incrementally increase water content by ~0.05 g/g or smaller until saturation.
  - The procedure described here yields a wetting characteristic; hysteresis means wetting curves differ from drying curves.

- Notes on data interpretation
  - The line shown in the example indicates a power-law fit to the data.
  - The resulting moisture-content versus water-potential curve can be used to characterize soil water storage and transport properties for environmental monitoring analyses.

- Output
  - A plotted soil moisture characteristic (g/g vs. MPa) derived from WP4C measurements.
  - A dataset suitable for inclusion in standardized environmental monitoring outputs and datasets.