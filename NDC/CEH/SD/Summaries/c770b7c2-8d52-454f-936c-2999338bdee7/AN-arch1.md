# AN Protocol

## Aim
- Detect and define changes in periodic mean atmospheric concentrations of nitrogen dioxide (NO2).
- NO2 is a key urban pollutant from combustion sources; it affects health and ecosystems and contributes to photochemical smog and acid rain.
- The method uses passive diffusion tubes; replication is required due to tube-to-tube variation; low cost and no on-site power needed.
- Consideration given to extending the ECN program to other gases (ammonia, SO2, ozone) but currently no reliably passive methods available.

## Background and context
- NOx are emitted from natural and human sources in roughly equal amounts; anthropogenic NOx is concentrated around population centers.
- NO and NO2 are the relevant oxides in urban atmospheres; NO2 has more pronounced health and ecological impacts.

## Method overview
- Diffusion tubes with NO2-absorbent discs mounted in upper tube region; three tubes per site plus three blanks.
- Deployment height: 1.5 m above ground; may be attached to bulk precipitation collector pole or a post; if a meteorological enclosure exists, use a post inside it.
- Sampling period: two weeks per deployment.
- Field blanks: three tubes transported to site but not exposed; returned to lab the same day for analysis with exposed tubes.
- Tubes are labeled with a unique ECN code, site and location codes, and tube identifiers (E1–E3 for exposed, B1–B3 for blanks).

## Equipment and construction
- Diffusion tubes: plastic tubes with 1 cm diameter stainless steel mesh discs coated with NO2 absorbent.
- Cleaning and preparation: tubes and caps cleaned; discs cleaned and dried; absorbent prepared with triethanolamine solution inside caps.
- Assembly: two dry discs placed in each cap; tube coupled to a colored cap and sealed with a white cap; stored in Sterilin vials and refrigerated until use.
- Storage: diluted absorbent prepared fresh just before use; clean disks stored dry.

## Field deployment and sampling procedure
- Before deployment: remove white cap; tubes mounted vertically with open ends pointing downward.
- After two weeks: collect tubes; re-fit white caps; transport to lab.
- Labelling conventions: ECN Measurement Code (AN), ECN Site ID, Location Code, Tube code (E1/E2/E3 or B1/B2/B3), Sampling Date.
- Recording: field forms and a data transfer workflow are provided for metadata and results.

## Analytical procedure (Appendix I)
- Absorbent analyzed to determine total NO2 absorbed; used to compute mean NO2 concentration over the sampling period.
- Safety: operators must wear gloves; tubes rinsed after analysis to avoid cross-contamination.
- Reagents (AR grade) and preparation:
  - Sulphanilamide, H3PO4, N-1-Naphthylethylene-diamine dihydrochloride (NEDA)
  - Reagent Y (sulphanilamide + water + NEDA)
  - Reagent X (sulphanilamide + NEDA)
  - Stock standards: NO2 solutions of known concentrations
  - Fresh daily calibration standards (0.25, 0.75, 1.25 µg/mL NO2)
- Analytical steps:
  - Prepare standards and reagents as specified.
  - For standards: add X reagent; for samples: add Y reagent; mix and react.
  - Measure absorbance at 542 nm against a water blank.
  - Use calibration curve to convert to µg of nitrite; convert to NO2 concentration in ppb using exposure time and tube geometry.

## Data recording, metadata, and reporting
- Core measurement: atmospheric chemistry – nitrogen dioxide (AN Protocol)
- Core dataset variables (fortnightly for each tube, including three experimental and three blank tubes):
  - Site Identification Code (unique ECN site code)
  - Core Measurement Code (e.g., AN)
  - Location Code (replicate location per site)
  - Setting out date/time (GMT, 1-minute precision)
  - Sampling date/time (GMT, 1-minute precision)
  - Tube code (E1, E2, E3 or B1, B2, B3)
  - Tube weight NO2 (µg, 3 significant figures)
- Additional data transfer and dataset formats are defined by ECNCCU; contact ecnccu@ceh.ac.uk for access to documentation.
- Data handling emphasis:
  - Maintain a clear linkage between sample identifiers, dates, and results.
  - Use blanks to control for background; ensure field blanks are processed with exposed tubes.

## Extensions and notes
- While consideration has been given to expanding to other pollutants (NH3, SO2, O3), reliable passive methods for these were not available at the time.
- Labs and field teams should follow the standardized recording forms provided (and Appendix II) to ensure consistent data capture and traceability.

## Appendices (summary)
- Appendix I: Analytical procedure, detailed reagents, preparation, and step-by-step absorbance measurement and calculation.
- Appendix II: Equipment details, including specific diffusion tube parts and supplier information.
- Additional notes on labeling, data recording conventions, and standard field forms for consistency.