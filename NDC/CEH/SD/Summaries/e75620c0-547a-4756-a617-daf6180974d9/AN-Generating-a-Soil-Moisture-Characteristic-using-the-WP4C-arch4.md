# Generating a Soil Moisture Characteristic Using the WP4C

- Purpose and concept
  - A soil moisture characteristic (moisture release curve) relates water potential to water content, describing soil water storage, plant-available water, and transport of water and contaminants.
  - The process described yields a wetting characteristic (measured during wetting); the moisture characteristic is hysteretic, with wetting and drying paths yielding different water contents at the same potential.

- Procedure (summary of steps)
  - Measure the mass of a clean WP4C sample cup (Mc).
  - Prepare soil and water to the desired water contents.
  - Seal each sample with a disposable lid.
  - Prepare multiple samples across a range of water contents (mixed soil can be reused for similar contents).
  - Measure water potential for each sample, then quickly weigh the wet soil + cup (Mw).
  - Dry the samples in an oven at 105°C for at least 16 hours; cool in a desiccator to prevent moisture uptake.
  - Weigh the dry soil + cup (Md).
  - Calculate water content (g/g) using: (Mw − Md) / (Md − Mc).
  - Plot the resulting data in a spreadsheet (Figure 1 reference).

- Important notes and tips
  - Sealing the sample cup (e.g., with Parafilm) can improve equilibration; post-seal improvements are suggested.
  - Mixing soil in larger quantities (e.g., 15 g or more) before aliquoting improves reliability and consistency.
  - If the water-content range is unknown, start at air-dry and incrementally increase by ~0.05 g/g or smaller until saturation.
  - The line in the sample figure is a power-law fit to the data; data are typically presented in a spreadsheet as shown in Figure 1.

- Data outputs and interpretation
  - The method yields a moisture release curve describing how water content changes with water potential for the soil sample, useful for understanding water storage and plant-available water.
  - The data are plotted to visualize the relationship, with the given example (Walla Walla silt loam) illustrating a typical curve.

- Data leadership considerations (relevant to data strategy and governance)
  - Documentation and reproducibility: clear protocol steps, timing (e.g., rapid weighing after potential measurement), and calculation formula enable repeatable data generation.
  - Data quality and metadata: record soil type, lot, water contents, measurement times, oven conditions, and sealing method to ensure traceability.
  - Data storage and discoverability: store raw measurements (Mw, Md, Mc), calculated water content (w/g/g), and the resulting curve in a structured format (e.g., spreadsheet) with appropriate metadata and versioning.
  - User needs and applicability: data support understanding of soil water storage and transport, enabling integration into broader soil-water models and decision-making.
  - Standards and coordination: the procedure references a specific instrument (WP4C) and its typical workflow; consistent use across teams reduces variability and duplicate effort.