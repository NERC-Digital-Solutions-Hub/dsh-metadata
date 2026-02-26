# WAG Protocol Aim ANALYTICAL GUIDELINES FOR WATER SAMPLES Version 1.1 (previously AG Protocol, updated Jan 2001)

## Overview
- Provides guidelines for analysis of water samples from ECN terrestrial sites.
- Labs are responsible for managing resources and must document methodology, methodological changes, and validation procedures.
- Analytical methods, detection limits, and periodic review are established by an Analytical Working Group.

## Approved and Reference Techniques
- Determinands include pH, conductivity, major cations (Na, K, Ca, Mg), Fe, Al, NH4-N, Cl-, NO3-, SO4(2-), PO4(3-), DOC, Total N, and alkalinity.
- Alternative techniques are listed for each determinand (e.g., AAS, ICP/OES, ion chromatography, colorimetry), with notes on when techniques quantify related fractions rather than the exact species.
- Reference techniques provide a benchmark for comparison and assessment of newer methods.
- For pH and conductivity, specialized handling (and cross-reference to Initial Water Handling Protocol) is required.

## Data Management and Metadata
- Laboratories keep detailed method information locally; ECN stores summary methodology metadata in a central meta-database.
- Each ECN data record links site, core measurement, determinand, date, and methodology (including precision) to indicate how data were produced.
- Example provided: nitrate analyzed by ion chromatography with site- and method-specific details, including typical concentrations, calibration range, detection limit, and error characteristics.

## Validation and Quality Assurance
- Validation relies on using approved techniques, uniform detection limits, and internal QC.
- Accuracy is assessed via participation in interlaboratory schemes (e.g., AQUACHECK) and ongoing recording of accuracy checks and any corrections.
- An example accuracy record shows how results are compared to reference means and percent relative error calculated.
- Precision is controlled with synthetic QC samples; results are reported to Site Managers and interlaboratory schemes are encouraged to validate performance.
- The protocol allows computing between-site correction factors to detect trends or rogue batches, managed by the analysts.

## Data Transfer and QC Data
- A separate QC system is used for ECN participants; laboratories may perform independent QC and join accredited interlaboratory exchanges.
- If sites share the same QC solutions and procedures, between-site correction factors can be computed.
- QC data should be submitted to the ECN Database Manager in a machine-readable format, alongside standard sample data.
- QC data records are batch-based and include two consolidated records: one for cation measurements and one for anion measurements, with preparation dates, analysis dates, and detailed determinand results (pH, conductivity, alkalinity, major ions, DOC, Total N, etc.).
- A single QC data record covers both anion and cation results; the example shows a Moor House QC record format.

## Operational Procedures and Records
- Two QC concentrates (one for cations, one for anions) are prepared annually; dilution and preparation procedures are specified.
- If pH and conductivity are measured locally by site managers, additional QC dilution steps are required; otherwise, procedures are repeated for a single batch.
- The format for QC data submission is free-format, comma-separated, with clearly defined fields (measurement code, site ID, QC sample code, preparation and analysis dates, results for each determinand, and quality codes).

## Priority Listing for Limited Sample Volumes
- 1 (highest priority): pH and conductivity
- 2: Cations (Ca2+, Mg2+), then K+, Na
- 3: Anions (NO3-, SO4(2-)), then PO4(3-), Cl-
- 4: NH4+-N
- 6: Cations requiring separate acidified portions (Fe2+, Al3+)
- 5: DOC
- 7: Total N and alkalinity
- Guidance to site operators and analysts when sample volume is limiting, with reference to the Initial Water Handling Protocol for sample handling, filtration, pH, and acidification.