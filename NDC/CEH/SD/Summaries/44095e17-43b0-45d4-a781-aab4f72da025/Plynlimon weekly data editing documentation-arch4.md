# Plynlimon long-term hydrochemistry data base Metadata: Quality control and data editing

- Purpose: Describes how the Plynlimon hydrochemistry dataset is published in two versions (Raw Data Archive and Edited Data) and documents the quality-control and data-editing procedures applied to produce a reliable long-term time series.

## Versions and data provenance

- Raw Data Archive (RDA): Unaltered measurements from laboratories, only transcription corrections traced to original sources. Provided for documentation and transparency about subsequent edits; allows reconstruction of longer time series but contains many values considered in error.
- Edited data (no RDA suffix): Measurements with high confidence, edited to remove unexplained outliers and to correct or exclude problematic values. Used for routine analyses and time-series interpretation.

## Editing principles and quality checks

- Editing aims to maximize data reliability while preserving plausible real-world signals. Editing includes:
  - Correcting or excluding values that defy typical correlations or flow relationships.
  - Deleting unlikely single outliers (flyers) or blocks of data with calibration issues or lab Artefacts.
  - Maintaining original data in the Raw Data Archive for traceability and potential reanalysis.
- Consistency checks used to validate edits:
  - Cross-checks like SO4 vs S, Alk vs pH, charge balance, Gran Alkalinity vs calculated ANC, N species vs TDN, and ionic strength vs conductivity.
  - Outliers identified via relationships with flow and other analytes; blocks with implausible variability often removed.

## Method changes and laboratory transitions

- Documented changes in analytical methods over time (e.g., metals analyzed by ICP-OES until 1988, then ICP-MS; 1998 transition from CEH Wallingford to CEH Lancaster).
- Abrupt changes in time-series statistics around method transitions lead to cautious handling:
  - Where changes caused mean/variance shifts, data with higher confidence around the transition are kept; other periods may be omitted.
  - Some time spans across transitions are flagged as potentially unreliable for trend analyses; users should exercise caution when spanning lab changes.

## Analyte-specific editing highlights

- General approach: Many analytes show calibration issues, spikes, or lab-specific artefacts; the team provides site- and analyte-specific notes.
- Notable patterns:
  - W omitted due to low concentrations dominated by analytical noise; Sb largely omitted except in cloudwater or Nant Iago.
  - Metals and metalloids (e.g., Cr, Mn, Fe, Co, Ni, Cu, Zn, Mo, Cd, Pb, U) frequently require site-specific culling or variance adjustments, particularly around laboratory transitions.
  - Some elements (e.g., Cs, La, Pr, Ce, Ba, W) have periods of calibration issues or coarse reporting intervals and are culled or down-weighted accordingly.
  - Documentation notes indicate many culling decisions are made to preserve plausible time-series dynamics, not to erase signals of interest, with exceptions where anomalies are clearly artefacts.
- Specific treatment examples:
  - Cr: Notable step changes around lab transition; pre- and post-transition data may differ; culling applied at some sites to avoid artefacts.
  - Cd, Cu, Zn, Mo, Sb: Suspect periods with calibration problems or lab contamination flagged; values culled where necessary, especially after method shifts.
  - Cl, Br, I, Li, Be, B, S, Se, etc.: Various degrees of culling or retention based on correlations, calibration issues, and known artefacts (e.g., intensity of short-term noise vs long-term trend).

## Sample handling and data characteristics

- Conductivity and pH/alkalinity measurements: Settled (unfiltered) samples used for some parameters; filtered samples used for solutes. Historical assessments showed no significant difference between filtered and unfiltered for the primary analytes.
- Derived variables:
  - ANC, ionic strength, and related relationships are calculated from edited data and used for quality checks.
  - DON is calculated as TDN minus NO3, NO2, and NH4 (based on edited inputs); some negative DON values may remain due to uncertainties.
- Time-series structure:
  - Analytes are presented in two groups: (1) IC/electrochemical/autoanalysis by atomic number; (2) cations/metals by ICP-OES/ICP-MS, also ordered by atomic number.
  - Unique daily chloride (Cl) records exist for rainfall, mist, streamwater, and groundwater.

## Data access, documentation, and user guidance

- The edited data are intended for routine analyses; the Raw Data Archive remains available for transparency and reconstruction, with caution advised due to uncorrected errors.
- For analyses spanning methodological changes or data blocks with noted anomalies, consult the accompanying data notes and metadata to understand edits, culling criteria, and potential artefacts.
- The documentation emphasizes data provenance, audit trails, and the need to consider instrument changes and site-specific issues when interpreting long-term trends.

## Practical implications for data-leader use

- Prioritize the Edited Data for most analyses to ensure data quality and consistency; refer to Raw Data Archive only when reconstructing longer histories or investigating specific artefacts.
- Monitor time periods around analytical-method changes and laboratory transitions, as these can introduce artificial shifts in mean, variance, or detection limits.
- Use the provided metadata and data notes to understand culling decisions, especially for key analytes (Cr, Cu, Zn, Mo, Sb, Pb, W, La, Ce, Pr, Cs, Ba, Ni, etc.) and site-specific conditions.
- Leverage the explicit documentation of sample handling (settled vs filtered) and consistency checks to assess data reliability for policy-facing or cross-organizational data-sharing contexts.