# AFEX Experiment

## Overview
- Full factorial nutrient addition experiment at the AFEX project area of BDFFP/INPA near Manaus, Brazil, initiated May 2017.
- Design: eight nutrient treatments (control, N, P, cations [Ca, Mg, K], and their combinations N+P, N+cations, N+P+cations) with four replicate plots per treatment, across four independent blocks.
- Central measurement area per plot is 30 m × 30 m within 50 m × 50 m plots.

## Site and Experimental Setup
- Location: BDFFP area ~80 km north of Manaus; tropical rainforest site with mean temp ~26°C, mean annual rainfall ~2,400 mm.
- Plot layout: 32 plots total, arranged in four blocks with at least 250 m between blocks.
- Nutrient application: dry granules applied three times per year, rates per year include 125 kg ha⁻¹ N (urea), 50 kg ha⁻¹ P (triple superphosphate), 50 kg ha⁻¹ Ca, 20 kg ha⁻¹ Mg (dolomitic limestone), and 50 kg ha⁻¹ K (potassium chloride).

## Data Collected
- Root ingrowth cores: five 12 cm-diameter, 30 cm-deep cores per plot installed August 2017; collected every three months.
- Sampling focus: fine roots produced in Nov 2017–Feb 2018 (wet-season middle); four blocks of 15 minutes sampling totaling 60 minutes per plot.
- Depths: 0–10 cm and 10–30 cm.
- Replicates: N = 64 (per depth and time interval combination across plots).
- Morphological traits: measurements on fine roots <2 mm: root mean diameter, total length, area, volume; calculated SRL (cm g⁻¹), SRA (cm² g⁻¹), RTD (g cm⁻³).
- Biomass metrics: root volume (cm³) and total dry weight (g).

## Data Acquisition and Processing
- Root handling: five cores per plot, homogenized by plot and soil depth; manual extraction of fine roots over 60 minutes, followed by reintroduction of root-free soil.
- Biomass estimation: Michaelis-Menten asymptotic curve used to extrapolate from 60 to 180 minutes sampling (Metcalfe et al. 2007).
- Subsampling: fine roots (<2 mm) dried at 60°C for dry mass and further analysis.
- Imaging and analysis: root samples scanned at 600 dpi; analysis performed with WinRHIZO to derive morphological metrics.

## Data Structure and Metadata
- Core dataset components include:
  - Block (1–4)
  - Plot (1–8 within each block)
  - TRT (8 treatments: Control, N, P, Cations, N+P, N+cations, N+P+cations)
  - Depth (0–10 cm, 10–30 cm)
  - root_volume (cm³)
  - tot_weight (g)
  - SRL (cm g⁻¹)
  - SRA (cm² g⁻¹)
  - RTD (g cm⁻³)
  - diameter (mm)
- Data dictionary fields provide descriptions for each variable to support interoperability and reuse.

## Quality Assurance, Limitations, and Governance
- Standardized sampling intervals and positions within plots to enable comparability across treatments and depths.
- Use of established protocols (ingrowth cores, RootMorph metrics, and WinRHIZO analysis) to enhance data consistency.
- Explicit documentation of sampling times, depths, and treatment codes supports traceability, reproducibility, and future data discovery.
- Awareness of potential limitations from field-based measurements (timing, core extraction efficiency, and depth-specific variability) to be considered in data interpretation.

## Tools, Formats, and References
- Data and measurements implemented via spreadsheets; detailed spreadsheet schema provided for block, plot, treatment, depth, and root metrics.
- Imaging and analysis performed with WinRHIZO; root scans at 600 dpi.
- Key references: Metcalfe et al. (2007, 2008) for root extraction and root morphology methodology; Araújo (2002) for site climatology context.