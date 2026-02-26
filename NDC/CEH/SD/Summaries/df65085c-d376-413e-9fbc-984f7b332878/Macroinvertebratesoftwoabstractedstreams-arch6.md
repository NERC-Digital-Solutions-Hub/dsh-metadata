# Macroinvertebrates of two abstracted streams - taxon data.csv

## Overview
- Dataset description for macroinvertebrate communities in two UK streams (Howes Beck and Heltondale Beck) upstream and downstream of water abstraction points in the Lowther catchment, Cumbria.
- Sampling conducted on 23–24 September 2010; streams are tributaries of the Lowther, within the Eden catchment.
- Aimed at providing species-level taxon data and accompanying habitat/environmental information to support analyses of biotic communities in relation to habitat and hydrology.

## Data structure and content
- Taxon data file: Macroinvertebrates of two abstracted streams - taxon data.csv
  - Columns:
    - A: Sample identifier (see sample codes)
    - B: Taxon name (as per Davies and Edwards 2011)
    - C: Taxon code (as per Davies and Edwards 2011)
    - D: Life stage (L, N = larva/nymph; P = pupa; A = adult; U = life stage not relevant)
    - E: Abundance in sample (per 0.0625 m2)
- Sample codes
  - Format: waterbody (HB Howes Beck or HDB Heltondale Beck) + position to abstraction (US upstream or DS downstream) + replicate number (1–5)
- Supporting information (Table 1: General environmental data)
  - Columns (A–R) include:
    - Stream name; Position (US/DS); Grid reference; Northings; Eastings; Altitude (m); Slope (m/km); Distance from source (km); Altitude of source (m); Geology codes (Solid; Drift); NCC geology; Wetted width (m); Depth (cm); Habitat Quality Assessment (HQA) from RHS; Habitat Modification Score (HMS) and HMS class
  - Streams and samples included:
    - Howes Beck (US and DS positions)
    - Heltondale Beck (US and DS positions)
  - Habitat characterization categories (RHS) indicate deformation/modification status; most records are "Predominantly un-modified" with at least one row indicating "Significantly modified."

## Methods and design
- Study design
  - Sampling reaches ≈100 m around abstraction points in two streams (Howes Beck and Heltondale Beck).
  - Five riffles sampled per reach; sampling within 50 m upstream and 50 m downstream of each position, across 2 positions (US, DS) per stream.
  - Replicates: 1–5 per reach.
- Field methods
  - Macroinvertebrates collected with Surber samplers (mesh 250 μm; area 0.0625 m2); depth targeted ~5 cm.
  - Field samples preserved in 4% formaldehyde; samples later washed through 250 μm sieve in the lab.
  - Taxonomic identification to the lowest feasible level (usually species); valid taxon names and unique codes provided.
  - Sample identifiers cross-checked against laboratory records for data integrity.
- Habitat and environmental data
  - Habitat assessment via River Habitat Survey (RHS) protocol (Environment Agency 2003).
  - Spatial and environmental variables derived using Intelligent River Network (Version 17); variables described by Dawson et al. (2002).
  - Supporting environmental data include grid references, elevations, slope, geology, widths, depths, HQA, HMS, and RHS class.
- Taxonomy and data standards
  - Taxa named and coded according to Davies, C. and Edwards, F.K. (2011) Code list for recording macroinvertebrates in freshwater in the British Isles.
  - Data entry validated by cross-checking printouts with laboratory sheets.

## Data provenance and quality
- Contributors
  - Sample collection: François Edwards, Peter Scarlett, Gearóid Webb
  - Laboratory analysis: Gearóid Webb, François Edwards, Helen Vincent
  - Supporting information: Peter Scarlett, Gearóid Webb, François Edwards
- Data integrity
  - Species identifications and codes follow a published taxonomy list; presence/absence and abundance recorded per 0.0625 m2 sample area.
  - Validation performed by cross-checking printed data with lab sheets.

## Usage notes
- The taxon dataset enables analysis of macroinvertebrate community composition across streams, positions relative to abstraction points, and replicates.
- Environmental data accompanying each sample provide context for habitat quality and hydrological setting, allowing exploration of relationships between taxa and habitat variables.
- The data are suitable for self-serve exploration and combination with other datasets, following the documented coding and metadata.

## Related references
- Davies, C. & Edwards, F.K. (2011). Code list for recording the macroinvertebrates in freshwater in the British Isles. Centre for Ecology and Hydrology.
- Dawson, F.H., Hornby, D.D. & Hilton, J. (2002). Method for automated extraction of environmental variables for river classification. Aquatic Conserv: Mar. Freshwater Ecosyst.
- Environment Agency (2003). River Habitat Survey in Britain and Ireland. Field Survey Guidance Manual: 2003 version.