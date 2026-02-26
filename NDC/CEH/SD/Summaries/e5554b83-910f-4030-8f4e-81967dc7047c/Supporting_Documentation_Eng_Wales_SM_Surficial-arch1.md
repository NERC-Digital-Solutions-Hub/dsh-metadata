# Supporting documentation for data resource Eng_Wales_SM_Surficial.csv

- Project context: Carbon Storage in Intertidal Environments (C-SIDE); Funding: NERC (NE/R010846/1); Staff Responsible: William Austin; Research Team includes multiple universities and the C-SIDE Citizen Science Team.

- Data resource overview: Dry bulk density, loss on ignition (LOI), and organic carbon content calculated from 212 surficial soil samples (top 10 cm) from 49 English and Welsh saltmarshes.

- Location and scope: Observations located in England and Wales with site coordinates provided in multiple formats (decimal degrees WGS84, OSGB36 grid references, and X/Y Easting/Northing); sites chosen to represent contrasting habitats (sediment types, vegetation, sea level history).

- Temporal coverage: Monitoring conducted January 2018 – December 2019; no repeat sampling planned.

- Variables and parameters observed: 
  - Soil texture (Sandy / Not-Sandy / Organic)
  - Dry bulk density (g cm-3)
  - Organic matter content (LOI, %)
  - Organic carbon content (OC, % by weight)

- Sampling and laboratory methods:
  - Field: Soil samples collected with a 50 ml syringe to 10 cm depth; GPS locations recorded with various devices; samples frozen at -20°C until analysis.
  - Soil texture classification following Ford et al. (2019).
  - Dry Bulk Density: dried at 60°C for 72 hours; density calculated from dry mass and sample volume.
  - LOI: milled samples combusted at 450°C for 4 hours; mass loss indicates organic matter.
  - Organic Carbon: 10 mg milled samples acidified with 10% HCl to remove carbonates; dried and analyzed with Elemental Analyzer (Vario EL Cube) per Verardo et al. and Nieuwenhuize et al.
  - Calibration and QA: Elemental analyser calibrated with Acetanilide; repeated analyses of a standard (B2178) across runs; citizen scientists performed pre-analysis QC.

- Quality control and data validation:
  - Citizen Science samples visually inspected for saltmarsh consistency; GPS coordinates cross-checked with habitat maps and aerial photos; soil texture classification done by four team members independently with a consensus approach.

- Data structure and formats:
  - Primary file format: .csv
  - Data resource description columns include: Saltmarsh_Name, Nation, Year, Lat_dec_deg, Long_dec_deg, Grid_Reference, X_easting, Y_northing, Sampling_Method, Depth_cm, Dry_Bulk_Density_g_cm_3, Soil_Texture, OC_Perc, LOI_Perc.

- Additional notes and references:
  - Sampling depth standardized at 10 cm; no repeat sampling planned.
  - References for methods and calibration provided (Craft et al. 1991; Dadey et al. 1992; Ford et al. 2019; Kennedy et al. 2005; Nieuwenhuize et al. 1994; Verardo et al. 1990).