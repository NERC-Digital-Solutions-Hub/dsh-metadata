ANALYTICAL GUIDELINES FOR WATER SAMPLES Version 1.1 (previously AG Protocol, updated Jan 2001)

- Purpose and scope
  - Guidelines for analysis of water samples from ECN terrestrial sites.
  - Labs are responsible for managed resources; must document methodologies, significant changes, and validation procedures.
  - Procedures reviewed annually by an Analytical Working Group.
  - Detection limits set as targets for labs’ chosen methods.

- Governance and oversight
  - Each laboratory operates under controlled conditions and maintains documentation.
  - Analytical Working Group (representatives from laboratories) conducts annual reviews.
  - Records of methodology changes are added as data stamps to the ECN database.

- Approved and reference techniques
  - Determinands covered include pH, conductivity, major cations (Na+, K+, Ca2+, Mg2+), Fe2+, Al3+, NH4+ N, Cl-, NO3- N, SO4 2-, HCO3-/alkalinity, PO43-, DOC, Total N.
  - For each determinand, there are approved techniques and primary reference techniques.
  - Techniques include pH and conductivity methods, AAS, ICP/OES, IC, various colorimetric and col–based methods.
  - Some techniques quantify related fractions rather than the exact species; notes indicate when comparative tests are needed.
  - Laboratories should report data for the fraction specified (e.g., SO4 2- as S or as sulfate), and monitor alternative techniques if bias is a concern.

- Data reporting and uniformity
  - Methods should be described in the ECN database; a data record per determinand per site captures methodology, precision, and related details.
  - Uniform detection limits are defined; laboratories may have different working ranges, but data near the limit must be evaluated for suitability or re-analysis.
  - Data reporting emphasizes consistency and traceability of methodology.

- Priority and sample handling
  - When sample volumes are limited (e.g., during low rainfall), a priority list guides analytical options:
    1) pH, conductivity
    2) Cations (Ca2+, Mg2+; then K+, Na+)
    3) Anions (NO3-, SO4 2-; then PO4 3-, Cl-)
    4) NH4+ N
    5) DOC
    6) Additional cations requiring separate acidified portions (Fe2+, Al3+)
    7) Total-N, alkalinity
  - Refer to Initial Water Handling Protocol for sample solution handling, filtration, pH, and acidification.

- Providing details of methodology (metadata for GIS)
  - Laboratories maintain detailed methodology records; ECN stores a metadata record for each determinand/site/date pair in a central meta database.
  - The metadata includes: determinand, sample type, method, calibration range, volume analyzed, typical concentrations, measurement basis, and QC measures.
  - Example format illustrates fields such as typical concentrations, calibration ranges, measurement results, detection limits, and interferences.

- Validation and quality assurance
  - Validation relies on approved techniques, uniform detection limits, and internal QC; participation in interlaboratory checks (e.g., AQUACHECK) is required.
  - Accuracy reflects agreement with the wider analytical community; maintain records of accuracy checks and corrections.
  - An accuracy example shows reporting in a chosen fraction with a mean, result, and percentage relative error; corrective actions are recorded if needed.
  - Precision is controlled via synthetic QC solutions; QC data must be reported with sample results; access to interlaboratory schemes is encouraged.

- Quality Control procedures (QC system)
  - A separate ECN QC system exists to support participants; continue independent QC validation and join interlaboratory exchanges.
  - Opportunity to compute between-site correction factors if all sites use the same QC solutions.
  - Periodic distribution of two concentrated QC solutions (one for cations, one for anions) from Merlewood; solutions diluted and prepared by analysts; a continuity check is performed annually.

- Data transfer and QC data format
  - QC data are submitted to the ECN CCU in a machine-readable format alongside sample data, with fields adapted for QC-specific dates.
  - The QC data record includes: measurement code (QC), site ID, local QC sample code, preparation dates, dates of analysis, pH measurements (unstirred and stirred), pH, conductivity, alkalinity, and concentrations of major determinands (Na, K, Ca, Mg, Fe, Al, PO4-P, NO3-N, NH4-N, Cl, SO4-S, DOC, Total N).
  - Quality code fields follow as needed; a Moor House QC record example is provided.
  - Concentrated QC solutions are prepared annually; data formatting is standardized for inclusion in the ECN database.

- Author and provenance
  - A.P. Rowland, C. Woods, M. Lane (revised August 1998; updated sources referenced in 1998 document).

- GIS-relevant implications
  - Provides essential metadata for each data point: method, detection limit, fractions measured, calibration ranges, and QC status.
  - Enables proper data harmonization, comparison across sites, and accurate spatial-temporal visualization by annotating maps with data provenance and reliability.
  - Supports data quality mapping, bias detection, and traceability through recorded methodology changes and interlaboratory checks.