# Soil pyrogenic carbon (PyC) data from across the Amazon Basin

## Data overview
- Dataset name: pyc.csv
- Contents: measurements of soil pyrogenic carbon (PyC), %PyC to %Bulk Carbon, and organic carbon
- Scope: collected in a soil fertility gradient across the Amazon Basin, all samples from old-growth forests
- Samples and plots: 49 forest plots, 395 soil samples total
- Plot history: 37 plots previously sampled with TOC analysis (Quesada et al. 2010), 12 plots sampled in 2017
- Funding and affiliations: NERC grant NE/N011570/1; CAPES Brazil; CNPq; PPBio; FAPEMAT; CAPES postdoctoral fellowship
- Related publications that include the dataset: 
  - de Oliveira et al. (2022) Frontiers in Forests and Global Change
  - Koele et al. (2017) Geoderma

## Collection methods
- Sampling technique: soil auger
- Plot sampling design: ≥1 ha plots sampled at a minimum of five locations (three in smaller plots)
- Depths sampled: 0-5, 5-10, 10-20, 20-30, 30-50, 50-100, 100-150, 150-200 cm
- Sample strategy: composite samples by depth interval, yielding one sample per depth range per plot

## Data analysis
- Preparation: air-dried, sieved soil samples
- Measurements: total organic carbon (TOC), PyC, and non-PyC fraction of organic carbon (OC)
- PyC quantification method: hydrogen pyrolysis (HyPy; Ascough et al. 2009)

## Nature and units of recorded values
- Cpyc and OC: expressed as percent of the sample
- Cpyc_Cbulk: ratio of pyrogenic carbon to bulk carbon, expressed as a percent

## Quality control
- Correction: Cpyc percentage corrected from %BC (black carbon) using Equation 2 from Wurster et al. (2012)
- Data screening: failed or non-convergent runs discarded and not included

## Details of data structure
- File format: comma-separated values (pyc.csv)
- Columns:
  - Plot_number: plot code number
  - Latitude: geographic latitude
  - Longitude: geographic longitude
  - depth_range: depth interval of the sample
  - Cpyc: pyrogenic carbon concentration (%)
  - Cpyc_Cbulk: pyrogenic carbon to bulk carbon ratio (%)
  - OC: organic carbon (non-pyrogenic %) 
  - forests_status: forest type (old-growth or disturbed)
  - Rep: number of repetitions for the same plot/depth

## References
- Ascough, P. L. et al. (2009). Hydropyrolysis for PyC quantification. Quaternary Geochronology
- Quesada, C. A. et al. (2010). Variations in soil properties in relation to genesis. Biogeosciences
- Wurster, C.M. et al. (2012). Quantifying PyC via hydrogen pyrolysis. Rapid Communications in Mass Spectrometry

## Data stewardship and usage considerations
- Provenance: clearly linked to field sampling across Amazon plots with historical TOC data in some plots
- Metadata depth: includes location, depth range, forest status, and replication
- Reuse potential: suitable for analyses of PyC stocks, PyC/OC dynamics, and depth-wise PyC distribution in old-growth Amazon forests
- Governance notes: data are described with collection, processing, and quality-control steps; provenance and methods should be maintained for future re-use and integration with other datasets
- caveats: combining with other datasets may require harmonization of depth intervals, units, and PyC quantification methods across studies