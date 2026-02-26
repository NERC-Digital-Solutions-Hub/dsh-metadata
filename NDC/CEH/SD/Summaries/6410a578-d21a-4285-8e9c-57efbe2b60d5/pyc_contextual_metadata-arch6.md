# Soil pyrogenic carbon (PyC) data from across the Amazon Basin

- Data overview
  - The pyc.csv dataset contains measurements of soil pyrogenic carbon (PyC), the ratio of PyC to bulk carbon, and organic carbon (OC) across a soil fertility gradient in the Amazon Basin, focusing on old-growth forests.
  - Sampling covers 49 forest plots (395 soil samples total); 37 plots were previously sampled for TOC, and 12 plots were sampled in 2017.
  - Collected under the NERC grant “Do past fires explain current carbon dynamics of Amazonian forests?” and supported by CAPES, CNPq, PPBio, FAPEMAT, and CAPES/Brazil fellowships.
  - Related research papers include de Oliveira et al. (2022) and Koele et al. (2017).

- Collection methods
  - Soil samples taken with an auger.
  - Plot design: in plots ≥1 ha, at least five locations (four corners and center); in plots <1 ha, three locations (two corners and center).
  - Depths sampled to 2 m, with main intervals: 0–5, 5–10, 10–20, 20–30, 30–50, 50–100, 100–150, 150–200 cm.
  - For each plot, samples were composited by depth interval to yield one sample per depth range per plot.

- Measurements and analysis
  - Air-dried, sieved samples analyzed for total organic carbon (TOC), PyC, and non-PyC organic carbon (OC).
  - PyC quantified using hydrogen pyrolysis (HyPy).
  - Units: Cpyc and OC in percent of sample; Cpyc/Cbulk (PyC to bulk carbon) in percent.
  - Cpyc values corrected from %BC (black carbon) using equation 2 from Wurster et al. (2012).

- Data quality and processing
  - Failed runs or non-convergent results discarded; only valid measurements retained.

- Data structure and file format
  - File: pyc.csv
  - Columns:
    - Plot_number: plot code
    - Latitude
    - Longitude
    - depth_range: sampling depth interval
    - Cpyc: PyC concentration (%)
    - Cpyc_Cbulk: PyC to bulk carbon ratio (%)
    - OC: Organic carbon (%)
    - forests_status: old-growth or disturbed
    - Rep: replication count for the given plot/depth range

- Context, usage, and references
  - Dataset supports cross-site synthesis of soil PyC across the Amazon and informs soil carbon dynamics studies.
  - References include methods and related findings (Ascough et al. 2009; Quesada et al. 2010; Wurster et al. 2012) and two key publications (de Oliveira et al. 2022; Koele et al. 2017).