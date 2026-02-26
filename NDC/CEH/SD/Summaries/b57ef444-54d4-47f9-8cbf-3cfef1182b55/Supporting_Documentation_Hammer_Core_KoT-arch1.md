# Supporting documentation for data resource Hammer_Cores_KoT.csv

## Overview
- Data resource describing sedimentological and organic carbon data from the Kyle of Tongue Saltmarsh (Hammer cores).
- Project: Carbon Storage in Intertidal Environments (C-SIDE), funded by NERC (NE/R010846/1).
- Research team includes Craig Smeaton, Luis Rees-Hughes, Natasha L.M. Barlow, and William E.N. Austin (universities of St Andrews and Leeds).
- Data linked to best-practice guidance for blue carbon stock and burial estimations (Geoderma 2020).

## Data Resource Details
- Name: Hammer_Cores_KoT.csv (Sedimentological and organic carbon data from the Kyle of Tongue Saltmarsh—Hammer cores).
- Location: Kyle of Tongue, Scotland (WGS84 coordinates; includes latitude/longitude, OSGB36 grid references, and x/y easting/northing).
- Observations: 39 soil samples from 4 hammer cores.
- Sampling: No planned repeat sampling.

## Sampling and Methods
- Core collection: 150 cm PVC tubes with 6.16 cm inner diameter; inserted to 100 cm depth, sealed at the top, and extracted.
- Core handling: Cores split lengthways into working/archive sections.
- Sub-sampling: Fixed volume samples (4 cm^3) taken at 10 cm intervals; weighed to obtain wet bulk density, dried at 60°C for 72 hours to derive dry bulk density and water content, from which porosity is calculated.
- Soil description: Troels-Smith (1955) classification used for dominant soil description; simplified for reporting.
- Elemental analysis: 10 mg milled samples acidified to remove carbonates, dried, and analyzed for organic carbon using an Elemental Analyzer (Calibrated with Acetanilide; replicates included).
- QA: Independent Troels-Smith classification by two team members; mean results reported.
- Replicates: Organic carbon measured in triplicates; three replicates reported with mean and standard deviation.

## Variables and Measurements
- CoreID (text)
- Collection_date (numeric date)
- Lat_dec_deg, Long_dec_deg (decimal degrees; WGS84)
- Grid_Reference (OS National Grid)
- X_easting, Y_northing (projected coordinates)
- Depth_cm, Mid_Point_Depth_cm
- Sampling_Method (Hammer Core)
- Simplified_Troels_Smith (soil description)
- Water_Content_perc
- Wet_Bulk_Density_g_cm_3
- Dry_Bulk_Density_g_cm_3
- Porosity (Φ)
- OC_perc_Rep1, OC_perc_Rep2, OC_perc_Rep3 (organic carbon content; % by weight)
- Mean_OC_perc (mean of three replicates)
- Std_Dev (standard deviation of OC replicates)

## Data Quality and Provenance
- Data descriptions produced by two independent assessors for quality assurance.
- Calibration and analytical procedures detailed (Athy 1930; Dadey et al. 1992; Verardo et al. 1990; Nieuwenhuize et al. 1994; Troels-Smith 1955).
- Reproducibility supported by triplicate OC measurements and standard calibration (Acetanilide; B2178 standard).
- File format: CSV; metadata provided to support discoverability and reuse.

## Location and Boundaries
- Site: Kyle of Tongue, Scotland.
- Coordinates provided in multiple formats (lat/long, grid reference, and easting/northing) to facilitate GIS use and spatial analyses.

## File Formats and Access
- Primary data file: Hammer_Cores_KoT.csv
- Data resource description file formats: includes detailed column definitions and formats for Hammer_Core_KoT.csv
- Related material: linked publication as background (Smeaton et al., 2020) and references for methods.

## References and Related Works
- Smeaton, C., Barlow, N. L., & Austin, W. E. (2020). Coring and compaction: Best practice in blue carbon stock and burial estimations. Geoderma, 364, 114180. DOI: 10.1016/j.geoderma.2020.114180.
- Athy, L.F. (1930). Density, porosity, and compaction of sedimentary rocks.
- Dadey, K.A., Janecek, T., Klaus, A. (1992). Dry-bulk density: its use and determination.
- Kennedy, P., Kennedy, H., Papadimitriou, S. (2005). The effect of acidification on determination of OC and N in marine sediments.
- Nieuwenhuize, J., Maas, Y.E., Middelburg, J.J. (1994). Rapid analysis of OC and N in particulate materials.
- Troels-Smith, J. (1955). Characterization of unconsolidated sediments.

## Potential Uses for Analysis
- Correlate organic carbon content with bulk densities and porosity across depth.
- Assess spatial variation of soil properties using precise core locations (GPS and grid references).
- Develop or test predictive models of carbon storage/burial in intertidal sediments at high-resolution, local scales.
- Use Troels-Smith descriptions alongside quantitative measures to explore sedimentary context and relationships to OC content.

## Limitations and Considerations
- Local-scale dataset (Kyle of Tongue); generalization to broader regions should be cautious.
- No planned repeat sampling limits temporal analyses.
- 39 samples across 4 cores provide a snapshot rather than a dense spatial coverage.
- OC replicates provide measurement uncertainty; mean and standard deviation are provided to support error analysis.
- Data integration may require harmonization with other datasets due to multiple coordinate systems and legacy classifications.