# Metaschoepite dissolution in sediment column systems - groundwater/soil geochemistry and uranium X-ray spectroscopy data

## Overview
- A data compilation describing solid and solution phase geochemical trends in metaschoepite-doped sediment columns reacting with oxic or electron-donor amended synthetic groundwater.
- Samples collected and sacrificed after 6 or 12 months to track uranium dissolution, transport, and speciation.
- Supports analysis of uranium mobility and speciation under varying redox and biochemical conditions; tied to a peer-reviewed study (Bower et al., 2019).

## Experimental design
- Four metaschoepite-doped sediment columns plus two controls, operated under:
  - Oxic groundwater conditions
  - Electron-donor amended groundwater conditions
- Timepoints: 6 months (6MO) and 12 months (12MO)
- Measurements span solid-phase, solution-phase, microbial, and spectroscopic analyses
- Horizons sampled along the columns at regular intervals (e.g., every 5 mm in some datasets)

## Datasets and key variables
- 1. Aqua_Regia_Sediment_Digests_ICPAES_UO3
  - Aqua regia extractions from multiple horizons; U and Fe content per horizon (mm intervals), oxic vs electron-donor amended; 6MO/12MO.

- 2. Column_Effluents_ICPMS_Control_UO3
  - Column effluent concentrations (U by ICP-MS; Fe, Mn, Mg by AES); four columns plus two controls; time-resolved up to 12 months; units mM; includes pore volumes (PV) and detections/limits.

- 3. Column_Effluents_IC_Control_UO3
  - Column effluent concentrations (SO4, NO3, VFA, NO2, PO4) by ion chromatography; oxic vs electron-donor amended; 6MO/12MO; mM; PV included.

- 4. Column_Effluents_pH_Control_UO3
  - pH of column effluents at selected timepoints; 6MO/12MO; oxic vs E-D AM; PV indicated; n.a. for not analysed.

- 5. Sediment_digests_Ferrozine_UO3
  - 0.5 N HCl sediment digests for Fe(II) fraction (as % of total Fe) across horizons; 6MO/12MO; oxic vs E-D AM.

- 6. Phylogenetic_abundance_control_UO3
  - Microbial sequencing: relative abundance of microbial strains across horizons; oxic vs E-D AM; 12 samples; includes Fe/S-reducing groups and higher-level phylogeny.

- 7. Bulk_MicroXANES_UO3
  - U L3-edge XANES data (bulk and microfocus) from selected horizons and regions; oxic vs E-D AM; 6MO/12MO; data include absorption coefficients and energy (eV).

- 8. MicroEXAFS_UO3
  - Microfocus EXAFS data (U L3-edge) from discrete U-rich regions; 6MO/12MO; wavenumber, Chi(k)3, R, FT magnitude; best-fit models.

- 9. BulkEXAFS_UO3
  - Bulk EXAFS data (U L3-edge) from discrete U-rich regions; 6MO/12MO; wavenumber, Chi(k)3, R, FT magnitude; best-fit models.

- 10–27. Synchrotron XRF mapping data
  - XRF maps from resin-embedded thin sections; multiple beamlines; formats .txt and .nxs (DAWN compatible).
  - Element maps include Ca, Ti, Cr, Mn, Fe, Ni, Cu, Zn, Pb, U, Rb, Sr; full spectra in Nexus files.
  - Data cover 6MO and 12MO systems, both oxic and electron-donor amended; horizons in mm from sediment base.
  - File IDs correspond to specific sample sections (e.g., 6MO, 12MO; oxic or E-D AM) and processed XRF images.

## Data structure and formats
- Horizons expressed in millimeters from sediment base (with 5 mm interval convention in several datasets).
- Timepoints labeled as 6MO and 12MO; “OXIC” and “E-D AM” denote system type.
- Experimental outputs include concentrations (mM), percent Fe(II), pH, and qualitative/directed spectroscopy results.
- XRF data provided as separate text maps (element intensities) and Nexus spectra for comprehensive elemental distribution.

## Analytical methods represented
- Solid and solution analyses:
  - Aqua regia digests for U and Fe
  - ICP-MS for uranium; AES for Fe, Mn, Mg
  - Ion chromatography for sulfate, nitrate, nitrite, phosphate, and VFAs
  - pH measurements of effluents
  - Ferrozine assay for Fe(II) content
- Microbial and biogeochemical characterization:
  - Microbial sequencing for relative abundance of Fe- and sulfate-reducing taxa
- Spectroscopy and imaging:
  - U L3-edge XANES and EXAFS (bulk and microfocus)
  - Synchrotron XRF mapping for spatial distribution of elements, including uranium

## Relevance for environmental monitoring and data use
- Enables standardised, time-resolved assessment of uranium speciation and transport under varying redox and biogeochemical conditions.
- Demonstrates how metaschoepite dissolution influences uranium mobility, coupled with Fe redox chemistry and microbial activity.
- Provides comprehensive datasets (solutions, solids, microbes, and spectroscopy) suitable for integration into monitoring dashboards, policy assessments, and cross-study comparisons.
- Datasets are organized to facilitate cross-reference across horizons, timepoints, and system types, with clear metadata and file formats for reuse and portal upload.

## Reference
- Bower, W. R. et al. Metaschoepite Dissolution in Sediment Column Systems-Implications for Uranium Speciation and Transport. Environmental Science & Technology 2019, 53(16), 9915-9925. DOI: 10.1021/acs.est.9b02292