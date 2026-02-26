# Em and Ex PARAFAC loadings

- A dataset of PARAFAC loadings for excitation (Ex) and emission (Em) modes, typical of EEM (excitation-emission matrix) fluorescence analysis.
- Ex loadings cover excitation wavelengths (e.g., from around 245 nm up to ~500 nm) for multiple components (commonly 7 components in this dataset).
- Em loadings cover emission wavelengths (e.g., from ~280–500 nm and beyond) for the corresponding components.
- The matrices include numerical loadings for each wavelength and component, with some entries missing or corrupted, indicating formatting or data-cleaning issues.

## What this document contains

- Ex PARAFAC loadings
  - For wavelengths (e.g., 245, 250, 255, …, up to about 500 nm).
  - Loadings are provided for seven components (1–7) across these wavelengths.
  - Some entries are missing or not consistently formatted.
- Em PARAFAC loadings
  - For emission wavelengths (e.g., 312.03, 314.06, 315.93, up to higher values).
  - Loadings are provided for the components (1–7), corresponding to each emission wavelength.
  - The data show a sequence of wavelength-value pairs, indicating the emission profiles for each component.
- The document appears to contain two parallel sets of loadings (Ex and Em) as well as multiple blocks labeled “Em PARAFAC loadings” and “Ex PARAFAC loadings,” with signs of incomplete or garbled formatting in places.

## How to interpret and use the data

- For each component, examine the Ex loadings to identify excitation wavelengths that contribute most to that component.
- For each component, examine the Em loadings to identify emission wavelengths that contribute most to that component.
- Use the pairings of high-loading excitation and emission wavelengths to infer the likely fluorophore groups represented by each component (e.g., protein-like, humic-like, or other DOM-related fluorophores).
- Combine the Ex and Em profiles to create component fingerprints that can be used to deconvolute samples or compare sample groups.

## Data quality and caveats

- The text shows formatting inconsistencies and occasional missing values, which will require cleaning before downstream analysis (e.g., parsing into two clean matrices: Ex loadings [wavelengths x components] and Em loadings [wavelengths x components]).
- Some lines contain garbled numbers or placeholders (e.g., incomplete entries or irregular separators), so careful data cleaning is essential.
- Ensure units are consistent (wavelengths in nm) and align Ex and Em axes with the original measurement ranges.

## Suggested data products and next steps

- Data cleaning and structuring
  - Parse Ex and Em loadings into two clean matrices: Ex_loadings (wavelength x components) and Em_loadings (wavelength x components).
  - Create a metadata layer mapping each wavelength to its corresponding excitation or emission value (nm).
- Interactive visualization dashboards
  - Heatmaps of Ex loadings by wavelength (x-axis: wavelength, y-axis: component).
  - Heatmaps of Em loadings by wavelength (x-axis: wavelength, y-axis: component).
  - Component fingerprint plots showing the full Ex-Em pairing for each component.
  - Score plots across samples to show how component contributions vary between samples.
- Documentation and data dictionary
  - Clear definitions of each matrix, the number of components, and the interpretation of loadings.
  - Explanation of how to link loadings to potential fluorophore types.
- Analytical uses
  - Identify dominant fluorophore signatures per component.
  - Compare sample groups or timepoints based on component scores and loadings.
  - Integrate with sample metadata to attribute DOM sources or treatment effects.