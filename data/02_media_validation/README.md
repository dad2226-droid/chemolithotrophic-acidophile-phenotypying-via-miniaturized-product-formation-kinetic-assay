# Media validation: source data and metadata

Shared materials, strain and recipe definitions are linked from [00_materials_and_strains](../00_materials_and_strains/README.md). See [reading shared YAML references](../00_materials_and_strains/README.md#reading-shared-yaml-references) for the `$ref` convention.

This collection contains endpoint absorbance measurements testing ratiometric pH and iron(III) indicators in acidophile media. It comprises twelve abiotic plates, 936 measured wells and 5,616 individual absorbance values. Each well was measured at six wavelengths. The same F2S plates support both indicator tests and are retained once.

Repository location: `data/02_media_validation/`. See the [dataset overview](../README.md) for the other experimental collections. This folder provides the underlying measurements and their annotations.

## Files and experimental groups

| Source exports | Media and source subfolder | Measurements | Measured region per plate |
|---|---|---|---|
| `Plate1-4-1-2026.xls`, `Plate2-4-1-2026.xls`, `Plate3-4-1-2026.xls` | [F2S](03_ratiometric_pH_and_iron_III_indicators/01_F2S_medium/) | Iron(III) additions and pH series with/without dye | Rows A–H, columns 1–9: 72 wells |
| `Plate4-4-1-2026.xls`, `Plate5-4-1-2026.xls`, `Plate6-4-1-2026.xls` | [AFM1 and AFM3](02_iron_III_indicator/01_AFM1_and_AFM3_media/) | Iron(III) additions without dye | Rows A–H, columns 1–6: 48 wells |
| `Plate7-4-1-2026.xls`, `Plate8-4-1-2026.xls`, `Plate9-4-1-2026.xls` | [AFM4 and AFM5](01_ratiometric_pH_indicator/01_AFM4_and_AFM5_media/) | pH series with/without dye | Rows A–H, columns 1–12: 96 wells |
| `Plate10-4-1-2026.xls`, `Plate11-4-1-2026.xls`, `Plate12-4-1-2026.xls` | [Starkey with brown or colloidal sulfur](01_ratiometric_pH_indicator/02_Starkey_with_brown_and_colloidal_sulfur_media/) | pH series with/without dye | Rows A–H, columns 1–12: 96 wells |

The supporting files are:

- [media_validation.yaml](media_validation.yaml): experimental design, preparation volumes, known medium recipes, complete well assignments, acquisition information, exact source filenames, checksums, and reference-measurement associations.
- [reference_measurements.csv](reference_measurements.csv): measured pH references and the measured iron concentration of the iron(III) stock. Its column definitions and measurement methods are included in the YAML.
- `README.md`: this guide.

## Reading the source exports

The `.xls` files contain UTF-16LE tab-delimited text, with a byte-order mark. They are not binary Excel workbooks. Import them as tab-delimited text using UTF-16 encoding when software does not recognize the contents automatically.

Every file contains one raw endpoint absorbance block. The wavelength order in the export is 380, 430, 485, 545, 428, 750 nm. Absorbance is reported in AU. Preserve the recorded numerical values and instrument tokens.

All internal `Plate:` headers say `Plate1`. Those repeated headers do not identify the physical plates. Use the exact source filename and the YAML's `physical_plate_id`; the export's `Original Filename` field also distinguishes the plates. The recorded endpoint times are dated 1 April 2026, and recorded reader temperatures range from 23.8 to 24.2 °C. The timestamp field is labelled `Date Last Saved` and indicates the measurement times; their time zone is unknown. Preserve the recorded clock values without assigning a time zone or converting them to UTC.

The [assigned plate reader](../00_materials_and_strains/chemicals_materials_equipment.md#materials-and-equipment) is identified through the YAML reader settings. Measurements followed 30 minutes at approximately 23 °C.

Only the measured regions listed above belong to this dataset. Columns outside those regions are unmeasured, not missing results or blank-control wells. All 5,616 observations within the measured regions are numeric, with no missing or overflow tokens detected in this collection.

## Well assignments and replication

Rows A–H correspond to eight dilution levels, in descending stock fraction: 1, 1/2, 1/4, 1/8, 1/16, 1/32, 1/64, 0. Each three-column block contains technical replicate wells at each row's level.

| Plates | Columns 1–3 | Columns 4–6 | Columns 7–9 | Columns 10–12 |
|---|---|---|---|---|
| 1–3 | F2S iron(III) series; no dye | F2S pH; dye | F2S pH; no dye | Unmeasured |
| 4–6 | AFM1 iron(III) series; no dye | AFM3 iron(III) series; no dye | Unmeasured | Unmeasured |
| 7–9 | AFM4 pH; no dye | AFM4 pH; dye | AFM5 pH; no dye | AFM5 pH; dye |
| 10–12 | Brown-sulfur Starkey pH; no dye | Brown-sulfur Starkey pH; dye | Colloidal-sulfur Starkey pH; no dye | Colloidal-sulfur Starkey pH; dye |

The four experimental families used the same calibration stocks, with three physical plate replicates per family and three technical wells per level on each plate. Physical plates are the replicate unit; the nine wells per condition do not represent nine independent stock preparations. The YAML links all four families to the same stock set. There are no organisms in these calibration wells.

The YAML's `groups` section encodes these assignments explicitly. Its `experiments` section assigns groups to physical plates, and `acquisitions` connects each physical plate to its export. The `matched_group_id` associates dye and no-dye groups within the same medium; comparisons should retain physical plate and dilution-level pairing.

## Preparation and concentration basis

Each well received 100 µL of 2× medium plus 100 µL of an acid or ferric standard. Dye-containing pH wells received an additional 10 µL of 200 µM thymol blue. Thus, undyed wells contain 200 µL, and dyed wells contain 210 µL. All ferric-series wells are undyed. Plates were non-UV-transparent and were measured without lids.

The nominal dye label is 10 µM. The shared medium formulations describe the standard 1× medium before the additional dye solution.

For the acid series, nominal 1 M sulfuric acid was serially diluted with water. Row H contains water in place of an acid standard. Acid contributed by this series is separate from acid already present in the medium.

For the iron(III) series, the stock contained 0.2094 M measured total iron and was diluted in 1 M sulfuric acid. The added iron is assigned as iron(III) from the reagent identity; ICP-OES measures total iron and does not itself determine oxidation state. Row H contains the acid solvent without iron(III) addition and is not an iron-free medium blank. Iron already present in a medium is specified by its recipe; a measured whole-mixture total-iron or speciation reference is not available.

## Media formulations

The complete recipes, preparation targets and parent-formulation references are in the shared [media formulation tables](../00_materials_and_strains/media_formulations.md). This collection uses `AFM1`, `AFM3`, `F2S`, `AFM4`, `AFM5`, `Starkey_brown` and `Starkey_colloidal`; its YAML `media` field references their context-specific stock and standard-medium definitions.

All calibration media were dispensed as 2× stocks. The listed 1× recipes describe medium before the extra dye solution. Stock-preparation quantities remain available through the shared definitions. The two Starkey sulfur conditions use distinct preparation identities; the colloidal condition is also labelled “Yellow Starkey.” Sulfur-containing stocks were aggressively vortexed before dispensing. Experimental acid/ferric additions and their reference measurements remain defined in this folder.

## Using the reference table

`reference_measurements.csv` is UTF-8 comma-separated text with one header row and 49 reference records:

- Eight final-mixture pH values associated with F2S.
- Eight final-mixture pH values for AFM4 and eight separately measured values for AFM5.
- Eight final-mixture pH values for brown-sulfur Starkey and eight separately measured values for colloidal-sulfur Starkey.
- Eight measured pH values for the acid/DI-water solutions before medium mixing.
- One measured total-iron concentration for the ferric stock.

The reference values retain the numerical precision provided in the CSV. The presence or absence of trailing zeros does not establish measurement precision. The CSV contains measured reference values; medium recipes and stock-preparation details are recorded in the YAML.

The CSV column names are case-sensitive: `reference_ID`, `reference_set_ID`, `level_ID`, `plate_row`, `quantity`, `value`, `unit`, `measurement_basis`, and `method_ID`. Use `reference_ID` as the unique lookup key; `reference_set_ID` identifies the reference series, and `method_ID` selects its method definition in the YAML. A reference set lists eight identifiers in the same order as plate rows A–H. pH was measured separately for each medium before dye addition. Identical values in the AFM4/AFM5 and two Starkey series represent separate measurements and therefore have distinct identifiers. Within a medium, its reference pH values are associated with both dye conditions and the three replicate plates; this reuse does not create additional reference measurements or establish pH after dye addition. Stock-solution pH and final-mixture pH are distinct reference measurements.

`NA` in `level_ID` and `plate_row` for the ferric-stock record means those fields are inapplicable because the reference describes the starting stock. Its measured Fe concentration is present. The CSV contains no empty fields. Preserve `NA` and YAML `null` values as specified; never convert them to numeric zero.

The pH-meter and ICP-OES method definitions are referenced through the YAML from the shared folder. For the Fe-stock reference, a 1 mL sample was centrifuged at 3,000 × g for 10 seconds; 750 µL of supernatant was transferred to a new tube and centrifuged at 17,000 × g for 1 minute. The clarified supernatant was diluted for ICP-OES analysis. The reported elemental concentration describes the starting ferric stock.

## Preservation and reuse

Preserve source exports exactly as recorded. Do not automatically remove edge wells; they contain assigned conditions and technical replicates.

File sizes and SHA-256 checksums are included with the acquisition entries. The source exports are organized in the subfolders linked in the table above; the reference CSV and YAML are stored alongside this README. Match each exact `source_filename` to its acquisition entry and use the recorded physical-plate, well and reference identifiers to interpret the measurements. The YAML uses the `media_validation` metadata format, version 1.

## Contributors

CRediT roles for this experimental collection are listed below. Names, affiliations and ORCIDs are provided in the [dataset contributor section](../README.md#contributors).

| CRediT role<sup>1</sup> | Contributors |
|---|---|
| Conceptualization | DAD, MAH |
| Methodology | DAD, MAH |
| Investigation | MAH, DAD |
| Validation | DAD, MAH, WW |
| Data curation | DAD, WW |
| Software | WW, DAD |
| Resources | SB |
| Supervision | SB |
| Project administration | SB |
| Funding acquisition | SB |

DAD conceived the thymol blue pH indicator approach, and MAH conceived the Fe(III) absorbance indicator approach evaluated in these media.

DAD and MAH designed the indicator-validation experiments in AFM1, AFM3, F2S, AFM4, AFM5 and the two Starkey sulfur media. MAH and DAD prepared the media-validation experiments and reference solutions, and MAH collected the plate-reader measurements. MAH and DAD measured reference pH and Fe(II), and DAD performed total-Fe reference measurements by ICP-OES.

DAD, MAH and WW contributed to validation of the indicator approaches using the medium-validation measurements.

DAD and WW curated the data and experimental metadata, and WW and DAD developed the supporting software. SB provided resources and supervision, administered the project and acquired funding.

## References

1. Elsevier. [CRediT Author Statement](https://www.elsevier.com/researcher/author/policies-and-guidelines/credit-author-statement) (accessed 2026-09-12).
