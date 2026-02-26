# ANALYTICAL GUIDELINES FOR WATER SAMPLES Version 1.1 (previously AG Protocol, updated Jan 2001)

## Aim and scope
- Provide guidelines for analysis of water samples from ECN terrestrial sites.
- Laboratories manage resources but must document methodologies, changes, and validation procedures.
- Annual review by Analytical Working Group; methods include defined detection limit targets.
- Ensures consistency and traceability across sites for data used in assessments and mapping.

## Approved techniques (highlights)
- Determinands covered include pH, conductivity, major cations (Na, K, Ca, Mg), major anions (NO3, SO4, Cl, PO4), NH4-N, alkalinity, DOC, and Total N.
- Multiple alternative methods are allowed per determinand; specific techniques are listed with references and notes.
- Some methods quantify related but not exact species; comparative tests may be required to ensure comparability.

## Reference techniques and bias considerations
- Establish a set of primary reference methods to compare alternatives and assess new methodologies.
- Laboratories must report fractions (e.g., SO4 2- by IC) and monitor alternative techniques for bias if swapping methods.
- Detection limits and measurement bases are defined for consistency across sites.

## Providing details of methodology and metadata
- Laboratories keep detailed method information locally; summary data is stored in the ECN meta-database.
- Data records are allocated per determinand, site, core measurement, and date, including method, precision, and suitability notes.
- Example provided for nitrate analysis (ion chromatography) including sample types, volumes, calibration, detection limits, and QC.

## Validation: accuracy and precision
- Accuracy: closeness to true value, assessed via interlaboratory controls (e.g., AQUACHECK) and recorded with corrective procedures if needed.
- Precision: ensured through QC samples and batch bias checks; synthetic QC solutions are used to monitor batch performance.
- Laboratories should participate in ongoing accuracy checks and document results to confirm conformity.

## Quality control procedures (ECN-specific)
- A dedicated QC system exists for ECN participants; independent QC validation is encouraged (e.g., interlaboratory exchange schemes).
- Opportunity to compute between-site correction factors and detect rogue batches or trends over time.
- Annual preparation of two concentrated QC solutions (one for cations, one for anions) at Merlewood; includes preparation and handling steps, with dilution procedures and matrix matching.

## Data transfer and QC data formatting
- QC data are transferred to the ECN CCU in a standardized, machine-readable format alongside sample results.
- Data record fields include measurement code, site ID, QC sample code, preparation dates, analysis dates, pH (un/ stirred), conductivity, and concentrations for determinands (Na, K, Ca, Mg, Fe, Al, PO4-P, NO3-N, NH4-N, Cl, SO4-S, DOC, Total N), plus a quality code.
- An explicit example (Moor House) demonstrates the required structure and coding.

## Priority listing for limited sample volumes
- When rainfall is low and sample volume is constrained, a priority order guides analytical decisions:
  1. pH, conductivity
  2. Cations: Ca2+, Mg2+ (then K+, Na+)
  3. Anions: NO3-, SO4 2- (then PO4 3-, Cl-)
  4. NH4+-N
  5. DOC
  6. Fe2+, Al3+ (cations requiring acidified portion)
  7. Total N, alkalinity
- Refer to the Initial Water Handling Protocol for sample handling and acidification details.

## Practical implications for GIS Specialists
- Data harmonization: standardized methods and detection limits support reliable cross-site GIS mapping and comparisons.
- Metadata and provenance: per-determinand, per-site methodology records enable transparent GIS layer labeling and quality assessment.
- Data quality: explicit QA/QC, interlaboratory comparisons, and correction factors facilitate uncertainty-aware mapping and trend analysis.
- Data ingestion: structured QC data formats and meta-database linkage streamline integration into GIS databases and dashboards.
- Resource planning: the volume-priority guidance informs data availability assumptions when building map products under data-scarce conditions.