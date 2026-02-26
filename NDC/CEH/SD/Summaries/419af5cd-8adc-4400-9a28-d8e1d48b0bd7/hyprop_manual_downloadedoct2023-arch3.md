# Operation Manual HYPROP

- HYPROP is an automated system to determine soil hydraulic properties by evaporation: it yields the water retention function (pF/WC curve) and the unsaturated hydraulic conductivity function (Ku) from soil samples.
- Based on Schindler's evaporation method with two tensio shafts at two depths and a balance to track mass change; HYPROP-FIT software evaluates and fits the data to standard hydraulic models.

## Key components and software
- Sensor unit with two tensio shafts (short and long) inserted into the soil sample in a sample ring; saturated and degassed water fills the shafts.
- HYPROP-VIEW software for data logging and device management; HYPROP-FIT software for evaluation, fitting, and export of results.
- HYPROP Refill Unit (vacuum pump setup) or syringes (manual) for degassing and filling tensio shafts.
- Optional accessories: saturation plate, beaker mounts, adapters, and WP4 data integration for additional data points.

## Measuring method and theory (overview)
- Evaporation from a saturated soil surface under open atmosphere is tracked. Two tensions (h1 and h2) are recorded at two depths; mass change provides water content changes.
- Medial pF value is derived from average tensions; medial WC from mass change; discharge (q) and hydraulic conductivity (Ki) are computed from time-series data using Darcian relations.
- The method can capture both the water retention curve and the conductivity function across a wide moisture range.
- The technique can determine dry bulk density via sample drying post-measurement; osmosis is negligible due to the ceramic pore size.

## Preparation, saturation, and filling
- Prepare a soil sample in a 250 ml sample ring; saturate by degassed water, ensuring air escape paths and preventing evaporation during setup.
- Saturation times vary by soil type (e.g., sands dry faster, clays take longer).
- The tensio shafts must be degassed to avoid air bubbles; cover tips with silicone caps to prevent evaporation during degassing.

## Degassing methods
- Refill Unit method: use vacuum pump with an external timer to degas tensio shafts and sensor unit water; follow color-coded connections and avoid introducing air.
- Syringe method: degas water in reservoir and vacuum syringe; fill tensio shafts progressively to remove air; ensure bubble-free connections.
- Both methods require careful handling to avoid pressure shocks that could damage sensors.

## Assembling and initiating a measurement
- Drill holes at correct positions on the soil sample and assemble the sensor unit with tensio shafts inserted and filled with degassed water.
- Connect the sensor unit to a HYPROP balance and to the computer; initialize zeroing and set up device IDs to avoid communication collisions.
- Use HYPROP-VIEW to manage devices and data; configure measurement mode (multi balance or single balance), and create sample metadata (soil sample name, ring type, balance type).

## Measurement modes and weighing
- Multi balance mode: one balance per sensor unit; streamlined setup and sample handling.
- Single balance mode: one balance handles multiple sensor units (up to 20 samples); weighing the sample mass is manual and performed roughly twice daily.
- Weighing workflow: weigh sample mass accurately, ensure proper tare accounting, and use the software to assign sensor units to balances.

## Data collection and evaluation
- HYPROP-VIEW logs tensions (h1, h2) and mass over time; provides graphical and tabular views of tensions and weights.
- HYPROP-FIT processes raw data to obtain:

  - Retention curve θ(h) by correlating WC with averaged tension h.
  - Conductivity curve K(h) by inverting Darcy’s law using mass loss and tension differences.
  - Fits to standard models (van Genuchten, Brooks-Corey, Kosugi, Fredlund-Xing, Peters-Durner-Iden) using nonlinear regression; both θ(h) and K(h) are optimized simultaneously.
  - Optional integral fit to avoid bias when soil distribution is coarse or structured.

- Data inputs include measured tensions, mass, and the soil’s dry mass (entered after measurement); HYPROP-FIT can also incorporate WP4 data for extended curves.
- Outputs are discrete data points (typically 100 points) for the pF/WC and Ku(h) curves, ready for reporting and further analysis.

## Finishing, data interpretation, and curves
- Four-phase optimal measuring curve: regular rise, boiling delay, cavitation, and air-entry; deviations may still be usable for evaluation.
- Finishing the measurement can be done when the upper tensio shaft reaches cavitation, or when using the air-entry approach to interpolate/average mid-curve values if possible.
- Typical measured curves vary by soil type (clay, silt, loamy sand, sands); the manual provides example descriptions and recommended models for each soil type.

## Determining dry weight and evaluating results
- Post-measurement, determine the soil’s dry weight by oven-drying, then weigh the sample to refine water content calculations.
- HYPROP-FIT provides step-by-step evaluation progress (Information, Measuring, Evaluation, Fitting, Export) and can export results for reporting.
- Dry mass input improves the accuracy of volume-based water contents.

## Troubleshooting and maintenance
- Common issues: dry tensio shafts, air bubbles, leaks, or insufficient pressure range; incorrect shaft seating; coercive sensor shaft interchanges.
- Troubleshooting steps include refilling, checking seals (O-rings), ensuring air-free filling, and verifying sensor unit connections.
- Cleaning and maintenance: sensor unit is IP65 protected and can be cleaned under running water; do not remove tensio shafts; replace O-rings if leakage occurs.
- Storage considerations to prevent algae growth; routine maintenance (e.g., O-ring replacement) as needed.

## Safety, warranty, and support
- Electrical safety and EMC compliance required; improper use voids warranty.
- Warranty typically minimum 12 months; excludes damage from misuse or external factors.
- Support and service processes described; device IDs and calibration considerations emphasized.

## Additional notes and references
- Typical curves and guidance for interpreting curves are provided, including bubble point behavior, air entry points, and model selection for different soils.
- The manual includes references to foundational literature on hydraulic properties and models (van Genuchten, Brooks-Corey, Kosugi, Peters-Durner-Iden) and notes on measurement ranges, vapor pressure effects, and osmotic considerations.
- Technical data overview: tensio shafts, balance specifications, measurement ranges, temperatures, accuracy, and IP protection; capacity for up to 20 sensor units; explicit hardware and software compatibility notes.