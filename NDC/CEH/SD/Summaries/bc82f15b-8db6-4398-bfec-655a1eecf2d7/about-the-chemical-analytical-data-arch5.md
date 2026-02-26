# Calibration of a sensor for mercury (II) ions using a Fluorimeter

- Purpose and scope
  - Describes dataset files used to calibrate a sensor for mercury(II) ions (Hg2+) using a fluorimeter.
  - Includes tests across sensor concentrations, varying water/methanol co-solvent ratios, and the impact of acid (nitric acid) on sensor sensitivity for HgNO3 stability.
  - Presents calibration by measuring luminescent response at 500 nm excitation to different Hg2+ concentrations, enabling linear calibration for unknown samples.
  - Provides validation data with ICP-MS and real samples (dental clinical and amalgam samples) to corroborate sensor calibration.

- Data contents and structure
  - Calibration experiments
    - Multiple sensor concentrations and water: methanol ratios.
    - File names indicate sensor concentration and solvent composition.
  - Documentation and graphs
    - PowerPoint file containing calibration graphs derived from raw fluorimeter data.
  - Real-sample testing
    - Dental clinical and amalgam samples tested with a 1 µM sensor.
    - Media used: saliva, distilled water, and amalgam separator supernatant.
  - ICP-MS data
    - Used to validate fluorimeter calibration and monitor soluble mercury in dental amalgam samples.
    - Samples held in water and saliva at 11°C or 37°C; supernatants filtered prior to ICP-MS measurement.

- Methods and metadata considerations
  - Mercury sources used in studies include HgCl2 and HgNO3.
  - Solvent systems and co-solvent ratios are key experimental factors; excitation wavelength is 500 nm.
  - Metadata to capture: sensor concentration, solvent ratio, acid presence, analyte form (Hg2+ vs HgNO3), media, temperature, and measurement units.
  - Data lineage: calibration data linked to real-sample measurements and ICP-MS validation data.

- Data governance implications for Data Stewards
  - Data quality and standards
    - Ensure consistent metadata across calibration, experimental conditions, and validation data.
    - Maintain links between raw fluorimeter data, processed calibration figures, and ICP-MS results.
  - Interoperability and formats
    - Harmonize formats across fluorimeter results, PowerPoint calibration graphs, and ICP-MS outputs.
  - Access, sharing, and embargoes
    - Assess whether any sensor chemistry details or dental-material data require restricted access or embargoes.
  - Provenance and updates
    - Document data provenance, experimental conditions, and any reprocessing or re-calibration steps.
  - Curation and dissemination
    - Upload to appropriate data portals with clear dataset descriptions and cross-references to related datasets (calibration, real-sample tests, and ICP-MS validation).