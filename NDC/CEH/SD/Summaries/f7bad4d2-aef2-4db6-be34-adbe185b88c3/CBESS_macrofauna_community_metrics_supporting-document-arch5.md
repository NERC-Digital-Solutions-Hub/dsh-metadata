# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) macrofaunal community metrics - total abundance (TA), total biomass (TB), species richness (SR), evenness (J) and community bioturbation potential (BPc) in mudflat and saltmarsh habitats..

## Overview
- Dataset describes macrofaunal community metrics (TA, TB, SR, J, BPc) across mudflat and saltmarsh habitats.
- Derived from 6 sites across 2 locations, with winter and summer sampling in 2013.
- 3 replicates across 22 quadrats at four spatial scales.
- Staff responsible: Christina Wood and Martin Solan.

## Data collection design and workflow
- Field campaign: CBESS field campaign during winter and summer 2013; no repeat sampling planned.
- Sampling structure: 6 sites (Essex and Morecambe Bay) across two habitat types (mudflat and saltmarsh) with 3 replicates on 22 quadrats.
- Habitat and site context: Essex saltmarsh (clay soils) vs. Morecambe Bay saltmarsh (sandy soils); mudflats with different sediment types; broader differences in inundation, creek structure, and vegetation.
- Procedures: at each quadrat, take 3 cylindrical cores (10 cm depth, 0.0 cm diameter), fix in 4% buffered formalin, sieve through 0.5 mm, preserve residues in 70% IMS, identify to species or major debris, and count/describe.
- Upload and documentation: dataset intended for sharing through portals and catalogues; potential documentation of work performed.

## Variables, measurements and calculations
- Observed metrics: Total abundance (TA), Total biomass (TB), Species richness (SR), Evenness based on abundance (J'abundance), Evenness based on biomass (J' biomass), Community bioturbation potential (BPc).
- Derived relationships and scales: Metrics calculated per square meter; calibration factor used to convert counts/weights to per m^2 units.
- Taxon and data structure: Species-level identifications where possible; major groups noted if damaged; all data organized with location, habitat, site, quadrat, replicate, season, and scale codes.
- Scales and formats: Data organized by Row Number, Season (Winter/W), Location (Essex/Morecambe), Site, Habitat (Mudflat/Saltmarsh), Quadrat, Scale (A-D), Replicate; specific metric fields for TA, TB, SR, H' max, H' (abundance), J' (abundance), H' (biomass), J' (biomass), BPc.

## Data processing, quality control and provenance
- Processing steps: Core collection, fixation, sieving, preservation, counting, weighing, and per-m^2 calculations; BPc components calculated from species abundances, biomasses, mobility, and reworking indices with a defined formula.
- Quality control: Data entry by two people with cross-checks; biomass values validated against abundance data; calculations double-checked.
- Transparency and provenance: Detailed procedural descriptions, including formulas, measurement units, and transformation steps; raw data file referenced (CBESS_macrofauna_abundance.csv) alongside derived metrics file.

## Data formats and storage
- Primary file format: CSV.
- Dataset field descriptions provided to support interpretation and reuse, including explicit definitions and cell formats for each field.
- Documentation and metadata alignment: Field-level metadata (Season, Location, Site, Habitat, Scale, etc.) supports discoverability and interoperability.

## Access, sharing and documentation
- Sharing approach: Datasets uploaded to relevant portals and catalogues; work is documented to support reuse and traceability.
- Documentation emphasis: Clear definitions for each metric, calculation methods, and data checks; site and habitat context described to aid correct interpretation.
- Update and maintenance: Monitoring occurred in 2013; no planned repeats indicated, affecting long-term update potential.

## Governance, challenges and considerations for data stewards
- Governance focus: Provenance, standardization of metadata, clear data processing workflows, and explicit quality control practices.
- Key challenges to anticipate:
  - Ensuring timely data from multiple sites and harmonized metadata across habitats and scales.
  - Maintaining interoperability across systems and formats when integrating with portals.
  - Handling one-off datasets without planned updates or revisions.
  - Managing potential discrepancies in site descriptions and environmental context over time.
- Data stewardship implications:
  - Preserve full methodological details (sampling design, core collection, processing steps, and calculation formulas) for auditability and reuse.
  - Maintain robust links between raw data (CBESS_macrofauna_abundance.csv) and derived metrics.
  - Ensure consistent metadata coding (Season, Location, Site, Habitat, Scale) to enable cross-dataset discovery and integration.