# The dark side of street lighting: impacts on moths and evidence for the disruption of nocturnal pollen transport

## Overview
- A dataset of moths captured at 20 lit-unlit site pairs near Wallingford, Oxfordshire, UK, collected May–September 2014.
- Three sampling methods used: night-time transects, light-trapping, and overhead flight-activity surveys.
- Pollen transported on moth proboscides was sampled and analyzed to assess nocturnal pollen transport.
- Data supporting a published analysis on the impacts of street lighting on moths and pollen transport (in press in Global Change Biology).
- Four CSV data files are provided, with explicit linking keys to enable traceability and re-use.

## Experimental design and sampling
- 20 lit sites paired with hedgerow unlit sites, each >100 m from any street lights.
- Pairs matched on road, verge/hedge, and field characteristics; lit-unlit distance within pairs ~207 m on average.
- Lighting intensity measured at lit sites (lux) and compared to unlit sites (0 lux at unlit).
- Sampling periods divided into three six-week blocks: spring, early summer, and late summer; weather conditions required for moth activity.
- Each pair sampled once per method per season; night transects and overhead counts conducted on the same night, light-traps on a separate night.
- Weather and environmental controls included alignment of site visits within pairs and proximity to full darkness.

## Data structure and files
- Four spreadsheets:
  - F1_sites.csv: site-level metadata for each pair (Site_Number, Site_Name, Lit_Site_Grid_Ref, Hedge_Height, Lamp_Height, Margin_Width, Crop, Distances to habitation and to unlit site, number of nearby lights, light meter lux).
  - F2_moths.csv: individual moth records (Date, Site, Method, Treatment, Reference, BinomialName, EnglishName, Family, Group).
  - F3_overhead.csv: overhead flight-activity counts (Date, Site, Treatment, FirstCount, SecondCount, ThirdCount).
  - F4_pollen.csv: pollen data linked to moths (MothReference, BinomialName) plus counts for 28 morphotypes with taxonomic notes.
- Key linking structure:
  - Site_Number connects F1 to F2 and F3.
  - MothReference in F4 links to F2 Reference.
- Data capture details in each file follow the study’s standardized methodology to enable reproducibility and cross-study comparability.

## Methods and instrumentation
- Night-time transects:
  - 25 m transects with a street light at the lit transect midpoint; red-filtered floodlight minimizes moth attraction.
  - Moths captured with a net after 1 minute per 5 m segment; attempts to avoid recapturing the same individual.
- Overhead flight-activity surveys:
  - 1-minute counts using a bright LED torch at the transect midpoint to quantify higher-altitude moth activity (3–12 m).
  - Repeated three times per sampling session; non-moth identifications excluded where possible.
- Light-trapping:
  - Heath-style traps with 8 W actinic bulbs, battery-powered; operated from dusk until battery depletion (~8 hours).
  - Trips conducted on separate nights from transects to avoid interference.
- Museum/field tools used:
  - CEM DT-1300 light meter; red-filter floodlight; Mactronic LED torch; Heath light-traps; standard microscopy for pollen processing.

## Pollen transport analysis
- Pollen sampling:
  - All captured moths were euthanized, relaxed, and swabbed on the proboscis with fuchsin jelly to capture pollen.
  - Swabs prepared on microscope slides and pollen morphotypes identified morphologically (400x) using published keys and reference collections.
  - Moths lacking functional proboscises (e.g., Hepialidae) were not swabbed.
- Morphotype approach:
  - Pollen morphotypes grouped when species-level resolution was not possible; identification anchors included local plant taxa and known insect-pollinated species.
- Timing:
  - Pollen analysis conducted from November 2014 to March 2015, after moth collection and storage.

## Data quality, provenance, and limitations
- Quality control:
  - No formal QC steps documented; dataset described as complete.
- Provenance and traceability:
  - Clear linking between site metadata, captured individuals, observational counts, and pollen data via unique identifiers.
  - Detailed metadata for site characteristics and sampling conditions to support replication and meta-analysis.
- Limitations and caveats:
  - Pollen identifications are morphotype-based and may not resolve to species for all morphotypes.
  - Overhead counts may include non-moth taxa despite efforts to exclude them.
  - Some values (e.g., pollen morphotype identifications) reflect known uncertainties inherent to morphological pollen work.

## Data governance, storage, and reuse
- Data structure is well-documented with explicit field definitions and units (e.g., lux, meters, counts).
- Joins across files enable tracing from site context to individual moths and to their pollen loads, supporting provenance and auditability.
- The dataset is tied to a peer-reviewed analysis and a published (in-press) paper, providing context for reuse and interpretation.
- For reuse beyond the original study, users should consult the associated publication for licensing and data-use terms and consider updating metadata if re-sharing within new governance frameworks.

## References
- Macgregor, C.J., Evans, D.M., Fox, R. and Pocock, M.J.O (in press) The dark side of street lighting: impacts on moths and evidence for the disruption of nocturnal pollen transport. Global Change Biology.