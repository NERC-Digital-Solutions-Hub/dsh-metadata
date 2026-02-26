# WAG Protocol

## Aim
- Provide guidelines for the analysis of water samples from ECN terrestrial sites.
- Define responsibilities: laboratories manage analyses under controlled conditions and document methodologies and validation procedures.
- Annual review of procedures by an Analytical Working Group with representatives from participating laboratories.
- Establish target detection limits and suitable analytical techniques for determinands.

## Approved techniques and reference techniques
- A range of approved techniques is specified for different determinands (e.g., pH, conductivity, major ions, DOC, total N, total P). Methods include HMSO Blue Book references, AAS, ICP/OES, IC, colorimetric and other established techniques.
- Reference techniques are kept to compare and assess new or alternative methodologies; these serve as primary standards for benchmarking.
- Laboratories may use techniques that quantify related species, but should report data as specified and monitor alternative techniques to confirm absence of bias when employing slightly different fractions or methods.

## Providing details of methodology and metadata
- Each laboratory is responsible for maintaining detailed methodological records; ECN uses a meta-database to store summary information for each determinand and site (linked by site, core measurement, determinand, and date) to indicate methodology and precision.
- An example is provided for nitrate analysis via chemically suppressed ion chromatography, including sample types, typical concentrations, calibration ranges, detection limits, and QC measures.
- Any changes in methodology generate a new database record with a date stamp; laboratories control instrument maintenance, calibration, drift, and staff training.
- Laboratories should report the fraction measured (e.g., sulfate as SO4 2−) and monitor alternate methods to confirm bias absence if a different technique is used.

## Validation: accuracy and precision
- Validation is achieved through approved techniques, uniform detection limits, and internal quality control; interlaboratory analysis (e.g., AQUACHECK) is required to assess accuracy over time.
- Accuracy is defined by closeness to the true value and inter-laboratory agreement; accuracy checks and any corrective procedures must be recorded.
- An example accuracy record illustrates reporting by element, fraction, date, method, lab, scheme, and relative error, informing corrective actions if needed.

## Precision and quality control
- Precision is managed via synthetic QC solutions; QC data must be reported with each batch to Site Managers.
- Labs should participate in independent QC validation and may join accredited interlaboratory schemes to benchmark performance.
- A mechanism is provided for generating between-site correction factors and detecting rogue batches or long-term trends.

## Quality Control procedures for ECN analyses
- A dedicated ECN QC system complements lab QC, enabling inter-site data validation and cross-site corrections.
- Two concentrated QC solutions (separate for cations and anions) are prepared annually at a central facility and distributed to sites for use in the following year.
- QC data must be submitted to the ECN Database Manager in the same data format as samples, with specific fields for preparation dates, analysis dates, measured values, and quality indicators.
- The QC data record format is detailed (free-format CSV) with fields covering measurement code, site, QC sample codes, preparation dates, analytical dates, parameter results, and quality codes.

## Data transfer and metadata records
- All methodology details and QC results are to be captured in machine-readable formats and stored in the ECN database.
- Data transfer includes fields for measurement, site, determinand, date, instrument and method specifics, detection limits, calibration ranges, and QC results.
- Laboratories should ensure data are stored consistently and use the same structure for both sample results and QC results.

## Priority listing of determinands
- A priority ranking guides decisions when sample volumes are limited (e.g., during low rainfall):
  1) pH and conductivity
  2) Cations (Ca2+, Mg2+; then K+, Na+) and anions (NO3−, SO4 2−; then PO4 3−, Cl−)
  3) NH4+–N
  4) Cations requiring separate acidified portions (Fe2+, Al3+)
  5) DOC
  6) Total N and alkalinity
- Refer to the Initial Water Handling Protocol for information on sample solution handling, filtration, pH, and acidification.

## Practical considerations and governance
- Data and metadata must be shared: summarize methodology in ECN database while sharing underlying data where appropriate.
- When evaluating data for policy or management decisions, apply uniform detection limits and consider re-analysis if near detection thresholds.
- Changes in methodology should be transparently recorded, enabling traceability and assessment of data suitability for purpose.
- The protocol emphasizes data quality, openness, and governance to support transparent monitoring and informed decision-making.