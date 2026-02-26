# Enteric virus concentrations, pH and turbidity in wastewater discharged to the Conwy River and estuary, North Wales (2016-2017)

- Overview
  - Purpose: Report pH, turbidity, and concentrations of enteric viruses in wastewater discharged to the Conwy River and estuary.
  - Timeframe and sites: 2016–2017 at three wastewater treatment plants (Betws-y-Coed, Llanrwst, Ganol/Llandudno Junction) with discharges to the river.
  - Data product: A single CSV dataset containing sampling and analytical results, suitable for map-based visualization of spatial and temporal trends.
  - Spatial coverage: Site coordinates provided for each sampling point; Betws-y-Coed and Llanrwst samples are effluent, Ganol samples include influent (autumn and winter).

- Sampling regime and collection methods
  - Sampling apparatus: ISCO automatic water samplers at each site.
  - Sampling pattern: Every second hour for three days per event, producing 36 samples per site per event.
  - Sample types by site: Betws-y-Coed and Llanrwst (effluent); Ganol (influent for autumn and winter; no Ganol summer data).
  - Data collection regime described with seasonal sampling events (summer, autumn, winter) and site-specific details.

- Laboratory instrumentation and analysis
  - Physicochemical measurements: pH and turbidity (pH meter S2K922; turbidity meter T-100).
  - Viral concentration and nucleic acid handling: Tangential flow filtration for concentration; nucleic acid extraction with NucliSENS miniMag; qRT-PCR/qPCR assays for target viruses.
  - Viral targets quantified: Norovirus GI (NoVGI), Norovirus GII (NoVGII), Sapovirus GI (SaVGI), Hepatitis A (HAV), Hepatitis E (HEV), Adenovirus (AdV), and Mengovirus (MgV) as process control.
  - Assay details: Duplex/triplex qRT-PCR setups with specified primers/probes; separate SYBR Green qPCR for Adenovirus.
  - Quality control: Process controls (mengovirus) spiked into autumn/winter samples with recovery >10% to validate extraction and concentration.

- Data structure and metadata
  - Dataset format: One CSV spreadsheet.
  - Key columns (examples): Sampling_event, Sample_type, Date_Time(GMT), pH, Turbidity_NTU, NoVGI_gc/l, NoVGII_gc/l, SaV_gc/l, HAV_gc/l, HEV_gc/l, AdV_gc/l.
  - Data units: pH (dimensionless), Turbidity in Nephelometric Turbidity Units (NTU), viral concentrations in genome copies per liter (gc/L).
  - Detection limits: Detection limit ~100 gc/L; quantification limit ~200 gc/L; below-detection values recorded as negative.
  - Column metadata: Table 3 provides descriptions of headings; some fields marked as not measured (n.m.) where applicable.

- Data interpretation and GIS relevance
  - Enables spatial mapping of wastewater quality and viral contamination along the Conwy River and estuary.
  - Temporal analysis possible using GMT timestamps and seasonal sampling events.
  - Useful for visualizing relationships between pH, turbidity, and viral presence across sites and over time.

- Data quality and limitations
  - Variability in sampling type across sites (effluent vs influent) and seasons; caution needed when comparing across sites.
  - Detection/quantification limits impose censoring for low concentrations.
  - Calibration and replication details are provided for instruments and PCR assays to support data reliability.
  - Data derived from environmental samples with complex matrices; the reported values include appropriate quality control acknowledgments.