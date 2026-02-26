# Background

- The NERC Soil Biodiversity Thematic Programme (established 1999) focused on a large field experiment at Sourhope, Scottish Borders, to study soil biodiversity and the functional roles of soil organisms. It supported 24 projects examining soil structure, carbon/nitrogen cycles, microfauna/mega-fauna, and related processes.
- The document describes baseline soil chemistry measurements, sampling methods, data structure, quality control, and the soil profile descriptions for the Sourhope Rigg Foot site across five blocks.

## Data Collected and Data Structure

- Baseline soil pH and moisture datasets derived from sampling in 1999–2003:
  - P2109_BASELINE_PH.csv
    - Columns: SAMPLE_DATE, TREATMENT, BLOCK, MAIN_PLOT, CELL_X, CELL_Y, SOIL_PH, MOISTURE (moisture calculated from fresh/dry weight; oven-dried in 1999 for moisture).
  - P2109_BASELINE_PHSUB.csv
    - Columns: SUID, SAMPLE_DATE, TREATMENT, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, SOIL_PH.
- Methods for pH measurement and moisture determination:
  - pH measured by mixing ~10 cm3 soil with deionised water, equilibration, calibrated with buffers (pH 7 and 4), and reading with a pH meter.
  - Moisture content calculated as 100*(fresh weight − dry weight)/dry weight after oven drying (25°C).
- Data quality and governance:
  - Quality control included numeric range checks, format conformity, and logical integrity checks.
  - NERC provides no warranty on data accuracy or fitness for a specific use; liability for data use is disclaimed.
- Access and provenance:
  - Data referenced to the SOURHOPE FIELD DATA HANDBOOK (2003) by Scott et al.; available via the EIDC catalogue record.

## Site Context and Soil Profiles (Blocks 1–5)

- The Sourhope Rigg Foot site comprises five blocks (Blocks 1–5), each with:
  - Grid reference, altitude (approximately 304–315 m), slope, soil drainage, soil series (SH 74711 or SH 74714), parent material, major soil subgroups (Brown forest soils with/without gleying), and rock types (andesite/igneous rocks).
  - Each block includes a soil profile description with horizon sequences and depths, documenting color, texture, structure, roots, mottling, boundaries, stones, and moisture status.
- Block-level summaries ( examples):
  - Block 1: Grid NT8545019630; drainage Moderate; Brown forest soil; detailed horizon sequence from LF to CR (0–95 cm).
  - Block 2: Grid NT8551019610; drainage Free; Brown forest soil; profile from LF to CR (0–80 cm).
  - Block 3: Grid NT8549019590; drainage Free; Brown forest soil; profile from LF to C (0–90 cm).
  - Block 4: Grid NT8546019550; drainage Imperfect; Brown forest soil with gleying; profile from LF to Cgx (0–95 cm).
  - Block 5: Grid NT8544019520; drainage Imperfect; Brown forest soil with gleying; profile from LF to Cg (0–100 cm).
- Horizon-level details (illustrative):
  - Horizons described with depth ranges (e.g., 0–1 cm LF; 1–4 cm FH; 4–6 cm H; 6–29 cm Ah or Ah-like horizons; deeper horizons Abg, B, BCx, etc.).
  - Descriptions include color (e.g., brown, dark reddish brown, black), texture (loamy sand, sandy silt loam, clay loam), structure (subangular blocky, platy), moisture status (moist, friable, firm), mottling, root density, and presence of stones or igneous fragments.
  - Some blocks note gleying and mottling patterns, reflecting varying drainage and soil development.

## Data Use and Potential Outputs

- The data enable self-serve exploration of:
  - Spatial variation in soil pH and moisture across blocks and plots.
  - Relationships between soil chemistry, drainage class, and horizon properties.
  - Visualizations and dashboards to compare baseline soil conditions by block, plot, and sub-plot.
- The rich soil-profile descriptions support detailed soil-derivation analyses, soil classification cross-checks, and context for interpreting pH/moisture data.

## References and Documentation

- Primary source: SOURHOPE FIELD DATA HANDBOOK (2003) by Scott, Bell, Kenny, Jeffers, Buckland, and Burt-Smith.
- Data linked to the NERC Soil Biodiversity Programme and the Sourhope field experiment dataset.
- Availability note: Data provided with QA steps but no warranty; access via supporting information in the EIDC catalogue.

 Key references:
- Scott et al., 2003. SOURHOPE FIELD DATA HANDBOOK 2003. Available through the EIDC catalogue.