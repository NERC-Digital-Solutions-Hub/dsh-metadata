# MOOR HOUSE VEGETATION RE-SURVEY 2008

## Overview
- Field survey recording plant species presence and abundance within 2x2 m plots.
- Collect general plot data (location, slope, aspect, peat depth, vegetation height), species presence/cover, and plot photos.
- Data captured digitally via Vegplots; plot photos stored weekly on a central network location.

## Data capture workflow and tools
- Data capture through Vegplots integrated with ArcMap plot maps.
- Plots identified in ArcMap; data entered on the Standard Recording screen in Vegplots.
- Two tablets (A and B) may be used; datasets must be labeled (VegetationPlotsA.mdb vs VegetationPlotsB.mdb) to avoid overwriting.
- For U plots (un-enclosed), 2x2 m plots recorded directly from the 2 m2 quadrat.

## Data fields and taxonomy
- Header/Plot Description:
  - Slope, Aspect, Location type, Peat Depth (cm), Photos taken (Yes/No).
  - Plot location coordinates and altitude captured via GPS tools.
- Vegetation Height:
  - Estimate/measure at three points (e.g., North Corner, South Corner, Plot Centre) with height classes (0–5 cm up to >1 m).
- Admin:
  - Surveyors’ initials; Plot Completed status (Complete/Complete with validation errors/Incomplete).
- Notes:
  - Free text; date of survey and altitude recorded.
- Listed Species:
  - Grouped lists (Common species, Grasses, Sedges/Rushes, Ferns, Forbs/Woody, Mosses/Lichens, Crops, Unidentified).
  - Tabs allow selection across groups; if needed, unidentified species can be recorded (A–C on Common; D–Z on Unidentified).
- Selected Species:
  - As species are identified, they appear as records for the plot with estimated total cover.
  - Cover recorded in 1% presence, then 5% cover categories; avoid double counting and account for layered canopy.
  - Overhanging canopies of trees/shrubs counted as present with normal cover; bare ground excludes leaf litter and rock.
  - Use BRC list for taxa and accept combinations (e.g., Cardamine hirsuta/flexuosa) when species cannot be separated.
- Completing Plots:
  - Regular saves; validation checks highlight missing fields in red; validation required before exiting or changing plots.
- Plot Photo Protocol:
  - Two photos per plot (north-facing and south-facing, using compass).
  - Include plot number/type in photos; use weather writer backing labels to identify plot.
  - Photos downloaded weekly to Plot Photos folder: S:\ECOPRO\Moorhouse Veg Resurvey 2008\Completed Data\Plot Photos.

## Data quality, validation and governance
- Emphasizes minimizing disturbance while conducting a full census of vegetation.
- Regular backups and saves; data transfer and archiving to central network locations.
- Validation step flags incomplete fields and ensures data integrity before uploading.
- Clear protocol for handling unidentified species and combinations to maintain comparability with other surveys.

## Data storage, backups and transfer
- Weekly transfer of:
  - Plot photo data from cameras to S:\ECOPRO\Moorhouse Veg Resurvey 2008\Completed Data\Plot Photos.
  - Tablet data to S:\ECOPRO\Moorhouse Veg Resurvey 2008\Completed Data\Field_data via USB stick.
- A date-based folder naming (e.g., 150708) used for data archives.
- Upload process via Vegplots: use Complete Square for Upload to Wiki to create a zip named sqcompleted_0001.zip on the USB stick; copy to dated archive folder.
- If two tablets are used, ensure datasets can be distinguished.

## Plot types and scope
- Plot Type:
  - 2x2 m vegetation plots.
  - U plots: Unenclosed 2x2 m plots with no header metadata.
- Data completeness:
  - Even with Unidentified species, plots can be finalized; alerts generated during validation.
- Bryophytes/Lichens:
  - Restricted to the taxa listed; only those bryophytes/lichens recorded with individual cover values.
- Sphagna (Sphagnum) taxa:
  - Detailed sub-classifications provided (Green/Thin, Green/Fat, Red/Thin, Red/Fat) with representative species lists.

## Plot photos and imagery
- Photos provide locational context to aid re-locating plots in future surveys.
- Photos must include identifiable markers and plot information; avoid glare and capture a view that helps relocation.

## Equipment and logistics
- Comprehensive field equipment list for data collection (tablet with Vegplots, GPS, digital cameras, weather writer labels, quadrats, depth poles, tape measures, markers, batteries, etc.).
- Tablet accessories and backup power provisions emphasized to prevent data loss.

## Data protocols and governance implications
- Data standards:
  - Standardized data capture through Vegplots and ArcMap integration ensures consistency across plots and survey teams.
  - Use of predefined taxonomic lists and combination taxonomy to maintain comparability with other surveys.
- Metadata and provenance:
  - Includes plot metadata (location, altitude, slope, aspect), date, and instrument IDs (GPS, tablet).
- Access, storage, and rights:
  - Data stored on institutional network paths with controlled access and periodic archiving.
  - Data sharing primarily through internal repositories and Wiki-upload workflow; zip-based data packaging for transfers.
- Versioning and traceability:
  - Tablet labeling (A/B) and zip-based upload process support traceability of data sources and versions.

## Practical takeaways for data stewardship
- Enforce standardized data capture templates and taxonomic lists to maintain data quality and interoperability.
- Maintain strict backup and transfer schedules; document data pipelines and storage locations clearly.
- Use validation routines to ensure completeness before data are finalized and uploaded.
- Preserve metadata richness (plot descriptors, environmental variables, dates, equipment IDs) to support future discovery, discovery, and reuse.
- Manage access and archiving through defined network paths and version-controlled packaging.