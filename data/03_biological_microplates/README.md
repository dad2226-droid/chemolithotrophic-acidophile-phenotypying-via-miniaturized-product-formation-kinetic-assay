# Biological microplate experiments

Shared materials, strain and recipe definitions are linked from [00_materials_and_strains](../00_materials_and_strains/README.md). See [reading shared YAML references](../00_materials_and_strains/README.md#reading-shared-yaml-references) for the `$ref` convention.

This collection contains plate-reader absorbance measurements and experimental metadata for AF, AT and LF, as identified in the [shared strain table](../00_materials_and_strains/strains.md). It covers iron- and sulfur-based culture experiments, including additive concentration series, copper treatments, and matched abiotic controls. The organism-specific experiment records define the included conditions.

This section is stored under `data/03_biological_microplates/`. Reader exports are organized in the species and condition subfolders below.

## Files and reading order

Read [biological_definitions.yaml](biological_definitions.yaml) first. It references the shared organism identities and medium formulations and records preparation methods, units, well layout, incubation conditions and measurement definitions. Then read the experiment YAML in the relevant species directory:

| Species directory | Experiment metadata |
|---|---|
| `01_Acidithiobacillus_ferrooxidans_ATCC_23270` | [AF_experiments.yaml](01_Acidithiobacillus_ferrooxidans_ATCC_23270/AF_experiments.yaml) |
| `02_Acidithiobacillus_thiooxidans_ATCC_19377` | [AT_experiments.yaml](02_Acidithiobacillus_thiooxidans_ATCC_19377/AT_experiments.yaml) |
| `03_Leptospirillum_ferriphilum_DSM_14647` | [LF_experiments.yaml](03_Leptospirillum_ferriphilum_DSM_14647/LF_experiments.yaml) |

The YAML files are plain-text documents. Named fields describe their values, indentation groups related information, and lists contain repeated records. Each species document's `definitions_id` connects it to `biological_definitions.yaml`. Media, preparation and readout identifiers select the corresponding shared definitions.

Each treatment compound's `reagent_id` selects its entry in the shared [chemical reagent table](../00_materials_and_strains/chemicals_materials_equipment.md) and [chemical_reagents.yaml](../00_materials_and_strains/chemical_reagents.yaml). The table adds reported hydrate forms and supplier/bottle information to the treatment names. Nominal-versus-measured concentration assignments are documented in the shared definitions; N in the inventory marks nominal additive stocks. Identifiers containing `citrate` denote citric acid. Experiment/group identifiers containing `sodium_selenate` denote the sodium selenite experiment; its component and reagent keys use `sodium_selenite`. Experiment/group identifiers containing `potassium_gluconate` denote D-gluconic acid sodium salt (sodium gluconate); their component and reagent keys use `sodium_gluconate`.

## Reading the source exports

The `.xls` files contain UTF-16LE tab-delimited text with a byte-order mark. Import them as text using UTF-16 encoding and a tab delimiter; their `.xls` extension does not indicate a binary Excel workbook. In a spreadsheet program, use its text-import option and select these settings if the format is not recognized automatically.

Keep the instrument headers and each measurement block separate. Read the wavelength labels recorded in each export: some files contain only 380 and 750 nm channels, while others contain additional channels. Preserve empty unmeasured positions, instrument flags, numerical precision and original filenames. A numerical zero remains a measurement.

Match each export to the `acquisition_series` label and ordinal under its physical plate in the species YAML. The naming conventions include both underscores and hyphens:

| Acquisition-series label | Acquisition ordinal | Source filename |
|---|---:|---|
| `HT1_1` | 0 | `HT1_1_0.xls` |
| `HT2-67-A` | 0 | `HT2-67-A-0.xls` |
| `L2-3` | 0 | `L2-3-0.xls` |

Use the metadata's physical plate identity and well assignments when combining files. Retain the `Date Last Saved` timestamp as recorded, with no assumed timezone. Acquisition ordinals identify readings and do not represent elapsed days.

## Experiments, plates and measurements

An `experiment_id` identifies a comparison. Its `plate_groups` list the physical `plate_ids` and the `column_conditions` for those plates. Each column condition specifies the added compound or compounds and their concentrations; `fixed_components`, when present, apply throughout the experiment in addition to the medium formulation.

The `plates` section identifies each physical plate, its `batch_id`, and its `acquisition_series`. Within an acquisition series, the key is a measurement label and the numeric list contains acquisition ordinals. Together, the label and ordinal connect a reader export to the physical plate. Several acquisition series can belong to the same physical plate, and repeated measurements retain the same well identities.

The earliest recorded reading of each physical plate is time zero. Elapsed time is calculated from recorded timestamps, rather than treating ordinal numbers as equally spaced times. The timestamp field and its interpretation are specified in `biological_definitions.yaml`; no time-zone offset is assigned. Recorded wavelength labels identify the measurements, and reader temperatures remain distinct from incubation temperatures.

## Well assignments and replication

For each assigned column, rows E, F and G contain biotic wells and rows B, C and D contain condition-matched abiotic wells. E, F and G correspond to three independent starter cultures. The same row within the same species and preparation batch uses the same starter culture across conditions and plates. Abiotic wells match the plate and column condition; individual abiotic rows are not independently paired with individual biotic rows.

A physical plate can support several experiments through different column assignments. A shared control well remains one physical well wherever it is referenced. `blank_condition_columns` identify columns without an assigned experimental condition; zero-dose controls are explicitly represented by numerical zero in `column_conditions`. Peripheral water-filled wells are defined separately in the shared layout.

## Concentrations and preparation volumes

Additive concentrations and initial OD600 values use the 200 µL preparation basis. Each plate group states its concentration unit. The shared definitions distinguish nominal concentrations from concentrations determined using elemental measurements and specify the chemical basis, including any explicit component-level exception. Added iron is additional to the iron already present in the medium.

Iron experiments contain no indicator dye and retain a 200 µL well volume. Standard pH preparations add 10 µL of dye stock, giving 210 µL; threefold-dye preparations add 30 µL, giving 230 µL. The shared preparation definitions give the volume factors for calculating final-well concentrations and OD600 while preserving the reported 200 µL values. Medium formulations, additive-stock pH, and experiment-specific pH values are separate quantities defined in the YAML files.

AFM1 additive stocks, including sodium gluconate, use pH 1.80 unless the experiment specifies an exception. This is stock pH, not the finished-well pH.

The reported gluconate values describe the supplied sodium gluconate reagent on a compound molar basis and have a measured-elemental classification, including the 0.438 M maximum stock concentration. No sodium/potassium mass conversion is applied.

Potassium fluoride, potassium thiocyanate, potassium dichromate, sodium chromate and sodium selenite were not measured for safety reasons and have nominal concentrations. Titanyl sulfate and zirconium(IV) sulfate stocks were measured by ICP-OES in 2% (w/v) HCl; their concentrations retain the compound basis and original numerical values. Sodium thiosulfate and potassium tetrathionate were always nominal, including additive screens and sulfur-substrate experiments. These experimenter-confirmed assignments override the general sodium/potassium measurement convention. Together with ammonium sulfate, citric acid, sucrose and sulfuric acid, these constitute 11 nominal additive reagents; see `concentration_conventions.nominal_reagents` in the shared definitions.

The shared [ICP-OES method and wavelengths](../00_materials_and_strains/experimental_definitions.yaml) specify the analytical matrix and processing order: subtract the corresponding 0 ppm blank, apply the analytical dilution factor, then convert to elemental molarity and, where applicable, compound molarity. A 1 ppm reference exists for each element; its use as a normalization denominator is not established. Deposited concentrations already include the documented corrections. The reported stock-only and stock–AFM1 solubility screen is in `stock_preparation.solubility_screen`; stock-specific day-0/day-7 measurements and pass outcomes have not been deposited.

All nominal stock concentrations, including citric acid and sucrose, were calculated from the mass added and final prepared volume in the [documented stock-preparation vessel](../00_materials_and_strains/chemicals_materials_equipment.md#materials-and-equipment), followed by the stated mixing and dilution volumes.

The reported initial pH summary for the identified SM4 experiments is 3.95 ± 0.03 (mean ± SD, three measurements). Exact pH was not recorded for each condition; the summary is not a collection of condition-specific measurements. The normalized inoculum suspension OD600 of 5.0 ± 0.1 also denotes mean ± SD from three measurements.

## Media formulations

The shared [media formulation tables](../00_materials_and_strains/media_formulations.md) provide the complete recipes and parent-formulation references. This collection uses `AFM1`, `AFM1_BS`, `AFM4`, `SM4_BS_microplate` and `HH`. The local `SM4_BS` identifier selects `SM4_BS_microplate`; the test-tube formulation is a separate entry.

Recipe amounts describe nominal 1× medium on the 200 µL preparation basis before dye addition. Medium is dispensed at 2× strength for equal-volume mixing. Substrate and treatment additions remain in the species experiment YAMLs. The `media` field in `biological_definitions.yaml` references the corresponding shared definitions while retaining these local IDs.

Preparation targets remain distinct from measured initial-mixture pH. Use the experiment metadata for measured values and their stated scope, including the SM4 summary described above.

## Unavailable acquisitions

The following acquisition ordinals have no available export:

| Physical plate / acquisition series | Unavailable ordinals |
|---|---|
| HT3-40-B | 9 |
| HT3-7-B | 9 |
| HT4-25-A | 11 |
| L2-3 | 7, 11 |

These gaps may have resulted from accidental file overwriting and were not intentional data exclusions. The exact cause is not established. Available exports retain their recorded identifiers and timestamps. The acquisition lists enumerate available files; they do not fill gaps with substitute measurements.

## Contributors

CRediT roles for this experimental collection are listed below. Names, affiliations and ORCIDs are provided in the [dataset contributor section](../README.md#contributors).

| CRediT role<sup>1</sup> | Contributors |
|---|---|
| Conceptualization | DAD, MAH |
| Methodology | DAD, LNM, STB |
| Investigation | DAD, MAH, NRL, LNM |
| Validation | DAD, MAH, WW |
| Data curation | DAD, WW |
| Software | WW, DAD |
| Resources | SB |
| Supervision | SB |
| Project administration | SB |
| Funding acquisition | SB |

DAD conceived the thymol blue pH indicator approach, and MAH conceived the Fe(III) absorbance indicator approach applied in the biological microplate experiments.

DAD designed the AFM1, AFM4 and LF experiments; DAD, LNM and STB designed the AF/AT soluble-sulfur series in SM4 basal salts.

DAD and NRL prepared and measured the AFM1 additive screen, with MAH contributing to a subset of those series. LNM and DAD prepared and measured the AFM4 series, the basal-AFM1 potassium tetrathionate series and the AF/AT soluble-sulfur experiments in SM4 basal salts. DAD and MAH prepared the LF experiments, and MAH and LNM collected their microplate measurements. DAD and NRL prepared the biological additive stocks and inocula; DAD performed the stock elemental measurements and initial inoculum pH and OD600 measurements.

DAD, MAH and WW contributed to validation of the indicator approaches using the biological microplate data.

DAD and WW curated the data and experimental metadata, and WW and DAD developed the supporting software. SB provided resources and supervision, administered the project and acquired funding.

## References

1. Elsevier. [CRediT Author Statement](https://www.elsevier.com/researcher/author/policies-and-guidelines/credit-author-statement) (accessed 2026-09-12).
