# RECOUP-Moor Environmental data: Methodology

## Overview
- Describes post-fire peatland field study at the Stalybridge estate (Saddleworth Moor, UK), where a wildfire in June–July 2018 removed surface vegetation over 18 km².
- Aims to generate a standardized dataset on plot-scale soil chemistry and temperature to enable robust analyses of burn severity and post-fire peat properties.

## Field Site and Study Design
- Field site: blanket bog dominated by Calluna vulgaris and Eriophorum vaginatum.
- Experimental plots: 10 plots, each 10 m x 10 m, established October 2018 at the post-fire site.
- Burn severity: 5 plots with shallow (less severe) burn, 5 plots with deep (more severe) burn; all plots had surface vegetation removed exposing bare peat.
- Geospatial metadata collected: location coordinates, elevation, slope.
- Temporal metadata: soil temperature measured at multiple time points over 24 months.

## Sampling, Preparation, and Laboratory Analysis
- Sampling date: July 23, 2019; peat surface samples (5 cm x 5 cm x 2 cm) collected from each plot, homogenized, and stored at approximately 5°C until analysis.
- Sample preparation: dried at 70°C for 72 hours, crushed to a fine homogeneous powder.
- Carbon and nitrogen analysis: three subsamples per plot, combusted at 1800°C; carbon and nitrogen percentages quantified with a Vario Micro Cube; per-plot values are the average of the three sub-samples.
- Elemental composition: ICP-MS analysis on two subsamples per plot to determine 22 elements; per-plot values are the average of the two sub-samples.

## Data Variables and Metadata
- Key field identifiers:
  - Plot_number, Plot_ID (distinguishes burn category and replicates: S1-5 shallow burn, D1-5 deep burn, R1-5 unburned/reference)
  - N_Coor (latitude), W_Coor (longitude)
  - Temp_Oct18, Temp_May19, Temp_Jul19 (soil temperatures at specified dates)
  - CN_ratio (carbon-to-nitrogen ratio)
  - C_cont (carbon content %), N_cont (nitrogen content %)
  - Slope (slope angle °), Elevation (m above sea level)
  - Al, As, B, Ca, Cd, Co, Cr, Cu, Fe, Hg (noted as Silver content in description), K, Mg, Mn, Mo, Ni, P, Pb, S, Si, Sr, Zn (mg/g)
- This structured variable key supports clear provenance, unit specification, and compatibility with data portals and catalogues.

## Data Quality, Provenance, and Reproducibility
- QA steps include homogenization checks by comparing three CN sub-samples for consistency within each plot.
- Replication: analysis uses averages across subsamples (three CN sub-samples; two ICP-MS sub-samples) to derive per-plot values.
- Clear documentation of sampling design (burn severity categories, plot size) and analytical methods (instruments, temperatures, and procedures) to support reproducibility and re-use.

## Data Management and Sharing Readiness
- The dataset is organized with explicit metadata fields and units, enabling cataloguing and discovery.
- Methodology aligns with data stewardship practices for sharing: prepares datasets suitable for upload to relevant portals and catalogues, with traceable provenance and well-defined variables.