# Metaschoepite dissolution in sediment column systems - groundwater/soil geochemistry and uranium X-ray spectroscopy data

## Overview
- Describes solid and solution phase geochemical trends for metaschoepite-doped sediment columns reacting with oxic or electron-donor amended synthetic groundwater, aged 6 or 12 months.
- Focuses on metaschoepite dissolution, uranium transport and speciation.
- Full experimental design, data collection, and interpretation are detailed in the associated peer-reviewed publication: Bower et al., Environmental Science & Technology, 2019, 53(16), 9915-9925. DOI: 10.1021/acs.est.9b02292.

## Data content and structure

- 1 Aqua_Regia_Sediment_Digests_ICPAES_UO3
  - Aqua regia extracts of U and Fe from multiple sediment horizons across four metaschoepite-doped columns.
  - Horizons listed in millimeters; oxic vs electron-donor amended (E-D AM); 6 months (6MO) and 12 months (12MO).

- 2 Column_Effluents_ICPMS_Control_UO3
  - ICP-MS U and AES Fe, Mn, Mg in column effluents from four metaschoepite-doped columns and two controls.
  - Periodic sampling up to 12 months; U analysed at higher temporal resolution.
  - Units in millimolar (mM); PV (cumulative pore volumes); data annotated as below detection (--) or not analysed (n.a.).

- 3 Column_Effluents_IC_Control_UO3
  - Ion chromatography of effluents for sulfate (SO4), nitrate (NO3), volatile fatty acids (VFA), nitrite (NO2), and phosphate (PO4).
  - Across four columns and controls; up to 12 months; 6MO/12MO; data in mM; timepoints in days.

- 4 Column_Effluents_pH_Control_UO3
  - pH of column effluents at selected time points.
  - Includes oxic vs E-D AM; up to 12 months; some values marked n.a. or PV.

- 5 Sediment_digests_Ferrozine_UO3
  - 0.5 N HCl extraction results showing Fe(II) proportion (as a percent of total Fe) by sediment horizon.
  - 6MO and 12MO; system type noted.

- 6 Phylogenetic_abundance_control_UO3
  - Microbial sequencing data for horizons from four columns and two controls.
  - Relative abundance of Fe- and sulfate-reducing strains; horizons in mm; 12 samples;  Oxic vs E-D AM distinctions.

- 7 Bulk_MicroXANES_UO3
  - Aligned and normalized raw U L3-edge XANES data (bulk and microfocus) from Diamond Light Source beamlines.
  - Data from bulk sediments or discrete elevated-U regions; system type (bulk vs micro-focus), oxic vs E-D AM, 6MO/12MO.
  - Includes absorption coefficient and standard alignment to yttrium foils; energy in eV; horizons in mm.

- 8 MicroEXAFS_UO3
  - Aligned and normalized raw U L3-edge EXAFS data from microfocus beamlines.
  - Regions of elevated U; system type (oxic vs E-D AM); 6MO/12MO; horizons in mm.
  - Data include wavenumber, Chi(k)3, R, FT magnitude, and fit models.

- 9 BulkEXAFS_UO3
  - Aligned and normalized raw U L3-edge EXAFS data from core spectroscopy beamline.
  - Similar structure to MicroEXAFS_UO3; includes k-space data, R, and FT Mag; 6MO/12MO; horizons in mm.

- Synchrotron XRF mapping data (.txt and .nxs)
  - XRF maps from resin-embedded thin sections; multiple beamlines at Diamond Light Source.
  - .txt files: coordinates (X, Y) and intensities for elements (Ca, Ti, Cr, Mn, Fe, Ni, Cu, Zn, Pb, U, Rb, Sr, etc.).
  - .nxs files: full emission spectra; used with DAWN Science Suite.
  - Data cover 6- and 12-month systems, including 12-month aged electron-donor amended and 6-month aged oxic datasets.
  - File naming includes multiple UO3-related maps (U-bearing regions across horizons).

- 10–28 Additional XRF map files
  - Specific UO3-related map files (e.g., UO3_1_1242_reform, UO3_2_1537_reform, etc.), corresponding to different horizons and aging conditions.

## Experimental design and conditions
- Columns doped with metaschoepite; exposed to oxic groundwater or electron-donor amended groundwater.
- Ageing periods: 6 months (6MO) and 12 months (12MO).
- Measurements span solid-phase digests (aqua regia), effluents (U, Fe, Mn, Mg, sulfate, nitrate, VFA, nitrite, phosphate, pH), sediment Fe(II) speciation, microbial community composition, and uranium speciation via XANES/EXAFS.
- Spatial dimension tracked via sediment horizons (millimeters from base) and XRF-mapped regions.

## Data governance and formats
- Multiple data types integrated for uranium geochemistry and microbiology (chemistry, spectroscopy, and imaging).
- Units and coding conventions documented (e.g., horizon in mm, concentrations in mM, PV).
- Data include quality indicators such as detection limits and not-analysed markers.
- Associated with a single peer-reviewed publication; full methods and interpretation available there and in supporting documentation.

## Provenance and usage
- Suitable for meta-analyses of uranium speciation and transport in sediment-column systems under varying redox conditions.
- Enables cross-dataset linkage between chemical speciation (aqua regia U/Fe, effluent chemistries, pH), solid-phase iron redox state (Fe(II) proportions), microbial community shifts, and uranium local structure (XANES/EXAFS) alongside spatial distributions from XRF maps.
- Ideal for data stewardship practices: comprehensive metadata, clear dataset identifiers, and formats conducive to discovery, interoperability, and reuse.

## Related publication
- Bower, W. R. et al. Metaschoepite Dissolution in Sediment Column Systems-Implications for Uranium Speciation and Transport. Environmental Science & Technology, 2019, 53(16), 9915-9925. DOI: 10.1021/acs.est.9b02292.