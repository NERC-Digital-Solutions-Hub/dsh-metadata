# Landwise Broad-scale Survey Lab Soil Analysis TEMPLATE

## Purpose and scope
- Documentation of equipment, laboratories, labeling, and step-by-step procedures for soil analysis in a Landwise Broad-scale Survey context.
- Covers volumetric soil moisture and bulk density by oven drying, soil organic matter by loss on ignition, HCl test for calcareous soil, slaking and dispersion, hand texturing, and texture analysis by sieving and laser particle sizing (MS2000).

## Equipment and laboratories
- Equipment
  - 45 foil sample trays (approx. 14 × 12 × 5 cm)
  - Glass desiccators with silica gel desiccant
  - Balance with 0.1 g precision; higher-precision balance (0.001 g) for OM
  - Muffle furnace with ±5 °C control
  - Drying ovens (±5 °C control)
  - 15 porcelain furnace crucibles
  - Furnace heat mats, porcelain tiles, trays, long-handle tongs, gauntlets
  - Pestle and mortar
  - Ovens room trolley
  - Landwise Broad-scale Survey Lab Soil Analysis TEMPLATE spreadsheet
  - Permanent marker, blue nitrile gloves, lab coat
- Laboratories
  - Ovens Balance Room (volumetric moisture, bulk density, OM)
  - Soil Hydrology Lab (slaking/dispersion, hand texturing, temporary storage)
  - Chemistry Lab Acid Fume Cupboard (HCl test for calcareous soil)

## Sample labeling and data recording
- Lab tray labeling and field correspondence
  - V samples: label with site code, field number, and V sample number; ensure correspondence with field sample bag labels on the Landwise spreadsheet.
  - A samples: label with site code, field number, and A sample number; ensure correspondence with field labels and crucible-to-tray mapping on the spreadsheet.
- Data management
  - Record all measurements in the Landwise Broad-scale Survey Lab Soil Analysis spreadsheet; save as site-specific workbook (e.g., UoR Sonning Field 1… .xlsx) in NEC06345_LANDWISE Broad-scale Survey Site Data.
  - Scan and save completed printouts with analogous naming in the same site sub-folder.

## Procedures (summary)

### Volumetric soil moisture and soil bulk density by oven drying (V samples)
- Pre-check balances (0.1 g and 0.001 g accuracy) and balance level.
- Weigh soil in sealed bag to 0.1 g (SOILMOIST + BAG).
- Weigh empty foil tray to 0.1 g; transfer soil from bag to tray, then weigh combined soil+tray.
- Weigh empty field bag for reference.
- Dry in oven at 105 °C for ~36–60 hours (start/end times logged).
- Weigh dry soil+tray immediately after removal; record to 0.1 g.
- Calculate:
  - Volumetric moisture: VOLWATER / VOLRING
  - Bulk density (dry): SOIL105 / VOLRING
  - Gravimetric moisture: (SOILMOIST − SOIL105) / SOIL105
  - Convert to volumetric moisture if needed: gravimetric moisture × (SOIL105 / VOLSAMPLE)
- Tray reuse: reuse allowed if mass is 3.8 g ± 0.1 g; relabel as needed.
- Data handling: transfer results to the site spreadsheet; keep traceable logs.

### Soil organic matter by loss on ignition (A samples)
- Label trays; air-dry ~60 g sub-sample, break lumps, and transfer to tray.
- From each tray, take ~20 g, crush, sieve to <0.4 mm.
- Prepare crucibles: weigh empty crucibles pre- and post-analysis; preheat as required.
- Weigh ~4 g of crushed dried soil into crucibles; oven-dry at 400 °C for 16 h overnight.
- Record crucible numbers and weights to 0.001 g.
- Calculate OM (%): ((SOIL105 − SOIL400) / SOIL105) × 100.
- Retain remaining dried soil for related analyses as needed; discard after completion of OM and calcareous tests.
- Ensure foil trays are not too dusty before reuse.

### HCl test for calcareous soil
- Use crushed, sieved soil. Follow Natural England method for calcareous content: apply 20% HCl and classify by visible effervescence into defined categories.
- Create and label fresh HCl 20% solution from stock stock (32%):

  - Rinse apparatus with deionised water; mix acid in steps as specified; store in labeled container.

### Slaking and dispersion test
- Use air-dried soil aggregates; place in beakers with DI water.
- Record start time; grade dispersion at 10 min and 2 hours on a 0–4 scale (0 = no dispersion; 4 = complete dispersion).
- Dispose of samples with ample water.

### Hand texturing
- Take a moist soil sample; knead until cohesive and crumbly; determine texture class by feel and record abbreviation.

### Texture by sieving and laser particle sizer (MS2000)
- Prepare 0.5–1.0 g of additional sample in a falcon tube; add 5 ml of 5% sodium hexametaphosphate; bring to 50 ml with DI water; mix and rest at least 1 h.
- Ultrasonic treatment for batch to reduce aggregates.
- MS2000 startup and operation:
  - Warm-up, background checks, calibrations, and measurement sequence (three replicates, then replicate checks).
  - Target obscuration: 10–40% (coarse ~35%, adjust per particle size class).
- Record obscuration and export results to Excel; ensure replicates align.

### Soil colour
- Retain a small bagged sample for colour analysis by UoR; return the rest to the sample bag.

## Notes and safety considerations
- Collect samples from walk-in fridge; analyze promptly (ideally within a month).
- Refer to Basic Furnace Operation Protocol and Oven Operation for usage; log furnace usage; ensure air extraction is functioning; schedule furnace use as required.
- Handle crucibles with tongs; hot handling for weighing; desiccators for cooling when needed.
- Silica gel desiccants: reactivate by heating to 80 °C; avoid silica gel dust inhalation; avoid carcinogenic blue silica gel.
- Rationale for LOI temperature: 400 °C removes organic matter with minimal dehydroxylation of clays (per cited literature).
- Special handling for oven-dried samples: weigh hot to avoid moisture uptake; batch handling in trays.

## Data governance and quality considerations
- Emphasizes traceability from field bags to lab trays and to the final site data workbook.
- Requires consistent metadata in the field-to-lab labeling, logs, and spreadsheet naming conventions.
- Encourages sharing of underlying data where appropriate, with clear documentation of methods and QA steps.
- Recommends maintaining notes on lab conditions, instrument status, and any deviations to support reproducibility.

## References
- Gardner, W.H. (1986); Nelson & Sommers (1996); Pansu & Gautheyrou (2006); NE Soil texture method; McKenzie et al. (1992) dispersion references; relevant Think Soils and EA Quickguide materials.
- Acknowledgement: James Blake & Emily Trill, Centre for Ecology & Hydrology, Wallingford, UK; Jan 2019.