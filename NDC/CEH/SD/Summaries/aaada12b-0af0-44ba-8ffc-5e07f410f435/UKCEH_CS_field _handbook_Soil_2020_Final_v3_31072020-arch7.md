# UK-CEH Countryside Survey Soil Handbook 2020

## Overview
- Purpose: Long-term soil and vegetation monitoring to assess soil change at national scale using rolling surveys.
- Scope: ~500 survey squares over 5 years, surveying ~100 squares per year; re-survey former Countryside Survey squares (from 1978, with additions from 1998/2007) and record soil and vegetation.
- Data aims: Create map-based data products and datasets to support understanding of soil function and change; part of UK-SCaPE national capability.
- Sampling unit: Each surveyed square includes five X plots where soil cores and vegetation are measured.

## Spatial Sampling Design and Layout
- X plots: Five per square, randomly located within dominant vegetation, away from field boundaries.
- Core layout per X plot: Five 15 cm soil cores (one Black, two White, two Grey).
  - Core types correspond to analysis/storage categories: Black (Chemistry), White (Ada/Adb – Storage), Grey (Ba/Bb – Biology).
- Core positioning: On the WEST line of the X plot, 15 cm outside the central 2x2 m vegetation quadrat.
- Historical context: Sampling framework aligns with past surveys (1978, 1998, 2007) and 2019–2022 activities, forming part of the national soil-vegetation platform.
- Depth reference: Target core depth is 15 cm; if depth is insufficient, record the measured depth from the base of the cross bar to ground.

## Core Types, Labelling and Coding
- Cores and labels:
  - Core 'C' (Chemistry): LONG BLACK core, 15 cm x 5 cm.
  - Core 'Ada' and 'Adb' (Storage): LONG WHITE cores, 15 cm x 5 cm.
  - Core 'Ba' and 'Bb' (Biology): LONG GREY cores, 15 cm x 5 cm.
- Labeling: Each plot bag contains labels for all five cores; barcodes scanned in the field.
- Data coding: Bags include plot identifiers and core-type labels; barcodes encoded to map to CS year, square, X-plot, and core type.

## Field Procedures (Core Sampling)
- Mineral soils:
  - Clean coring device; insert core upright, cut around bottom edge, hammer to drive core to depth.
  - If a full 15 cm depth cannot be achieved, note the depth from cross bar to ground and record in software; log as a note on the bag.
  - Extract core, twist to break bottom, and remove; use crowbar or wood muddler if needed to protect equipment.
  - If soil is loose or sandy, use trays to prevent contamination; push core out, cap top (red) and bottom (black).
- Organic soils:
  - Core device may not work; place core on surface and cut around bottom edge; push into ground and capture soil without compressing the sample.
  - Remove soil with trowel/pliers carefully to avoid loss; trim bottom as needed.
- Peaty/organic horizons:
  - In peat soils, use avalanche rod to test O horizon depth at three marked locations; record depth if depth exceeds 2 cm.
  - For organic layers >15 cm, adjust core method to minimize compression; measure and log any deviations.
- Scree/rocky soils:
  - If core cannot be collected, use a trowel to collect fine material; label as “scree.”
- Post-sampling handling:
  - Cap cores (RED top, BLACK bottom), seal in corresponding bags, and add short notes if core is shorter than 15 cm (short vs compressed, or comp).
  - Record SQ number on bag exterior; log any obstacles or unusual vegetation.

## Peat Depth and Organic Horizon Guidelines
- Peat depth: Measure O horizon depth using avalanche rod at three star-marked locations; record in cm.
- Organic layer guidance: If an organic layer is present, document depth and layer characteristics; follow forest-floor guidance for distinguishing litter, fermentation (F), and humic (H) horizons.

## Label Scanning and Data Capture
- After sealing, scan all labels with a tablet to associate cores with the correct plot and core type.
- If scanning is not possible (e.g., rain, device issues), manually enter the barcode.
- If no barcode exists, generate one using a logical pattern (year, square, X-plot, core type) and maintain consistency for later lab processing.

## Sample Storage and Dispatch
- Transport: Bring cores to accommodation or lab in a cool storage system (cool box or fridge) to maintain sample integrity.
- Posting guidelines:
  - Pack cores from the same SQ into the same bag; ensure leak-proof packaging and add absorbent material if liquids are possible.
  - Post only on suitable days; refrigerate if not posting immediately (do not post Thursday/Friday or weekends).
- Destination and storage:
  - Black and White cores: Send to UKCEH Bangor; store in a 4°C cold room.
  - Grey biology cores: Post to Lancaster; freeze at -20°C as soon as possible (Lancaster Environment Centre; some logistics may route via Wallingford).
  - Detailed addresses and contact options provided in the handbook.

## Practical Considerations for GIS Integration
- Spatial design: The five-core per X plot layout and WEST-line placement create a repeatable geospatial sampling pattern suitable for temporal GIS analyses.
- Metadata to collect: SQ number, square ID, X-plot ID, core type, depth to bottom, O horizon depth, any notes on obstacles or vegetation, and bag contents.
- Data quality: Use notes to flag deviations (e.g., short/comp cores) to support accurate bulk density estimation and lab analyses.
- Temporal dimension: Re-surveying ~500 squares over 5 years enables change detection and landscape-scale soil function assessments.
- Data product potential: Core-level chemistry, storage/biological data, and horizon-depth measurements can be integrated into map-based visualizations and analyses of soil change over time.