# VEGETATION PLOTS FIELD HANDBOOK: UK-SCaPE 2020

## Overview
- This handbook standardises vegetation plotting in UK-SCaPE, detailing methods to record plant presence, abundance, and habitat context across two plot sizes (200 m² and 4 m² soil plots).
- Aims to create a relocatable, long-term dataset to quantify vegetation change by habitat and landscape location.
- Emphasises careful relocation, consistent data formats, and digital data capture via ESRI Survey123 and Collector apps.

## Data Model and Key Fields
- Plot identifiers: Square, Plot Type (X = 200 m²; XX = 2×2 m), Plot Number, Plot ID (Square+Plot Type+Plot Number).
- Meta-data: Surveyors, location (GPS), slope, aspect, shade, plot map status, photos, and notes.
- Habitat classification: Broad Habitat and Priority Habitat (with episode-specific descriptors and wider polygon context).
- Plot type data: X plots ( vegetation) and XX plots (soil), with nested quadrats (Nest 0 to Nest 5 for X plots; 4 m² nest for soil).
- Data capture: Five nested nests per 200 m² X plot recording vascular plants (Nest 0 supports initial presence and % cover; Nest 5 covers outer area). Soil plots record presence and total cover similarly but limited to soil quadrats.
- Species data: Use drop-down lists with auto-type assist; enter unknowns via “Other,” and attach photos if needed. Total cover per species across nests is required.
- Bryophytes and lichens: Record major bryophytes and listed mosses where possible; other bryophytes/lichens are typically not required.
- Quality checks: Software prompts for missing fields before submission; warnings about blank or duplicate species entries.

## Data Entry Workflow and Tools
- Apps: ESRI Collector for navigation and plot targeting; Survey123 for entering plot data forms (header, headers, vegetation/soil data).
- Workflow:
  - Locate plots via Collector map; open plot form via Survey123.
  - For new plots, enter header data (Plot ID, square, plot type/number, surveyors).
  - For relocations, select status (Found, Not Found, New Plot Replacement, New Feature, Not Appropriate, Access Denied, Too Dangerous) and record exact location (geopoint) with GPS when available.
  - Capture plot photos and a sketch map to aid future relocation.
  - Enter Nest data on Page 3 (vegetation or soil) with nested quadrats for 200 m² plots and complete 4 m² nest data for soils.
  - Submit online via Send Now or Save Draft/Outbox for offline work; Survey123 auto-saves progress.
- Relocation and accuracy: Use GPS where possible; if relocation is uncertain, document in Notes and treat as not a strict repeat if necessary. Five-sector rules guide new X-plot placements when land is scarce.

## Plot Types and Nest Structure
- X Plots (200 m² vegetation plots): Five predetermined random positions; nested quadrats (Nest 0 through Nest 5) record presence and increasing % cover to build a full 14.14×14.14 m plot.
- XX Plots (2×2 m soil plots): Nested within the X plot area; record presence and % cover for soil-associated species.
- Nest recording: 
  - Nest 0: record all vascular plants plus bryophyte categories and ground features; total cover should approach 100% (or more in layered vegetation).
  - Nest 1–Nest 5: progressively search larger areas; add new species found; record additional species absent in Nest 0 as needed; total cover updated for all nests.
- Plot location and measurement: GPS reading taken at the south corner for X plots; for 4 m² nests, project from the south corner; careful orientation and measurement using tape and compass when drawing plots.

## Plot Relocation and Data Integrity
- Plot relocation options:
  - Found: location sufficiently matches previous survey to represent the same vegetation snapshot.
  - Not Found: use available maps/photos and mark as not re-recorded in the same position.
  - New Plot (Replacement for unfound plot) or New Plot (New feature/Land cover): records new locations when repeat plotting isn’t possible.
  - Not Appropriate/Access Denied/Too Dangerous: note disturbances or access limits; may deprioritize repeats.
- Relocation rules:
  - Prioritise repeating previous plots, add new plots only if time allows.
  - If land-use change renders a plot inappropriate (e.g., housing development), mark accordingly.
  - Use five-sector overlay to identify feasible new X-plot locations if land is scarce.
  - In arable fields, place 12 m inside the crop edge to avoid edge effects; avoid trampling by using drill lines when possible.
- Plot maps and sketch maps:
  - Plot sketch maps provide reference points and GPS marks; update or redraw as needed with notes.
  - When re-finding plots, ensure photography and maps reflect any landscape changes since the last recording.

## Data Quality, Validation, and Outputs
- Validation: software prompts for missing header data, incorrect locations, or missing nest entries before submission.
- Data submission: online submission via Send Now; offline workflow stores data in Drafts/Outbox; duplicates avoided by using Copy to new survey for edits.
- Outputs: outputs are designed to be self-serve dashboards and reports for end users; outputs may be promoted and refined with user feedback.

## Bryophytes, Lichens, and Taxonomy
- Bryophytes and lichens: record major bryophytes (soil-associated) and listed mosses where possible; focus remains on vascular plants for most of the data entry.
- Aggregations/Combinations: use species-level identifications when possible; where difficult, use established amalgamations (e.g., Cardamine hirsuta/flexuosa) to maintain comparability with past data.
- Do not uproot invasive species; if identification requires uprooting or sampling, use photos or “Other” entries to minimize disturbance and preserve data integrity.

## Habitat Classification and Priority Habitats
- Broad Habitat categories and Priority Habitats guide habitat allocation. Major sections include:
  - Broadleaved mixed and yew woodland; coniferous woodland; boundary/linear features; arable & horticulture; improved/neutral grassland; hay meadows; calcareous and acid grasslands; bracken; dwarf shrub heath; fen/marsh/swamp; bog; standing water; montane; urban; inland rock; and more.
- Priority Habitats provide finer classification within Broad Habitats (e.g., limestone pavement, inland rock outcrop, cliff/ledges, sand dunes, reedbeds, purple moor grass and rush pastures, etc.).
- The Habitat Key and Appendix IV offer detailed habitat descriptions and criteria to assign plots to Broad and Priority Habitats (including urban and alpine/montane contexts).

## Appendices and Supplemental Guides
- Appendix I: Collector & Survey123 generic reference guides (installation, map use, collecting data, and surveys management).
- Appendix II: Random numbers between 0 and 1 (for reference on random point allocation in plot selection).
- Appendix III: Plot types recorded in previous surveys (codes and definitions for areal, X plots, soil plots, Y plots, margins, hedgerows, etc.).
- Appendix IV: Habitat descriptions and Priority Habitat details to aid accurate classification across broad geographic contexts.

## Practical Considerations for Data Support
- Ensure data completeness by enforcing header, relocation, and nest data entry through the survey software.
- Facilitate data usability by maintaining consistent plot IDs, location accuracy, and thorough notes on plot disturbances.
- Promote outputs by developing data products (dashboards, self-serve analyses) and collecting user feedback for iterative improvements.
- Maintain cross-system compatibility by standardising data formats (Survey123/Collector integration, GPS and sketch maps, and habitat classifications) to enable broader data reuse.