# Soil pyrogenic carbon (PyC) data from across the Amazon Basin

## Data overview
- Dataset 'pyc.csv' contains measurements of soil pyrogenic carbon (PyC), the ratio of %PyC to %Bulk Carbon, and organic carbon, from a soil fertility gradient in the Amazon Basin, all samples from old-growth forests.
- 49 forest plots sampled, 395 soil samples in total.
- 37 plots previously sampled for total organic carbon (TOC) following Quesada et al. 2010; 12 plots sampled in 2017.
- Collected under the NERC grant "Do past fires explain current carbon dynamics of Amazonian forests?" and CAPES Brazil support; additional support from CNPq, PPBio, FAPEMAT, and CAPES (postdoctoral fellowship) and CNPq scholarships.
- Related papers using this dataset include de Oliveira et al. (2022) and Koele et al. (2017).

## Collection methods
- Soil sampling with an auger.
- For plots ≥1 ha: minimum of five locations (four corners and center); for plots <1 ha: 3 locations (two corners and center).
- Depths sampled to 2 m, with intervals: 0–5, 5–10, 10–20, 20–30, 30–50, 50–100, 100–150, 150–200 cm.
- For each plot, samples were composite by depth interval (one sample per depth range per plot).

## Data analysis
- Samples air-dried, sieved, and analyzed for total organic carbon (TOC), PyC, and non-PyC fraction of organic carbon (OC) at the Centre for Tropical Environmental and Sustainability Science (James Cook University, Australia).
- PyC quantified using hydrogen pyrolysis (HyPy) as per Ascough et al. 2009.

## Nature and Units of recorded values
- Cpyc and OC reported as percentages of the sample.
- Cpyc/Cbulk reported as a percentage ratio (PyC to bulk carbon).

## Quality control
- Cpyc corrected from %BC using equation 2 from Wurster et al. 2012.
- Failed or non-convergent runs discarded; only valid data included.

## Details of data structure
- Data file: pyc.csv
- Columns:
  - Plot_number: plot code
  - Latitude, Longitude: geographic coordinates
  - depth_range: depth interval of the sample
  - Cpyc: Pyrogenic carbon concentration (%)
  - Cpyc_Cbulk: PyC to bulk carbon ratio (%)
  - OC: Organic carbon percentage (non-PyC)
  - forests_status: old-growth or disturbed
  - Rep: replication number for the same plot and depth range

## References
- Ascough, P. L., et al. (2009). Hydropyrolysis as a new tool for radiocarbon pre-treatment and the quantification of black carbon. Quaternary Geochronology, 4, 140-147.
- Quesada, C. A., et al. (2010). Variations in chemical and physical properties of Amazon forest soils in relation to their genesis. Biogeosciences, 7(5), 1515-1541.
- Wurster, C. M., et al. (2012). Quantifying the abundance and stable isotope composition of pyrogenic carbon using hydrogen pyrolysis. Rapid Communications in Mass Spectrometry, 26, 2690-2696.
- de Oliveira, E. A., et al. (2022). Soil pyrogenic carbon in southern Amazonia: Interaction between soil, climate, and aboveground biomass. Frontiers in Forests and Global Change, 5.
- Koele, N., et al. (2017). Amazon Basin forest pyrogenic carbon stocks: First estimate of deep storage. Geoderma, 306, 237-243.