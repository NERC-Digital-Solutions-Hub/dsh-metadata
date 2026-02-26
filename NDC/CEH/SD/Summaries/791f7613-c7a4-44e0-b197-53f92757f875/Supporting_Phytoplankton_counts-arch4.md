# Supporting information

- This document describes the BLEL_Phytoplankton_counts.csv dataset, collected from Blelham Tarn in the Lake District, NW England, during 2016 (weekly from June to November) at depths from 1 to 6 meters.
- Collected by Emma Gray for project NEC05744, with preservation in Lugols iodine and careful handling to minimize evaporation and light exposure.

## Sampling and preservation

- Water samples taken at metre intervals from 1 m to 6 m depth using the automated monitoring buoy (deepest point ~14.5 m).
- Samples stored in dark bottles with Lugols iodine, kept cool and protected from light; checked periodically for evaporation losses and topped up as needed.

## Laboratory processing and measurement

- Phytoplankton were counted and measured using PlanktoMetriX (PMX) software, which supports counting and biovolume calculations for organisms in the 1–1000 µm size range.
- A PMX database was created using 2011–2015 data to identify species common to Blelham Tarn; 142 phytoplankton species identified.
- Biovolume calculations used CEN (2014) guidance to assign geometric shapes and equations to each species.
- Sub-sampling performed at 1 m depth to identify species presence; ten measurements per species were averaged and applied to samples from 1–5 m.
- Phytoplankton counts were conducted with an Olympus BX45 inverted microscope in a Lund chamber (Lund, 1959) using random fields of view (100 fields at x100 magnification and 100 fields at x400 magnification).
- Counting limits: 100 individuals counted per session; beyond that, counts were not continued.

## Data structure and contents

- File contents include: sampling date, depth (1–6 m), species name, AvX (mean x-dimension in µm), AvY (mean y-dimension in µm), AvZ (mean z-dimension in µm), Biovolume (µm³/mL).
- Measurements reflect means based on 10 measurements per species.
- Depth-related biovolume applications: biovolumes calculated for samples at 1–5 m using species-specific shapes and equations.

## Data quality, standards, and provenance

- Standards and references used: CEN (2014) guidance for estimating phytoplankton biovolume; Lund (1959) counting chamber methodology; Ramsbottom (1976) depth charts; Zohary et al. (2016) PMX system description.
- Data provenance: explicit documentation of sampling procedure, preservation, laboratory workflow, and software-based counting/biovolume calculations, enabling reproducibility and auditability.
- Quality control measures include preservation protocol, controlled laboratory conditions, standardized counting methods, and clear criteria for including cells in counts (50% visibility threshold within field of view).

## Usage notes and limitations

- Temporal and spatial scope: data cover weekly samples only from June–November 2016 at depths 1–6 m; wider depth range or different timeframes are not included.
- Sub-sampling approach: species ID based on a 1 m subsample; biovolumes applied to deeper samples (1–5 m), which may introduce assumptions about species distribution and abundance across depths.
- Counting cap: analysis limited to 100 individuals per field of view; beyond this, counts are not extended, which may affect abundance estimates for highly abundant species.
- Metadata availability: essential fields (date, depth, species, dimensions, biovolume) are provided, supporting data discovery and re-use within broader aquatic ecology datasets.

## Figure and references

- Figure 1: Location of Blelham Tarn with monitoring buoy at the deepest point (14.5 m).
- References: CEN (2014) guidance on phytoplankton biovolume; Lund (1959) counting chamber methodology; Ramsbottom (1976) depth charts; Zohary et al. (2016) PlanktoMetrix system.