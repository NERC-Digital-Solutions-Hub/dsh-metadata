# Analytical dataset and metadata for water quality survey (Plynlimon)

- The document is a detailed metadata and data-quality description for a multi-element dissolved constituent dataset from water samples (Plynlimon survey). It includes per-determinand entries with measurement units, detection/quality indicators, filtration, preservation, analytical methods, and data qualifiers.

- Key aim for monitoring framework authors:
  - Provide an auditable evidentiary basis of environmental health measures across many chemical determinants.
  - Document data provenance, QA/QC procedures, and data management steps to support policy scrutiny and future decisions.

- Structure and content at a glance:
  - For each determinant (e.g., Al, Ca, Cl, NO3, PO4, Fe, etc.), the dataset specifies:
    - Form (e.g., Dissolved)
    - DETERMINAND (what is measured)
    - UNITS (e.g., ug/l, mg/l)
    - LQDC (lower limit of detection/quantitation indicator)
    - QUOTE TO (lab- or standards-related rounding/quoting guidance)
    - ANALYTICAL METHOD QC (quality-control tier)
    - DATA QUALIFIER (data quality category)
    - FILTRATION (field or lab filtration details)
    - PRESERVATION (sample preservation protocol)
    - METHOD (analytical technique; e.g., ICP-MS, ICP-OES, colorimetry)
    - COMMENT (notes; some entries include method-specific notes)

  - Data quality and validation:
    - Proficiency testing and standards used to verify accuracy:
      - Aquacheck LGC Interlaboratory Proficiency Testing Scheme for ICP-OES/ICP-MS elements.
      - Standard Reference Material 1643b (NBS) for trace element determinations.
    - Documentation of data quality issues:
      - Instances of data that are deemed unreliable (e.g., “Very strange data with systematic patterns… removal from database”).
      - Acknowledgement of reduced sensitivity during certain periods due to method changes (1992–1998).
    - Raw vs processed data:
      - Notes on raw instrument data with no LQD and guidance on when to apply LQDC and Quarter-To values for laboratory standards.

- Sampling design and data scope:
  - The dataset includes flow-related sampling descriptions used during the survey, with distinctions such as:
    - Baseflow samples
    - Stormflow samples
  - This indicates a consideration of hydrological context in interpreting concentrations and mass fluxes.

- Analytical methods and instrumentation:
  - Common techniques represented:
    - Inductively Coupled Plasma Mass Spectrometry (ICP-MS) for multiple trace elements (e.g., Al, Ba, Cr, Mn, Ni, Pb, Zn, etc.).
    - Inductively Coupled Plasma Optical Emission Spectrometry (ICP-OES) for several elements.
    - Automated colorimetry (e.g., for Cl, NH4, NO3, PO4, F, Si).
    - TOC/organic carbon analyses for dissolved organic carbon (DOC).
    - pH measurement (electrometric with pH meter and electrode).
  - Filtration and preservation details:
    - Field filtration typically using 0.45 μm membranes or filtration to obtain dissolved fractions.
    - Preservation often involves acidification with high-purity nitric acid to 1% or cooling (4°C) and protection from light.
  - Other data qualifiers:
    - Some determinants have multiple LQDC/QUOTE TO combinations indicating tiered reporting or calibration practices.

- Metadata and governance implications for monitoring frameworks:
  - The document exemplifies rigorous metadata practices needed to interpret environmental health indicators:
    - Clear specification of analytical method, QC level, data qualifiers, filtration, and preservation.
    - Documentation of data provenance, external validation, and instrument-specific notes.
  - It highlights potential barriers and considerations for policy use:
    - Completeness and consistency of metadata across determinants are critical for data reuse and comparability.
    - Data quality flags and notes on questionable data require careful handling before policy interpretation.
    - Historical method changes can affect comparability over long time series; explicit notes aid trend analysis.

- End-state and data usability signals:
  - Where robust QA is described (external proficiency testing, SRMs), the dataset supports policy scrutiny with quantified confidence.
  - Where data quality is flagged as questionable or data are removed, monitoring frameworks should exercise caution in using those records for decision-making.
  - The combination of detailed per-determinand metadata and explicit data-quality notes provides a model for traceable, governance-ready environmental monitoring data.