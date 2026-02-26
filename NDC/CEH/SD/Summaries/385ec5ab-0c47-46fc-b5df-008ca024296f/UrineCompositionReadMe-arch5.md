# UrineComposition.csv

## Overview
- Dataset of sheep (Welsh Mountain ewe) urine chemical composition and associated metadata.
- Project: Uplands-N2O; Grant NE/M015351/1.
- Authors listed; data reuse should be fully cited.
- Aims aligned with robust data governance: traceable provenance, clearly defined methods, and metadata to support reuse.

## Data Content
- Contains chemical composition measurements for sheep urine and related metadata.
- Sample handling and storage:
  - Urine filtered on ice through Whatman No.1 filter (11 μm) to remove particulates.
  - Samples stored frozen at -20 °C before analysis.
- Measurements and methods:
  - pH and electrical conductivity (EC) measured with standard electrodes.
  - Total nitrogen (TN) and dissolved organic carbon (TOC) measured with Multi N/C 2100S analyser.
  - Urea quantified via enzymatic method (Orsenneau et al., 1992).
  - Ammonium (NH4+) and nitrate (NO3−) measured colorimetrically (Mulvaney 1996; Miranda et al., 2001).
  - Free amino acids quantified fluorometrically (Jones et al., 2002).
  - Allantoin, creatinine, uric acid, hippuric acid, benzoic acid quantified by HPLC (Varian Pro Star 310; C18 column; 218 nm detection; 1 mL/min; mobile phase A/B composition provided).
  - K+, Na+, Ca2+ measured with flame photometry (Sherwood Model 410).
- Emphasis on detailed, method-specific parameters to enable reproducibility.

## Data Headers (Variables)
- Season: Spring, Summer, or Autumn.
- Site: Semi-improved or improved pasture locations.
- Sheep: Replicate sheep number.
- Date: Date of urine collection (dd/mm/yyyy).
- Time: Approximate urination time (hh:mm).
- Vol: Urine event volume (ml).
- TOC: Urine dissolved organic carbon (g C L−1).
- TN: Urine total nitrogen (g N L−1).
- pH: Urine pH.
- EC: Urine electrical conductivity (mS cm−1).
- Urea: Urine urea content (g urea-N L−1).
- Nitrate: Nitrate content (mg NO3−-N L−1).
- Ammonium: Ammonium content (mg NH4+-N L−1).
- AA: Amino acid content (mg amino acid-N L−1).
- Allantoin: Allantoin content (g compound L−1).
- Creatinine: Creatinine content (mg compound L−1).
- Uric: Uric acid content (mg compound L−1).
- Hippuric: Hippuric acid content (g compound L−1).
- Benzoic: Benzoic acid content (mg compound L−1).
- Ca: Calcium content (mg Ca L−1).
- Na: Sodium content (mg Na L−1).
- K: Potassium content (g K L−1).

## Data Provenance and Citation
- Project: Uplands-N2O; grant NE/M015351/1.
- Authors: Karina A Marsden et al.
- Data reuse: Please provide full citation.
- References for methods:
  - Jones et al. 2002 (amino acids determination in soils/solutions).
  - Miranda et al. 2001 (nitrate/nitrite detection).
  - Mulvaney 1996 (inorganic nitrogen forms; Methods of Soil Analysis).
  - Orsenneau et al. 1992 (urea determination).

## Quality, Standards, and Governance
- metadata-rich dataset with explicit units for each variable, aiding interoperability and reuse.
- Clear documentation of sample processing, instrument methods, and analysis parameters to support reproducibility.
- Governance considerations for data stewards:
  - Maintain complete provenance: project, grant, authors, collection dates, and locations.
  - Preserve explicit units and measurement contexts; consider including a data dictionary and unit harmonization notes.
  - Ensure proper citation and licensing information accompanies any data reuse.
  - Plan for updates or versioning if additional samples or corrected analyses are added.
  - Facilitate discoverability by indexing key attributes (Season, Site, Date, Sheep, Vol, measured constituents).

## Access and Sharing Notes
- Data likely intended for sharing in data portals or catalogues; ensure upload includes full metadata, method details, and references.
- If data are reused, users must cite the dataset per the provided guidance.