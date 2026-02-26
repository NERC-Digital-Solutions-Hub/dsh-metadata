# Plynlimon long-term hydrochemistry data base Metadata: Quality control and data editing

- Two public versions exist: Raw Data Archive (RDA) containing unaltered measurements (with only transcription error corrections) and Edited data (without RDA suffix) where data have been cleaned and quality-checked for routine analyses.
- Raw data provide transparency and traceability back to original laboratory files; edited data are recommended for routine analyses to avoid common errors and outliers.

## Data Versions and Provenance

- RDA: raw measurements as reported by laboratories; corrected only for trace transcription errors; designed for documentation and potential reconstruction.
- Edited data: measurements with high confidence, after removing unexplained flyers and outliers not consistent with flow or correlations among analytes; certain inter-analyte discrepancies resolved or omitted.
- Where possible, edited data preserve consistency checks (see below) and note method/change impacts in metadata.

## Data Editing and Quality Control

- Core principle: edit to remove anomalies that defy expected relationships (e.g., with flow, major ions) and to exclude clearly erroneous values.
- Procedures include: removal of duplicate same-day samples, misattributed data, blocks with implausible variability, and values likely due to calibration, labeling, or contamination issues.
- Data notes and sample time-series plots show edits; culled or changed raw values are highlighted in red in the presentation.
- Consistency checks performed where possible (e.g., pH vs alkalinity, charge balance, ionic strength vs conductivity, and relationships among major ions). Inconsistencies lead to dropping problematic analytes or observations.

## Analytical Changes and Effects on Data

- Documented method changes across decades (e.g., metals analysis shifting from ICP-OES to ICP-MS; lab changes from CEH Wallingford to CEH Lancaster).
- Time series are inspected around method changes; abrupt mean/variance shifts may trigger data exclusion or cautious interpretation.
- Some time periods/labs introduce blocks of higher variance or calibration issues; these blocks are culled in edited data.
- Notable shifts around walls/lanaster labs: some elements show abrupt changes in mean/variance around lab transitions; users should exercise caution when analyzing periods spanning these changes.

## Data Structure, Variables, and Groupings

- Analytes arranged in two groups:
  - Group 1: determined by ion chromatography and electrochemical methods (e.g., DOC, Gran alkalinity, inorganic species) in order of increasing atomic number.
  - Group 2: cations and metals measured by ICP-OES/ICP-MS in order of increasing atomic number.
- Specially derived variables:
  - SO4_by_ICP: sulfate calculated from ICP-measured sulfur (not the ion sulfate); used in edited data while SO4 (measured as sulfate ion) remains separately documented.
  - DON: dissolved organic nitrogen calculated as TDN minus NO3, NO2, and NH4 (with some missing NO2 handled by replacement).
- Some data and notes emphasize daily records (e.g., daily Cl) and the differences between filtered vs settled/unfiltered measurements for certain parameters (conductivity, pH, alkalinity).

## Data Cleaning Rules and Examples

- Flyers and outliers culled when:
  - They are singletons without plausible hydrological context.
  - They do not correlate with flow, major ions, or other quality checks.
  - They appear to be calibration artifacts or lab contamination (especially for trace elements).
- Block-level removals:
  - Anomalous blocks of measurements (e.g., July–Aug 2010 alkalinity, 1999 blocks at some sites) culled if they indicate calibration problems.
- Laboratory transitions:
  - The shift from Wallingford to Lancaster (late 1998) is associated with changes in variance/means for several elements; pre/post-transition data may be retained but should be treated with caution in trend analyses.
- Specific element considerations:
  - Cr: notable lab-change-related step and variance shifts; some data culled where inconsistent with nearby measurements.
  - Sb, Cs, La, Ce, Pr, Ba, W, Tl, etc.: several periods culled due to calibration issues or coarse reporting intervals; some data retained for cloudwater or select sites.
  - Cu, Zn, Mo, Cd, Sn, Se, Pb, U, etc.: culling decisions reflect instrument calibration issues, lab contamination concerns, or apparent artifacts; long-term usage advised with caution.
- Some site- and period-specific corrections are documented (e.g., re-labelling corrections, cross-site substitutions) to maintain data integrity.

## Temporal and Sampling Considerations for GIS

- Intensive 7-hourly rainfall and two-stream sampling (2007–2009) used to cross-check weekly time-series; where discrepancies are large, expert judgment determines which dataset is retained.
- Daily chloride records offer high-resolution temporal data for mapping temporal dynamics.
- Data quality caveats may affect spatial analyses that span method changes, calibration blocks, or site relocations.

## Guidance for GIS Use and Cautions for Mapping

- Use Edited data for most map-based analyses to ensure data quality and consistency across time and sites.
- Refer to metadata notes for each analyte and site to understand periods affected by method changes or calibration issues.
- For long-term trend mapping, be cautious about interpretations that span lab transitions (Wallingford to Lancaster) and apply appropriate segmentation or sensitivity analyses.
- Raw Data Archive remains available for reconstructing longer histories or specialized studies, but routine analyses should rely on edited data.
- Data products should include provenance indicators (RDA vs Edited), method-change annotations, and notes about culling blocks or corrected observations to inform end users.

## Access, Metadata, and Documentation

- Detailed notes accompany each analyte, including examples of edited values, blocks culled, and the rationale behind decisions.
- Analytical methods metadata files document method changes and their potential impact on time series.
- Not all time series are shown in the example plots; the most heavily edited series are highlighted to illustrate the editing approach.