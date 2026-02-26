# Physical, chemical and biological data from peatland ponds, Pennines, UK, 2012-2014

## Overview
- Dataset of biological, physical, and chemical data from peatland ponds in the Pennine hills, northern England, collected between 2012 and 2014.
- Biological data: invertebrate abundances (macroinvertebrates) per pond; physical data include location, altitude, pond morphology; chemical data include dissolved ions and on-site measurements (e.g., pH).
- Primary aim: to investigate how invertebrate communities colonise and establish in restored peatland ponds over time, quantify changes in abundance and diversity (alpha, beta), and identify associations between physico-chemical variables and ecological communities.
- Study led and interpreted by Beadle et al. (University of Leeds).

## Data collected and measurements
- Biological data: invertebrate abundances identified to species level where possible; CHIRONOMIDAE subsampling for detailed resolution when total abundance was high.
- Physical data: location coordinates, altitude, pond aspect, pond dimensions (long axis, short axis, perimeter), and estimated pond volume.
- Chemical data: on-site measurements of dissolved oxygen, water temperature, pH; laboratory analyses for total nitrogen (TN), total phosphorus (TP), dissolved organic carbon (DOC), aluminum (Al), iron (Fe), and silica (Si).
- Data completeness: dataset is complete; five pH values missing due to sensor failure were imputed using a statistical relationship with magnesium ([Mg]).

## Study design and sampling regime
- Study sites: six peatlands used for a chronosequence approach (Moor House, Tennant Gill, Cold Fell, Yad Moss, Halton Lea, Oughtershaw Beck), with additional naturally formed ponds at several sites.
- Pond sampling regime:
  - For chronosequences: sampling conducted on each visit across five ditches with one pond sampled per ditch; sampling months varied across 2013–2014.
  - For other sites: random sampling within accessible ponds, subject to landowner access; total ponds sampled across sites: 105.
- Temporal coverage: field sampling from 2012 to 2014, with regular two-monthly visits (ages of ponds documented for each year).
- Pond status: mixture of restored/ageing ponds and naturally formed ponds (some natural ponds denoted with a prefix 'n').

## Site characteristics and metadata
- Detailed site attributes provided per pond, including:
  - Site name, location coordinates, mean altitude, restoration year, pond age in 2013 and 2014.
  - For some ponds, natural status is noted (e.g., WiddyBank Fell, Harwood Fell, Butterburn Flow, Geltsdale noted as natural).
- Data files reference pond codes to connect biological and physical–chemical data.

## Data structure and formats
- Four CSV files comprising the dataset:
  1. Chron_nat_inverts.csv (82 columns): pond code plus abundances for all invertebrate taxa per pool.
  2. MH_inverts.csv (45 columns): pond code plus invertebrate taxa abundances per pool.
  3. Chron_natural_physical_chemical.csv (26 columns): pond code, location, sampling date, pond age, coordinates, aspect, elevation, pond dimensions, volume, temperature, DO, pH, and solutes (TN, TP, DOC, Al, Fe, Si).
  4. MH_physical_chemical.csv (26 columns): detailed physical and chemical measurements per pool with many field and lab-derived variables (units and methodologies noted for each variable).
- Coding and labeling:
  - Pond codes align across files (e.g., MHC06 for Moor House Chronosequence pond 06; n-prefixed codes indicate natural ponds).
  - Numerous fields document location, pond morphology, and sampling metadata (date, age, GPS coordinates, etc.).

## Field and laboratory methods
- Macroinvertebrate collection: long-handled net (250-µm mesh); two minutes sampling across mesohabitats plus one minute surface search; samples preserved in 70% methylated spirits.
- Taxonomic processing: sorting and identification under a microscope; Chironomidae sub-sampling when total abundance was high; chemical and elemental analyses performed on filtered water samples.
- On-site measurements: altitude/ location via GPS; pond aspect and dimensions measured in the field; depth measurements (minimum/maximum/mean) documented.
- Water quality measurements: on-site DO, temperature, and pH using a portable HACH HQ30d meter.
- Laboratory analyses: TN, TP, DOC, Al, Fe, Si measured with appropriate instruments (Analytikjena multi N/C 2100, San++ analyzer, and ICP-OES).
- Data handling: full methodology and data collection details are described in Beadle et al. (in press).

## Quality control and data integrity
- Independent experts verified macroinvertebrate identifications.
- Calibration: water temperature, DO, and pH sensors calibrated before each field visit.
- Laboratory instruments calibrated with standards across and beyond sample ranges.
- Data completeness notes: pH sensor failure addressed by statistical imputation for five values.

## Reuse and relevance for monitoring frameworks
- The dataset exemplifies comprehensive monitoring data collection, including:
  - Linking biological communities to physical habitat structure and chemical conditions.
  - Longitudinal assessment across restoration chronosequences and natural ponds.
  - Transparent data structure with explicit metadata, units, and methodologies to facilitate reproducibility and policy evaluation.
- Useful for evaluating environmental health measures related to peatland restoration, invertebrate community responses, and the influence of physico-chemical drivers on aquatic ecosystems.