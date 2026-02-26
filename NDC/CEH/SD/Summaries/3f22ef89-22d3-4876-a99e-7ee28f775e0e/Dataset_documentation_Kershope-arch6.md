# Solute concentrations in water samples from clearfelled and standing Sitka spruce ( Picea sitchensis ) forest ecosystems, Kershope Forest

## Overview
- Dataset describes solute concentrations in drainage water and other water samples from a Sitka spruce forest ecosystem at Kershope, England.
- Focuses on solutes including potassium, calcium, magnesium, iron, sodium, aluminium, phosphate, nitrate, ammonium, chloride, sulphate, plus pH, suspended solids (TSS), and total organic carbon (TOC).
- Timeframe: drainage water samples collected 17/6/1981–30/12/1987; water samples 17/6/1981–23/12/1985.
- Study design centers on six plots in Block 1 of a drainage experiment: three plots remained standing, three were clearfelled at 35 years; weekly sampling across various pathways to understand nutrient fluxes and the hydrological impact of felling.

## Geographic coverage and site description
- Location: Kershope Forest, Cumbria, England; peaty gley soil over calcareous till; Sitka spruce planted in 1948.
- Experimental setup: six plots (approximately 2–3 ha each) with different drain spacings and depths; three plots felled in 1983, three left as controls.
- Plot treatments include variations in drain spacing (10–40 m) and drain depth (60–90 cm); felled periods in 1983 (May–Dec or Apr–Oct depending on plot).

## Sampling design and data collection
- Water collected from six ditch systems draining individual plots; weekly drainage-water sampling begun two years pre-felling and continued through and after felling.
- Additional sampling of ecosystem components: soil solution samplers, lysimeters, rainfall, stemflow, throughfall, throughflow, and needle-tray brash throughfall.
- Drainage-water sampling used a 2 m PVC sampling pipe at the main exit drain; discharge measured with a V-notch weir.
- Other ecosystem samples collected at plot-level intervals (commonly fortnightly for some components); Knapp throughflow data noted as unreliable due to equipment issues.

## Data files and structure
- Drainsker.csv: solute data from drainage water across six main drains; includes sampling occasion, date, sample code, discharge (m3 s-1), soluble constituents (mg L-1 or related units), pH, TOC, TSS. A value of -1 indicates no sample.
- Soilsker.csv: solute data from diverse samplers in the forest ecosystem (e.g., stemflow, stem, lysimeters, soil horizons, throughfall, needle trays); includes week codes, sampling volumes, pH, and nutrient concentrations (K, Ca, Mg, Fe, Na, Al, PO4P, NO3N, NH4N, Cl, SO4S, TOC).
- Kershope_sampling_points.csv: sampling-location metadata (plot name, felled status, block, drain spacing and depth, geographic coordinates in Easting/Northing).
- Kershope_codes (referenced as the key for soil sampler/sample codes): mapping between sample codes and their meanings (e.g., sample types, horizons, felled/unfelled).

## Measurements and analytical methods
- Chemical analyses performed at the Merlewood Chemical Analysis Section; methods included:
  - pH measurement after settling.
  - Filtration through Whatman GF/F.
  - Atomic absorption for Ca, Mg, Al, Fe; flame emission for K and Na.
  - Phosphate (PO4-P) via molybdenum blue; ammonium (NH4-N) via indophenol blue.
  - Chloride by thiocyanate method (early years); nitrate via reduction with hydrazine and Griess-Hosvay method; sulfate by barium chloride turbimetric method (later IC methods used for some ions).
  - TOC and suspended solids measured by standard techniques.
- Data include both historical measurement methods and overlapping methods to ensure comparability.

## Site-specific study design details
- Block 1 of the original drainage experiment contained six plots with varying drain configurations; three plots felled in 1983, three remained unfelled.
- Drainage water was sampled from the main exit drain with careful avoidance of floor disturbance; instantaneous discharge recorded.
- Additional water-pathway measurements captured nutrient fluxes through soil horizons, rainfall input, stemflow, throughfall, and organic-rich inputs (needle litter), enabling assessment of nutrient sources and fluxes through the forest system.

## Data use, potential products, and analyses
- Suitable for analyses of:
  - Temporal trends in nutrient concentrations and pH associated with clearfelling.
  - Differences in nutrient fluxes between felled and unfelled plots.
  - Partitioning of nutrients across different hydrological pathways (drainage water, soil solution, rainfall, stemflow, throughfall, lysimeters, needles).
  - Impacts on soil fertility and potential downstream ecological effects.
- Data products that Data Support can help generate:
  - Time-series dashboards of key solutes by plot, treatment, and year.
  - Pivot tables comparing pre- and post-felling periods.
  - Nutrient flux calculations using paired discharge and concentration data.
  - Geographic and sampling-path visualizations using Kershope_sampling_points.csv coordinates.
- Potential integration with publications and related datasets (e.g., studies from Beddgelert Forest) for broader analysis of conifer harvesting effects on soil and water chemistry.

## Data quality, limitations, and considerations
- Patchy data across multiple components and methods; some historical methods overlapped with newer ones.
- Some sampling pathways (e.g., Knapp throughflow) have reliability caveats noted in the metadata.
- -1 values denote missing samples; interpretation requires consulting the code mappings in Kershope_codes.csv.
- The dataset is context-specific to upland British forestry and may require geospatial and unit alignment when combining with other datasets.

## References and further reading
- Key publications relating to this dataset and its analyses:
  - Adamson, J. & Hornung, M. (1990). The effect of clearfelling a Sitka spruce plantation on solute concentrations in drainage water. Journal of Hydrology.
  - Adamson, J., Hornung, M., Pyatt, D., & Anderson, A. (1987). Changes in solute chemistry of drainage waters following the clearfelling of a Sitka spruce plantation. Forestry.
  - Allen, S. E. (Ed.). (1989). Chemical Analysis of Ecological Materials.
  - Pyatt, D. G., Anderson, A. R., Stannard, J. P., & White, I. M. S. (1985). A drainage experiment on a peaty gley soil at Kershope Forest.
  - Rowland, A. P. (1983). Automated method for ammonium-N determination.
- Additional context and methodological references for sampling and analysis are provided within the dataset description.