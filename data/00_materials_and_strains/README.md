# Materials and strains

This folder gathers the study-wide chemicals, materials, equipment, strains and medium formulations documented in the data deposit. Markdown tables provide a reading view; paired YAML files provide the corresponding data, retained identifiers and source mappings. It contains experimental documentation, not measured outcomes or analytical results.

| Subject | Tables | Data |
|---|---|---|
| Chemicals, materials, and equipment used in this study | [chemicals_materials_equipment.md](chemicals_materials_equipment.md) | [chemicals_materials_equipment.yaml](chemicals_materials_equipment.yaml) |
| Strains used in this study | [strains.md](strains.md) | [strains.yaml](strains.yaml) |
| Media formulations used in this study | [media_formulations.md](media_formulations.md) | [media_formulations.yaml](media_formulations.yaml) |

The inventory contains 84 chemical/reagent-preparation entries (58 tested additives, four excluded preparations and 22 medium/assay reagents or preparations), 32 materials/equipment entries, five strains and 13 medium formulations. An entry identifies a documented material; it does not establish a supplier, bottle, batch or acquisition detail that was not recorded. Missing YAML values are `null`, and missing table values are dashes.

This folder provides the shared inventories and definitions. Family YAMLs reference its recipes, strains, instruments and shared reference methods; experiment-specific assignments are documented within each family.

The two source records named `SM4_BS` remain distinct here: `SM4_BS_microplate` contains 0.19 g/L citric acid, whereas `SM4_BS_tube` contains none. Strain designations likewise do not merge independently prepared starter cultures. Source links identify the corresponding family records.

The [stock preparation records](chemicals_materials_equipment.md#stock-preparation-records) incorporate supplied reagent masses and final volumes for 19 preparations: ten nominal additive stocks, the thymol blue stock, three excluded preparations and five stocks with a measured/ICP-based concentration classification. Gallium sulfate also has a supplied formula mass of 745.35 g/mol for both pH-specific preparations; its pH 1.8 record has no supplied mass or volume. Preparation records are nested under the applicable `maximum_additive_stocks` or `attempted_stock_preparations` entries in [the inventory YAML](chemicals_materials_equipment.yaml), and under `reagent_preparations.thymol_blue` in [experimental_definitions.yaml](experimental_definitions.yaml).

Mass-derived concentrations use the documented formula mass or the supplied preparation formula mass without a purity correction. A calculation fraction of 1 represents this nominal convention, not a measured reagent purity. Preparation amounts and calculated nominal concentrations accompany the reported stock concentrations and their measured/nominal classifications. Excluded preparation amounts do not establish dissolved concentrations.

Contributor identities and roles are recorded in the [dataset overview](../README.md#contributors) and the relevant family READMEs. Return to the [data overview](../README.md).

## Reading shared YAML references

A mapping containing only `$ref` selects a value from another YAML file. The path is relative to the file containing the reference; the part after `#` is a JSON Pointer into that file. For example, `../00_materials_and_strains/strains.yaml#/strains/AF/strain` selects the AF strain designation. A pointer can select a scalar, list or full definition. Plain YAML parsers show the reference object; follow it to read the value.

[experimental_definitions.yaml](experimental_definitions.yaml) retains context-specific source schemas for medium recipes and shared reference methods, reagent preparations and material identity fields. These source schemas preserve original field names, units, stock stages and qualifications alongside the study-wide reading tables. Local `medium_id`, `species_id`, physical-vessel, culture, acquisition and treatment assignments remain in their experimental folders.

[chemical_reagents.yaml](chemical_reagents.yaml) exposes the established `reagents` mapping by referencing each maintained bottle record in the complete materials inventory. No second set of bottle records is stored in that file.

Keep this shared folder with the experimental data when transferring a subset of the deposit. Resolve each `$ref` by opening its relative YAML path and selecting the stated JSON Pointer; missing targets or cycles indicate incomplete or invalid metadata.
