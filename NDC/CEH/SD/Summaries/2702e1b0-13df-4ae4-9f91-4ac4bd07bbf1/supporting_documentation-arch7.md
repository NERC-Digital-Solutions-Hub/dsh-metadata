# Metaschoepite dissolution in sediment column systems - groundwater/soil geochemistry and uranium X-ray spectroscopy data

## Overview
- Describes solid and solution phase geochemical trends in metaschoepite-doped sediment columns under oxic or electron-donor amended groundwater.
- Tracks metaschoepite dissolution, uranium transport, and speciation after 6 or 12 months.
- Linked to the peer-reviewed publication: Bower et al., Environ. Sci. Technol. 2019; DOI: 10.1021/acs.est.9b02292.

## Experimental design and scope
- Four metaschoepite-doped columns plus two control systems.
- Sampling along column horizons at 5 mm intervals (dataset 1).
- Timepoints: 6 months (6MO) and 12 months (12MO).
- System types: oxic groundwater (OXIC) and electron-donor amended groundwater (E-D AM).
- Multimodal data types spanning geochemistry, microbiology, and mineral speciation.

## Datasets and content (summaries)
- Dataset 1: Aqua Regia Sediment Digests_ICPAES_UO3
  - Aqua regia extractable U and Fe by horizon (mm intervals; horizons compression-adjusted).
- Dataset 2: Column_Effluents_ICPMS_Control_UO3
  - U, Fe, Mn, Mg in column effluents; high-temporal-resolution U by ICP-MS; 6MO/12MO; OXIC/E-D AM; values in mM; PV noted.
- Dataset 3: Column_Effluents_IC_Control_UO3
  - Sulfate, nitrate, volatile fatty acids, nitrite, phosphate in effluents; timepoints up to 12 months; same system categories.
- Dataset 4: Column_Effluents_pH_Control_UO3
  - pH of effluents; up to 12 months; labels for not analysed (n.a.) and pore volumes (PV).
- Dataset 5: Sediment_digests_Ferrozine_UO3
  - 0.5 N HCl extraction; Fe(II) fraction by horizon (% of total Fe); 6MO/12MO; OXIC/E-D AM.
- Dataset 6: Phylogenetic_abundance_control_UO3
  - Microbial relative abundance by horizon; Fe and sulfate-reducing strains; 6MO/12MO; OXIC/E-D AM.
- Dataset 7: Bulk_MicroXANES_UO3
  - Aligned/normalized U L3-edge XANES data (bulk and microfocus) from bulk sediments or XRF-mapped regions; horizons in mm; system type, 6MO/12MO.
- Dataset 8: MicroEXAFS_UO3
  - Aligned/normalized microfocus EXAFS data; k-space data; R and FT Mag; 6MO/12MO; horizons in mm.
- Dataset 9: BulkEXAFS_UO3
  - Aligned/normalized core/external EXAFS data; k-space data; 6MO/12MO; horizons in mm.
- Synchrotron XRF mapping data (text (.txt) and Nexus (.nxs) files)
  - XRF maps from resin-embedded thin sections; multiple beamlines; text files contain X, Y coordinates and intensities for elements (Ca, Ti, Cr, Mn, Fe, Ni, Cu, Zn, Pb, U, Rb, U, Sr); Nexus files contain full emission spectra.
- Datasets 10–28: Specific XRF map files
  - UO3_1_1242_reform, UO3_2_1537_reform, UO3_3_4159_reform, UO3_4_i18-83854_processed_170207_100633, …, UO3_19_i18-98894-xrf_window2-Xspress3A
  - XRF maps cover 6-month and 12-month aged systems under oxic or electron-donor amended conditions.

## Spatial and temporal scope
- Horizons expressed in millimeters from sediment base; column axis as the primary spatial dimension.
- Four metaschoepite-doped columns plus two controls (spatial context: along column).
- Temporal resolution at 6MO and 12MO timepoints; XRF maps provide spatial distributions at these ages.

## Data formats and access
- Data include raw and processed forms; some datasets are aligned and normalized (EXAFS/XANES).
- File formats: .txt and .nxs (Nexus) for XRF maps; DAWN Science Suite-compatible Nexus files; energy values in eV; XRF coordinates and intensities; XAFS data with k-space, R, FT Mag.
- Full methodological details and interpretation available in the cited publication; related data and documentation described in the associated supporting materials.
- Access notes: XRF Nexus files are intended for use with Diamond Light Source data tools (DAWN).

## GIS relevance and potential applications
- Enables creation of geospatial layers showing mm-scale chemical and mineralogical distributions along sediment columns.
- Integrates multi-omic, redox, and mineral data with geochemical concentrations to produce layered GIS visuals.
- Time-series GIS visuals contrasting 6MO vs 12MO under oxic vs electron-donor amended conditions.
- 2D cross-sections and potential 3D visualizations of uranium speciation, transport, and mineral phase changes.
- Ability to map element distributions (U, Fe, Mn, Mg, S, P, etc.) against microbial communities and pH changes.
- Supports spatially explicit modeling of uranium speciation and transport in controlled sediment-column analogs.

## Data quality, notes and caveats
- Some measurements have detection-limits or are not analysed (noted in datasets).
- Horizon-based sampling introduces fixed-grid spatial interpretation; PV and horizon compression considerations apply.
- Data are specific to controlled column experiments and may require careful translation for field-scale GIS analyses.

## Reference
- Publication: Bower, W. R., et al. Metaschoepite Dissolution in Sediment Column Systems - Implications for Uranium Speciation and Transport, Environmental Science & Technology, 2019; DOI: 10.1021/acs.est.9b02292