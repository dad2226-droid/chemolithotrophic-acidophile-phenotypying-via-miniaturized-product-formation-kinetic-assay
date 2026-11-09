# Test-tube validation experiments

Shared materials, strain and recipe definitions are linked from [00_materials_and_strains](../00_materials_and_strains/README.md). See [reading shared YAML references](../00_materials_and_strains/README.md#reading-shared-yaml-references) for the `$ref` convention.

Preparation reagent identities are linked through `preparation_reagent_id` to the shared [chemical reagent table](../00_materials_and_strains/chemicals_materials_equipment.md) and [chemical_reagents.yaml](../00_materials_and_strains/chemical_reagents.yaml). The table records supplied bottle information; bottle lots have not been assigned to every experimental batch.

This folder contains 96 tubes in 32 triplicate conditions, spanning five acidophile species and abiotic controls. Experiments began on 4 August 2026. HH iron cultures were followed through 11 August; elemental-sulfur and tetrathionate cultures were followed through 25 August.

This section is stored under `data/05_test_tube_validation/`.

## Files

| File | Contents |
|---|---|
| [test_tube_measurements.csv](test_tube_measurements.csv) | Individual tube measurements and sampling times, shared initial-reference assignments, and endpoint planktonic fluorescence. |
| [test_tube_validation.yaml](test_tube_validation.yaml) | Organism and culture identities, condition assignments, medium recipes, methods, data dictionary and the qualitative LF starter follow-up observation. |
| `README.md` | Guide to using these files. |

Keep this experimental folder together with `00_materials_and_strains`. The CSV and YAML, including the referenced shared definitions, describe this section. The CSV has one header row and 21 columns; the YAML's `columns` section defines those exact column names in the same order.

## Experimental design

| Timing block | timing_block_ID | Tube IDs | Conditions | Tubes | Sampling events after the start |
|---|---|---|---:|---:|---:|
| HH iron medium | `HH` | GT-S2-1–36 | 12 | 36 | 9 |
| SM4 with brown elemental sulfur | `brown_sulfur` | GT-S2-37–66 | 10 | 30 | 9 |
| SM4 with potassium tetrathionate | `tetrathionate` | GT-S2-67–96 | 10 | 30 | 16 |

The strain codes AF, AT, LF, AFur and AC are defined in the [shared strain table](../00_materials_and_strains/strains.md). `Ab` denotes an abiotic control. The YAML assigns every physical tube to its organism, medium, treatment and incubation temperature.

Cultures contained 6 mL prepared medium in the [documented capped culture tubes](../00_materials_and_strains/chemicals_materials_equipment.md#materials-and-equipment), with 20 µL washed, normalized inoculum added at an initial target OD600 of 0.003. Abiotic tubes received matching cell-free basal salts. Tubes were shaken at 150 rpm at their specified 30 or 37 °C. Evaporation was compensated with sterile ultrapure Milli-Q water before measuring pH or ORP directly in the tubes.

Three independent starter cultures were used per organism, and the same starters were shared across treatments. `inoculum_culture_ID` preserves these relationships; it does not require a paired treatment analysis. Repeated sampling rows represent the same physical tubes. The fresh test-tube starters are distinct from the unknown-age LF microplate starters.

## Media formulations

The shared [media formulation tables](../00_materials_and_strains/media_formulations.md) provide complete recipes, preparation targets and parent-formulation references for `HH`, `SM4_BS_tube`, `SM4_S0` and `SM4_tetrathionate`. The local `SM4_BS` identifier selects `SM4_BS_tube`; the microplate basal formulation is a separate entry. The YAML `media` field references these tube-context definitions.

Recipe concentrations apply to the 6 mL prepared medium before inoculum addition. The substrate media inherit the tube basal-salt recipe. The 2× medium and treatment solutions were mixed in equal volumes; the treatment solution was prepared at pH 1.8. A 200 mM Ga stock gives 100 mM in the prepared mixture; a 20 mM In stock gives 10 mM. These treatment additions are separate from the recipes. Recorded initial mixed-medium pH values remain distinct from stock-preparation targets.

## Reading the CSV

The unique record key is `tube_ID` plus `sampling_event`. Use `condition_ID` to find each condition in the YAML. The `medium_ID`, `treatment_ID` and `timing_block_ID` values identify the corresponding definitions there. Column names are case-sensitive. `NA` means no available or applicable value and must not be treated as zero; no CSV fields are empty.

There are 1,074 time-course rows and 96 shared initial-reference rows, giving 1,170 rows in total. The measured time course includes 749 numerical pH readings and 323 numerical ORP readings. These counts exclude the assigned initial-reference values.

`record_role` distinguishes three types of row:

- `shared_initial_reference`: event 0, with reference values assumed to apply across comparable conditions. No independent initial sample was taken from each tube. Repeated `initial_reference_ID` values identify the same assignment.
- `measurement`: an intermediate tube-reading event.
- `endpoint`: the final time-course event for that tube's block, with its endpoint fluorescence value or missing-value status.

The 96 event-0 rows reuse 21 reference assignments. Do not count these repeated baseline values as 96 independent measurements. The YAML lists every shared reference and its assignment rule; its `initial_reference_ID` values match the CSV.

Use `time_average_d` as the common sample time for each `timing_block_ID` and `sampling_event`. `time_sd_d` is the sample SD across all tube times in that block/event, using n − 1. It describes the spread of sampling times, not biological variability. The three blocks have separate schedules; the same sampling-event number does not imply the same date between blocks.

Individual `tube_datetime` values allow these summaries to be reconstructed. They use ISO 8601 dates and clock times, without a timezone offset. `datetime_basis` identifies a recorded, interpolated or assigned-start time. For HH sampling event 6, times for GT-S2-2–35 are linearly interpolated between GT-S2-1 at 06:23:10 and GT-S2-36 at 07:34:15 on 8 August 2026. That block/event summary includes two recorded times and 34 interpolated times; this procedure and the counts are specified in the YAML. Its SD partly reflects the interpolation assumption. Other poststart times are recorded. Event 0 is assigned time zero, with `time_average_d` and `time_sd_d` both zero.

The two absent readings within the intended time-course measurement channels are ORP for GT-S2-36 at event 4 and pH for GT-S2-72 at event 10; both are `NA`.

## Endpoint fluorescence

`planktonic_background_corrected_rfu` contains 96 reported endpoint SYBR Green measurements: 36 for HH iron cultures, 30 for brown elemental-sulfur cultures and 30 for tetrathionate cultures. These rows have `fluorescence_status=reported`.

All endpoint rows have a numerical fluorescence measurement. Negative readings, including −0.2 RFU for GT-S2-58, are retained. All non-endpoint rows have RFU `NA` and `fluorescence_status=not_scheduled`.

SYBR Green I dsDNA fluorescence was measured as previously described.<sup>1</sup> The reported RFUs already have the TE Buffer blank subtracted. Do not subtract the blank again or apply an OD600 baseline.

## LF starter follow-up

The YAML contains the recorded qualitative follow-up of the original LF microplate starters. Three replicate HH tubes were incubated at 37 °C and 150 rpm for 14 days, beginning on the day the LF microplate experiments ended. They did not become more red than abiotic controls. This record is separate from the freshly thawed starter cultures used for the numbered test-tube series.

## Contributors

CRediT roles for this experimental collection are listed below. Names, affiliations and ORCIDs are provided in the [dataset contributor section](../README.md#contributors).

| CRediT role<sup>2</sup> | Contributors |
|---|---|
| Methodology | DAD |
| Investigation | DAD, STB, SVRA, LNM |
| Validation | DAD, MAH, WW |
| Data curation | DAD, WW |
| Software | WW, DAD |
| Resources | SB |
| Supervision | SB |
| Project administration | SB |
| Funding acquisition | SB |

DAD designed the test-tube validation experiments and designed, prepared and recorded the 14-day qualitative follow-up of the original LF microplate starters. DAD, STB and SVRA prepared the iron, elemental-sulfur and potassium tetrathionate experiments and their abiotic controls.

STB, SVRA and DAD measured the iron-medium experiments; STB, DAD and LNM measured the elemental-sulfur experiments; and LNM, STB and DAD measured the potassium tetrathionate experiments. STB, SVRA, DAD and LNM contributed to preparation of the pH/ORP and endpoint fluorescence assays and to pH/ORP measurements, while STB and LNM measured endpoint SYBR Green fluorescence.

DAD, MAH and WW contributed to assay validation using the test-tube reference measurements and LF starter follow-up.

DAD and WW curated the data and experimental metadata, and WW and DAD developed the supporting software. SB provided resources and supervision, administered the project and acquired funding.

## References

1. Dailey, D. A.; Hernández-Pagán, E.; Bailey, S.; Bavaresco, S. T.; Raffaele, N. E.; Piatt-Price, A.; Carneiro, J. S. A.; Austin, R. N.; Doherty, C. J.; Banta, S. Biophytometallurgy: Biomining Metals from Plant Resources. *bioRxiv* (preprint), **2026**. DOI: [10.64898/2026.08.27.747594](https://doi.org/10.64898/2026.08.27.747594).

2. Elsevier. [CRediT Author Statement](https://www.elsevier.com/researcher/author/policies-and-guidelines/credit-author-statement) (accessed 2026-09-12).
