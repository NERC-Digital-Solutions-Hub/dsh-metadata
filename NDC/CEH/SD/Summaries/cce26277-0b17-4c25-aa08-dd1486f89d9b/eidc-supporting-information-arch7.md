# Hydraulic mobility of aquatic insect (Trichoptera) bioconstructions and incorporated sediments

## Overview
- Experimental focus: hydraulic flume study quantifying how caddisfly case construction affects sediment transport in rivers.
- Species/case styles: two tubular case builders (Potamophylax latipennis, Sericostoma personatum) and one domed case builder (Agapetus fuscipes).
- Method: 11 increasing discharge steps; bed sediment transport assessed by photos at each stage; cases/sediment placed at flume center.
- Temporal scope: flume experiments conducted 20 Aug–20 Sep 2019; caddisflies collected 17 Jun and 18 Aug 2019.
- Outputs: four data files containing post-processed velocimetry, grain-size distributions, entrainment data, and case/sediment thresholds.

## Data files (S1–S4)

- S1_Velocimetry_data
  - Description: acoustic Doppler velocimetry outputs per discharge step; post-processed velocities and turbulence metrics.
  - Key variables: Date, Discharge_step, Umean_raw/Ustd_raw, Umean/Ustd, Vmean_raw/Vstd_raw, Vmean/Vstd, Wmean_raw/Wstd_raw, Wmean/Wstd, U_corr, U_SNR, V_corr, V_SNR, W_corr, W_SNR, TKE, Tb.
  - Purpose: derive mean flow fields and bed shear stress for each flow stage.

- S2_Case-grain-size-distribution_data
  - Description: grain-size distributions from sieving case sediments; mass before/after sieving and losses.
  - Key variables: Sample_ID, Sed_mass, Sieved_mass, Loss_mass, Loss_percent, sieve size references (mm).
  - Purpose: characterize sediment packaging within each case for transport potential.

- S3_Entrainment_data
  - Description: percentage of sediment entrained during each flow stage; derived from photographic analysis.
  - Key variables: Sample_ID, State (Case or loose sediment), Discharge_step, Values (cumulative % area transported).
  - Purpose: quantify entrainment response as flow increases.

- S4_Case-and-entrainment-threshold_data
  - Description: case characteristics (mass, axes) and bed-shear-threshold metrics; entrainment/movement thresholds.
  - Key variables: Case/Sediment ID, State, Mass, a (long axis), b_D50 (intermediate axis or D50), c (short axis), E_10 (bed shear stress threshold for entrainment), E_90 (threshold for 90% transport).
  - Purpose: relate physical case geometry to hydrodynamic thresholds.

## Data collection and scope
- Setting: controlled flume environment; non-natural spatial context, suitable for mechanistic interpretation and model parameterization.
- Temporal and sample details: 12–13 specimens across 3 species; measurements tied to 11 discharge steps; specimen identifiers indicate species and individual.
- Data provenance: collected and interpreted by Mason et al.; includes raw-to-processed value transitions and quality indicators (S1).

## GIS relevance and usage
- Potential spatial representations:
  - Case geometry and dimensions (a, b_D50, c) as vector features for 3D reconstructions or site-scale analogs.
  - Bed shear stress (Tb) and velocity components (U/V/W) as raster/vector layers across flow stages; could be used to visualize hydraulic regimes around bioconstructions.
- Integrative maps/visualizations:
  - Temporal sequences showing how thresholds (E_10, E_90) relate to entrainment percentages across discharge steps.
  - Grain-size distributions linked to individual cases to explore transport likelihood by sediment class.
  - Species-level comparisons (three morphologies) mapped against transport metrics.
- Data integration ideas:
  - Join Sample_ID to species and axis dimensions; combine with velocity and Tb fields to generate case-specific hydraulic risk maps.
  - Export GIS-ready layers (e.g., GeoJSON, shapefiles, or GeoTIFFs) for end-user dashboards or policy briefs.

## Data quality and limitations
- Post-processing: Series include adjusted means/standard deviations and data quality indicators (SNR, correlation) to support reliability assessment.
- Sample characteristics: relatively small, controlled flume sample (8 individuals per relevant group in S4); caution when extrapolating to natural rivers.
- Scale considerations: flume boundaries and controlled conditions may limit direct riverine applicability; emphasize mechanistic insights over field-scale generalization.
- Documentation needs: ensure consistent units, clearly defined variables, and metadata for cross-dataset integration.

## Use cases and visualization ideas
- Interactive dashboards:
  - Explore how bed shear stress and velocity fields evolve with discharge steps for each case type.
  - Compare entrainment curves (S3) across species and case geometries.
- Spatial analytics:
  - Map case geometries and overlay with hydraulic metrics (Tb, velocity) to identify zones of higher transport risk.
  - Visualize grain-size distributions per case to relate sediment packaging to transport thresholds.
- Reporting products:
  - Summaries of threshold values (E_10, E_90) per case to support design or ecological interpretation in river engineering contexts.

## Metadata and processing recommendations
- Ensure GIS-ready metadata:
  - Document units, variable definitions, measurement methods, and the relationship between raw and adjusted values.
  - Associate Sample_ID with species, individual, and corresponding case geometry.
- Standardization steps:
  - Harmonize date formats and, if georeferencing is applied, define coordinate reference systems.
  - Convert S1 velocity fields and Tb to consistent raster/vector formats for time-series visualization.
- Data packaging:
  - Provide a consolidated data package including S1–S4 with a readme describing variable meanings, scale, and potential GIS applications.