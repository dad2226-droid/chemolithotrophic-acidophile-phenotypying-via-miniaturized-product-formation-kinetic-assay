# Chemolithoautotrophic acidophile phenotyping via miniaturized product-formation kinetic assay

This collection provides the underlying measurements and experimental annotations for testing the tolerance of some iron- and/or sulfur-oxidizing acidophiles to some more (non-)metals<sup>1</sup> using microplate-based absorbance measurements. It includes indicator calibration, medium validation, and flask and test-tube culture experiments. The documentation identifies preparations, conditions, experimental units, reference measurements and sampling times so that the data can be interpreted independently of a particular analysis workflow.

## Dataset information

| Field | Information |
|---|---|
| Dataset title | Chemolithoautotrophic acidophile phenotyping via miniaturized product-formation kinetic assay |
| Dataset creators, in citation order | Daniel A. Dailey; Wei Wang; Scott Banta |
| Corresponding contacts | Scott Banta; Daniel A. Dailey |
| Contact emails, in the same order | sbanta@columbia.edu; dad2226@columbia.edu |
| Data and documentation license | [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/); SPDX identifier: `CC-BY-4.0`.<sup>2</sup> |
| Funders | U.S. National Science Foundation (NSF) |
| Grants and awards | U.S. National Science Foundation: DGE-2437839 |

## Organization

A shared materials-and-strains folder and the five experimental families have folders directly inside the repository's `data/` directory, alongside this README. Each family has a README and YAML documentation alongside its data. Folder number prefixes control display order; experimental identifiers define the relationships among measurements.

The shared [materials and strains catalog](00_materials_and_strains/README.md) provides tables and machine-readable data for chemicals, materials, equipment, strains and medium formulations. Reagent identities are distinct from experiment-specific concentrations and concentration-determination methods. Experiment-specific assignments are documented with each experimental family.

| Folder within `data/` | Contents | Documentation to read first |
|---|---|---|
| [00_materials_and_strains](00_materials_and_strains/) | Shared chemicals, materials, equipment, strains and media formulations, with tables and YAML records. | [README.md](00_materials_and_strains/README.md). |
| [01_indicator_calibration](01_indicator_calibration/) | Thymol-blue pH and iron absorbance calibrations, spectra, configuration and storage measurements, and paired lid/no-lid readings. | The family [README.md](01_indicator_calibration/README.md), followed by the pH, iron or lid-comparison YAML. |
| [02_media_validation](02_media_validation/) | Abiotic measurements in iron- and sulfur-containing media, with pH and iron reference values. | [README.md](02_media_validation/README.md) and [media_validation.yaml](02_media_validation/media_validation.yaml). |
| [03_biological_microplates](03_biological_microplates/) | AF, AT, and LF culture measurements, additive concentration series and corresponding abiotic wells. | [README.md](03_biological_microplates/README.md), [biological_definitions.yaml](03_biological_microplates/biological_definitions.yaml), then the relevant organism's experiment YAML. |
| [04_flask_validation](04_flask_validation/) | AF flask cultures and abiotic controls, including citric acid–gallium combinations, chemistry measurements and fluorescence. | [README.md](04_flask_validation/README.md) and [flask_validation.yaml](04_flask_validation/flask_validation.yaml). |
| [05_test_tube_validation](05_test_tube_validation/) | Acidophile and abiotic tube cultures, pH/ORP time courses, endpoint fluorescence and documented starter-culture observations. | [README.md](05_test_tube_validation/README.md) and [test_tube_validation.yaml](05_test_tube_validation/test_tube_validation.yaml). |

Organism codes and strain designations are defined in the shared [strain table](00_materials_and_strains/strains.md). Experimental metadata select the applicable strain and preserve starter-culture identities.

## Reading the collection

Start with the README for the experimental family of interest. Its YAML documents contain named fields and lists that can be read in a text editor. They define the applicable methods, units, concentrations, well assignments, replication and identifiers. Shared definitions use the [documented `$ref` convention](00_materials_and_strains/README.md#reading-shared-yaml-references); retain `00_materials_and_strains` with any experimental family. The CSV column definitions describe the corresponding data tables.

Reader exports retain their supplied formats. The family READMEs explain how their measurement blocks and wavelength labels are organized. The indicator-calibration and media-validation families each have a `reference_measurements.csv`; these are separate reference collections and should be used with their own family's YAML. `flask_measurements.csv` and `test_tube_measurements.csv` contain one row per flask or tube and sampling event, as defined in their documentation. Test-tube rows also explicitly identify shared initial-reference assignments.

Use identifiers to connect measurements to their definitions. A repeated reading of a plate, well, flask or tube remains an observation of that same physical experimental unit. Shared starter cultures and reference values are identified in the family metadata. Replicate numbers alone do not establish relationships between different experiments or preparation batches.

## Values, units and missing observations

Curated CSVs use a period as the decimal separator and `NA` for an unavailable or inapplicable value. `NA` is distinct from numerical zero. Where status columns are present, use them to distinguish reported values from absent observations. Instrument flags in reader exports retain the meanings described in the corresponding family documentation.

Use the stated unit and concentration basis for each experiment. Stock, preparation and final-well concentrations are distinct quantities. Elemental-analysis concentrations already account for analytical dilution. Measured, nominal and assigned-reference values are identified in the documentation. All populated initial flask chemistry values are assignments from measured starting-medium references, including pH, ORP, Fe(II), total Fe, Ga, Cu, V and Al. They are not separate measurements of individual flasks. The test-tube initial-reference rows also represent shared assignments.

All nominal stock concentrations were calculated from the mass added and the final prepared volume in the [documented stock-preparation vessel](00_materials_and_strains/chemicals_materials_equipment.md#materials-and-equipment). Subsequent mixing and dilution volumes determine the stated preparation or final-culture concentration; nominal concentrations are distinct from elemental measurements.

All ORP values are reported in mV versus Ag/AgCl with 3 M KCl reference electrolyte.

All deposited fluorescence values have the TE Buffer background-blank subtracted. The fluorescence methods and bibliography are provided in the flask and test-tube documentation.

Preserve the supplied numerical precision. Negative readings and explicitly identified below-baseline values remain part of the data. Use each family's documented timing fields and time origin; acquisition indices are not elapsed times. Where an instrument clock's time zone is unspecified, no time-zone conversion is implied.

## Contributors

| Initials | Name | Affiliation | ORCID |
|---|---|---|---|
| DAD | Daniel A. Dailey | Department of Chemical Engineering, Columbia University | [0000-0003-1908-7196](https://orcid.org/0000-0003-1908-7196) |
| MAH | Mallori A. Herishko | Department of Chemical Engineering, Columbia University | [0009-0009-0165-2098](https://orcid.org/0009-0009-0165-2098) |
| WW | Wei Wang | Department of Chemical Engineering, Columbia University | [0009-0002-5905-2318](https://orcid.org/0009-0002-5905-2318) |
| LNM | Lauren N. Murray | Department of Chemical Engineering, Columbia University | [0009-0000-5291-5200](https://orcid.org/0009-0000-5291-5200) |
| STB | Sofia T. Bavaresco | Department of Chemical Engineering, Columbia University | [0009-0007-4652-5733](https://orcid.org/0009-0007-4652-5733) |
| NRL | Natalie R. Ling | Department of Chemical Engineering, Columbia University | [0000-0002-3824-9122](https://orcid.org/0000-0002-3824-9122) |
| SVRA | Sebastian Valentino Rojas Abregu | Department of Biomedical Engineering, Columbia University | [0009-0002-9372-3226](https://orcid.org/0009-0002-9372-3226) |
| SB | Scott Banta | Department of Chemical Engineering, Columbia University | [0000-0001-7885-0150](https://orcid.org/0000-0001-7885-0150) |

The following roles summarize contributions to the dataset using the CRediT taxonomy.<sup>3</sup> Experimental design is represented by Methodology; experimental preparation and measurements are represented by Investigation. The family READMEs specify contributions to each experimental collection.

| CRediT role | Contributors |
|---|---|
| Conceptualization | DAD, MAH |
| Methodology | DAD, MAH, LNM, STB |
| Investigation | DAD, MAH, LNM, STB, NRL, SVRA |
| Validation | DAD, MAH, WW |
| Data curation | DAD, WW |
| Software | WW, DAD |
| Resources | SB |
| Supervision | SB |
| Project administration | SB |
| Funding acquisition | SB |

DAD conceived the use of thymol blue as the pH indicator in this assay, and MAH conceived the Fe(III) absorbance indicator approach.

DAD contributed experimental design across all five families; DAD and MAH co-designed media validation, and MAH designed the final ferric-indicator series. DAD, LNM and STB co-designed the AF/AT soluble-sulfur series in SM4 basal salts.

MAH and DAD prepared calibration and media-validation experiments; MAH collected their optical data, with SVRA and NRL contributing to the final iron studies and NRL to the lid comparison. DAD, MAH and NRL contributed to AFM1 screening; LNM and DAD prepared and measured the AFM4 and soluble-sulfur series, while MAH and LNM measured the LF series prepared by DAD and MAH. DAD performed the flask chemical measurements, and DAD and NRL measured flask fluorescence. DAD, STB and SVRA prepared the tube cultures, with STB, SVRA, DAD and LNM contributing measurements and STB and LNM measuring endpoint fluorescence; DAD carried out the original LF starter follow-up.

DAD, MAH and WW contributed to assay validation using the calibration, medium-validation, biological microplate, flask and test-tube datasets.

DAD and WW curated the data and experimental metadata, and WW and DAD developed the supporting software. SB provided resources and supervision, administered the project and acquired funding.

## References

1. Tuovinen, O. H.; Niemelä, S. I.; Gyllenberg, H. G. Tolerance of *Thiobacillus ferrooxidans* to Some Metals. *Antonie van Leeuwenhoek* 1971, *37*, 489–496. [DOI: 10.1007/BF02218519](https://doi.org/10.1007/BF02218519).

2. Creative Commons. *Attribution 4.0 International (CC BY 4.0).* [License terms](https://creativecommons.org/licenses/by/4.0/) (accessed 2026-09-12).

3. Elsevier. [CRediT Author Statement](https://www.elsevier.com/researcher/author/policies-and-guidelines/credit-author-statement) (accessed 2026-09-12).

