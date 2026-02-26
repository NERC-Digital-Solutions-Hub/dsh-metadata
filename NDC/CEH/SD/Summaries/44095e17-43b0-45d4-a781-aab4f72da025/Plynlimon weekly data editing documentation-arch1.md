# Plynlimon long-term hydrochemistry data base Metadata: Quality control and data editing

## Overview
- The Plynlimon hydrochemistry dataset is published in two versions: Raw Data Archive (RDA) and Edited data.
- RDA contains unaltered measurements (except transcription corrections) for transparency and reproducibility, but is not recommended for routine analyses due to known errors.
- Edited data prioritize high confidence measurements, removing unexplained outliers and issues while retaining some corrupted-but-correlated blocks when justified.
- The data span nearly three decades and include notes on analytical-method changes, quality checks, and extensive data curation details.

## Data Versions and Access
- Raw Data Archive (RDA): unaltered/raw measurements with traceable corrections; allows reconstruction of longer series but contains substantial errors.
- Edited data: curated, cleaned measurements with problematic values corrected or removed; designed for routine analyses.
- Raw data remain accessible for reconstructive work; edited data come with notes explaining edits and rationale.

## Editing Principles and Procedures
- Data edits aim to maximize internal consistency (e.g., correlations among analytes, flow relationships, and derived metrics).
- Consistency checks performed where possible (e.g., SO4 vs S, Alk vs pH, charge balance, Gran alkalinity vs ANC, conductivity vs ionic strength).
- Problematic data values (flyers/outliers) are identified and culled or corrected; in rare cases, correlated flyers may be retained if justified.
- Datasets are adjusted to remove blocks with implausible variability or calibration issues; duplicate same-day samples are omitted to avoid over-representation.
- When misattributions or labeling errors are evident, corrections are applied in the edited data and noted.
- For some analytes, data are redefined (e.g., SO4_by_ICP) to reflect corrected calculation methods.

## Method Changes and Their Impact
- Multiple changes in analytical methods over time (e.g., metals analysis via ICP-OES, then ICP-MS; lab changes from CEH Wallingford to CEH Lancaster).
- Changes are explicitly noted; time series around method changes are scrutinized, and data with abrupt shifts in mean/variance are treated with caution.
- Some years or decades of data may be excluded from the edited data if method changes cause non-credible shifts.
- Certain analyte time series show step changes or increased variance around lab transitions; such shifts are sometimes culled or annotated to avoid misleading trend analyses.
- For critical metals like Cr, Ca, Mn, Co, Ni, Mo, Cd, etc., the effects of laboratory changes are documented, and data handling varies by site (some values culled, some kept with caveats).

## Sampling Regimes and Data Coverage
- 2007–2009: intensive rainfall and two streams were sampled approximately every seven hours in addition to regular weekly sampling.
- When weekly vs seven-hourly data diverged, expert judgment determined which dataset was more plausible; in some cases both were retained if differences were not large.

## Data Quality Assurance and Flagging
- Edits rely on relationships among variables (pH–alkalinity, turbidity relationships, flow correlations) to identify outliers.
- Specific blocks showing calibration issues, anomalous blocks (e.g., July 2000s, 1999 blocks), or inconsistent temporal patterns are culled.
- Certain elements exhibit calibration issues, lab-specific anomalies, or analytical noise (e.g., W often omitted due to very low concentrations; Sb largely culled due to synchronous artificial fluctuations; Cs and La often culled due to coarse reporting intervals and calibration problems).
- Data marked as questionable (flyers) are highlighted in the documentation; in many cases the raw values exist in the RDA but are not used in the edited dataset.

## Analyte-Specific Notes (Representative Themes)
- Major ions and derived metrics: consistency checks used to validate pH, alkalinity, and charge balance; anomalous blocks culled, with some exceptions kept if plausibly real.
- Sulfate and sulfur: sulfate data derived from ion measurements vs. ICP sulfur data reclassified into SO4_by_ICP; culling of inconsistent values.
- Trace metals and metalloids: many analytes (e.g., Cr, Mn, Fe, Co, Ni, Cu, Zn, Mo, Cd, Sn, Sb, Cs, Ba, La, Ce, Pr, W, Pb, U) frequently subjected to culling, calibration issues, or lab-transition adjustments; some data retained with cautions due to lab changes or potential contamination.
- Organic and nitrogen species: DOC generally shows a long-term increasing trend with larger seasonal amplitude; NO3–N and NH4–N contain singleton flyers and blocks culled based on flow context and associations with other species.
- Chloride, bromide, iodide, and halides: chlorine data curated to maintain correlations with Major ions; bromide and iodine values culled in places due to variability and calibration concerns.
- Rare and trace elements: several elements (e.g., Y, Sc, La, Ce, Pr) show culling or highlighted calibration limits; some data are omitted or treated with caution due to coarse reporting or lab-specific issues.
- Tungsten: all W values culled due to severe calibration problems.
- Cloudwater and rainfall: specific notes about differences between cloud/rainfall data and stream/groundwater data; some values retained if they show meaningful correlation patterns.

## Practical Guidance for Analysts
- For routine analyses, use the Edited data to ensure reliability and consistency.
- Use the Raw Data Archive only when needed for reconstructing longer histories or investigating potential phenomena, with careful consideration of known errors.
- Always consult the methods metadata and data notes for each analyte to understand changes in analytical technique, laboratory, and any blocks of data that were removed or altered.
- Be cautious when performing trend analyses across laboratory transitions; verify whether the time window spans a method change and consider segmenting analyses accordingly.
- Leverage the documented consistency checks (e.g., pH–Alk, ANC vs ion sums, conductivity vs ionic strength) to validate results and detect potential residual issues.