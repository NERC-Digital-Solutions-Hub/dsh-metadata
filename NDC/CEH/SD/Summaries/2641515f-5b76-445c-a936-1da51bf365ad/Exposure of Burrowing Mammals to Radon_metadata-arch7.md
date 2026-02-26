# Exposure of Burrowing Mammals to Rn-222 in Northwest England - MATERIALS & METHODS 1.1 Field sites and methods

- Purpose and spatial context
  - Aim to obtain a range of soil gas 222Rn concentrations using radon potential data.
  - Radon potential maps derived from measurements in about 460,000 homes; seven NW England sites chosen to span radon potential from <1% to >30%.
  - Highest radon potentials (Sites 1, 6, 7) lie in limestone-type bedrock; potentials estimated from Miles et al. (2007).

- Field site design and burrow construction
  - Seven study sites with three artificial burrows per site (Site 1 had only one due to shallow soil).
  - Burrow design: ~1.2 m long, 10 cm diameter perforated HDPE pipe, buried ~50 cm; open end at ground surface; burr end flap for passive detectors; cane-marked location; wire poultry fencing to deter animals.
  - Replicates located within ~100 m² per site.
  - Initiation: Sites 1–5 began July 2009; Sites 6 and 7 began August and October 2009.

- Sampling schedule and site maintenance
  - About one week after burrow construction, passive detectors inserted; soil repacked to original condition.
  - Relocation occurred at Site 5 (burrow filled with water) and Site 4 (subsequent relocation) as needed.
  - Passive detectors replaced every 4–6 weeks until June 2010; dates recorded.
  - Rodent damage observed; protective poultry wire installed around detectors to prevent further damage.

- Environmental measurements (ancillary data)
  - Soil moisture: 0–10 cm soil samples within 2 m of each burrow at each detector change; moisture determined by drying at 60°C.
  - Soil temperature: Tinytag data loggers placed within ~30 cm of the buried end, at ~50 cm depth; log every 30 seconds; data downloaded during detector changes.

- 1.2 222Rn measurements by passive track etch detectors
  - Detectors: PADC (CR-39) passive detectors from HPA, designed for indoor radon; diffusion chamber discriminates against thoron; moisture-resistant variant in a 200 μm polyethylene bag.
  - Handling: detectors stored in a ventilated area prior to analysis; some detectors treated as controls.
  - Analysis: detectors analyzed with automated slide scanner counting system; results expressed as time-integrated radon exposure (kBq 222Rn h m⁻³) and converted to 222Rn concentrations (kBq m⁻³) using exposure duration.

- 1.3 222Rn measurements by instrumentation
  - Burrow air measurements: AlphaGUARD active radon monitor; sampling via 0.8 cm diameter tube (~90 cm into burrow); pump at 1 L/min; readings averaged after reaching approximate equilibrium; instrument purged between readings.
  - Site 1 additional measurements: three natural burrows within ~200 m also measured.
  - Soil gas radon in interstitial pores: 0.8 cm tube driven to ~80 cm depth; sacrificial tip to prevent blockage; gas pumped into ZnS-lined Lucas scintillation cell linked to Pylon AB5 monitor; background-corrected counts converted to Bq m⁻³ (three consecutive one-minute counts after background).
  - Calibration: instrument/calibration via Fast Radon Exposure Device (FRED) at HPA.
  - Sampling locations around each burrow: three sites (approximately 1 m from detector, two at right angles, and one opposite).
  - Depth/occurrence: some samples shallower than 80 cm due to rock/root presence; Site 5 had only one measurement per burrow at shallow depths; three measurements at most other burrows; three measurements at most sites; Site 7 had no AlphaGUARD measurements (late establishment).

- 1.4 Dosimetric methodologies
  - Dose assessment uses adapted whole-body dose conversion coefficients (DCCs) for 222Rn in equilibrium with short-lived daughters (218Po, 218At, 214Pb, 214Bi).
  - Allometric scaling to different animal geometries (mouse-like small rodent, rabbit-like herbivorous mammal, fox-like carnivorous mammal) to reflect burrow-dwelling wildlife; based on Vives i Batlle et al. (2008) methodology.
  - Equilibrium factor (F) between 222Rn and progeny discussed; due to lack of burrow-specific data, F = 0.8 is assumed for dose calculations; sensitivity discussed.
  - The study uses DCCs as applied in a spreadsheet implementation; considers three exposure geometries: immersion in soil, on soil surface, and immersion in above-ground air; burrow air exposure treated as equivalent to above-ground air exposure (soil exposure routes not modeled).
  - Note on radon equilibrium: typically not in equilibrium with short-lived daughters; equilibrium equivalent concentration (measured 222Rn × F) used for dose calculations; literature range for outdoor F values discussed (0.4–0.97); UK outdoor estimate ~0.65±0.03; mines as low as 0.25; choice of F = 0.8 discussed for implications on dose rates.

- Data integration and GIS considerations (implicit)
  - Spatial context relies on radon potential mapping to select diverse sites; multiple measurement types (passive, active, soil gas) provide geospatially related data around burrows.
  - Data collection combines fixed point measurements with environmental covariates (soil moisture, temperature) for spatial interpretation and modeling of radon exposure in burrows.
  - Field-compiled metadata (sampling times, detector changes, site relocations) essential for spatial-temporal analysis and reproducibility.

- Key challenges and quality considerations (implicit)
  - Data distributed across multiple sites with varying access and substrate; detector damage and burrow waterlogging requiring adjustments.
  - Depth restrictions due to subsurface conditions; some measurements limited by rocks, roots, or moisture.
  - Assumptions in dosimetric modeling (F value, exposure routes) introduce uncertainty acknowledged in methodology.