# Operation Manual HYPROP

## Overview of HYPROP and Data Generated
- HYPROP is a fully automated system to determine soil hydraulic properties by measuring water tension at two depths with two tensio shafts while the sample evaporates.
- Outputs include:
  - Tensions h1 and h2 over time (two depths)
  - Sample mass changes and dry weight after measurement
  - Derived volumetric water content θ from mass change
  - pF/WC curve (retention curve) derived from θ(h)
  - Hydraulic conductivity function K(h) derived from mass loss and tension differences
  - Median tension (h) based on the average of h1 and h2
- Data points are generated as discrete time points (typically 100) and are prepared for curve fitting and evaluation.

## Data Products and Modeling
- HYPROP-FIT performs data evaluation and curve fitting to obtain θ(h) and K(h) curves.
- Supported models for retention and conductivity curves include:
  - van Genuchten, Brooks-Corey, Kosugi, Fredlund-Xing
  - Bi- and multi-modal forms; Peters-Durner-Iden (PDI) variant
- HYPROP-FIT uses nonlinear regression to fit both θ(h) and K(h) simultaneously (integral fit is available for retention).
- Output data can be exported for further use and visualization, and WP4 data can be integrated post-measurement.

## Software and Workflow
- HYPROP-VIEW
  - Data logging, device management, and basic visualization of tensions and masses
  - Guided by a wizard for measuring configuration, with an option to enter settings directly
- HYPROP-FIT
  - Dedicated evaluation and curve fitting of HYPROP data
  - Explanations and manuals available via links in the software
- Setup steps
  - Install HYPROP-VIEW and HYPROP-FIT
  - Connect HYPROP balance to USB; software auto-detects devices
  - Ensure unique device IDs for sensor units to avoid communication conflicts

## Measuring Method and Data Capture
- Two tensio shafts measure tensions at different soil depths; the middle plane corresponds to the soil’s symmetry plane.
- Measurement workflow (high level)
  - Soil sampling and saturation
  - Degassing of water and filling of tensio shafts
  - Assembly of sensor unit and connection to balance
  - Evaporation measurement with continuous mass and tension logging
  - Post-measurement determination of dry mass
  - Evaluation with HYPROP-FIT
- Saturation and degassing
  - Saturation times vary by soil type (e.g., coarse sand ~10 min; silt ~24 h; clay up to weeks)
  - Degas water via HYPROP Refill Unit or syringes; ensure no air bubbles in tensio shafts
- Measuring modes
  - Multi balance mode: one balance per sensor unit
  - Single balance mode: one balance for multiple sensor units (up to 20 samples)
- Data capture requirements
  - Record metadata: soil sample name, sample ring type, balance type, measurement mode
  - Weigh dry mass after measurement for accurate θ computation
- Data quality considerations
  - Air entry, vapor pressure limits, and boiling delay constrain the measuring range
  - Atmospheric pressure and elevation affect the practical measurement range
  - Avoid osmosis effects (negligible but noted)

## Data Interpretation and Range Limitations
- Key physical concepts
  - Tension (matrix potential) is the driving force for water retention; measured as vacuum in the tensio shaft
  - pF value relates to the soil water tension; 1 pF unit corresponds to a logarithmic scale of water column height
  - Bubble point, cavitation, boiling delay define the measuring range and curve shape
- Measuring range limits
  - Air entry point of tensio shafts around 8.8 bar (not typically limiting)
  - Water vapor pressure imposes a practical limit when ambient pressure is low or at higher elevations
  - Boiling delay and cavitation influence the upper end of K(h) and θ(h) data
- Data interpretation
  - The evaporation method yields a ΔV/Δt-based flow, which is converted to q and then K(h) via Darcy’s framework
  - Suboptimal curves can still be evaluated; HYPROP-FIT provides modeling options for diverse soils, including clays and sands
- Typical curves and model selection
  - Sand: strong bubble point, steep drop in retention after air entry; suitable for Brooks-Corey, van Genuchten, Simmons-Fayer
  - Clay and loam: broader pore distributions; may require bimodal or PDI approaches

## Post-Measurement Processing and WP4 Integration
- After HYPROP measurement, add WP4 data (if available) by entering WP4 masses and pF data into HYPROP-FIT to update gravimetric and volumetric water contents.
- Weighing and data weighting are incorporated into the curve fitting process, with WP4 data given the same weighting as HYPROP data.

## Maintenance, Safety, and Cleaning
- Safety
  - Electrical installations must comply with local safety and EMC standards
  - Do not touch tensio shaft ceramics with bare fingers; avoid inserting sharp objects into sensor holes
- Cleaning
  - Sensor unit is IP65; can be rinsed under running water
  - Clean upside down to prevent soil ingress; remove tensio shafts before thorough cleaning
- O-rings and maintenance
  - If tension curves indicate leakage, replace red O-rings in the sensor unit
  - Use fine tweezers carefully to avoid damaging the sensors
- Storage
  - Store to prevent algae growth and maintain system readiness

## Technical Data Highlights
- Tensio shafts: two levels with ceramic tips; degassed water required
- Measuring range: approximately -0.3 to 3000 hPa (-0.3 to 300 kPa); temperature -30 to 70 °C
- Accuracy: pressure ±2.5 hPa; temperature ±0.2 K
- Compatibility: sensor units support up to 20 USB connections; HYPROP balance supports 2200 g with 0.01 g readout
- Software: HYPROP-VIEW for data capture and management; HYPROP-FIT for evaluation and export

## References and Notes
- HYPROP-FIT manual and other cited literature linked in the HYPROP documentation for detailed modeling approaches and evaluation methodology