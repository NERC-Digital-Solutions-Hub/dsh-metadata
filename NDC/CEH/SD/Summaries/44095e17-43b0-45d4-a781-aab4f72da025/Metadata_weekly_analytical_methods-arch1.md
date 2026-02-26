# LOCATION OF ANALYTICAL DATA PRE-CONCENTRATION PRIOR TO ANALYSIS TO IMPROVE

- A comprehensive metadata and data-dictionary for a water-quality dataset collected at the Plynlimon site, detailing pre-concentration and analysis specifics to improve detection limits.
- Covers numerous chemical species (e.g., aluminium, ammonium, chloride, nitrate, sulfate, metals, dissolved organic carbon, nitrogen, etc.) with dissolved forms predominating.
- Data span multiple decades (from the 1980s into the 2000s) and are associated with different laboratories and analytical platforms.

## Data schema and key fields

- For each analyte, core fields include:
  - Determinand and Form (e.g., Aluminium, Dissolved) and Units (ug/l, mg/l).
  - Lower Quantification Data Complex (LQDC) values, and a QUOTE TO value indicating reporting concentration thresholds.
  - Temporal extent: START and END dates, with occasional ongoing (cont.) periods.
  - Location of analysis (e.g., Wallingford, Lancaster, Lancaster, Staylittle, Bangor, etc.).
  - Analytical method and QC qualifier(s) describing data provenance and quality (e.g., ICP-ICP-OES, ICP-MS, AAS, IC, TOC analyzer).
  - Filtration and preservation details (e.g., 10/47 mm GF/C filters, 0.45 μm membranes, field rain and cloud, preservation with reagents, storage conditions).
  - Pre-concentration and dilution procedures (e.g., evaporation steps, dilution to flasks, specific volumes) used to achieve target detection limits.
  - Detection limit notes, with some entries listing no explicit detection limit.
- Data are organized repetitively by analyte, with each entry capturing the above attributes for the period and site of analysis.

## Analytical methods and laboratories

- Multiple laboratories and methods across time:
  - Wallingford, Lancaster, Staylittle, Bangor, Bangor, and other sites.
  - Techniques include Inductively Coupled Plasma Optical Emission Spectrometry (ICP-OES), Inductively Coupled Plasma Mass Spectrometry (ICP-MS), Atomic Absorption (AAS), Ion Chromatography (IC), Technicon Autoanalyzers, and TOC analyzers.
  - Pre-concentration and matrix-adjustment steps described per analyte to improve detection limits.
- Data are linked to specific SOPs and standard operating procedures (e.g., SOP 3115b, SOP 3149, 3504) and instrument configurations (e.g., VG PlasmaQuad, DRC 11, Perkin Elmer 3300 DV).

## Data quality and QC

- Data quality is governed by:
  - Data quality flags and QC qualifiers (QC Data Qualifier codes) indicating issues such as instrument drift, method changes, or raw data.
  - Analytical Method QC Codes describing interlaboratory proficiency and ISO/IEC/ISO 17025 affiliations.
  - LQDC values indicating the lowest quantifiable concentration or reporting thresholds used for each analyte.
  - Data qualifiers include codes for raw data, detection limit issues, unusual patterns, and corrections (e.g., interference corrections, method-change adjustments).
- Interlaboratory and proficiency testing context is documented for several analytes (e.g., Aquacheck LGC schemes, NBS SRMs).
- Several analytes show method changes over time, with corresponding notes about comparability and data treatment (e.g., time periods with different detection capabilities).

## Sampling types, timing, and data integration

- Sampling types include:
  - Grab samples: streams and boreholes.
  - Time-integrated input samples: rainfall, throughfall, stemflow, and cloud water.
- Time-stamps and sampling semantics:
  - Stream and borehole samples are grab at the specified collection time.
  - Rainfall, throughfall, stemflow, and cloud samples are time-integrated over the interval since the previous sample.
  - Volume-weighted sampling times are computed to reflect the influence of rainfall timing on concentrations and fluxes.
- Year mean sampling is derived from volume-weighted sampling times.
- The dataset provides guidance on how to use volume-weighted timing for analyses sensitive to precipitation/runoff timing.

## Hydrology: flow, runoff, and data conversions

- A dedicated section provides conversion formulas to translate streamflow data into area-weighted runoff:
  - Catchment areas (in sq. km) for sites: Lower Hore, Upper Hore, Tanllwyth (Tanllwyth site), Lower Hafren, Upper Hafren, with specified values.
  - Conversions:
    - mm/15 min (flow) = cumecs × 0.9 / catchment area
    - cumecs = (mm/15 min) × catchment area / 0.9
- This enables integrating hydrological and chemical data to compute area-weighted runoff and associated nutrient/solute fluxes.
- Site codes and catchment-area values support site-specific flux calculations.

## Site details and sampling geometry

- Site names and codes indicate a network around Plynlimon and its rivers and wetlands (e.g., Tanllwyth, Lower/Upper Hafren, Hore, etc.).
- Sampling times and locations are tied to catchment areas, flow structures, and sampling points used for chemistry versus hydrology.

## Practical guidance for analysts

- Use the QC data qualifiers to determine which data points are suitable for analysis and whether corrective actions are needed.
- When combining data across laboratories or methods, account for method-specific detection limits, QC flags, and potential interlaboratory biases (as described by the QC codes and proficiency notes).
- For flux analyses, rely on the provided conversion formulas to convert flow to area-weighted runoff and to compute mm/15 min or cumecs as appropriate.
- When analyzing time series, consider the volume-weighted sampling times for precipitation-related samples to accurately relate rainfall events to chemical responses.
- Be mindful of periods with method changes or gaps, and apply the recommended data handling notes (e.g., using “cont.” periods with caveats) to ensure robust conclusions.
- Leverage the detailed filtration, preservation, and pre-concentration notes to reproduce or validate laboratory conditions and to assess potential biases in measured concentrations.

## Notable caveats and limitations

- Long-term data include changes in analytical methods and laboratories, which may affect comparability across time.
- Some analytes have limited or no explicit detection-limit information in certain periods.
- Data quality flags indicate occasional irregularities or uncertainties requiring careful treatment in analyses.
- The volume-weighted timing approach is crucial for precipitation–runoff analyses but requires complete rainfall data from available AWS stations; gaps are bridged with alternate weather stations when needed.