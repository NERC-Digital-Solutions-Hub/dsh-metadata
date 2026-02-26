# Soil pyrogenic carbon (PyC) data from across the Amazon Basin

## Data overview
- Dataset pyc.csv contains measurements of soil pyrogenic carbon (PyC), the ratio of %PyC to %Bulk Carbon, and organic carbon (OC) across a soil fertility gradient in the Amazon Basin.
- Samples come from old-growth forests: 49 forest plots with a total of 395 soil samples.
- 37 plots had prior sampling for total organic carbon (TOC) using a protocol from Quesada et al. 2010; 12 plots were sampled in 2017.
- Supported by: NERC grant NE/N011570/1 and CAPES Brazil; additional support from CNPq, PPBio, and FAPEMAT; CAPES postdoctoral fellowship; and CNPq postdoctoral scholarship.
- Related publications using this dataset include studies by de Oliveira et al. (2022) and Koele et al. (2017).

## Collection methods
- Auger sampling conducted in forest plots.
- Plot sampling design: plots ≥1 ha sampled at least at five locations (corners and centre); plots <1 ha at three locations (two corners and centre).
- Depths sampled to 2 m with intervals: 0–5, 5–10, 10–20, 20–30, 30–50, 50–100, 100–150, 150–200 cm.
- For each plot, samples were composited by depth interval, yielding one sample per depth range per plot.

## Measurements and variables
- For each sample, measurements include:
  - PyC concentration (Cpyc) as a percentage of the sample.
  - PyC to bulk carbon ratio (Cpyc_Cbulk) as a percentage.
  - Organic carbon (OC) as a percentage.
- Units: Cpyc and OC are percentages; Cpyc_Cbulk is a percentage ratio.
- All samples processed to quantify PyC using hydrogen pyrolysis (HyPy) after air-drying and sieving.

## Data processing and quality assurance
- PyC quantified via HyPy; TOC and non-PyC fractions measured as part of the dataset.
- Cpyc values corrected from %BC (black carbon) following equation 2 from Wurster et al. (2012).
- Samples with failed runs or non-convergent results were discarded.

## Data structure and content
- File: pyc.csv (CSV format).
- Columns:
  - Plot_number: plot code
  - Latitude: plot location
  - Longitude: plot location
  - depth_range: depth interval of the sample
  - Cpyc: pyrogenic carbon concentration (%)
  - Cpyc_Cbulk: PyC to bulk carbon ratio (%)
  - OC: organic carbon (%)
  - forests_status: forest type (old-growth or disturbed)
  - Rep: replication count for the same plot and depth

## References and context
- Methodologies and context:
  - Ascough et al. (2009): Hydrogen pyrolysis for PyC quantification
  - Quesada et al. (2010): TOC properties in Amazonian soils
  - Wurster et al. (2012): Correction for PyC via black carbon adjustments
- Related studies using the dataset:
  - de Oliveira et al. (2022): Soil PyC in southern Amazonia; interactions among soil, climate, and aboveground biomass
  - Koele et al. (2017): Amazon Basin forest PyC stocks and deep storage

## Data provenance and usage
- Collected as part of ongoing research on soil carbon dynamics in the Amazon and linked to broader questions about fire history and carbon cycling.
- The dataset is attached as pyc.csv and is suitable for analyses of PyC distribution across depth, plot location, forest status, and PyC/OC relationships.
- Suitable for modelling the influence of depth, location, and forest status on PyC concentration and PyC_Bulk relationships.

## Funding and acknowledgments
- Supported by NERC grant NE/N011570/1; CAPES Brazil (PVE177-2012); CNPq; PPBio; FAPEMAT; CAPES (postdoctoral fellowship) and Brazilian research productivity scholarships.