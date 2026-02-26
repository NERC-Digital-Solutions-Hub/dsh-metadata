# WAG Protocol

## Aim
- Provide analytical guidelines for water samples from ECN terrestrial sites.
- Laboratories must manage analyses under controlled conditions, document methodologies and changes, and validate procedures.
- An Analytical Working Group annually reviews procedures with representatives from participating laboratories.
- Detection limits are targets for laboratories’ chosen methods.

## Approved and reference techniques
- For each determinand, multiple approved techniques are listed; laboratories may use alternatives but must reference the primary methods for comparison.
- Reference techniques include established methods (e.g., HMSO Blue Book references) and standard analytical approaches (e.g., FES/AAS, ICP/OES, ion chromatography, colormetric methods).
- Guidelines specify reporting formats (e.g., results for pH, conductivity, ions, DOC, total N) and encourage consistency of fraction measured (e.g., sulfate as S).
- When techniques quantify different fractions or species, laboratories should monitor alternative methods to check for bias.

## Providing details of methodology and data recording
- Detailed analytical methods stay with the laboratory; ECN database stores summary information for each determinand at each site.
- Data records link site, core measurement, determinand, date, and the methodology used, including precision and any changes.
- Example format is provided (nitrate) to illustrate how methodology and performance characteristics are documented.

## Validation: accuracy and precision
- Accuracy: assessed by agreement with the wider analytical community; participation in interlaboratory schemes (e.g., AQUACHECK) is encouraged.
- Laboratories must record accuracy checks and any corrections applied; data recorded should reflect true performance.
- An example accuracy record demonstrates reporting, comparison to mean, and corrective actions (if any).

## Precision
- Precision is controlled using synthetic QC solutions for batch bias assessment.
- QC data must be reported with each batch; data should not be submitted if QC indicates unacceptable performance.

## Quality Control (QC) procedures within the ECN
- A separate ECN QC system exists; laboratories should continue their independent QC validation and participate in interlaboratory exchanges.
- Opportunity to compute between-site correction factors if all sites use the same QC solutions and procedures.
- QC helps detect rogue batches and long-term trends; managed by the analysts.

### QC solution program
- Two concentrated QC solutions (one for cation analyses, one for anion analyses) are prepared at Merlewood and distributed to sites annually.
- QC solutions are prepared fresh, diluted appropriately, and analytes are measured in a batch-equivalent manner to those for samples.
- A continuity check is performed by analyzing the previous year’s QC solutions with the new year’s new solution.

## Data transfer for QC and methodology
- QC data are submitted to the ECN Central Coordination Unit (CCU) in the same data format as water samples, with dates and preparation dates differentiated.
- A detailed, fixed, comma-separated format is specified for reporting QC batch data, including:
  - Measurement code (QC)
  - Site ID
  - Local QC sample code
  - Preparation and analysis dates
  - pH (AQC unstirred and stirred), conductivity, alkalinity, and concentrations for determinands (Na, K, Ca, Mg, Fe, Al, PO4-P, NO3-N, NH4-N, Cl, SO4-S, DOC, Total N)
  - Quality code and optional quality fields
- An example Moor House QC record is provided to illustrate the data structure.

## Priority listing of determinands (sample-volume constraints)
- If sample volumes are limited, a priority order guides analytical options:
 1) pH and conductivity
 2) Cations (Ca2+, Mg2+ first; then K+, Na+)
 3) Anions (NO3-, SO4 2-, then PO4 3-, Cl-)
 4) NH4+-N
 5) DOC
 6) Cations requiring acidified portions (Fe2+, Al3+)
 7) Total N and alkalinity
- Refer to the Initial Water Handling Protocol for sample handling, filtration, pH adjustment, and acidification guidance.

## Recording and reporting details
- Labs should retain full methodological details for operators; ECN stores summary methodology with site, determinand, and date.
- Data records indicate the methodology used and its precision, including guidance on reporting fractions (e.g., sulfate as sulfur).
- When method changes occur, a new data record is created with a timestamp to indicate the change.

## Notes for analysts
- Analytical performance (detection limits, ranges) is a common guideline across labs; critical evaluation is needed when concentrations approach detection limits.
- Documentation and traceability are required to ensure data comparability across sites and over time.
- Regular interlaboratory participation and internal QC are integral to data quality and reliability.