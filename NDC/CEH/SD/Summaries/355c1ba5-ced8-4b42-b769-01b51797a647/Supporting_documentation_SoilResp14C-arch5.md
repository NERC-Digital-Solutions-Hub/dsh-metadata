# Soil respired radiocarbon as CO2 and CH4 from peatland plateaus and thawing peatland plateaus and from burnt and unburnt forests from permafrost in subarctic Canada

## Overview
- Study of radiocarbon content in soil-respired CO2 and CH4 collected during summer 2013 (near Teslin) and 2014 (near Yellowknife) in subarctic Canada.
- Sampling across multiple sites representing peatland plateaus, thawed peatland features, and burnt/unburnt black spruce forests.
- Data capture includes replicate locations, sample types, and measurement results for 14C enrichment and conventional radiocarbon ages.

## Dataset scope and structure
- Gas types: CO2 and CH4.
- Sites for CO2: FFU (FireFox Unburnt), FFB (FireFox Burnt), TPP (Teslin Peatland Plateau), TWM (Teslin Wetland Margin), MCU (Mosquito Creek Unburnt), MCB (Mosquito Creek Burnt), WTP (White Truck Plateau), WTM (White Truck Moss), WTS (White Truck Sedge), WTW (White Truck Wetland).
- Sites for CH4: TW (Teslin Wetland; includes TW5m and TWMID positions), WTM, WTS, WTW.
- Replicates: three replicate locations per site (e.g., FFU1, FFU2, FFU3).
- Sample types: DEEP, BOTTOM (PVC collars), and PROBE (stainless steel tube with permeable membrane) at specified depths.
- Measurements: radiocarbon enrichment as percent modern carbon; ages as conventional radiocarbon years BP.
- Data identifiers: Publication_code for linking samples to analysis in the radiocarbon facility workflow.
- Analytical workflow: samples sent to NERC Radiocarbon Facility (East Kilbride, UK) for graphitization and AMS 14C analysis.

## Sampling design
- Temporal scope: summer sampling in 2013 (near Teslin) and 2014 (near Yellowknife).
- Replication: three replicates per site/location to capture spatial variability.
- Depths and sample types:
  - CO2: DEEP and BOTTOM collars; vegetation clipped at surface to minimize CO2 contributions from vascular plants.
  - CH4: CH4 sampling from collars and PROBE without vegetation clipping (to preserve CH4 transport pathways).
- PROBE sampling: gas collected from a specific depth via a perforated stainless steel tube with a gas-permeable membrane, connected to tubing to prevent atmospheric air ingress.

## Measurement and processing workflow
- CO2 (DEEP/BOTTOM):
  - Chamber headspace accumulates CO2 to ~800 ppm, then CO2 is reduced in the headspace to ~200 ppm using soda lime.
  - Two sequential sampling events across the growing season (end of July/early August and end of August/early September) using a zeolite Type 13X sieve to capture CO2 for 14C analysis.
- CH4 (DEEP/BOTTOM):
  - CH4 collected in PVC chambers; headspace monitored with a DP-IR analyzer; samples transferred to 10 L foil bags for lab processing.
  - CH4 from PROBE collected by degassing soil water into headspace of a 10 L gas bag.
  - Laboratory processing follows Garnett et al. 2012: remove CO2, combust CH4 to CO2, trap on zeolite 13X.
- Data for all samples are sent to AMS facility for 14C analysis; results tied to Publication_code.
- Radiocarbon values expressed as percent modern carbon; ages reported as years BP.

## Data variables and metadata
- Core variables: site code, gas type (CO2/CH4), replicate ID, sample type (DEEP/BOTTOM/PROBE), depth (where applicable), location description, 14C enrichment (% modern carbon), conventional 14C age (years BP), and Publication_code.
- Metadata considerations: clear linkage between field sample, processing steps, and AMS results; documentation of sampling conditions (e.g., vegetation clipping for CO2, lack of clipping for CH4).

## Data provenance and quality
- Provenance trail: field collection (collars and probes), in-field handling (vegetation clipping decisions), laboratory processing (CO2 capture, CH4 handling, sieving, and drying), AMS measurement at NERC facility.
- Quality assurance anchors: replication, season-long sampling for representative hydrocarbon flux, referencing established methods (Garnett et al., 2012) for CH4 processing.

## Data access and stewardship considerations
- Data are organized with a Publication_code to enable cross-referencing between field samples and AMS results.
- Measurements include both gas-specific samples (CO2 vs CH4) and depth-specific samples (DEEP/BOTTOM/PROBE), enabling reproducibility and comparative analyses across site types (peatlands, thaw features, burnt vs unburnt forests).
- Units and representations are explicit (percent modern carbon for enrichment; years BP for ages).

## Limitations and caveats
- Seasonal and geographic scope limited to two summers in subarctic Canada; results reflect conditions during sampling windows.
- Vegetation handling differs between CO2 and CH4 sampling, which may influence comparative interpretations of gas flux pathways.
- Some sites and sample types are more challenging to transfer or replicate (e.g., deep soil layers, complex peatland structures).

## References
- Garnett, M. H., Hardie, S. M. L. & Murray, C. Radiocarbon analysis of methane emitted from the surface of a raised peat bog. Soil Biology and Biochemistry 50, 158-163 (2012).