# Earthworm diversity and the integration of physical, biochemical and microbiological functions.

## Aim
- Document the earthworm diversity study within the NERC Soil Biodiversity Programme, focusing on understanding soil biota diversity and the functional roles of soil organisms in key ecological processes.
- Provide two endpoint datasets from the Sweethope mesocosm that enable spatial analysis of earthworm abundance/biomass and botanical composition.

## Scope and context
- Location: Sweethope mesocosm97, modeled after Sourhope main plots in the Scottish Borders; Sweethope sits about 100 m from the main plots.
- Experimental design: Soil from Sourhope main plots rebured in 100 boxes (0.035 m3 each) with treatments including no inoculation, single functional groups (epigeic, endogeic, or anecic) and a full ABC combination; lime treatment applied to some boxes to mirror main plots.
- Duration and timing: Inoculation occurred April 2000; end-point sampling of earthworms and botany conducted October 16–17, 2001.
- Spatial structure: Grid-like layout with blocks, main plots, sub-plots, and cell coordinates (CELL_X, CELL_Y) to enable per-box spatial mapping.

## Datasets included
- Dataset 1009: Sweethope Endpoint Botanical Composition Data (2129_BOTANICAL_COMPOSITION.csv)
  - Fields include SAMPLE_ID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT (C=Control, L=Limed), SPECIES, BOTANICAL_COMPOSITION (Braun-Blanquet cover scale 0–6).
  - Provides end-of-study plant species presence and relative abundance per treatment/plot cell.
- Dataset 1010: Sweethope Endpoint Earthworm Survey Data (P2129_EARTHWORM_SURVEY.csv)
  - Fields include SAMPLE_ID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT (C/L), SPECIES, ABUNDANCE (per m2), BIOMASS (per m2).
  - End-of-study census of earthworm abundance and biomass by species, aggregated per cell/plot.

## Data structure and geographic alignment
- Both datasets are CSVs with parallel spatial indexing: BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y enable granular GIS mapping.
- Temporal marker: Sampling date is Oct 2001 for the endpoint data.
- Taxa and measurements:
  - Botanical data linked to treatment and cell location; Braun-Blanquet scale records presence/cover per plant species.
  - Earthworm data capture species-level abundance and biomass per square meter under each treatment and location.

## How this data can be used in GIS
- Create spatial maps of earthworm abundance and biomass by cell location (CELL_X, CELL_Y) across the Sweethope grid.
- Visualize botanical composition per treatment and plot cell to assess plant-soil biota relationships.
- Explore effects of lime treatment and earthworm inoculation on soil biodiversity and structure by spatially correlating earthworm metrics with plant community data.
- Integrate with the Sourhope main plots for comparative GIS analyses of managed upland grassland plots.
- Link to related soil processes studies (carbon/nitrogen cycling) for richer map-based storytelling of soil biota–function interactions.

## Quality control and data notes
- Quality control included numeric range checks, data formatting conformity, and logical integrity checks.
- Data are provided with caveats: NERC cannot guarantee accuracy or fitness for a particular use; liabilities are disclaimed.
- Endpoints reflect controlled mesocosm conditions with a designed manipulation (inoculation and lime), and note the multi-user plot context and contamination risk considerations.

## References and provenance
- Core study and datasets originate from the Sweethope/Sourhope Soil Biodiversity experiments within the NERC programme.
- Related literature and handbooks provide methodological context (e.g., Sims & Gerard earthworm keys; Sourhope Field Data Handbook; publications on lime effects and earthworm communities).