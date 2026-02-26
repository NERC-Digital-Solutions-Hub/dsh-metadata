# Landwise Broad-scale Survey Lab Soil Analysis TEMPLATE

- Standardized protocols for soil analysis to obtain volumetric moisture, bulk density, organic matter, calcareous content, soil structure characteristics, texture, and particle size distributions.
- Emphasizes traceability, data capture, QA, and reproducible calculations, with results stored in site-specific spreadsheets and archived in a shared data portal.

## Equipment and Laboratories

- Equipment (examples):
  - 45 foil sample trays; desiccators with silica gel; precision balances (0.1 g and 0.001 g); balance test weights
  - Muffle furnace; drying ovens; porcelain crucibles; furnace heat mats; long-handled tongs; gauntlets
  - Pestle and mortar; permanent markers; gloves; lab coat
  - Landwise Broad-scale Survey Lab Soil Analysis TEMPLATE spreadsheet for recording results
- Laboratories:
  - Ovens Balance Room: volumetric soil moisture, bulk density, soil organic matter
  - Soil Hydrology Lab: slaking and dispersion, hand texturing, temporary sample storage
  - Chemistry Lab Acid Fume Cupboard: HCl test for calcareous soil
- Documentation and labeling:
  - Consistent labeling between field bags and lab trays; field-to-lab correspondence logged in the Landwise spreadsheet
  - Sample types: V = volumetric moisture; A = soil organic matter; crucibles linked to tray labels

## Sample Labelling and Data Capture

- Lab tray labels: site code, field no., sample type and number (e.g., SON F1 V1; SON F1 A1)
- Ensure correspondence with field sample bags; record date/time, sample IDs, and tray numbers in the Landwise spreadsheet
- Data flow: field collection -> lab labeling -> lab measurement -> transfer to site-specific spreadsheet -> scanned copy saved in project folder

## Core Laboratory Procedures

- Volumetric soil moisture and soil bulk density by oven drying (V samples)
  - Pre-check balances; weigh sample in sealed bag; weigh empty tray; transfer soil to tray; dry at 105°C (36–60 h); weigh warm to minimize moisture uptake
  - Calculations include: Volume water, sample volume, mass wet/dry, volumetric moisture content, and bulk density
  - Formulas (summary):
    - Gravimetric moisture = (SOILMOIST - SOIL105) / SOIL105
    - Volumetric moisture = Gravimetric moisture × (SOIL105 / VOLSAMPLE) [equivalently VOLWATER / VOLRING]
    - Bulk density (dry) = SOIL105 / VOLRING
- Soil organic matter by loss on ignition (A samples)
  - Sub-sample, air dry, crush, sieve to <0.4 mm
  - Dry at 105°C; prepare crucibles; weigh crushed soil from SOIL105; heat crucibles to 400°C for ~16 h
  - Weigh post-analysis crucibles; calculate Organic matter (%) = ((SOIL105 - SOIL400) / SOIL105) × 100
- HCl Test for calcareous soil
  - Use 20% HCl on crushed soil; classify calcareous content into none/slight/moderate/strong based on visible effervescence
  - Create fresh HCl 20% solution from stock via specified dilution procedure
- Slaking and dispersion test
  - Use air-dried soil aggregates in DI water; record dispersion after 10 minutes and 2 hours on a 0–4 scale
  - Slaking vs dispersion definitions described for soil structure interpretation
- Hand texturing
  - Moisten a desert-spoonful of soil; knead to attribute texture; record texture class abbreviation
- Texture by sieving and laser particle sizer (MS2000)
  - Prepare 0.5–1.0 g subsample in 5% sodium hexametaphosphate; bring to 50 ml with DI water; mix; rest; ultrasound as needed
  - MS2000: startup, background check, measurement sequence (3 replicates; target obscuration 10–40%)
  - Obscuration guidance and replicate check; ensure consistency across measurements
- MS2000 data workflow
  - File naming, operator log-in, background checks, calibration steps, measurement execution, replicate validation
  - Data export to Excel and project folder; save and archive routinely
- Sample preparation nuances
  - Pre- and post-measurement handling: process trays in controlled order; reuse trays only if mass is within tolerance and cross-contamination is minimal
  - Colour analysis and additional soil analyses (e.g., for colour) may be sent to external labs (e.g., UoR)

## Data Handling, Quality Assurance, and Recording

- Data capture and storage:
  - Record all raw measurements on the field/spreadsheet printouts; transfer finalized values to the Landwise Lab Soil Analysis spreadsheet
  - Completed spreadsheets are saved to ..\NEC06345_LANDWISE\Broad-scale Survey Site Data; scan and save as site-specific files
- Traceability:
  - Link each measurement to field labels, tray numbers, crucibles, and sample IDs
- Quality assurance:
  - Balance checks, oven temperatures, and times logged; 100-sample batch QA per MS2000 run; follow standard operating procedures (QAS) as documented
  - Document background checks, measurement replicates, and any deviations
- Data accessibility and discoverability:
  - Store datasets with metadata; upload to portals; ensure datasets created are discoverable and usable
- Output and reporting:
  - Produce a coherent dataset combining volumetric moisture, bulk density, LOI, calcareous content, slaking/dispersion, hand texture, and MS2000 results
  - Generate colour analyses and other tests as needed; maintain a linked archive of all results and related logs

## Operational Notes and Safety

- Sample handling:
  - Collect soil in walk-in fridge; analyze as soon as feasible (ideally within a month)
- Furnace and oven use:
  - Record furnace/oven usage in logs; ensure ventilation and safety protocols are followed
  - Use desiccants, handle hot crucibles with tongs; avoid contamination from fingertips
  - Reactivate silica gel desiccant by heating to red/pink; avoid inhaling dust
- Waste disposal:
  - Calcareous test effluent disposed via fume cupboard sink with ample dilution
- Data integrity:
  - Back up data; ensure file naming consistency; follow the prescribed folder structure
- References and standards:
  - Nelson & Sommers (1996), Pansu & Gautheyrou (2006), Gardner (1986), NE Soil texture method; Think Soils quickguide
  - Documented procedures reflect established soil analysis methodologies

## End-of-Batch and Documentation

- Data finalization:
  - Ensure all batch measurements are complete; export and save data; close software and power down bench
- Colour and extra analyses:
  - Preserve representative samples for potential external analyses; send colour samples as needed
- Documentation:
  - Maintain logs of all operational steps, times, temperatures, and instrument settings for reproducibility

## References

- Gardner, W.H. (1986)
- Nelson, D.W. & Sommers, L.E. (1996)
- Pansu, M. & Gautheyrou, J. (2006)
- James Blake & Emily Trill; Centre for Ecology & Hydrology
- Natural England (2008); NE Soil texture method
- Environment Agency Think Soils quickguide