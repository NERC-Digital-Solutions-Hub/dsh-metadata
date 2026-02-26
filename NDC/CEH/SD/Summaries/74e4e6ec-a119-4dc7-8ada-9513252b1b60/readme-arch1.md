# Description This deposit contains river (fluvial) and surface water (pluvial) flooding maps for the Central Highlands of Vietnam and surrounding Provinces.

- What it is: flood inundation depth maps in metres at 30 m horizontal grid spacing for 10 return periods (1 in 5 to 1 in 1000 year events) across 11 provinces.
- Flood types: fluvial undefended (FUD), fluvial defended (FD), and pluvial (P); file names encode province, flood type, and return period.
- Purpose: support planners and policy makers in assessing areas at risk and inform policy relevant to sustainable development goals.

## Collection and generation methods

- Based on an updated Fathom 3.0 global flood model; improvements include channel conveyance capacity (Neal et al., 2021), design flood estimation (Zhao et al., 2021), and a 30 m FABDEM elevation dataset (Hawker et al., 2022).
- Model validation: compared against satellite imagery and household surveys (Hawker et al., in prep).

## Nature, units, and coverage

- Output: flood depth in metres for 10 return periods: 1in5, 1in10, 1in20, 1in50, 1in75, 1in100, 1in200, 1in250, 1in500, 1in1000.
- Provinces covered: Binh Dinh, Dak Lak, Dak Nong, Gia Lai, Khanh Hoa, Kon Tum, Lam Dong, Ninh Thuan, Phu Yen, Quang Nam, Quang Ngai.
- Three flood types: FUD (undefended), FD (defended), P (pluvial). FD adjusts river conveyance to reflect defence standards; FUD uses FABDEM-only defences.

## Data structure and file naming

- Contents: 330 GeoTiff files and 1 readme.
- For each province: 30 maps (10 per flood type).
- File naming convention: Province_FloodType_ReturnPeriod.tif (e.g., Quang_Ngai_FD_1in20.tif).
- Depth values: 0 = 0 m flooded; treat 0 as no-data for visualization or adjust color scales as needed.

## Experimental design and analysis

- Ten return periods selected to cover frequent to rare events and typical design 100-year benchmarks.
- Analytical use: compare modeled floods with observations (remote sensing, photos, articles, wrack marks) and compute skill scores (critical success index, hit rate, false alarm ratio, bias).

## Use in GIS and analysis recommendations

- Visualization: open GeoTiffs in GIS software (QGIS, ArcMap); consider setting 0 as no-data or start color scale at a small flooded threshold (e.g., 0.1 m).
- Spatial/statistical analysis: best performed in R or Python; track and utilize metadata and provenance for reproducibility.

## Limitations and notes

- Validation challenges: pluvial floods are difficult to validate due to short event durations.
- Defence realism: differences between FD and FUD are small given the 30 m resolution FABDEM data; defences not explicitly modeled beyond this resolution.
- Data use caution: model does not explicitly include non-visible defences beyond the elevation dataset.

## Data access and references

- Practical use: designed to inform planners and policy makers and contribute to SDG-related planning.
- References for model and data context include Sampson et al. (2015); Hawker et al. (2022); Neal et al. (2021); Zhao et al. (2021); and related validation work (Hawker et al., in prep).