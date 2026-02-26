# LLYN HIR RAIN GAUGE READ ME DOCUMENT

## Overview
- Document notes installation of storage and tipping bucket (TB) rain gauges on Llyn Hir and documents a series of data-quality events and time-related adjustments observed during monitoring (2007–2009).

## Data sources and equipment
- Two rain measurement devices: storage gauge and tipping bucket rain gauge.
- Installation date recorded: 28/09/07.
- Field observations include occasional anomalies affecting readings (e.g., wind, water in storage gauge, ice).

## Key events and data adjustments
- 29/11/07 around 10:55: wind caused the tipping bucket to tip once; base of the storage gauge found to be full of water.
- 30/05/08: accidental tips of the TB rain gauge noted; these tips are to be ignored.
- 03/11/08: time stamp issue suspected due to discrepancy with the previous download; time adjusted to follow immediately after the last record from the prior download.
- 27/01/09: disparity between TB and storage gauge >13%; likely due to frozen conditions; ice present in one TB bucket and subsequently removed.
- 06/04/09: time stamp issue possibly resulting from GMT to BST change; this is accounted for in the analysed data file.

## Data quality implications
- Physical disturbances (wind, ice, water in storage gauge) introduce spurious or biased readings.
- Time stamp inconsistencies and timezone shifts (GMT/BST) complicate alignment of sequential data.
- Some TB tips are valid readings; others are artifacts needing exclusion or correction.

## Recommendations for analysts
- Flag or remove the accidental TB tips and any readings tied to identified disturbances.
- Ensure consistent time referencing; apply corrections for GMT/BST changes and align with prior downloads.
- Document environmental impacts (e.g., ice, water accumulation) and adjust analyses accordingly to avoid bias.
- Maintain and reference metadata for all adjustments and known anomalies to enable reproducibility.

## Notes / Next steps
- Analyzed data files reflect the noted timestamp corrections (03/11/08, 06/04/09) and anomaly handling.
- Ongoing monitoring recommended to detect and address similar issues in future data collection.