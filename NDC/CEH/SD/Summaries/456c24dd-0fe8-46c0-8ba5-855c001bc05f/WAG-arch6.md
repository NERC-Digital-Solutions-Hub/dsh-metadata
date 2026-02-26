# WAG Protocol

## Aim
- Provide guidelines for analysis of water samples from ECN terrestrial sites.
- Laboratories are responsible for managing their own analytical resources and must conduct analyses under controlled conditions.
- Document methodologies, significant changes, and validation procedures.
- Analytical procedures reviewed annually by an Analytical Working Group with representatives from each laboratory.

## Approved techniques and determinands
- A range of approved methods for key determinations (pH, conductivity, major cations and anions, DOC, total N, etc.).
- Alternative approved techniques are allowed for each determinand, with notes on suitability and suitability testing.
- Some methods quantify related fractions rather than the exact species; laboratories should monitor alternative techniques for bias when used.
- Reference techniques provide primary benchmarks for comparison and assessment of new or alternative methodologies.
- Detection limits are provided as targets and laboratories may have different working ranges, which should be considered when data are at the detection limit.

## Reference techniques
- List of reference methods to compare new or alternative methodologies against.
- For each determinand, documentation includes species of interest, reference technique, and ultimate detection limit.
- Labs must monitor potential bias if deviating from reference techniques, and report on fraction reporting (e.g., reporting sulfate as SO4, or as S).

## Priority listing of determinands
- In periods of low rainfall with limited sample volumes, a priority order guides analytical options:
  1. pH and conductivity
  2. Cations (Ca2+, Mg2+, then K+, Na) and anions (NO3−, SO4 2−, then PO4 3−, Cl−)
  3. NH4+ N
  4. Cations requiring separate acidified portions (Fe2+, Al3+)
  5. DOC
  6. Total N and alkalinity
- Refer to the Initial Water Handling Protocol for sample handling details.

## Providing details of methodology
- Laboratories keep detailed method information for operators; a summary is stored in the ECN database.
- A meta-record per determinand per ECN site captures methodology, precision, typical concentrations, calibration ranges, sample volumes, detection limits, and QC measures.
- Example records illustrate data fields such as substance, matrix, method, calibration range, detection limit, and accuracy indicators.

## Validation: accuracy and precision
- Validation via approved techniques, uniform detection limits, and internal QC; regular interlaboratory analysis (e.g., AQUACHECK).
- Accuracy: assesses closeness to true value and inter-laboratory agreement; requires recording accuracy-check results and any correction procedures.
- Precision: ensured through synthetic QC samples; QC data must be reported with results; data submission should be withheld if QC indicates unacceptable performance.

## Accuracy (detailed)
- Accuracy records document element, fraction measured, method, laboratory, and comparison to reference schemes.
- Example illustrates reporting of accuracy, mean, percentage relative error, and corrective measures (if any).

## Precision (detailed)
- Use of synthetic QC solutions to assess potential batch bias.
- QC data are reported to Site Managers; data should not be submitted if QC is failing.
- Encourages ongoing validation of batch performance and trend detection.

## Quality control procedures for the ECN Terrestrial Network
- A separate QC system exists for ECN participants to validate batches and monitor performance.
- Encourages independent QC assessment and participation in interlaboratory comparisons.
- Allows computation of between-site correction factors if sites use consistent QC solutions.
- Aimed at detecting rogue batches and long-term analytical trends.
- Procedures include preparing QC solutions (two concentrates for cations and anions), diluting to defined volumes, acidification where needed, and distributing to sites.
- QC data must be transferred in the ECN data stream in a specified format.

## Data transfer and QC data format
- QC data are submitted in the same dataset as sample results, with fields adjusted to reflect QC preparation and analysis dates.
- Data record fields include: measurement code (QC), site ID, QC sample code, QC preparation dates, analysis dates, pH values (with and without stirring), conductivity, alkalinity, major ions (Na, K, Ca, Mg, Fe, Al, PO4-P, NO3-N, NH4-N, Cl, SO4-S), DOC, Total N, and a quality code.
- Example records illustrate free-format, comma-separated data and a single QC record per batch combining anion and cation results.
- Quality codes can be appended if required to indicate data quality status.

## Governance and authorship
- The protocol emphasizes governance via the ECN Analytical Working Group and ongoing annual reviews.
- Authoring and revision responsibilities are noted (examples include Rowland, Woods, Lane).