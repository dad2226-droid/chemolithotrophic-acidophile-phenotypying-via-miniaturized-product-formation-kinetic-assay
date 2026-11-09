# Indicator calibration source data

Shared materials, strain and recipe definitions are linked from [00_materials_and_strains](../00_materials_and_strains/README.md). See [reading shared YAML references](../00_materials_and_strains/README.md#reading-shared-yaml-references) for the `$ref` convention.

This section contains abiotic absorbance measurements used to evaluate the thymol-blue pH indicator and the iron(III) absorbance indicator. It includes calibration concentration series, spectra, repeated storage measurements, plate-material and temperature comparisons, gas-exchange membrane measurements, and paired readings with and without a lid. Iron(II) preparations provide specificity controls.

Repository location: `data/01_indicator_calibration/`. See the [dataset overview](../README.md) for the other experimental collections. This folder provides the underlying measurements and their annotations.

## Contents

| Subfolder | Experimental documentation | Source data |
|---|---|---|
| [01_ratiometric_pH_indicator](01_ratiometric_pH_indicator/) | [ratiometric_pH_indicator.yaml](01_ratiometric_pH_indicator/ratiometric_pH_indicator.yaml) | 96 reader exports covering initial calibrations, spectra, plate configurations and pH storage measurements. |
| [02_iron_III_indicator](02_iron_III_indicator/) | [iron_III_indicator.yaml](02_iron_III_indicator/iron_III_indicator.yaml) | 201 reader exports covering iron concentration series in different acid backgrounds, spectra, plate configurations, the final iron(III) storage series and initial iron(II) measurements. |
| [03_lid_comparison](03_lid_comparison/) | [lid_comparison.yaml](03_lid_comparison/lid_comparison.yaml) | [acid-iron.xlsx](03_lid_comparison/acid-iron.xlsx), containing 12 measured sheets: paired lid and no-lid readings of three pH plates and three iron(III) plates. |

The shared [reference_measurements.csv](reference_measurements.csv) contains the measured total-Fe and Fe(II) reference values for the final iron(III) and iron(II) preparations. Reference pH values and the configuration-series Fe concentrations are included directly in the corresponding YAML files. The YAML files contain the preparation details, reference methods, well assignments and acquisition associations needed to interpret these data.

There are 298 optical source files: 297 reader exports and one workbook. The YAML files describe 309 acquisitions because each of the workbook's 12 measured sheets is a separate acquisition.

## Reading the files

The `.xls` files are UTF-16LE tab-delimited reader exports, despite their spreadsheet extension. They contain instrument headers and wavelength-specific measurement blocks. `acid-iron.xlsx` is an Excel workbook; preserve its sheet names, instrument settings, channel times and well coordinates.

The pH/iron and paired-lid reader assignments are documented in the shared [materials and equipment table](../00_materials_and_strains/chemicals_materials_equipment.md#materials-and-equipment) and referenced by the YAML `readouts`. The lid-comparison workbook’s literal instrument header remains distinct from its experimenter-confirmed model.

Endpoint acquisitions measure absorbance at 380, 428, 430, 485, 545 and 750 nm. Wavelength order can vary, so identify channels by their recorded wavelength. Spectra generally span 200–750 nm in 10 nm steps; the relevant pH scans ending at 700 nm are identified individually in the metadata. The spectral grid does not directly measure 485 or 545 nm. Any interpolation, absorbance correction or ratio calculation produces a derived quantity.

Open a YAML file in a text editor to read its labelled sections. `experiments` describes preparation and replication; `reference_sets` provides calibration values and well assignments; `physical_plates` identifies the prepared plates; and `acquisitions` associates each export or workbook sheet with an experiment, physical plate, reference set and readout. Identifiers connect these sections. Match each exact `source_filename`, including capitalization, within its corresponding subfolder; workbook acquisitions also specify `source_sheet`.

The plate uses rows A–H and columns 1–12. A `values_by_column` list follows its accompanying `plate_columns` list in order. In the initial pH calibrations, rows A–D and E–H are different pH ranges and both contain dye. In the pH standard spectra and storage series, the final iron calibrations, and the iron configuration experiments, rows A–D are undyed and rows E–H contain dye. Each four-row group supplies four technical wells per concentration. Use the explicit reference set for every acquisition.

## Physical plates, replication and time

Several files describe repeated readings of the same physical plate. Match readings using `physical_plate_id`, well and wavelength. A repeated filename number, a new temperature or a new sheet does not establish an independent preparation.

The configuration experiments used three independently prepared standard series, prepared on separate days. Corresponding UV-transparent and non-UV-transparent plates used the same standards within a preparation run. The 20 µM and 200 µM pH dye-stock experiments used separate physical plates. The initial pH calibrations used three independently prepared 24-standard series and three UV-transparent plates for each dye-stock concentration. The `acid-final` endpoint and spectral exports come from three non-UV-transparent plates containing three independently prepared 12-standard series, with one plate per preparation and four technical wells per condition per plate. The spectra and repeated endpoint readings share these physical plates. The final iron calibration series used one preparation per series distributed among three technical plates. These replication structures are recorded separately in the YAML files.

For the configuration sequence, the same plates were read after 30 minutes at 23 °C, 2 hours at 4 °C, 2 hours at 30 °C, 2 hours at 75 °C, and overnight at 23 °C with the [documented sealing film](../00_materials_and_strains/chemicals_materials_equipment.md#materials-and-equipment) applied before that incubation. The [documented gas-exchange membranes](../00_materials_and_strains/chemicals_materials_equipment.md#materials-and-equipment) were then attached for an additional reading. These are prescribed incubation conditions; recorded reader temperatures and timestamps are separate fields.

The pH temperature and plate-type comparison used three UV-transparent and three non-UV-transparent plates, with four technical wells per condition per plate. Its initial UV-transparent measurements are shared with the nominal 10 µM initial pH calibration. The same six plates were used for the membrane comparison after overnight incubation at 23 °C with lids and Parafilm. Paired measurements were acquired immediately before and after membrane attachment.

The pH lid comparison used three independently prepared 12-standard series distributed among three separate UV-transparent plates, with four technical wells per condition per plate. Each plate was measured without and with a non-UV-transparent low-evaporation lid on the same day. The pH storage experiment used three independently prepared 12-standard series distributed among three separate non-UV-transparent plates, with four technical wells per condition per plate. These plates were stored on the benchtop for approximately 15 days with low-evaporation lids, which were removed for measurements. The pH lid-comparison and storage experiments used the same 12 nominal sulfuric-acid levels.

The final iron(III) endpoint series and its corresponding spectra share physical plates. The iron(III) lid comparison used three separate UV-transparent plates. Each plate was measured without and with a lid; these plates were distinct from those used for the final iron(III) calibration and storage series. The lid experiment retains one recorded standard preparation and uses the same recorded reference concentrations; its stock-preparation relationship to the final series is not independently documented. During the final iron(III) storage series, plates were stored at approximately 23 °C with low-evaporation lids obtained from sacrificial donor non-UV-transparent plates. Those lids were removed for measurements. Measurement lids were present only in `acid-iron.xlsx` sheets ending in `-lid`; `-nolid` sheets and the other indicator-calibration acquisitions were measured without lids.

The final iron(II) controls include initial endpoint readings only. The 1 M sulfuric-acid series also includes spectra; the 0.001 M series has no spectra in this deposit. Neither iron(II) series includes repeated measurements over time.

Final-series filename suffixes are sequential reading indices, not elapsed days. Use the documented timestamps and time origin to calculate elapsed time. Timestamp interpretations are specified for each experiment; a field labelled “Date Last Saved” is not automatically an acquisition-start time. The instrument clock time zones are unknown. Retain the literal timestamps without assigning a time zone or converting them to UTC.

## Reference measurements and concentration basis

Undyed wells contained 200 µL of standard. Dyed wells contained that standard plus 10 µL of dye solution, giving 210 µL. The usual 200 µM dye stock produces a calculated final concentration of approximately 9.52 µM; the 20 µM stock produces approximately 0.952 µM. The YAML files distinguish these calculated values from the nominal 10 and 1 µM labels.

Iron reference concentrations and stated sulfuric-acid concentrations describe the 200 µL standard. Iron values are expressed on an elemental-iron basis, not as moles of the preparation salt. Iron calibration values represent measured total iron unless explicitly identified as iron(II) titration measurements. Configuration-series iron arrays are in M and retain the reported values at three significant figures. Reference solutions were prepared by serial dilution. The reported concentrations reflect measurements of each sample after serial dilution. These reference-solution measurements are shared by the associated optical wells; they are not separate chemical assays of every well. For the final reference series, the CSV contains one reported total-Fe value and three separate Fe(II) titration values per reference sample.

`reference_measurements.csv` is UTF-8 comma-separated text with a byte-order mark and one header row. Read it with a BOM-aware UTF-8 decoder so that its first column is recognized as `measurement_ID`. It has 144 reported concentration rows for 36 reference samples: 36 total-iron values and 108 iron(II) values. Its three `series_ID` values are `ferric`, `ferrous_1M` and `ferrous_0.001M`. Select measurements using `series_ID`, `plate_column` and `analyte`; `measurement_ID` identifies an individual row. `reference_replicate` identifies iron(II) reference replicates and does not pair them with optical plates. `NA` in this column means not applicable for the single total-iron value, not that the total-iron measurement is missing.

`measured_concentration_M` is the concentration before dye addition, with analytical sample dilutions already accounted for. For undyed wells, use this concentration unchanged. For dyed wells, a final-well concentration is calculated by multiplying by 200/210. The CSV's `optical_final_volume_uL` value of 210 applies to dyed wells only. This conversion has not already been applied to the reference values. Total iron minus iron(II), if calculated, is a derived estimate of iron(III); the original measurements remain separate. This difference can be negative, and the reported values are retained without clipping.

Final pH reference values were measured after dye addition. Their association with undyed wells does not imply an independent pH measurement of those wells, and pH was not remeasured at every storage acquisition. Use the recorded pH directly; the concentration dilution factor is not a pH correction.

The pH reference for the iron configuration series in 0.001 M sulfuric acid, preparation run 1, column 4, is unavailable and is recorded as `null` in `iron_III_indicator.yaml`. The corresponding optical measurements remain included.

## Preservation and interpretation

Keep source numerical precision, instrument flags, original filenames and workbook structure intact. Preserve explicit overflow or error tokens separately from numeric values. Numerical values above an analysis threshold remain numerical measurements in the source. A YAML `null` represents an unknown, unavailable or inapplicable value as explained in its field; it never represents zero.

The reference CSV retains its supplied precision. Decimal places retained during calculations do not establish additional measurement precision. Significant-figure formatting belongs in reported results and must not alter source measurements. Use the reference concentrations as listed in the YAML arrays.

The YAML files document source filenames, header labels and acquisition associations. Match sources through those explicit acquisition entries, retain a single copy of each selected source, and keep calculated signals, fitted models and manuscript outputs separate from this source collection.

## Contributors

CRediT roles for this experimental collection are listed below. Names, affiliations and ORCIDs are provided in the [dataset contributor section](../README.md#contributors).

| CRediT role<sup>1</sup> | Contributors |
|---|---|
| Conceptualization | DAD, MAH |
| Methodology | DAD, MAH |
| Investigation | MAH, SVRA, NRL, DAD |
| Validation | DAD, MAH, WW |
| Data curation | DAD, WW |
| Software | WW, DAD |
| Resources | SB |
| Supervision | SB |
| Project administration | SB |
| Funding acquisition | SB |

DAD conceived the thymol blue pH indicator approach evaluated in these calibrations, and MAH conceived the Fe(III) absorbance indicator approach.

DAD designed the pH calibrations, iron configuration tests, ferrous specificity controls and lid comparison; MAH designed the final ferric-indicator calibration, spectra and storage series. MAH and DAD prepared the experiments and reference solutions, and MAH collected optical measurements across the calibration sets.

MAH, SVRA, NRL and DAD measured the final ferric series; MAH, SVRA and NRL measured the ferrous specificity controls, and MAH and NRL performed the lid comparison. MAH and DAD measured reference pH and Fe(II), and DAD performed total-Fe measurements by ICP-OES.

DAD, MAH and WW contributed to validation of the indicator approaches using the calibration measurements.

DAD and WW curated the data and experimental metadata, and WW and DAD developed the supporting software. SB provided resources and supervision, administered the project and acquired funding.

## References

1. Elsevier. [CRediT Author Statement](https://www.elsevier.com/researcher/author/policies-and-guidelines/credit-author-statement) (accessed 2026-09-12).
