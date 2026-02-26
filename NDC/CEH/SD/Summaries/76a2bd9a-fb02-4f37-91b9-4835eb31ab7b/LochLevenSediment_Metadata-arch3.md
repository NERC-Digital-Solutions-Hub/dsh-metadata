# LochLeven_SedimentDataset.csv

## Overview
- Dataset from a project on phosphorus cycling between bed sediments and overlying water in Loch Leven (April 2004–April 2005).
- Includes indicators of benthic algal biomass.
- Used in multiple publications to describe phosphorus mobilisation and the role of benthic microalgae in Loch Leven.

## What the dataset contains
- Measurements of water quality, sediment chemistry, and phosphorus fractions.
- Focus on sediment-water interactions and phosphorus mobility.
- Data used to describe internal phosphorus loading and phytobenthic regulation of cycling.

## Sampling regime and sites
- Monthly sampling from April 2004 to April 2005.
- Six permanent sites along a depth transect (2.0, 2.5, 3.5, 5.5, 10.0, 22.0 m).
- At each visit: field measurements and laboratory analyses of collected samples.
- Consistent sampling regime throughout the study period.

## Determinands and measurements
- Physical/chemical parameters: dissolved oxygen (%sat), conductivity (mS/cm), pH, temperature (°C).
- Nutrients: soluble reactive phosphorus (SRP, µg/L), total soluble phosphorus (TSP, µg/L), total phosphorus (TP, µg/L), ammonium-nitrogen (NH4-N, µg/L), soluble silica (SiO2, mg/L).
- Biological indicator: Chlorophyll a (µg/L and µg/g dry weight).
- Sediment phosphorus fractions: labile P, reductant-soluble P, reductant-soluble unreactive P, metal oxide P, organic P, apatite-bound P, residual P; total P including sediment fractions.
- Data captured for surface, bottom, pore water, and sediment where applicable.

## Methods and analysis
- In situ measurements: depth profiles of temperature, DO%, pH, and conductivity with handheld probes.
- Sampling: single sediment cores (approx. 67 mm internal diameter) with ~30 cm overlying water and 20 cm sediment.
- Laboratory processing: filtration (Whatman GF/C), storage at 4 °C, pigment analysis after extraction; chlorophyll a quantified spectrophotometrically with phaeopigment correction.
- SRP/TP: colorimetric methods (Murphy & Riley 1962; Wetzel & Likens 2000) with digestion steps for TP/TSP.
- NH4-N and SRSiO2: standard colorimetric methods with absorbance measurements.
- Chlorophyll a: acetone extraction and spectrophotometric measurement.
- Sediment-P fractionation: sequential chemical extraction (NH4Cl, NaHCO3/Na2S2O4, NaOH, HCl) to partition P into fraction types; subsequent SRP measurements after each step.
- All extractions conducted in dark at ~20 °C; analyses performed on supernatants after centrifugation and filtration.

## Data format and structure
- Data stored in a single ASCII CSV file.
- Columns include: Site, Depth, Month, Date, DO, Cond, pH, Temp, SRP, TSP, TP, NH4, SiO2, Chl a, labile P, reductant soluble P, reductant soluble SRP, metal oxide P, organic P, apatite bound P, residual P, and chlorophyll a (gdw and gdw-based values as applicable).
- Table entries indicate site position (OS grid references), depth, and counts of observations per site.
- Units and measurement context specified (e.g., surface, bottom, pore, sediment where relevant).

## Data usage and relevance
- Data underpin analyses of phosphorus mobilisation from bed sediments and the role of epipelic/benthic microalgae in regulating cycling.
- Widely referenced in publications (Spears et al.; related works) to support understanding of phosphorus fractions, mobility, and internal loading in a large shallow lake.

## Data access and governance considerations
- Data are linked to published studies and standard analytical methods (APHA 1992 standards).
- Metadata in the document describe sampling method, site characteristics, determinands, units, and analytical procedures.
- The dataset is formatted for reuse (CSV with clear column labeling); sharing of underlying data is feasible given the publication history and methods transparency, though explicit governance details are not provided in the document.

## References (methods and context)
- APHA (1992). Standard methods for the examination of water and wastewater.
- Murphy & Riley (1962); Wetzel & Likens (2000) for phosphate determination and TP/TSP procedures.
- Psenner et al. (1988); Farmer et al. (1994) for phosphorus fractionation and mobility methods.
- Golterman et al. (1978) for SRSiO2 methods.
- Related Spears et al. (2006–2012) publications on sediment phosphorus fractions and lake phosphorus dynamics.