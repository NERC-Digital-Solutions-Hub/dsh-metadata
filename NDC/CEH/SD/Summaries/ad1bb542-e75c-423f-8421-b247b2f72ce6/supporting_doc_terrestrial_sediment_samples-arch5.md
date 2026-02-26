# Collection, generation methods and quality control

- Seven terrestrial sediment sampling sites across Harehill and Swineshaw Moors, Stalybridge, Tameside were studied using Time Integrated Mass Samplers (TIMS). Samplers were removed from metal uprights, contents collected in 5-L containers, stored cold (<4 °C) for four days, supernatant discarded, sediment dried at 40 °C, and mass measured after drying.
- Samples allowed to settle in cold storage; supernatant (<0.5% of total mass) siphoned off carefully to avoid disturbing sediment.

## Sample sites
- Harehill (Near): Site 1, OS Grid SD 99831 01404
- Harehill (Far): Site 2, OS Grid SE 00026 01261
- Lower Iron Tongue: Site 3, OS Grid SE 00289 01645
- Middle Iron Tongue: Site 4, OS Grid SE 00625 01096
- Upper Iron Tongue: Site 5, OS Grid SE 00430 01004
- Higher Swineshaw: Site 6, OS Grid SK 00911 99937
- Iron Tongue Hill: Site 7, OS Grid SE 01184 00155

## Analytical methods

- Sediment geochemistry: X-ray fluorescence (XRF) with a XEPOS 3 Energydispersive XRF. Samples lightly ground, pressed, measured under a He atmosphere with Pd and Co excitation; detected with a high-resolution silicon drift detector. Daily standardization and verification using 18 certified reference materials.
- Organic content correction: Loss on ignition (LOI) determined by heating to 105 °C (moisture removal) followed by 450 °C for 4.5 hours to combust organic matter.
- Calibration and quality: Standardization and accuracy checks performed routinely to ensure reliable elemental concentrations.

## Particle size analysis

- Instrument: Coulter LS 13 320 SingleWavelength Laser Diffraction Particle Size Analyser.
- Preparation: Organic components digested with H2O2; samples dispersed in Na6O18P6, then sonicated under specific measurement conditions.
- Processing: Results are the average of three repeats with outliers removed to minimise intra-sample noise.
- Statistics: Particle size distributions summarized using standard Folk and Ward methods via GRADISTAT 8.0; reported metric is D50 (median particle size in mm).
- Instrument calibration: Regular calibration checks using known size distribution standards.

## Data structure, nature and units of recorded values

- Sample data fields include:
  - Sample ID (sample_id)
  - Location (sampling location)
  - Elemental analysis (element in mg/g) with notes for selected elements (e.g., Na, Mg, Al, Si, P, S, Cl, K, Ca, Ti, etc.)
  - Elemental ratios (e.g., Fe/Mn, Si/Al, Zr/K, Zr/Ti)
  - Median particle size (D50 in mm)
  - Loss On Ignition (LOI, in %)
- Missing values are represented as blanks. Values reported with '<' indicate measurements at the limit of detection.
- Data table includes detailed element oxide forms and derived ratios, alongside particle size metrics and LOI values.

## Quality control and provenance

- QA measures include daily XRF standardization, cross-checks with certified reference materials, and verification procedures to ensure accuracy.
- LOI corrections account for organic content; digestion and dispersion steps are standardized to reduce analytical variability.
- Multiple repeats (three) for particle size measurements with outlier removal to improve data reliability.
- Clear documentation of methods and references supports traceability and reproducibility.

## References

- Blott SJ, Pye K. 2001. Gradistat: A grain size distribution and statistics package for the analysis of unconsolidated sediments. Earth Surface Processes and Landforms 26: 1237-1248.
- Boyle JF, Chiverrell RC, Schillereff D. 2015. Approaches to water content correction and calibration for μXRF core scanning: comparing X-ray scattering with simple regression of elemental concentrations. In Micro-XRF Studies of Sediment Cores. Springer; 373-390.
- Folk RL, Ward WC. 1957. Brazos River bar: a study in the significance of grain size parameters. Journal of Sedimentary Research 27: 3-26.
- Phillips JM, Russell MA, Walling DE. 2000. Time-integrated sampling of fluvial suspended sediment: a simple methodology for small catchments. Hydrological Processes 14: 2589-2602.

## Data stewardship implications for Data Stewards

- The dataset is multi-method, multi-parameter, and heterogeneous (elemental mg/g, LOI %, D50 mm, various derived ratios). Requires harmonized metadata and consistent units to enable interoperability with other datasets.
- Ensure robust provenance: document sample IDs, site names, coordinates, methods, QA/QC steps, and calibration materials to support reuse and audit trails.
- Administrative considerations: clarify data availability, update/versioning plans, and potential inclusion in data portals with clear licensing and attribution.
- Governance needs: establish and enforce metadata standards, controlled vocabularies for site names and elements, and data quality flags to communicate uncertainty and detection limits.
- Practical challenges echoed by the archetype (timely data provision, standardization across systems, handling of large and diverse datasets) should be mitigated through standardized data schemas, interoperable formats, and documented data processing workflows.