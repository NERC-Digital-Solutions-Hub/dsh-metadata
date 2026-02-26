# Soil mid-infrared spectroscopy data from arable and grassland in Countryside Survey, Great Britain 2007 Version: 2: 13-01-2021

- A dataset of diffuse reflectance mid-infrared (MIR) spectroscopy data for archived soils from 427 plots across 151 1 km squares in Great Britain, surveyed in 2007.
- Data files:
  - MIR_raw_data.csv: Contains absorbance values from MIR measurements and site metadata.
  - MIR_wavenumbers.csv: Maps absorbance columns to specific wavenumbers (cm-1).
- Context: Part of the Countryside Survey sampling framework, designed to produce reliable national statistics representing Great Britain (England, Scotland, Wales).

## Sampling design and site coverage

- Sampling framework:
  - Based on Countryside Survey stratified Land Classes to reflect environmental gradients.
  - 1 km x 1 km sample squares randomly selected within Land Classes; 591 squares surveyed in 2007 (289 England, 107 Wales, 195 Scotland).
- Soil plots and selection:
  - 427 plots distributed across Great Britain selected from archived Countryside Survey 2007 soil samples.
  - Selection criteria (sequential filters):
    - Current Broad Habitat: Arable, Improved Grass, or Neutral Grass.
    - Plots sampled in both 1998 and 2007.
    - Aggregate Vegetation Classification: Crops and Weeds, Tall Grass and Herb, Fertile Grassland, or Infertile Grassland.
    - Sufficient soil mass for archival material requests.
- Sample collection:
  - Soil samples from top 0–15 cm; 15 cm south of the southern corner of the five Main Plots in 1978, then re-sampled in subsequent surveys.
  - For 2007, soils collected from western corner of Main Plots across 591 squares; 15 g subsamples used for analysis.
- Laboratory archive:
  - Archived at UKCEH Soil Archive, Lancaster; dried and sieved to 2 mm; homogenised before analysis.

## Laboratory methodology

- Instrument and technique:
  - Diffuse reflectance mid-infrared spectroscopy (DRIFT) using Bio-Rad FTX3000MX FTIR with diffuse reflectance attachment.
- Sample preparation:
  - Dry soil (~150 mg), ground for ~45 seconds, no KBr added.
  - Two spectra recorded per sample: initial hold and a second after rotating the sample cup 180 degrees.
- Spectral data:
  - Spectra collected from 4000 to 400 cm-1 with 2 cm-1 resolution; 100 internal scans per acquisition.
- Data processing:
  - Spectra inspected for quality; six spectra discarded; a single representative spectrum used for each sample (flagged in MIR_raw_data.csv SINGLE_SCAN column).

## Data structure and fields

- MIR_raw_data.csv:
  - SQUARE_ID: 1 km square sampling site code.
  - PLOT_ID: Plot identifier within each square (one of five plots).
  - SINGLE_SCAN: Indicates if the sample is represented by a single spectrum.
  - R1…R1868: Absorbance values at 1868 measured wavenumbers (cm-1).
- MIR_wavenumbers.csv:
  - REFLECTANCE_ID: Identifier linking absorbance columns to wavenumbers.
  - WAVENUMBER: Specific wavenumber (cm-1).
- Data interpretation:
  - Each sample has a single or dual spectra represented by absorbance across a wide MIR range; wavenumber mapping allows linking each R-column to its spectral position.

## Quality control and quality assurance

- Field and lab QC:
  - Field teams trained with a sampling manual; standardized workflow for core logging, processing, chemical analyses, and archiving.
  - Pre-average QC: visually inspected spectra from both scans; discarded faulty scans; SINGLE_SCAN flag indicates final representation.
- Data governance:
  - UKCEH operates a Quality Management System (ISO 9001:2015) with QA policies to ensure consistent research quality.
  - Countryside Survey data are owned by UKCEH; usage requires acknowledgment and appropriate copyright/citation.

## Data usage, provenance, and access

- Ownership and acknowledgement:
  - Countryside Survey data owned by UK Centre for Ecology & Hydrology (UKCEH).
  - All use of Countryside Survey data must be acknowledged; data are copyright-restricted.
- Citations and references:
  - Multiple foundational Countryside Survey documents and technical reports are cited (e.g., 2007 UK results, soils report, soils manual, land classification references).
- Metadata considerations:
  - Metadata exist for sampling strategy and QA, with some details (e.g., per-sample metadata completeness) managed via archival processes and dataset originators.

## Relevance for monitoring and decision-making

- Provides a large-scale, standardized MIR spectral dataset suitable for developing and validating soil property models (e.g., organic matter, carbon content) across arable and grassland soils.
- Demonstrates a rigorous, stratified sampling approach designed to support national statistics and environmental monitoring.
- Highlights practical data governance and QA practices relevant to establishing transparent, reproducible monitoring datasets in government or quasi-government contexts.

## Acknowledgements

- Funded through the NERC Soil Security Programme (Project NE/P014364/1).
- Data use requires acknowledgment of Countryside Survey and UKCEH.