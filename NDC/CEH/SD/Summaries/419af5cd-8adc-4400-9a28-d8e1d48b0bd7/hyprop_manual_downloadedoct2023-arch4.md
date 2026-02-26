# Operation Manual HYPROP

## Overview
- HYPROP is a fully automated system to determine the hydraulic properties of soil samples.
- It measures water tension at two depths with two tensio shafts, uses mass change to derive water content, and computes pF/WC curves and hydraulic conductivity (Ku) curves based on Schindler's evaporation method.
- Data can be evaluated with HYPROP-FIT; HYPROP-VIEW handles logging and basic data management.

## Scope and components
- Scope of delivery includes: sensor unit, HYPROP, two tensio shafts (50 mm and 25 mm), saturation plate, reservoirs, vacuum syringe, droplet syringe, refilling attachments, tubes, auger, sample rings, and related accessories.
- Software tools: HYPROP-VIEW (data logging and device management) and HYPROP-FIT (data evaluation, fitting, and export). Manuals for HYPROP-FIT are linked in the document.

## Safety and intended use
- Electrical installations must meet national safety/EMC requirements; HYPROP is intended for measuring soil water retention and unsaturated hydraulic conductivity functions.
- Safety notes emphasize avoiding contact with tensio shaft ceramics, not penetrating sensor holes, and proper handling of degassed water.
- Warranty covers material/production defects for at least 12 months, with exclusions for misuse.
- IP65-rated sensor unit allows cleaning under running water; keep tensio shafts in place during cleaning.

## How HYPROP works (principle)
- Two tensio shafts in a saturated soil sample (in a ring) transduce matric potentials from two depths to the sensor unit.
- The sample sits on a balance; the weight loss over time yields water content changes.
- The medial pF value is computed from the average tensions h1 and h2; the hydraulic conductivity function Ku(h) is derived from mass change and the tension gradient, using Darcy’s law.
- The system supports wide measurement ranges; the air-entry point of the ceramic tips is around 8.8 bar; water vapor pressure limits the practical range (boiling point considerations); osmosis through the ceramic is negligible.

## Measuring method and procedure
- Steps:
  - Soil sampling and preparation.
  - Saturating the soil sample.
  - Preparing the measuring system.
  - Installing the sample and starting the measurement.
  - Evaluating results with HYPROP-FIT.
- Saturating the soil:
  - Prepare sample rings with architecture to prevent soil loss.
  - Capillary saturation times vary by soil type (e.g., coarse sands ~10 min; clays up to 2 weeks in some cases).
- Filling the device:
  - Degas the tensio shafts and sensor unit water either with the HYPROP Refill Unit or syringes.
  - Ensure bubble-free water; keep tensio shafts filled and the ceramic tips wet.
  - Connect refilling attachments, fix components, and run a vacuum/degassing cycle until bubbles are removed.
  - After degassing, install tensio shafts into the sensor unit carefully, monitor pressure increase, and avoid exceeding 2000 hPa (200 kPa) during tightening.
- Attaching dirt protection and preparing the sensor unit for measurement:
  - Install dirt protection O-rings, reassemble tubes, and ensure air-free connections.
- Drilling holes and assembly:
  - Position the tensio shaft adapters and drill holes in 10 mm steps, fill with water to avoid air ingress, and carefully place the sensor unit onto the soil sample without air gaps.
- Set-up and weighing:
  - Two operation modes: multi balance (one balance per sensor unit) and single balance (one balance for multiple sensor units).
  - Weighing is required in the single-balance mode (usually twice daily); the software identifies which sensor unit is on the balance.
  - Weighing routines can be guided by an on-screen wizard or performed manually.
- Optimal measuring curve and phases:
  - Phase 1: regular measurement range (tension rises to the boiling point of the water).
  - Phase 2: boiling delay (desirable but not mandatory).
  - Phase 3: cavitation (water vapor reduces tension).
  - Phase 4: air entry (tensions drop to zero as air enters; used for evaluation in some cases).
- Finishing a measurement:
  - Stop at cavitation, or use the air-entry point for extended data (requires both tensio shafts to reach appropriate phases).
  - HYPROP-FIT is used for evaluation after finishing.

## Data handling, software, and operation
- HYPROP-VIEW:
  - Displays connected devices and real-time measurement data (tensions and weights over time).
  - Supports a measurement configuration wizard or direct entry.
  - Requires setting unique device IDs for each sensor unit to avoid communication collisions.
- HYPROP-FIT:
  - Evaluates HYPROP data step-by-step from information to measuring to evaluation, fitting, and export.
  - Generates 100 time-point data sets by spline interpolation; computes θ(h) (water content vs. tension) and K(h) (hydraulic conductivity vs. tension).
  - Supports multiple models for fitting: van Genuchten, Brooks & Corey, Kosugi, Fredlund-Xing, and Peters-Durner-Iden (PDI) variants; both uni- and bi-modal forms.
  - Uses integral fit to reduce bias in coarse/structured soils.
  - Parameter optimization via nonlinear regression, fitting θ(h) and K(h) simultaneously.
  - Can incorporate WP4 WP4 data (gravitimetric water contents) by adding WP4 data to HYPROP-FIT evaluation with appropriate weighting.
- Data generation and units:
  - HYPROP measures tensions h1 and h2 and, in multi-balance mode, sample mass concurrently; in single-balance mode, mass is weighed manually.
  - Output points include θ(h) and K(h) with corresponding tensions; dry mass, sample ring mass, and tare data required for volumetric conversions.
  - Units for soil water and matrix potentials are provided (pF, hPa, kPa, MPa, bar, psi, %rF, etc.).
- Typical curves and addendum:
  - The manual provides typical curves for different soils (sandy loam, clayey silt, loamy sand, pure sand) and notes characteristics to aid interpretation.
  - The addendum includes standard pF curves and conversion tables for various states (air dry, oven dry, etc.).

## Data interpretation and modeling
- The medial pF value is derived from the average of h1 and h2 tensions.
- θ(h) and K(h) are modeled and fitted simultaneously; integral fitting is used for accurate θ(h) in coarse or structured soils.
- Model options include standard soil hydraulic models (van Genuchten, Brooks-Corey, Kosugi, etc.) and the Peters-Durner-Iden (PDI) approach.
- The method yields both water-retention characteristics and unsaturated hydraulic conductivity across a wide moisture range, with lossy data handled via model fitting.

## Influences on measuring range and limitations
- Air entry point: specific to the ceramic and soil; stated around 8.8 bar for HYPROP shafts.
- Water vapor pressure and boiling point: limit effective range; at 20°C, practical limit is near atmospheric pressure minus vapor pressure (~97.7 kPa).
- Elevation effects: actual atmospheric pressure can be lower with altitude; this changes the effective measurement range.
- Osmosis: negligible due to pore size of the ceramic shaft.
- Other potential issues: leaks, incorrect shaft seating, air entrainment, and sensor damage.

## Troubleshooting and maintenance
- Common issues include dry tensio shafts, air bubbles, leaks, sensor saturation, and device communication problems.
- Remedies include re-degassing, reseating tensio shafts, replacing O-rings, checking for leaks, ensuring bubble-free connections, and verifying USB/energy settings on computers.
- Cleaning and storage:
  - Sensor unit is IP65; clean under running water with tensio shafts in place.
  - Dry and reassemble after cleaning; store to prevent algae growth if not used for long periods.

## Technical data and specifications
- Tensio shafts: materials and dimensions; bubble point > 200 kPa for large shafts; small shafts ~31 mm; big shafts ~56 mm.
- Sensor unit: pressure range -3.0 to 3000 hPa; temperature -30 to 70 °C; accuracy ~2.5 hPa, ±0.05 hPa per day.
- Balance: weighing range up to 2200 g; readout 0.01 g; reproducibility 0.01 g; internal linearity 0.01 g.
- System supports up to 20 sensor units with tensioLINK; USB connectivity to computer.
- Protected hardware and software versions: HYPROP, HYPROP-VIEW, HYPROP-FIT; references and manuals provided for detailed instructions.

## How to cite and references
- The manual provides extensive references to foundational literature (Brooks & Corey, van Genuchten, Peters & Durner, Schindler, Durner, and others) for the theoretical basis and comparative assessments.
- For detailed evaluation procedures and fitting methods, consult HYPROP-FIT manual and cited literature within the document.

## Notes and additional information
- The document includes numerous vendor-specific accessories, part numbers, and configuration details (extension sets, beaker mounts, saturation plates, etc.) for complete implementation.
- Links are provided for additional manuals: HYPROP-FIT and related software/user guides.