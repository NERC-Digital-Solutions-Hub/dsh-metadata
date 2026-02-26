# Hirrhos Uchaf tipping bucket and  storage rain gauge

## Data summary
- Site equipment: tipping bucket rain gauge and storage rain gauge.
- Installation dates: tipping bucket installed 07/11/06; storage gauge installed 09:30 GMT 08/11/06.
- Data quality notes:
  - Feb/07: Data considered dodgy due to significant snow; wind-blown snow likely not recorded properly by gauge.
  - 03/11/08: Time stamp issue suspected; overlap with previous download; time adjusted to follow immediately after last record from prior download.
  - 06/04/09: Time stamp issue possibly from GMT to BST change; accounted for in the analysed data file.
  - May/09: Data only available for 26–27 May; reason unknown.

## Data quality issues and corrections
- Snow events affecting recording accuracy (Feb/07).
- Time stamp inconsistencies and overlaps (03/11/08; 06/04/09, DST adjustment).
- Partial data gaps (May/09) with unclear cause.
- Corrections implemented or noted in analysed data files; need for clear audit trail and flags.

## Data management and sharing considerations
- Importance of documenting issues in dataset metadata (installation details, gauge types, data gaps, and corrections).
- Maintain provenance and versioning for corrected timestamps and interrupted periods.
- Use data quality flags for:
  - Snow-related data doubt
  - Timestamp adjustments
  - DST-related adjustments
  - Data gaps/unknown causes
- Provide clear data dictionary: units, time zone, sampling frequency, and coverage.
- Ensure updates and re-sharing follow governance processes to keep datasets discoverable and usable.

## Recommendations for ongoing stewardship
- Keep a centralized issue log with dates, nature of issue, actions taken, and status.
- Require metadata updates for any future corrections or data additions.
- Implement automated validation checks for timestamp continuity and DST transitions.
- Communicate limitations to data users and offer versioned datasets with explicit provenance and quality notes.