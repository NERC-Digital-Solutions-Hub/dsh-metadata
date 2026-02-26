# Em and Ex PARAFAC loadings

- The document presents PARAFAC loadings for two modes: Em (emission) and Ex (excitation), typical of multi-way fluorescence or spectroscopy analysis.
- Em PARAFAC loadings appear as a long sequence of numeric entries associated with emission-related spectra, including values that resemble wavelengths (e.g., 312.0299988, 315.9299927, 324, 335, 350, 360, 380, 390, 400) interleaved with loading values.
- Ex PARAFAC loadings are organized by component indices (e.g., 245, 250, 255, 260, up to 500) with multiple sub-loadings per component (labeled 1, 2, 3, etc., up to 7), suggesting a decomposition into several excitation-related profiles per component.
- The data sections show:
  - Em loadings: numerous pairs/triples of values that appear to map emission wavelengths to loading magnitudes across components, with many small numbers (e.g., E-06 to E-01 scale) and occasional apparent wavelength markers.
  - Ex loadings: a structured table for each component (245, 250, 255, …) listing seven loading values (1 through 7) per component, indicating multi-dimensional loading patterns across excitation-related dimensions.
- Formatting issues are evident: inconsistent delimiters, truncated lines, and mixed presentation of wavelength-like numbers and loading magnitudes, which makes parsing and precise interpretation challenging without cleaning.
- The overall content represents detailed factor loadings from a PARAFAC decomposition, intended to define spectral profiles for underlying components in emission and excitation dimensions.

- Practical use for analysts:
  - Use the Em loadings to interpret emission spectra associated with each fluorescent component.
  - Use the Ex loadings to interpret excitation spectra associated with each fluorescent component.
  - Combine Em and Ex loadings to characterize individual PARAFAC components (i.e., fluorophores) by their spectral signatures.
  - Validate components by reconstructing spectra and comparing to observed data, or by cross-referencing with known fluorophore signatures.

- Data quality and preparation considerations:
  - The text requires cleaning and parsing into clean, machine-readable matrices (emission loading matrix and excitation loading matrix).
  - Verify units and scales (loadings vs. wavelengths) and align emission wavelengths with corresponding loading values.
  - Check for missing or corrupted entries and address formatting inconsistencies to enable reliable downstream analysis.

- Recommended next steps:
  - Extract Em loadings into a structured emission-loading matrix (emission wavelengths x components).
  - Extract Ex loadings into a structured excitation-loading matrix (components x excitation factors).
  - Plot spectral profiles for each component in both Em and Ex to identify characteristic fluorophores.
  - Compute component scores for samples and explore correlations with environmental or experimental variables.
  - Document metadata (e.g., wavelength ranges, component naming) to facilitate reproducibility and sharing.