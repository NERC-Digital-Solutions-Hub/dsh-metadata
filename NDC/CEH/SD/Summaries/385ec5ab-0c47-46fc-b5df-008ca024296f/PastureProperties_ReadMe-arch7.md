# PastureProperties.csv

## Overview
- Dataset describing properties of pasture fed to Welsh Mountain ewes during urine collection experiments.
- Collected at two study sites within Henfaes Research Station, North Wales, under the Uplands-N2O project (Grant NE/M015351/1).
- Data support analysis of pasture composition in relation to carbon and nitrogen content and other nutritional metrics.

## Geographic context
- Study area: Henfaes Research Station, Abergwyngregyn, North Wales (53°13′N, 4°0′W).
- Site 1: Semi-improved upland grassland (~270 m a.s.l.) with NVC vegetation types U4 and MG6.
- Site 2: Lowland improved pasture (<100 m a.s.l.) of Lolium multiflorum.
- Data suitable for spatial comparisons with vegetation classifications and site characteristics.

## Temporal coverage
- Semi-improved site: Spring, Summer, and Autumn 2016.
- Improved site: Autumn 2016.

## Data content and structure
- Samples: Forage (n = 4) per season per site.
- Analyses:
  - Total carbon (C) and nitrogen (N) content.
  - Crude protein (Protein).
  - Neutral detergent fibre (NDF).
  - Sugar.
  - Ash.
  - Metabolizable energy (ME).
  - Digestible organic matter (D).
  - Neutral detergent fibre (ADF).
  - Oil by acid hydrolysis (OAH).
  - Neutral cellulase gammanase digestibility (NCGD).
- Data headers (CSV): Season, Site, N, CN, Protein, NDF, Sugar, Ash, ME, NCGD, D, ADF, OAH.
- Analytical methods:
  - Forage analyses via TruSpec® Analyzer (Leco Corp., St. Joseph, MI).
  - Nutritional analyses performed by Sciantec Analytical (Cawood Scientific Ltd., North Yorkshire, UK).

## Data provenance and notes
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick.
- Data description emphasizes citation if data are reused.
- Data captured from two sites with season-specific sampling; analyses provide a range of nutritional and digestibility metrics.

## GIS use and considerations
- Site-level spatial context enables comparative mapping of pasture types (semi-improved upland vs. improved lowland) and seasonal variation in nutrient content.
- Attributes align with potential joinable GIS layers: vegetation classifications (NVC), site elevation, and plot locations if available.
- To map sampling points, precise coordinates or polygonal site boundaries are needed; currently, data are anchored to two sites with defined elevations and vegetation types.

## Data quality and usage notes
- Units: protein (g kg-1 dry weight), NDF, ADF, OAH (g kg-1), ME (MJ kg-1), D (%), CN (carbon-to-nitrogen ratio), etc.
- Limited spatial extent (two sites) but rich in chemical/nutritional detail across seasons.
- Ensure full citation per the dataset’s guidance when reused.