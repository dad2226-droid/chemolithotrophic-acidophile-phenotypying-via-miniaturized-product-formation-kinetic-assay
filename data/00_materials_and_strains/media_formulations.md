# Media formulations used in this study

These 13 formulations consolidate the recipes documented for media validation, biological microplates, flasks and test tubes. [media_formulations.yaml](media_formulations.yaml) contains numeric concentrations, units, preparation-pH definitions, references and source-field mappings.

Amounts describe nominal 1× prepared medium before extra dye or inoculum, as applicable. They retain the source recipe precision. Stock strength, dispensing volumes, treatment additions and measured mixture pH remain in the experiment records. A component absent from a recipe is not added by that recipe; experimental additions are separate. Each table below has one formulation and one concentration schema.

| Formulation ID | Medium | Preparation pH | Source recipe |
| --- | --- | --- | --- |
| AFM1 | AFM1 | 1.8 | [media_validation.yaml](../02_media_validation/media_validation.yaml) (`media.AFM1`); [biological_definitions.yaml](../03_biological_microplates/biological_definitions.yaml) (`media.AFM1`); [flask_validation.yaml](../04_flask_validation/flask_validation.yaml) (`medium_definition`) |
| AFM3 | AFM3 | 1.8 | [media_validation.yaml](../02_media_validation/media_validation.yaml) (`media.AFM3`) |
| F2S | F2S | 1.8 | [media_validation.yaml](../02_media_validation/media_validation.yaml) (`media.F2S`) |
| AFM4 | AFM4 | 3.5 | [media_validation.yaml](../02_media_validation/media_validation.yaml) (`media.AFM4`); [biological_definitions.yaml](../03_biological_microplates/biological_definitions.yaml) (`media.AFM4`) |
| AFM5 | AFM5 | 3.5 | [media_validation.yaml](../02_media_validation/media_validation.yaml) (`media.AFM5`) |
| Starkey_brown | Starkey with brown sulfur | 2.5 | [media_validation.yaml](../02_media_validation/media_validation.yaml) (`media.Starkey_brown`) |
| Starkey_colloidal | Starkey with colloidal sulfur | 2.5 | [media_validation.yaml](../02_media_validation/media_validation.yaml) (`media.Starkey_colloidal`) |
| AFM1_BS | AFM1 basal salts | 1.8 | [biological_definitions.yaml](../03_biological_microplates/biological_definitions.yaml) (`media.AFM1_BS`) |
| HH | HH iron medium | 1.8 | [biological_definitions.yaml](../03_biological_microplates/biological_definitions.yaml) (`media.HH`); [test_tube_validation.yaml](../05_test_tube_validation/test_tube_validation.yaml) (`media.HH`) |
| SM4_BS_microplate | SM4 basal salts with citric acid | Experiment-specific | [biological_definitions.yaml](../03_biological_microplates/biological_definitions.yaml) (`media.SM4_BS`) |
| SM4_BS_tube | SM4 basal salts without citric acid | 2.2 | [test_tube_validation.yaml](../05_test_tube_validation/test_tube_validation.yaml) (`media.SM4_BS`) |
| SM4_S0 | SM4 with brown elemental sulfur | 2.2 | [test_tube_validation.yaml](../05_test_tube_validation/test_tube_validation.yaml) (`media.SM4_S0`); [test_tube_validation.yaml](../05_test_tube_validation/test_tube_validation.yaml) (`media.SM4_BS`) |
| SM4_tetrathionate | SM4 with potassium tetrathionate | 2.2 | [test_tube_validation.yaml](../05_test_tube_validation/test_tube_validation.yaml) (`media.SM4_tetrathionate`); [test_tube_validation.yaml](../05_test_tube_validation/test_tube_validation.yaml) (`media.SM4_BS`) |

## AFM1: AFM1

| Component | Concentration | Unit |
| --- | --- | --- |
| (NH4)2SO4 | 0.8 | g/L |
| KH2PO4 | 0.1 | g/L |
| MgSO4·7H2O | 2 | g/L |
| ATCC Trace Mineral Supplement | 5 | mL/L |
| FeSO4·7H2O | 20 | g/L |

Preparation pH: 1.8. Medium preparation target. Parent formulation adapted as documented for this dataset; measured mixture pH and experimental additions remain in family metadata. Parent-formulation references: 1.

## AFM3: AFM3

| Component | Concentration | Unit |
| --- | --- | --- |
| (NH4)2SO4 | 0.8 | g/L |
| KH2PO4 | 0.1 | g/L |
| MgSO4·7H2O | 2 | g/L |
| ATCC Trace Mineral Supplement | 5 | mL/L |
| citric acid | 1.92 | g/L |
| FeSO4·7H2O | 27.8 | g/L |

Preparation pH: 1.8. Medium preparation target. Parent formulation adapted as documented for this dataset; measured mixture pH and experimental additions remain in family metadata. Parent-formulation references: 1, 2.

## F2S: F2S

| Component | Concentration | Unit |
| --- | --- | --- |
| (NH4)2SO4 | 0.8 | g/L |
| KH2PO4 | 0.1 | g/L |
| MgSO4·7H2O | 2 | g/L |
| ATCC Trace Mineral Supplement | 5 | mL/L |
| citric acid | 1.92 | g/L |
| FeSO4·7H2O | 27.8 | g/L |
| elemental sulfur, brown | 1 | g/L |

Preparation pH: 1.8. Medium preparation target. Parent formulation adapted as documented for this dataset; measured mixture pH and experimental additions remain in family metadata. Parent-formulation references: 2, 3.

## AFM4: AFM4

| Component | Concentration | Unit |
| --- | --- | --- |
| (NH4)2SO4 | 3.0 | g/L |
| K2HPO4 | 3.0 | g/L |
| MgSO4·7H2O | 0.5 | g/L |
| CaCl2 | 0.18875 | g/L |
| Na2S2O3 | 3.1859 | g/L |

Preparation pH: 3.5. 2x stock target. Parent formulation adapted as documented for this dataset; measured mixture pH and experimental additions remain in family metadata. Parent-formulation references: 4.

## AFM5: AFM5

| Component | Concentration | Unit |
| --- | --- | --- |
| (NH4)2SO4 | 3.0 | g/L |
| K2HPO4 | 3.0 | g/L |
| MgSO4·7H2O | 0.5 | g/L |
| CaCl2 | 0.18875 | g/L |
| K2S4O6 | 6.09435 | g/L |

Preparation pH: 3.5. 2x stock target. Parent formulation adapted as documented for this dataset; measured mixture pH and experimental additions remain in family metadata. Parent-formulation references: 4.

## Starkey_brown: Starkey with brown sulfur

| Component | Concentration | Unit |
| --- | --- | --- |
| (NH4)2SO4 | 2.0 | g/L |
| KH2PO4 | 3.0 | g/L |
| MgSO4·7H2O | 0.5 | g/L |
| FeSO4·7H2O | 0.001 | g/L |
| CaCl2·2H2O | 0.25 | g/L |
| elemental sulfur, brown | 1 | g/L |

Preparation pH: 2.5. Medium preparation target. Parent formulation adapted as documented for this dataset; measured mixture pH and experimental additions remain in family metadata. Parent-formulation references: 5.

## Starkey_colloidal: Starkey with colloidal sulfur

| Component | Concentration | Unit |
| --- | --- | --- |
| (NH4)2SO4 | 2.0 | g/L |
| KH2PO4 | 3.0 | g/L |
| MgSO4·7H2O | 0.5 | g/L |
| FeSO4·7H2O | 0.001 | g/L |
| CaCl2·2H2O | 0.25 | g/L |
| elemental sulfur, colloidal | 1 | g/L |

Preparation pH: 2.5. Medium preparation target. Parent formulation adapted as documented for this dataset; measured mixture pH and experimental additions remain in family metadata. Parent-formulation references: 5.

## AFM1_BS: AFM1 basal salts

| Component | Concentration | Unit |
| --- | --- | --- |
| ammonium sulfate | 0.8 | g/L |
| potassium phosphate monobasic | 0.1 | g/L |
| magnesium sulfate heptahydrate | 2.0 | g/L |
| ATCC Trace Mineral Supplement | 5 | mL/L |

Preparation pH: 1.8. Basal-medium preparation target. AFM1 basal salts without the iron(II) sulfate substrate. Parent-formulation references: 1.

## HH: HH iron medium

| Component | Concentration | Unit |
| --- | --- | --- |
| ammonium sulfate | 0.132 | g/L |
| magnesium chloride hexahydrate | 0.053 | g/L |
| potassium phosphate monobasic | 0.027 | g/L |
| calcium chloride dihydrate | 0.147 | g/L |
| iron(II) sulfate heptahydrate | 20 | g/L |
| ATCC Trace Mineral Supplement | 5 | mL/L |

Preparation pH: 1.8. Medium preparation target. The tube recipe expresses its first four salts in mg/L (132, 53, 27 and 147 mg/L); these are the same nominal amounts as the g/L values documented for microplates. MD-TMS is the local trace-mineral supplement. Parent-formulation references: 7.

## SM4_BS_microplate: SM4 basal salts with citric acid

| Component | Concentration | Unit |
| --- | --- | --- |
| ammonium sulfate | 0.8 | g/L |
| magnesium sulfate heptahydrate | 2.0 | g/L |
| potassium phosphate dibasic | 0.1 | g/L |
| citric acid | 0.19 | g/L |
| ATCC Trace Mineral Supplement | 5 | mL/L |

Preparation pH: specified by experiment. Initial pH specified by experiment when measured. Contains 0.19 g/L citric acid. Sulfur substrate identities and doses are experiment-specific. Source medium ID: SM4_BS. Parent-formulation references: 6.

## SM4_BS_tube: SM4 basal salts without citric acid

| Component | Concentration | Unit |
| --- | --- | --- |
| ammonium sulfate | 0.8 | g/L |
| magnesium sulfate heptahydrate | 2 | g/L |
| potassium phosphate dibasic | 0.1 | g/L |
| ATCC Trace Mineral Supplement | 5 | mL/L |

Preparation pH: 2.2. Basal-salt stock target; treatment-solution target is pH 1.8. No citric acid added. Source medium ID: SM4_BS. Recorded initial mixture pH is separate. Parent-formulation references: 6.

## SM4_S0: SM4 with brown elemental sulfur

| Component | Concentration | Unit |
| --- | --- | --- |
| ammonium sulfate | 0.8 | g/L |
| magnesium sulfate heptahydrate | 2 | g/L |
| potassium phosphate dibasic | 0.1 | g/L |
| ATCC Trace Mineral Supplement | 5 | mL/L |
| brown elemental sulfur | 1 | g/L |

Preparation pH: 2.2. Basal-salt stock target; treatment-solution target is pH 1.8. Uses the complete citrate-free tube basal formulation. Treatment additions are separate from the medium recipe. Parent-formulation references: 6.

## SM4_tetrathionate: SM4 with potassium tetrathionate

| Component | Concentration | Unit |
| --- | --- | --- |
| ammonium sulfate | 0.8 | g/L |
| magnesium sulfate heptahydrate | 2 | g/L |
| potassium phosphate dibasic | 0.1 | g/L |
| ATCC Trace Mineral Supplement | 5 | mL/L |
| potassium tetrathionate | 10 | mM |

Preparation pH: 2.2. Basal-salt stock target; treatment-solution target is pH 1.8. Uses the complete citrate-free tube basal formulation. Treatment additions are separate from the medium recipe. Parent-formulation references: 6.

## References

1. Li, X.; Mercado, R.; Kernan, T.; West, A. C.; Banta, S. Addition of Citrate to *Acidithiobacillus ferrooxidans* Cultures Enables Precipitate-Free Growth at Elevated pH and Reduces Ferric Inhibition. *Biotechnol. Bioeng.* 2014, *111* (10), 1940–1948. [DOI: 10.1002/bit.25268](https://doi.org/10.1002/bit.25268).

2. Kernan, T.; West, A. C.; Banta, S. Characterization of Endogenous Promoters for Control of Recombinant Gene Expression in *Acidithiobacillus ferrooxidans*. *Biotechnol. Appl. Biochem.* 2017, *64* (6), 793–802. [DOI: 10.1002/bab.1546](https://doi.org/10.1002/bab.1546).

3. Jung, H.; Inaba, Y.; Jiang, V.; West, A. C.; Banta, S. Engineering Polyhistidine Tags on Surface Proteins of *Acidithiobacillus ferrooxidans*: Impact of Localization on the Binding and Recovery of Divalent Metal Cations. *ACS Appl. Mater. Interfaces* 2022, *14* (8), 10125–10133. [DOI: 10.1021/acsami.1c23682](https://doi.org/10.1021/acsami.1c23682).

4. Silverman, M. P.; Lundgren, D. G. Studies on the Chemoautotrophic Iron Bacterium *Ferrobacillus ferrooxidans*. I. An Improved Medium and a Harvesting Procedure for Securing High Cell Yields. *J. Bacteriol.* 1959, *77* (5), 642–647. [DOI: 10.1128/jb.77.5.642-647.1959](https://doi.org/10.1128/jb.77.5.642-647.1959).

5. Starkey, R. L. Concerning the Physiology of *Thiobacillus thiooxidans*, an Autotrophic Bacterium Oxidizing Sulfur under Acid Conditions. *J. Bacteriol.* 1925, *10* (2), 135–163. [DOI: 10.1128/jb.10.2.135-163.1925](https://doi.org/10.1128/jb.10.2.135-163.1925).

6. Inaba, Y.; Banerjee, I.; Kernan, T.; Banta, S. Transposase-Mediated Chromosomal Integration of Exogenous Genes in *Acidithiobacillus ferrooxidans*. *Appl. Environ. Microbiol.* 2018, *84* (21), e01381-18. [DOI: 10.1128/AEM.01381-18](https://doi.org/10.1128/AEM.01381-18).

7. Leibniz Institute DSMZ–German Collection of Microorganisms and Cell Cultures. *Leptospirillum (HH) Medium*; DSMZ Medium 882, 2024. [Medium formulation](https://www.dsmz.de/microorganisms/medium/pdf/DSMZ_Medium882.pdf) (accessed 2026-09-12).
