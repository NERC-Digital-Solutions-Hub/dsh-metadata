# Metaschoepite dissolution in sediment column systems - groundwater/soil geochemistry and uranium X-ray spectroscopy data

## Overview
- A multi-modal dataset accompanying a study of metaschoepite-doped sediment columns reacting with oxic or electron-donor amended groundwater, tracked over 6 and 12 months.
- Aims to characterize metaschoepite dissolution, uranium transport, and speciation using geochemical, microbial, and spectroscopic data.
- Full experimental methods, data collection, and interpretation are documented in the related peer-reviewed publication and supporting materials (Bower et al., ENV SCI TECHNOL 2019; DOI: 10.1021/acs.est.9b02292).

## Experimental design and scope
- System setup: four metaschoepite-doped columns plus two control columns.
- Redox conditions: oxic groundwater and electron-donor amended groundwater.
- Timepoints: 6 months (6MO) and 12 months (12MO).
- Spatial resolution: sediment horizons sampled at 5 mm intervals from the base of the column.
- Data breadth: combines aqua regia digests, effluent chemistries, pH, Fe(II) fractions, microbial communities, and advanced spectroscopy plus XRF imaging.

## Key datasets and what they contain
- 1. Aqua_Regia_Sediment_Digests_ICPAES_UO3
  - Aqua regia extractable U and Fe by horizon; horizons are compression-adjusted (mm).
- 2. Column_Effluents_ICPMS_Control_UO3
  - U by ICP-MS; Fe, Mn, Mg by AES in effluents for all columns over up to 12 months; includes detection limits and pore volumes.
- 3. Column_Effluents_IC_Control_UO3
  - IC measurements of Sulfate, Nitrate, Volatile Fatty Acids (VFA), Nitrite, Phosphate; timepoints across columns (6MO/12MO).
- 4. Column_Effluents_pH_Control_UO3
  - pH of effluents at selected times; oxic vs electron-donor amended conditions.
- 5. Sediment_digests_Ferrozine_UO3
  - 0.5 N HCl extraction giving Fe(II) proportion (% of total Fe) by horizon.
- 6. Phylogenetic_abundance_control_UO3
  - Microbial sequencing: relative abundance of Fe- and sulfate-reducing strains by horizon; includes broader phylogenetic classifications.
- 7. Bulk_MicroXANES_UO3
  - U L3-edge XANES (bulk and microfocus) on sediments and discrete elevated-U regions; includes absorption coefficients and beamline context.
- 8. MicroEXAFS_UO3
  - Microfocus EXAFS (U L3-edge) for discrete elevated-U regions; k-space data and model fits.
- 9. BulkEXAFS_UO3
  - Core beamline EXAFS on discrete elevated-U regions; includes R and Fourier transform details and fits.
- 10–28. Synchrotron XRF mapping data and related files
  - XRF maps from resin-embedded thin sections; text files contain X, Y coordinates and element intensities for Ca, Ti, Cr, Mn, Fe, Ni, Cu, Zn, Pb, U, Rb, Sr; Nexus (.nxs) files offer full emission spectra.
  - Specific UO3 data files correspond to 6MO and 12MO systems under oxic and electron-donor amended conditions (examples: 10–13, 14–17, 18–28 with system-specific naming).

## Data context, variables, and metadata considerations
- System identifiers: OXIC (oxic) vs E-D AM (electron-donor amended); timepoints 6MO/12MO; horizons in millimeters from column base.
- Units and measurements:
  - Concentrations reported in millimolar (mM) for aqueous species.
  - Fe(II) percentages as a fraction of total Fe.
  - X-ray spectroscopy data includes standard XANES/EXAFS metadata (k-space, R, FT magnitude, fits).
- Data lineage and provenance:
  - Linked to a peer-reviewed study and Diamond Light Source beamline data; references and supporting documentation provide full methodological context.
- Data formats and access notes:
  - XRF mapping data provided as text (.txt) and Nexus (.nxs) files; Nexus files require DAWN Science Suite to open.
  - Other datasets are tabular or spectrum data from standard geochemical and spectroscopic analyses.

## Data governance, quality, and interoperability considerations
- Rich, cross-domain dataset enabling integrated analyses across chemistry, microbiology, and mineralogy, suitable for uranium transport and speciation modeling.
- Metadata discipline needed for discoverability: clearly defined units, system type, timepoint, horizon, method, instrument, and beamline identifiers.
- Potential data gaps or considerations:
  - Detection limits and non-detections clearly indicated (e.g., “--” for below detection).
  - Temporal and spatial alignment across datasets essential for integrative analyses.
- Best-practice reuse potential:
  - Benchmark for uranium speciation and transport under varying redox and organic-carbon conditions.
  - Cross-study comparisons within a broader data platform focusing on geochemical and microbiological drivers of U mobility.
  - Standardization opportunities for multi-modal datasets (chemical, microbial, spectroscopic, and imaging data).

## Reuse and citation guidance
- Primary publication: Bower, W. R. et al., Metaschoepite Dissolution in Sediment Column Systems—Implications for Uranium Speciation and Transport, Environmental Science & Technology, 2019, 53(16), 9915-9925.
- DOI: 10.1021/acs.est.9b02292
- For data access and detailed method notes, refer to the publication and associated supporting documentation from Diamond Light Source data packages.