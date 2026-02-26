# Operation Manual HYPROP

## Overview and purpose
- HYPROP is a fully automated system to determine hydraulic properties of soil samples, producing:
  - water retention (pF/WC) curve
  - unsaturated hydraulic conductivity (Ku) curve
- Based on an evaporation method with two tensio shafts measuring tensions at two depths and a balance recording sample mass over time.
- Two software components:
  - HYPROP-VIEW for data logging, device management, and visualization
  - HYPROP-FIT for data evaluation, curve fitting, and export
- Data stewardship focus: the process supports standardized, traceable, and auditable data generation for large datasets, with clear documentation of samples, devices, procedures, and results.

## How HYPROP works (data products)
- Two tensions h1 and h2 are measured in the soil at two depths; the medial water potential corresponds to an average of h1 and h2.
- Mass loss over time yields water content changes; together with sample geometry (dry mass) this yields θ(h) (retention curve).
- The evaporation-driven flow enables calculation of hydraulic conductivity K(h) via Darcy-based relations across the mid-plane of the sample.
- Data points are generated at defined times (default: 100 points after spline interpolation) and can be modeled with standard soil hydraulic models (van Genuchten, Brooks-Corey, Kosugi, Fredlund-Xing, Peters–Durner–Iden, etc.).
- HYPROP-FIT supports integral fitting and multi-model evaluation, with options to export results and to incorporate WP4 data points (gravimetric to volumetric conversion).

## System components and workflow
- Hardware:
  - Sensor unit with two tensio shafts (50 mm and 25 mm), saturation plate, beakers, degassing accessories, sample rings, balance and cables
  - HYPROP-Refill Unit (vacuum degassing) or syringes for degassing and filling
  - TensioLINK connections, dirt protection, O-rings, and related hardware
- Software:
  - HYPROP-VIEW: device discovery, data logging, real-time displays of tensions and weights
  - HYPROP-FIT: evaluation, curve fitting, model selection, and export
- Data workflow:
  - Prepare and saturate soil in sample ring
  - Degas water and tensio shafts
  - Assemble tensio shafts into sensor unit and connect to balance and computer
  - Run evaporation measurement; HYPROP-VIEW records tensions and mass over time
  - Weigh dry soil after measurement
  - Import dry mass into HYPROP-FIT to generate θ(h) and K(h) curves
  - Optionally add WP4 data and export final results

## Preparing measurements and data governance considerations
- Strict documentation of
  - sample identity (name, ring type), soil type, and ring capacity
  - device IDs for each sensor unit and balance (to avoid communication collisions)
  - measurement mode (multi balance or single balance), and balance configuration
  - degassing method used, volumes, and timeframes
  - dry mass and total masses used for θ(h) calculations
- Data provenance and metadata:
  - Record hardware serial numbers, software versions (HYPROP-VIEW and HYPROP-FIT), and configuration settings
  - Capture times, durations, and any deviations from standard procedures
  - Maintain versioned data files and exportable formats for interoperability and audit trails

## Measuring procedure (highlights)
- Saturation and sample preparation:
  - Clean rings, cap for handling, and ensure air can escape during saturation
  - Capillary saturate for soil types with species-specific times (ranges noted for sands, silts, clays)
- Degassing:
  - Refill Unit method: use vacuum pump, ensure bubble-free water in tensio shafts and sensor unit, monitor vacuum, avoid leaks
  - Syringes method: degas water manually in reservoirs and syringes; fill tensio shafts bubble-free
- Filling and installation:
  - Attach tensio shafts to sensor unit with degassed water; monitor pressure rise and avoid exceeding ~2000 hPa; do not exceed 3000 hPa
  - Drill holes and position sample; reassemble sensor unit onto soil, ensuring no air gaps or soil compression
- Mode selection and weighing:
  - Multi balance mode: one balance per sensor unit; up to 20 samples with one balance; automatic device connections
  - Single balance mode: one balance for multiple sensor units; manual weighing of each sample (twice daily)
  - Weighing sequence and data capture are integrated in HYPROP-VIEW
- Data capture and finishing:
  - HYPROP collects tension and weight data over time; finishes when cavitation or air-entry criteria are reached or when measurement is terminated per protocol
  - Weigh dry soil after measurement; then HYPROP-FIT uses dry mass to convert masses to volumetric water contents

## Data processing and outputs
- Curve generation:
  - Retention curve θ(h) computed from mass change and sample volume
  - Ku(h) derived from flow between two zones and tensions using Darcy’s law
- Modeling and fitting:
  - HYPROP-FIT performs non-linear regression to fit θ(h) and K(h) simultaneously
  - Supports multiple models (van Genuchten, Brooks-Corey, Kosugi, Fredlund-Xing, PDI)
  - Integral-fit option to reduce bias near saturation
- Data integration:
  - WP4 data can be added (gravimetric and cup masses) to refine θ(h) points
  - Standard units and scales are documented (pF, hPa, kPa, MPa, bar, psi, %rF)
- Outputs and documentation:
  - Final datasets include θ(h), K(h), and metadata for each sample
  - Results exportable for reporting, sharing, and integration with other datasets

## Modes and practical considerations for data stewards
- Multi balance mode:
  - Higher throughput; clear attribution of each sample to its sensor unit
  - Requires careful tracking of device IDs and sample ids for traceability
- Single balance mode:
  - Flexibility to run many samples with one balance; manual weighing required
  - Emphasizes the need for robust metadata to link sample rings to balances and times

## Maintenance, safety, and quality control
- Safety and compliance:
  - Electrical safety and EMC considerations; avoid contact with sharp or wet ceramic surfaces
  - IP65-rated sensor unit; allow washing under running water; avoid disassembly beyond recommended steps
- Maintenance:
  - Cleaning sensor unit and replacing O-rings if leakage detected
  - Regular balance adjustment to local conditions (monthly or per workflow)
  - Storage to prevent algae growth when not in use
- Troubleshooting (highlights):
  - Dry tensio shafts or air bubbles require re-degassing
  - Readings out of expected range may indicate leaks, improper filling, or damaged sensors
  - If measurement data stop recording, check USB connection and computer power settings
  - Ensure proper addressing of sensor units to avoid communication conflicts

## Theory, interpretation, and literature (context for data stewardship)
- HYPROP is based on the Wind (1968) evaporation method, Schindler’s refinements, and subsequent developments expanding range and reliability
- Two-tension measurement captures differential drainage; medial pF and volumetric water content derived from the evaporation process
- Typical curves vary by soil texture (sand, loamy sand, clayey silt, etc.); interpretation relies on robust fitting and model selection
- Comprehensive references and manuals are provided with HYPROP for in-depth methodological and modeling details

## Appendices and quick references (data stewardship essentials)
- Typical pF and pressure unit mappings (pF, hPa, kPa, MPa, bar, psi)
- Data point generation and interpolation approach (Hermitian splines; 100-point default)
- Final export capabilities and integration with WP4 data
- Hardware and accessory catalog (refill unit, tensio shafts, sample rings, etc.)