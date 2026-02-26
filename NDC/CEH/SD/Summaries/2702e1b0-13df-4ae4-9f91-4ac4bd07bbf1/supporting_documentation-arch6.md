# Metaschoepite dissolution in sediment column systems - groundwater/soil geochemistry and uranium X-ray spectroscopy data

- Overview
  - A data collection describing solid and solution phase geochemical trends in metaschoepite-doped sediment columns reacting with flowing oxic or electron-donor amended synthetic groundwater.
  - Columns were sacrificed after 6 or 12 months to track metaschoepite dissolution, uranium transport, and speciation.
  - Full experimental details, data collection, and interpretation are published in Bower et al., Environmental Science & Technology, 2019 (DOI: 10.1021/acs.est.9b02292).

- Experimental design and scope
  - Four metaschoepite-doped columns plus two control systems.
  - Conditions: oxic groundwater and electron-donor amended groundwater; 6-month and 12-month reaction ages.
  - Data cover solid-phase digests, aqueous effluents, pH, redox-related species, microbial community shifts, and uranium speciation via X-ray spectroscopy.

- Datasets and contents
  - 1. Aqua_Regia_Sediment_Digests_ICPAES_UO3
    - Aqua regia extractable U and Fe by horizon (5 mm intervals) across oxic and electron-donor amended systems; 6MO and 12MO.
  - 2. Column_Effluents_ICPMS_Control_UO3
    - U (ICP-MS) and Fe, Mn, Mg (AES) in column effluents; four metaschoepite-doped columns plus two controls; up to 12 months; timepoints tabulated; units in mM; includes pore volumes (PV) and detection-limit flags.
  - 3. Column_Effluents_IC_Control_UO3
    - Ion chromatography of effluents; sulfate, nitrate, volatile fatty acids, nitrite, phosphate; up to 12 months; four columns plus controls; 6MO/12MO; units in mM; PV and special flags.
  - 4. Column_Effluents_pH_Control_UO3
    - pH of effluents at selected timepoints for all columns; up to 12 months; PV and not-analysed markers.
  - 5. Sediment_digests_Ferrozine_UO3
    - 0.5 N HCl extraction results (Fe(II) fraction as % of total Fe) by horizon; oxic and electron-donor amended; 6MO/12MO.
  - 6. Phylogenetic_abundance_control_UO3
    - Microbial sequencing: relative abundance of Fe- and sulfate-reducing strains by sediment horizons; includes broader phylogenetic class divisions; sampled up to 12 months; oxic and amended systems.
  - 7. Bulk_MicroXANES_UO3
    - Aligned and normalized U L3-edge XANES data (bulk sediments and microfocus) from selected horizons or regions; system type (bulk vs microfocus; oxic vs E-D AM); 6MO/12MO; data include absorption coefficients and energy in eV; horizons in mm from column base.
  - 8. MicroEXAFS_UO3
    - Aligned and normalized U L3-edge EXAFS data from discrete elevated-U regions; 6MO/12MO; wavenumber (Å^-1), Chi(k)3, R, FT Mag; best-fit model reported.
  - 9. BulkEXAFS_UO3
    - Core spectroscopy EXAFS data from discrete elevated-U regions; 6MO/12MO; wavenumber (Å^-1), Chi(k)3, R, FT Mag; best-fit model reported.
  - Synchrotron XRF mapping data (files 10–28)
    - XRF maps from resin-embedded thin sections; multiple beamlines; .txt files contain X, Y coordinates and element intensities (Ca, Ti, Cr, Mn, Fe, Ni, Cu, Zn, Pb, U, Rb, Sr, etc.); .nxs Nexus files contain full emission spectra.
    - Data describe element distributions in the soil matrix after 6 or 12 months of simulant groundwater flow.
    - Notable groupings:
      - 10–13: UO3_XRF maps from 12-month aged, electron-donor amended system (example filenames provided).
      - 14–17: UO3_XRF maps from 6-month aged, electron-donor amended system.
      - 18–24: UO3_XRF maps from 6-month aged, oxic system.
      - 25–28: UO3_XRF maps from 12-month aged, electron-donor amended system.
  - General notes across datasets
    - System design uses metaschoepite-doped columns and control columns; measurements span major elements relevant to uranium geochemistry (U, Fe, Mn, S ranges via VFA/Nitrate/Sulfate, etc.), redox indicator data (pH, Fe(II) from ferrozine digestion), microbial community shifts, and advanced spectroscopic characterization (XANES/EXAFS) for uranium speciation.
    - Temporal resolution includes 6-month and 12-month endpoints with periodic sampling for effluents.
    - Some data are reported as below detection limits (--), not analysed (n.a.), or cumulative pore volumes (PV).

- Related publication and data accessibility
  - Experimental framework and interpretation described in Bower et al., 2019, EST 53(16), 9915-9925.
  - DOI: 10.1021/acs.est.9b02292
  - Data types span standard geochemical analyses, microbial sequencing, and synchrotron-based spectroscopic techniques, enabling multi-omics and geochemical modelling approaches.

- Practical considerations for data use
  - Data are suitable for cross-dataset integration to study uranium dissolution, speciation, and transport under oxic vs electron-donor conditions.
  - Allows comparison of solid-phase U/Fe partitioning (aqua regia digests, ferrozine Fe(II)) with aqueous phase chemistry (U, Fe, Mn, Mg, sulfate, nitrate, VFA, nitrite, phosphate) and redox-sensitive parameters (pH, microbial community shifts).
  - Rich spectroscopic and imaging data (XANES/EXAFS and XRF maps) support spatially-resolved uranium speciation and distribution analyses.
  - Users should note data flags (below detection, not analysed, PV) and horizon-based sampling (5 mm intervals) when aggregating or modelling.