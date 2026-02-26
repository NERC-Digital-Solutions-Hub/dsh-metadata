# LANDWISE Broad-scale Survey Lab Soil Analysis

## Overview
- A comprehensive lab protocol for analysing Soil samples collected in the Landwise Broad-scale Survey.
- Produces map-ready and attribute-based data products focused on soil moisture, bulk density, organic matter, calcareous content, texture, and particle size distributions.
- Emphasises careful data handling, traceability, and iterative QA with end-user needs in mind.

## Data Outputs and Variables
- Volumetric soil moisture content (cm3/cm3) derived from oven-dried vs. fresh mass, using VOLWATER, VOLRING, and VOLSAMPLE calculations.
- Bulk density (dry, g/cm3) calculated from dry mass and sample volume (VOLRING = 100.1 cm3).
- Gravimetric soil moisture content (g/g) derived from wet and dry masses.
- Soil organic matter (SOM) by loss on ignition (%) using SOIL105 and SOIL400 (OM% = ((SOIL105 - SOIL400) / SOIL105) × 100).
- Calcareous soil content assessed by HCl test with categorical interpretations (None to Strong effervescence).
- Slaking and dispersion scores (0–4) from dispersion test.
- Hand texture classification (qualitative feel-based texture).
- Texture by sieving and laser particle sizing (MS2000): sub-sample preparation, 5% sodium hexametaphosphate pretreatment, obscuration targets (10–40%), replicates, and data export workflow.
- Data referenced to field/site identifiers and stored in Landwise spreadsheets for subsequent GIS integration.

## Data Collection Process
- Equipment: foil sample trays, desiccators, precision balances (0.1 g and 0.001 g), muffle furnace, drying ovens, crucibles, furnace heat mats, pestle and mortar, tongs, gloves, markers, and related safety gear.
- Laboratory setup: Ovens Balance Room (moisture, bulk density, SOM), Soil Hydrology Lab (slaking/dispersion, hand texturing), Chemistry Lab (HCl tests).
- Sample labeling:
  - Volumetric samples labeled with V and corresponding site/field codes; correlation with field sample bags recorded in Landwise Lab Soil Analysis spreadsheet.
  - SOM samples labeled with A; correspondence with field samples documented.
- Data recording: results entered into a Landwise Broad-scale Survey Lab Soil Analysis spreadsheet; file names include site name and field number; saved to NEC06345_LANDWISE\Broad-scale Survey Site Data; completed spreadsheets scanned and stored in the same folder.

## Procedures and Calculations
- Volumetric soil moisture and bulk density by oven drying:
  - Pre-check balances, weigh V samples and trays, oven dry at 105°C for ~36–60 hours, reweigh promptly, and compute VOLWATER, VOLRING, and VOLSAMPLE.
  - Bulk density = SOIL105 / VOLRING.
- Soil organic matter by loss on ignition (SOM by LOI):
  - Dry sub-samples, weigh ~4 g of crushed soil into crucibles, burn at 400°C for 16 hours, weigh post-analysis (SOIL400), and compute OM% from SOIL105 and SOIL400.
- HCl test for calcareous soil:
  - Prepare 20% HCl solution from stock, apply to crushed soil in labelled beakers, observe and classify calcareous content per defined categories.
- Slaking and dispersion test:
  - Immerse air-dried aggregates in DI water, score dispersion at 10 min and 2 hours on a 0–4 scale.
- Hand texturing:
  - Wet and knead soil to assess particle feel and record texture class.
- Texture by sieving and laser particle sizer (MS2000):
  - Prep sub-samples (0.5–1.0 g), pretreat with 5% sodium hexametaphosphate, dilute to 50 ml, mix, and ultrasonicate as needed.
  - Run MS2000 following SOPs; perform initial batch checks; obtain replicates for consistency; ensure obscuration levels (optimal ~35% for coarse, ~25% for D50 ≥ 50 μm, ~15% for D50 ≤ 5 μm).
  - Export data to_excel; maintain records for batch QC.

## Data Quality, QA and Traceability
- Timely and careful weighing (hot from oven where required) to minimize moisture gain.
- Unique sample IDs linked to field labels; detailed labeling and cross-checks to prevent mix-ups.
- Tray mass controls (3.8 g ± 0.1 g) to monitor potential contamination and mass error.
- Replicate measurements in MS2000; background checks and clean cycles for instrument calibration.
- Documentation: log times, oven/furnace usage, and equipment settings; all data transferred to site-specific spreadsheets and scanned copies stored in the project folder.

## Safety, Handling, and Equipment Notes
- Furnace and desiccant safety procedures; silica gel handling and reactivation guidance; avoid inhalation of silica gel dust.
- HCl handling in fume cupboards; disposal procedures for acidic residues.
- Use of hot crucibles and desiccators; orderly cooling sequences to prevent contamination and accidents.

## GIS Integration Considerations
- Standardized identifiers: site code, field number, sample IDs, and sample type (V, A, etc.) enabling seamless joining to GIS attribute tables.
- Variables suitable for mapping:
  - Soil moisture (volumetric and gravimetric), bulk density, SOM (%), calcareous category, slaking/dispersion scores, hand texture, and texture class data from MS2000.
- Data products and layers:
  - Moisture and bulk density maps, SOM maps, calcareous soils map, textural class maps, and particle size distribution maps (from MS2000 data).
- Data management:
  - Centralized file naming conventions (site name + field number); keep raw vs. processed data separate; export and archive MS2000 results and spreadsheet data.
  - Ensure data provenance by retaining lab worksheets, logbooks, and scanned spreadsheets alongside GIS-ready extracts.
- Potential data gaps and considerations:
  - Resolution and coverage gaps due to sample collection timing or lab capacity.
  - Variability in lab procedures across batches; emphasis on QA to maintain consistency for spatial analyses.

## Notes and References
- References include Gardner (1986), Nelson & Sommers (1996), Pansu & Gautheyrou (2006), and McKenzie et al. (1992) for LOI, soil texture, and dispersion methodologies.
- Documentation and templates provided by Landwise project (NEC06345_LANDWISE) and linked lab work sheets.