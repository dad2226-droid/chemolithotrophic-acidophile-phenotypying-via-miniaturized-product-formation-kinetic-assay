# Chemicals, materials, and equipment used in this study

This inventory gathers 58 tested additive records, 4 additional attempted preparations excluded from the additive tests, and 22 documented medium or assay reagents/preparations, plus 32 materials/equipment entries. The corresponding data are in [chemicals_materials_equipment.yaml](chemicals_materials_equipment.yaml). Each entry records its source; chemical identities do not assign a bottle lot to every experiment.

## Chemicals and reagent preparations

The first 58 rows identify tested additives and their reported bottle information, CAS numbers, grades and supporting identity references where applicable. The next four rows are preparations excluded from additive testing; their starred concentrations are explained below. The final 22 rows identify materials already named in the medium recipes or measurement methods. A dash means unavailable or unestablished identity information; in the concentration columns it identifies a reagent that was not used as an additive, except that starred entries retain the attempted preparation target. **NV** means an additive solubility has not yet been verified; it does not mean insoluble or zero. Recipe formulas do not verify the purchased bottle form. No additional supplier or lot is inferred.

**Source number** contains a verified catalog/product number where available, otherwise the distinct recorded Source#/Parent# identifier. It excludes supplier names, lot numbers and verification commentary. The YAML retains the supplied identifiers, their types, verification status and provenance; a recorded Source#/Parent# is not automatically a catalog number. Lot and source fields retain the experimenter’s supplied assignments; their column placement does not independently verify a catalog/batch match. Superscripts beside reagent names reference identity evidence. Purity strings retain their reported basis, including Fe basis and trace metals basis.

| Reagent | Chemical formula | CAS number | Supplier | Lot number | Source number | Purity | [Stock] (M) | Solubility (M) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| aluminum sulfate octadecahydrate<sup>1,2</sup> | Al₂(SO₄)₃·18H₂O | 7784-31-8 | Sigma-Aldrich | MKCQ1795 | 227617 | ≥97% | 0.952; 1.00, pH 3.0 | NV |
| Ammonium Sulfate | (NH₄)₂SO₄ | 7783-20-2 | Sigma-Aldrich | 0000418448 | 399014 | ≥99.0% for molecular biology | 0.942<sup>N</sup> | 4.1 (25 °C) <sup>S1</sup> |
| cadmium sulfate<sup>4,5</sup> | CdSO₄ | 10124-36-4 | Sigma-Aldrich | MKCG2625 | 383082 | ACS reagent ≥99.0% | 1.91 | NV <sup>S8</sup> |
| cerium(III) sulfate<sup>6</sup> | Ce₂(SO₄)₃ | 13454-94-9 | Thermo Scientific | A0434313 | 378660500 | 99.9% | 0.138 | 0.150 (25 °C) <sup>S2,S3</sup> |
| cerium(IV) sulfate tetrahydrate<sup>7,8</sup> | Ce(SO₄)₂·4H₂O | 10294-42-5 | GFS Chemicals | C691223 | 2258 | >85% | 0.100 | NV |
| Chromium(III) sulfate hydrate | Cr₂(SO₄)₃·xH₂O | 15244-38-9 | Aldrich Chemistry | MKBJ8402V | 342432 | 22% Cr by weight | 0.500 | NV |
| citric acid | C₆H₈O₇ | 77-92-9 | Sigma-Aldrich | 1003178896 | MKCL2222 | ACS reagent ≥99.5% | 0.592<sup>N</sup> | NV <sup>S10</sup> |
| Cobalt(II) sulfate heptahydrate | CoSO₄·7H₂O | 10026-24-1 | Sigma-Aldrich | SLBQ9230V | 1002793232 | ReagentPlus, ≥99% | 2.00; 2.00, pH 3.0 | NV |
| copper(II) sulfate pentahydrate<sup>10,14</sup> | CuSO₄·5H₂O | 7758-99-8 | Sigma-Aldrich | MKBJ8979V | 209198 | ACS reagent ≥98.0% | 1.03; 0.612, pH 3.0 | NV |
| Dysprosium(III) sulfate octahydrate | Dy₂(SO₄)₃·8H₂O | 10031-50-2 | ChemCruz | C2723 | sc-223955 | — | 0.0466 | NV <sup>S3,S12,S14</sup> |
| Erbium sulfate | Er₂(SO₄)₃·8H₂O | 10031-52-4 | GFS chemicals | 22070024 | 2212 | assay (metals basis): 99.9% min | 0.120 | NV <sup>S3,S12</sup> |
| europium(III) sulfate octahydrate<sup>18</sup> | Eu₂(SO₄)₃·8H₂O | 10031-55-7 | Thermo Scientific | M28G022 | 029106.09 | Reacton 99.9% | 0.0294 | NV <sup>S3,S13</sup> |
| gadolinium(III) sulfate<sup>19,20</sup> | Gd₂(SO₄)₃ | 155788-75-3 | Sigma-Aldrich | MKCQ5722 | 575143 | ≥99.99% trace metals basis | 0.0346 | NV <sup>S3,S12</sup> |
| gallium(III) sulfate hydrate<sup>21,22</sup> | Ga₂(SO₄)₃·xH₂O | 13780-42-2 | BeanTown Chemical (BTC) | 50019021 | 215105-50G | 99.999% trace metals basis | 0.606; 0.600, pH 3.0 | NV |
| Indium(III) sulfate | In₂(SO₄)₃ (hydration unreported) | 13464-82-9 | aablocks | 1554335 | AA003QX6 | 99% | 0.622 | NV |
| Iron(II) sulfate heptahydrate | FeSO₄·7H₂O | 7782-63-0 | Sigma-Aldrich | 0000446398 | 0000436301 | ReagentPlus, ≥99% | 0.600 | NV |
| iron(III) chloride (anhydrous)<sup>26,27</sup> | FeCl₃ | 7705-08-0 | Sigma-Aldrich | SZBE1900V | 157740 | reagent grade 97% | 1.89 | NV |
| Iron(III) sulfate hydrate | Fe₂(SO₄)₃·xH₂O | 15244-10-7 | Honeywell | K314A | 10094524 | 21-23% Fe basis | 0.596 | NV |
| lanthanum(III) sulfate (anhydrous)<sup>10,29</sup> | La₂(SO₄)₃ | 10099-60-2 | Sigma-Aldrich | MKCF7729 | 575208 | ≥99.99% trace metals basis | 0.0298 | 0.0369 (25 °C) <sup>S2,S3</sup> |
| Lithium sulfate anhydrous | Li₂SO₄ | 10377-48-7 | Sigma-Aldrich | 1003784329 | MKCW8587 | 99.5% trace metals basis | 2.50 | NV |
| Magnesium sulfate heptahydrate | MgSO₄·7H₂O | 10034-99-8 | Sigma-Aldrich | 102819884 | BCCM5848 | BioUltra, ≥99.5% (KT) | 2.00 | NV <sup>S9</sup> |
| Manganese(II) sulfate monohydrate | MnSO₄·H₂O | 10034-96-5 | Sigma Life Science | 091M0172V | 1001256756 | BioReagent, plant cell culture tested, cell culture tested | 2.00 | NV |
| Potassium phosphate monobasic | KH₂PO₄ | 7778-77-0 | Sigma Life Science | SLBQ1072V | 1002316423 | ≥99.0%, powder, suitable for cell culture, suitable for insect cell culture, suitable for plant cell culture | 0.600 | NV |
| neodymium(III) sulfate octahydrate<sup>34</sup> | Nd₂(SO₄)₃·8H₂O | 13477-91-3 | Thermo Scientific | T24J010 | 040253.14 | Reacton 99.9% | 0.0408 | 0.0838 (25 °C) <sup>S2,S3</sup> |
| Nickel(II) sulfate heptahydrate | NiSO₄·7H₂O | 10101-98-1 | Chem-Impex Int’l Inc. | 002154-2020-109 | 30629 | 100.33% (titration) | 1.92 | NV |
| Potassium bromide | KBr | 7758-02-3 | Sigma-Aldrich | 1003301444 | MKCP6136 | ACS Reagent, ≥99.0% | 0.614 | NV |
| Potassium chloride | KCl | 7447-40-7 | Sigma-Aldrich | 0000416330 | 0000410768 | ACS Reagent, 99.0-100.5% | 2.04 | ≈4.00 (20 °C) <sup>S5,S6</sup> |
| Potassium dichromate | K₂Cr₂O₇ | 7778-50-9 | Sigma-Aldrich | MKBV0900V | 1002223324 | ACS Reagent, ≥99.0% | 0.00292<sup>N</sup> | NV |
| potassium fluoride dihydrate<sup>10,41</sup> | KF·2H₂O | 13455-21-5 | Sigma-Aldrich | MKCP7519 | 221872 | reagent grade 98% | 0.0568<sup>N</sup> | NV |
| Sodium gluconate (D-gluconic acid sodium salt) | C₆H₁₁NaO₇ | 527-07-1 | Sigma Life Science | SLBC1472V | 1001673832 | ≥99% | 0.438 | NV |
| Potassium iodate | KIO₃ | 7758-05-6 | Sigma-Aldrich | MKCF34?? | 1002655071 | ACS Reagent, 99.5% | 0.0666 | NV |
| Potassium iodide | KI | 7681-11-0 | Sigma-Aldrich | 102887815 | BCCN5153 | ReagentPlus, 99% | 0.592 | NV <sup>S5</sup> |
| Potassium nitrate | KNO₃ | 7757-79-1 | Sigma-Aldrich | 1003458844 | MKCR3008 | ACS Reagent, ≥99.0% | 1.96 | NV <sup>S5</sup> |
| potassium perrhenate<sup>46</sup> | KReO₄ | 10466-65-6 | Sigma-Aldrich | MKCN6384 | 243590 | 99% | 0.0394 | NV <sup>S11</sup> |
| Potassium sulfate | K₂SO₄ | 7778-80-5 | Sigma-Aldrich | 0000461956 | 0000382469 | ReagentPlus, ≥99.0% | 0.612; 1.00, pH 3.0 | NV <sup>S5,S9</sup> |
| potassium tetrathionate<sup>48</sup> | K₂S₄O₆ | 13932-13-3 | Sigma-Aldrich | 0000446606 | 0000401579 | — | 0.612<sup>N</sup> | NV |
| Potassium thiocyanate | KSCN | 333-20-0 | Sigma-Aldrich | 1003508787 | MKCQ7476 | ReagentPlus, ≥99.0% | 0.0324<sup>N</sup> | NV |
| praseodymium(III) sulfate octahydrate<sup>51</sup> | Pr₂(SO₄)₃·8H₂O | 13510-41-3 | AA Blocks | 1305733 | AA003TVJ | 99% | 0.0980 | NV <sup>S3,S13</sup> |
| samarium(III) sulfate octahydrate<sup>10,52</sup> | Sm₂(SO₄)₃·8H₂O | 13465-58-2 | Sigma-Aldrich | MKCQ4221 | 325880 | 99.9% trace metals basis | 0.0294 | NV <sup>S3,S13</sup> |
| silver sulfate<sup>53</sup> | Ag₂SO₄ | 10294-26-5 | Sigma-Aldrich | MKCX8069 | 497266 | >99.99% | 0.0108 | NV |
| Sodium chloride | NaCl | 7647-14-5 | Sigma | SLCJ2677 | 1003281350 | ≥99% (titration), for molecular biology, DNase, RNase, and protease, none detected | 2.08 | NV <sup>S5</sup> |
| sodium chromate tetrahydrate<sup>10,55</sup> | Na₂CrO₄·4H₂O | 10034-82-9 | Sigma-Aldrich | MKCQ9900 | 216623 | 99% | 0.00218<sup>N</sup> | NV |
| sodium formate<sup>56,57</sup> | HCOONa | 141-53-7 | Sigma | BCBZ1955 | 71539 | BioUltra ≥99.0% | 0.202 | NV |
| Sodium molybdate dihydrate | Na₂MoO₄·2H₂O | 10102-40-6 | Sigma-Aldrich | MKBJ8200V | 1001481540 | ACS Reagent, ≥99% (99.5-103.0% ACS specification) | 0.00664 | NV |
| Sodium selenite | Na₂SeO₃ | 10102-18-8 | Sigma Life Science | 071M0044V | 1001266320 | BioReagent, suitable for cell culture ≥98% | 0.0202<sup>N</sup> | NV |
| Sodium sulfate anhydrous | Na₂SO₄ | 7757-82-6 | EMD | 16C090007 | SX0760-3 | ACS reagent | 1.49 | NV <sup>S9</sup> |
| sodium sulfite, anhydrous<sup>62</sup> | Na₂SO₃ | 7757-83-7 | Acros Organics | A0370440 | 219272500 | 98.5% | 2.02 | NV |
| Sodium thiosulfate | Na₂S₂O₃ | 7772-98-7 | Sigma-Aldrich | 1003351008 | MKCP9731 | ReagentPlus, 99% | 0.600<sup>N</sup> | NV |
| sodium tungstate dihydrate<sup>65</sup> | Na₂WO₄·2H₂O | 10213-10-2 | Sigma | BCBF6100V | 72069 | BioUltra ≥99.0% | 0.00660 | NV |
| Sucrose | C₁₂H₂₂O₁₁ | 57-50-1 | Sigma-Aldrich | 1003495902 | SLCN7655 | ≥99.5% (GC), for molecular biology | 2.00<sup>N</sup> | 2.69 (25.05 °C) <sup>S4</sup> |
| Sulfuric acid | H₂SO₄ | 7664-93-9 | Sigma-Aldrich | 4103761605 | MKCW4970 | ACS reagent 95.0-98.0% | 0.200<sup>N</sup> | Miscible <sup>S7</sup> |
| terbium(III) sulfate octahydrate<sup>68</sup> | Tb₂(SO₄)₃·8H₂O | 13842-67-6 | Sigma-Aldrich | 19416KI | 325953 | 99.9% trace metals basis | 0.0330 | NV <sup>S3,S12</sup> |
| titanyl sulfate hydrate<sup>69,70</sup> | TiOSO₄·xH₂O | 13825-74-6 | GFS Chemicals | 19380194 | 1050 | >65.0% | 2.16 | NV |
| Vanadium(IV) oxide sulfate hydrate | VOSO₄·xH₂O | 123334-20-3 | Sigma-Aldrich | 1003523404 | MKCS5691 | 97% | 2.00 | NV |
| ytterbium(III) sulfate octahydrate<sup>72,73</sup> | Yb₂(SO₄)₃·8H₂O | 10034-98-7 | AA Blocks | 8431745 | AA0001L4 | 95% | 0.300 | NV <sup>S3,S12</sup> |
| yttrium(III) sulfate hydrate<sup>74,75,76</sup> | Y₂(SO₄)₃·xH₂O | — | Thermo Scientific | W22I014 | 013155.14 | Reacton 99.99% | 0.0978 | 0.132 (25 °C) <sup>S2,S3</sup> |
| zinc sulfate heptahydrate<sup>77,78</sup> | ZnSO₄·7H₂O | 7446-20-0 | Sigma-Aldrich | MKCT9832 | 221376 | ACS reagent 99% | 2.04; 2.00, pH 3.0 | NV |
| Zirconium(IV) sulfate hydrate | Zr(SO₄)₂·xH₂O | 34806-73-0 | Sigma-Aldrich | 1003822319 | MKCX6038 | 99.99% trace metals basis | 0.576 | NV |
| Ammonium metavanadate | NH₄VO₃ | 7803-55-6 | Sigma-Aldrich | MKCL4102 | 1003024890 | ACS reagent ≥99.0% | 0.300<sup>*</sup> | — |
| Tin(II) sulfate | SnSO₄ | 7488-55-3 | Sigma-Aldrich | 1003846190 | MKCZ1949 | ≥95% | 0.600<sup>*</sup> | — |
| Bismuth sulfate | Bi₂(SO₄)₃ | 7787-68-0 | aladdin | C2304331 | — | CP, ≥98% | 0.500<sup>*</sup> | — |
| thallium(I) sulfate<sup>84</sup> | Tl₂SO₄ | 7446-18-6 | — | — | — | — | 0.0300<sup>*</sup> | — |
| Potassium phosphate dibasic | K₂HPO₄ | 7758-11-4 | Sigma-Aldrich | SLBN6313V | 1002090630 | ACS Reagent, ≥98% | — | — |
| Calcium chloride, plant cell culture tested, anhydrous | CaCl₂ | 10043-52-4 | Σ Life Science | 098K00191 | — | Plant cell culture tested | — | — |
| Calcium chloride dihydrate | CaCl₂·2H₂O | 10035-04-8 | Sigma-Aldrich | SLBP3147V | 1002191256 | ReagentPlus, ≥99.0% | — | — |
| Magnesium chloride hexahydrate | MgCl₂·6H₂O | 7791-18-6 | Sigma-Aldrich | 102547940 | BCCJ0827 | BioXtra, ≥99.0% | — | — |
| Elemental sulfur, brown preparation | S | 7704-34-9 | Toronto Research Chemicals Inc. | 1-LWF-28-1 | S789400 | >80% | — | — |
| Elemental sulfur, colloidal powder | S | 7704-34-9 | Sigma-Aldrich | MKCC3309 | 1002511265 | powder, colloidal, ≥99.0% | — | — |
| ATCC Trace Mineral Supplement | — | — | ATCC | 70071354 | MD-TMS | — | — | — |
| Thymol blue | — | 76-61-9 | Chem-Impex Int’l Inc. | 002126-01-38 | 01268 | 98% (dye content) | — | — |
| Ethanol | C₂H₆O | 64-17-5 | Decon Laboratories, Inc. | — | 2701 | 200 proof, anhydrous | — | — |
| Sodium hydroxide | NaOH | 1310-73-2 | Sigma Aldrich | SLBT8498 | 2488407 | ≥ 98% | — | — |
| Nitric acid | HNO₃ | 7697-37-2 | Sigma-Aldrich | 4104110432 | MKCX6119 | ACS reagent, 70% | — | — |
| Ferroin indicator solution | — | 14634-91-4 | Chem-Impex | 000878-6256161 | 42509 | 0.1 wt % in water, 1,10-phenanthroline iron(ii) sulfate complex, clear red liquid | — | — |
| SYBR(TM) Green I Nucleic Acid Gel Stain | — | 163795-75-3 | Sigma-Aldrich | 105377 | — | 10,000X concentrate in DMSO | — | — |
| TE Buffer | — | — | — | — | — | — | — | — |
| Water | H₂O | 7732-18-5 | — | — | — | ultrapure Milli-Q water | — | — |
| pH calibration standard, pH 1.68 | — | — | — | — | — | — | — | — |
| pH calibration standard, pH 4.01 | — | — | — | — | — | — | — | — |
| pH calibration standard, pH 7.00 | — | — | — | — | — | — | — | — |
| Iron Standards, CRM for AA and ICP | — | — | SPEX CertiPrep | — | — | Assurance Grade | — | — |
| Disodium ethylenediaminetetraacetate | C₁₀H₁₄N₂Na₂O₈ (hydration unreported) | — | Sigma | SLBM2279V | 1001987424 | 99.0–101.0% | — | — |
| Tris(hydroxymethyl)aminomethane hydrochloride | C₄H₁₂ClNO₃ | 1185-53-1 | Sigma | SLBR1378V | 2286292 | ≥99.0% | — | — |
| Cerium(IV) sulfate titrant, 0.1 N | Ce(SO₄)₂ (solution) | 13590-82-4 | Thermo Scientific | R15J510 | 035650.K2 | 0.1 N standardized solution | — | — |

**Stock concentrations.** Unstarred values are the maximum documented 2× additive concentration for each reagent and each recorded additive-stock pH, across the AF, AT and LF microplate experiment records. Unlabelled, unstarred entries are pH 1.8; other pH values follow the concentration. All stocks have three significant figures. The calculation is twice the maximum concentration on the records' 200 µL basis, converted from µM or mM to M: 100 µL of 2× additive is mixed with 100 µL of 2× medium. Values are salt formula-unit molarities, not elemental-ion molarities; the explicit elemental Ga concentrations in the gallium/citric-acid combination are divided by two before comparison. Later dye/inoculum volume additions do not change the concentration of the stock before mixing. Fixed additive components were included when searching for maxima. Stock-pH labels reproduce the metadata, including the sulfuric-acid series; they are not calculated from concentration or replaced by the initial well pH. These entries do not establish equilibrium solubility or experimentally verify every stock pH.

**N — Nominal concentration.** The 11 marked additive reagents are ammonium sulfate, citric acid, sucrose, sulfuric acid, potassium fluoride, potassium thiocyanate, potassium dichromate, sodium chromate, sodium selenite, sodium thiosulfate and potassium tetrathionate. Their concentrations are based on the recorded preparation and dilution volumes. Potassium fluoride, potassium thiocyanate, potassium dichromate, sodium chromate and sodium selenite were not measured for safety reasons; sodium thiosulfate and potassium tetrathionate were always nominal, including additive-screen and sulfur-substrate uses. These assignments override the general Na/K measurement convention. The experimenter confirmed that titanyl sulfate and zirconium(IV) sulfate were measured by ICP-OES in 2% (w/v) HCl. Existing numerical concentrations are retained. The remaining 47 additive reagents have an ICP-based working classification, including these confirmed Ti and Zr stocks. N is distinct from the asterisk identifying preparations excluded from additive tests.

Sources: [shared preparation and concentration definitions](../03_biological_microplates/biological_definitions.yaml), [AF experiments](../03_biological_microplates/01_Acidithiobacillus_ferrooxidans_ATCC_23270/AF_experiments.yaml), [AT experiments](../03_biological_microplates/02_Acidithiobacillus_thiooxidans_ATCC_19377/AT_experiments.yaml), and [LF experiments](../03_biological_microplates/03_Leptospirillum_ferriphilum_DSM_14647/LF_experiments.yaml). The companion YAML records the full-precision maximum and a contributing experiment/group/column for each stock.

**\* Prepared but excluded from additive tests.** These four chemicals were not visibly soluble at the indicated preparation concentrations or after a further fourfold dilution (concentration ÷ 4) in sulfuric acid at the target pH. Starred values are nominal compound preparation targets, not growth-assay stock maxima or measured dissolved concentrations. No numeric target pH is recorded for these preparations, so the unstarred pH 1.8 convention does not apply. Their Solubility (M) cells remain — because they were not tested as additives. The visual observations do not establish equilibrium solubility limits.

**Solubility scope and remaining gaps.** Numeric values refer to salt formula units per litre of aqueous solution at the stated literature temperature, with water as solvent and no imposed assay pH. They are reference values, not measured solubilities in pH 1.8/pH 3.0 assay stocks or growth media. The reported saturation solid phase may differ from the purchased hydrate. Seven additives have verified numerical entries and sulfuric acid is recorded as miscible; the remaining 50 additives are **NV** pending verification. References alongside NV are identified literature leads, not evidence for an unreported numerical value. No density of 1 g/mL is assumed, and mol/kg water or g/100 g water are not relabelled as M. See [Solubility references](#solubility-references) for source locations and conversions.


The medium and assay reagent entries include the supplied bottle details. MD-TMS is the purchased ATCC supplement, lot `70071354`. TE Buffer was prepared as previously described.<sup>85</sup> Preparation-specific reagent-lot assignments are unreported.


## Stock preparation records

The experimenter supplied 19 mass-and-final-volume pairs and a formula-mass-only entry for the pH 1.8 gallium sulfate stock. Masses and volumes are recorded as supplied. The nominal calculations below use the documented chemical formula and CIAAW 2024 abridged atomic weights, except that the gallium calculation uses the supplied 745.35 g/mol. This gallium value does not establish hydrate stoichiometry. No purity correction is applied; the nominal factor of one is not a purity measurement.

Nominal concentration is mass (g) divided by formula mass (g/mol) and final solution volume (L). Final volume is distinct from the nominal capacity of the preparation vessel. Nominal preparation concentrations are distinct from measured concentrations and excluded-preparation targets. These records do not establish that all experiments with a matching reagent used one physical stock batch.

| Reagent / stock | Stock pH | Mass (g) | Final volume (mL) | Formula mass used (g/mol) | Nominal from preparation (M) | Reported stock or target (M) |
|---|---:|---:|---:|---:|---:|---:|
| Ammonium Sulfate | 1.8 | 3.2489 | 26.1 | 132.134 | 0.94206584 | 0.942 |
| citric acid | 1.8 | 2.9049 | 25.5 | 192.123 | 0.59294123 | 0.592 |
| Potassium dichromate | 1.8 | 0.0434 | 50.4 | 294.181 | 0.0029271473 | 0.00292 |
| potassium fluoride dihydrate | 1.8 | 0.2662 | 49.8 | 94.126 | 0.056789639 | 0.0568 |
| potassium tetrathionate | 1.8 | 4.557 | 24.6 | 302.43 | 0.61251828 | 0.612 |
| Potassium thiocyanate | 1.8 | 0.0776 | 24.6 | 97.176 | 0.032461426 | 0.0324 |
| sodium chromate tetrahydrate | 1.8 | 0.0258 | 50.5 | 234.032 | 0.0021829967 | 0.00218 |
| Sodium selenite | 1.8 | 0.0876 | 25.0 | 172.948 | 0.020260425 | 0.0202 |
| Sodium thiosulfate | 1.8 | 4.7487 | 50.1 | 158.097 | 0.59953339 | 0.6 |
| Sucrose | 1.8 | 17.0949 | 25.0 | 342.297 | 1.9976687 | 1.998 |
| Thymol blue | 4.0 | 0.0047 | 50.0 | 466.592 | 0.00020146081 | 0.0002 |
| Ammonium metavanadate (excluded target) | — | 0.8763 | 25.0 | 116.978 | 0.29964609 | 0.3 |
| Tin(II) sulfate (excluded target) | — | 3.2131 | 24.8 | 214.766 | 0.60326348 | 0.6 |
| Bismuth sulfate (excluded target) | — | 8.8655 | 25.0 | 706.128 | 0.50220357 | 0.5 |
| aluminum sulfate octadecahydrate (ICP-based classification) | 3.0 | 33.3215 | 50.0 | 666.402 | 1.000042 | 1.00 |
| copper(II) sulfate pentahydrate (ICP-based classification) | 3.0 | 7.6451 | 50.0 | 249.677 | 0.61239922 | 0.612 |
| gallium(III) sulfate hydrate (ICP-based classification) | 1.8 | — | — | 745.35 | — | 0.606 |
| gallium(III) sulfate hydrate (ICP-based classification) | 3.0 | 22.3823 | 50.0 | 745.35 | 0.60058496 | 0.6 |
| Potassium sulfate (ICP-based classification) | 3.0 | 8.7136 | 50.0 | 174.252 | 1.0001148 | 1 |
| zinc sulfate heptahydrate (ICP-based classification) | 3.0 | 28.754 | 50.0 | 287.541 | 1.999993 | 2 |


The pH 1.8 gallium sulfate entry supplies its calculation formula mass. Titanyl sulfate and zirconium(IV) sulfate concentrations were measured by ICP-OES.

The records are embedded in [chemicals_materials_equipment.yaml](chemicals_materials_equipment.yaml) under each matching stock or attempted preparation. The thymol blue preparation is in [experimental_definitions.yaml](experimental_definitions.yaml) under `reagent_preparations.thymol_blue.preparation_record`. Formula-mass reference: [CIAAW abridged atomic weights](https://www.ciaaw.org/abridged-atomic-weights.htm).

## ICP-OES elemental measurements

The emission wavelengths below were supplied by the experimenter for the Horiba Ultima Expert (radial viewing). The shared method is recorded in [experimental_definitions.yaml](experimental_definitions.yaml) under `reference_methods.ICP_OES_elemental_analysis` and referenced by the stock, iron-reference and flask methods.

| Element | Emission wavelength (nm) |
|---|---:|
| Ag | 328.068 |
| Al | 167.018 |
| Cd | 214.441 |
| Ce | 416.561 |
| Co | 228.615 |
| Cr | 205.571 |
| Cu | 327.395 |
| Dy | 338.502 |
| Er | 369.265 |
| Eu | 412.97 |
| Fe | 259.94 |
| Ga | 417.204 |
| Gd | 342.247 |
| In | 230.606 |
| K | 766.49 |
| La | 379.478 |
| Li | 670.791 |
| Mg | 280.271 |
| Mn | 260.575 |
| Na | 588.995 |
| Nd | 386.333 |
| Ni | 230.3 |
| Pr | 417.939 |
| Sm | 359.26 |
| Tb | 334.942 |
| Ti | 334.941 |
| V | 309.311 |
| Y | 371.029 |
| Yb | 328.937 |
| Zn | 206.201 |
| Zr | 343.823 |

The analytical diluent was 2% (w/v) HNO₃, except that Ti and Zr samples used 2% (w/v) HCl. The corresponding 0 ppm blank was subtracted from the instrument-reported mass concentration before applying the analytical dilution factor and converting to elemental molarity. Compound concentrations then account for elemental stoichiometry. These analytical steps are already reflected in the deposited concentrations and must not be applied again. Analytical dilution is distinct from stock serial dilution and medium/well mixing.

A 1 ppm reference is available for each element as a reference/QC record.

The reported additive-stock solubility protocol is recorded in [biological_definitions.yaml](../03_biological_microplates/biological_definitions.yaml) under `stock_preparation.solubility_screen`. It compares centrifuged/filtered stock-only and stock–AFM1 samples at preparation and day 7 against a fresh uncentrifuged/unfiltered stock reference, with a ≤3% absolute relative difference criterion after accounting for dilution and the AFM1 elemental contribution. Nominal stocks instead use visible-solids observations and a ≤0.05 absolute pH change over 7 d. The protocol reports a 0.2 µm filter. These experimental criteria are separate from the literature-solubility values above.

## Materials and equipment

Product identities, available lots and study-specific usage were supplied by the experimenter on 2026-09-15. Catalog numbers and supplier identifiers are recorded separately from model names. Listed lots are not assigned to individual physical plates or experimental batches. Missing values are shown as dashes.

| Type | Item | Manufacturer | Model or product | Catalog number | Supplier, if different | Reported lot | Documented use and limits |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Equipment | Microplate reader | Molecular Devices | SpectraMax M2 | — | — | — | Calibration, media and biological absorbance; flask and tube fluorescence. |
| Equipment | Microplate reader | Tecan | Infinite M Plex | — | — | — | Paired lid comparison. The workbook header literally reads “infinite 200Pro”; metadata records the experimenter-confirmed model separately. |
| Equipment | Benchtop pH meter | Oakton | pH 700 | — | — | — | Reference and culture pH measurements. |
| Equipment | ICP-OES | Horiba | Ultima Expert | — | — | — | Radial-view elemental measurements; Fe wavelength 259.94 nm. |
| Equipment | ORP electrode | Oakton | Oakton ORP Electrode, epoxy body, double-junction | WD-35805-15 | Spectrum Chemical Mfg. Corp. | — | Flask and tube ORP measurements. Ag/AgCl reference with 3 M KCl electrolyte as documented by the experimenter. |
| Equipment | Microcentrifuge | Thermo Scientific | Sorvall Legend Micro 17 Centrifuge | — | — | — | Both reference-sample clarification steps, at 3,000 × g and 17,000 × g, used the Sorvall Legend Micro 17. |
| Equipment | Vortex mixer | Scientific Industries | Vortex-Genie | — | — | — | Sulfur-suspension and titration mixing. Model reported as Vortex-Genie; no numbered variant is assigned. |
| Equipment | Temperature-controlled shaking apparatus | New Brunswick | I26 shaking incubator | — | — | — | All flask experiments used this I26 at 150 rpm; tube culture shaking is also assigned to this apparatus. Flasks were held individually and tubes in mounted wire racks at 60°. The 4 °C calibration incubations used a separate I26R. |
| Equipment | Refrigerated incubator for 4 °C calibration | New Brunswick | I26R shaking incubator | — | — | — | A separate I26R was used for the 4 °C calibration incubations; all flask experiments used the I26. Shaking during the 4 °C incubations is unreported. |
| Material | UV-transparent microplate | Corning | Costar | 3635 | — | — | Product identified for the calibration physical plates carrying this catalog number; not assigned to other plates from optical type alone. |
| Material | UV-transparent 96-well microplate for pH lid comparison | Corning | Costar UV Plate, 96 Well With UV Transparent Flat Bottom No Lid | 3635 | — | 21225049 | Corning 3635 identified for the pH lid comparison. Supplied lot 21225049 is retained at product level; no individual physical-plate lot assignment is established. |
| Material | Non-UV-transparent microplate | Corning | Costar | 3370 | — | — | Product identified for the calibration physical plates carrying this catalog number. |
| Material | Non-UV-transparent 96-well microplate for storage, media and biological assays | Corning | Costar Assay Plate, With Low Evaporation Lid 96 Well Flat Bottom Non-Treated | 3370 | — | 17725025 | Corning 3370 identified for pH storage, media validation and biological absorbance assays; supplied with a low-evaporation lid. Supplied lot 17725025 is retained at product level. |
| Material | Low-evaporation plate lids | Corning | Low-evaporation lids from sacrificial non-UV Corning 3370 plates | — | — | — | Between-reading storage and paired lid comparisons. Donor lids came from sacrificial non-UV Corning 3370 plates, as confirmed by the experimenter. No donor-lid lot is assigned. |
| Material | Parafilm | Bemis | Parafilm™ M Laboratory Wrapping Film, 4" Width | PM999 | — | — | Plate sealing and storage as specified per experiment; 4-inch Parafilm M, catalog PM999. |
| Material | Gas-exchange membrane | Sigma-Aldrich | Breathe-Easy® sealing membrane | Z380059 | — | — | Gas-exchange membrane for calibration configuration comparisons. |
| Material | 50 mL stock-preparation tube | Environmental Express | CertiTube™, Digestion Tubes with Green Caps | UX-53203-13 | Cole-Palmer | — | 50 mL nominal stock-preparation container established in the concentration documentation; supplied catalog UX-53203-13 is a Cole-Parmer identifier. |
| Material | 250 mL baffled borosilicate-glass culture flask | Corning | PYREX® 250 mL Delong Shaker Erlenmeyer Flask with Baffles | 4444-250 | — | — | Flask validation with 100 mL initial liquid volume. Baffled PYREX borosilicate glass, fitted with 38 mm polypropylene Chemglass CLS-1503-10 closures and held in individual shaker flask holders. |
| Material | 14 mL capped polystyrene culture tube | CELLTREAT | 14 mL Culture Tube, PS Dual Cap | 230440 | — | 250810-1571-A | Tube validation with 6 mL prepared medium. Polystyrene tube with LDPE dual-position cap, vented during culture; held at 60° in mounted wire racks. |
| Material | Sterile 1.5 mL microcentrifuge tubes | — | Sterile 1.5 mL microcentrifuge tubes | 972-95685-CS | Spectrum Chemical | — | Reference-sample clarification. Sterile 1.5 mL microcentrifuge tubes were supplied by Spectrum Chemical, catalog 972-95685-CS. |
| Material | Sterile syringe filter | CELLTREAT | PVDF Syringe Filter, 0.22μm, 30mm, Sterile | 229743 | — | — | Biological additive-stock sterile filtration; 0.22 µm PVDF membrane, 30 mm diameter. |
| Material | Water beaker adjacent to incubating plates | — | — | — | — | — | 100 mL sterile water as documented; vessel capacity and product unreported. |
| Equipment | ORP meter | Oakton | pH 700 Benchtop Meter | EW-35419-03 | — | — | Flask and tube ORP measurements; paired with the separately identified ORP electrode. |
| Equipment | pH electrode | Oakton | Oakton® pH Electrodes with Glass Body | WD-35805-04 | Spectrum Chemical Mfg. Corp. | — | Reference and culture pH measurements with the documented Oakton pH 700 meter. |
| Equipment | Centrifuge | Thermo Scientific | Sorvall ST Plus centrifuge | — | — | — | Cell pellets were prepared by centrifugation in 50 mL tubes as previously described.<sup>85</sup> |
| Equipment | Incubator | Thermo Scientific | Heratherm General Incubator | 51028064 | — | — | LF biological microplate incubation, batch LF_2026-05-29 (33 physical plates). |
| Material | Black 96-well fluorescence microplate | Corning | Costar Assay Plate, 96 Well, No Lid Black, Flat Bottom | 3915 | — | 09525004 | SYBR Green fluorescence measurements. Corning 3915 is distinct from the Corning 3370 absorbance plates; supplied lot 09525004 is retained at product level. |
| Material | 50 mL sterile centrifuge tube | CELLTREAT | 50mL Centrifuge Tube, Sterile | 229436 | — | — | Containment of sterile-filtered additive stocks. Nominal concentrations use the documented 50 mL CertiTube preparation vessel. |
| Material | 15 mL sterile centrifuge tube | CELLTREAT | 15 mL Centrifuge Tube, Sterile | 229414 | — | — | Preparation of serial dilutions of additive stocks. Tube capacity does not establish the final dilution volume. |
| Material | 38 mm polypropylene culture-flask closure | Chemglass | Polypropylene closure, 38 mm | CLS-1503-10 | — | — | Closure used on culture flasks. |
| Equipment | Biological-plate incubator for the KF-containing batch | Thermo Scientific | Heratherm IMC18 | — | — | — | All 55 physical plates in batch AF_2026-01-06, including all additives in the KF-containing experimental set, used the Heratherm IMC18. It is distinct from the Heratherm catalog 51028064 used for LF. |
| Equipment | Biological-plate incubator for remaining batches | Thermo Scientific | MaxQ 6000 | — | — | — | The 350 biological plates outside AF_2026-01-06 and LF_2026-05-29 used the MaxQ 6000. Incubation was static; the product's shaking capability does not establish use of shaking during these experiments. |

Culture tubes were vented and held at 60° in mounted wire racks; flasks were held individually and fitted with the specified Chemglass closures. All laboratory water was ultrapure Milli-Q water; preparation-specific sterility requirements remain as documented.

Biological incubator assignments follow preparation batches: all 55 plates in the KF-containing batch `AF_2026-01-06` used the Thermo Scientific Heratherm IMC18; all 33 LF plates used the Heratherm catalog `51028064`; the remaining 350 plates used the Thermo Scientific MaxQ 6000.

The [I26/I26R manufacturer manual, p. 43](https://www.eppendorf.com/product-media/doc/en/141423_Operating-Manual/New-Brunswick_Shakers_Operating-manual_I-26_I-26R_New-Brunswick-I26-26R-Shaker.pdf) specifies a 25 mm orbital diameter: the diameter of the circular path traced by the shaker platform. All flask experiments used the I26; a separate I26R was used for the 4 °C calibration incubations, as confirmed by the experimenter.

Product specifications: [CELLTREAT 230440 culture tubes](https://www.celltreat.com/product/230440/), [CELLTREAT 229743 filters](https://www.celltreat.com/product/229743/), [Thermo 51028064 incubator](https://www.thermofisher.com/order/catalog/product/51028064), [Chemglass CLS-1503-10 closures](https://chemglass.com/closures-polypropylene), and [Corning 4444-250 flasks](https://ecatalog.corning.com/life-sciences/b2c/US/en/Bioprocess-and-Scale-up/Erlenmeyer-Flasks/Erlenmeyer-Flasks,-Glass/PYREX%C2%AE-Flask-with-Baffles/p/4444-250). Manufacturer specifications establish product properties; reported study applications are attributed separately to the experimenter.

Machine-readable `sources` identify the experimental documentation associated with each entry where an application is established. The Tecan export's literal instrument header and the confirmed instrument model remain distinct.

## Identity notes

- Bottle information supplied by the experimenter on 2026-09-15 is recorded in the table and YAML. Reported grades retain their assay bases, including 22% Cr by weight, 21–23% Fe basis, dye content, and titration assay. The chromium assay was handwritten on the bottle label.
- Sodium gluconate is the reagent associated with experiment/group identifiers containing `potassium_gluconate`. Sodium hydroxide is the additive-stock pH-adjustment base. Nickel(II) sulfate is the heptahydrate. Iron(III) sulfate is an unspecified hydrate; five waters of hydration are not assigned. The experimenter confirmed that the reported gluconate values came from the supplied sodium gluconate.
- Experiment identifiers containing `sodium_selenate` refer to sodium selenite; those containing citrate refer to citric acid. Potassium tetrathionate is the tetrathionate preparation reagent; Sigma-Aldrich lot `0000446606` and source number `0000401579` are recorded. Purity information is unavailable.
- Indium sulfate hydration remains unreported. The supplied sodium sulfate name specifies anhydrous material, and the supplied sodium thiosulfate CAS identifies the anhydrous salt. CAS formatting in the table is normalized; verbatim supplied strings remain in the YAML bottle records.
- The potassium iodate lot `MKCF34??` remains incomplete. Potassium thiocyanate and sodium selenite retain separately documented catalogs P3011 and S5261 in the YAML; supplied source identifiers are recorded separately and are not substituted for independent catalog verification.
- The supplier SDS for yttrium(III) sulfate hydrate leaves CAS unassigned and gives a variable hydrate formula; an octahydrate CAS is not substituted.<sup>74,75,76</sup>
- GFS product 1050 is titanyl sulfate hydrate. Its listed CAS identifies the titanyl sulfate parent species; the number of waters is unspecified. The reported >65.0% is retained; the manufacturer specifies ≥65% as TiOSO₄.<sup>69,70</sup>
- Silver sulfate’s reported >99.99% is retained although the matched supplier product specifies ≥99.99%. Sodium sulfite’s reported 98.5% matches the product title; its current detailed specification instead states 98% minimum by iodimetry. These catalog differences are not substituted for the supplied bottle values.<sup>53,62</sup>
- The standardized 0.1 N cerium(IV) sulfate titrant is a separate purchased solution from the cerium(IV) sulfate additive bottle. Disodium EDTA and Tris–HCl have separate reagent records. TE Buffer was prepared as previously described.<sup>85</sup> MD-TMS is recorded as the purchased ATCC supplement, lot 70071354.

CAS identifiers supplied by identity lookup are [sodium hydroxide, 1310-73-2](https://webbook.nist.gov/cgi/cbook.cgi?ID=1310-73-2), [Tris–HCl, 1185-53-1](https://www.sigmaaldrich.com/US/en/product/sigma/t3253), [elemental sulfur, 7704-34-9](https://www.sigmaaldrich.com/US/en/product/aldrich/213292), [water, 7732-18-5](https://www.sigmaaldrich.com/US/en/product/sigma/w4502), and [SYBR Green I, 163795-75-3](https://www.sigmaaldrich.com/US/en/product/sial/s9430). These lookups establish chemical identity, not the supplied bottle’s catalog or batch. The SYBR identifier denotes the active dye in the reported 10,000× DMSO formulation. Disodium EDTA hydration and the yttrium-sulfate hydrate CAS remain unestablished; missing bottle information is recorded as unavailable.

## References

1. Sigma-Aldrich. *Certificate of Analysis: Product 227617, Batch MKCQ1795*. [Certificate](https://www.sigmaaldrich.cn/certificates/COFA/22/227617/227617-BULK_______MKCQ1795__.pdf) (accessed 2026-09-12).
2. Sigma-Aldrich. *Aluminum sulfate octadecahydrate, ≥97%, Product 227617*. [Source](https://www.sigmaaldrich.com/US/en/product/sigald/227617) (accessed 2026-09-12).
3. Sigma-Aldrich. *Ammonium sulfate, Molecular Biology, ≥99.0%, A4418*. [Source](https://www.sigmaaldrich.com/US/en/product/sigma/a4418) (accessed 2026-09-12).
4. Sigma-Aldrich. *Lab Chemicals outlet inventory: 383082-100G, batch MKCG2625*. [Source](https://www.sigmaaldrich.com/IN/en/campaigns/outlet-store-india/lab-chemicals) (accessed 2026-09-12).
5. Sigma-Aldrich. *Cadmium sulfate ACS reagent, ≥99.0%, 383082*. [Source](https://www.sigmaaldrich.com/US/en/product/sigald/383082) (accessed 2026-09-12).
6. Thermo Fisher Scientific. *Cerium(III) sulfate, 99.9%, (REO=Rare Earth Oxides), 378660500*. [Source](https://www.thermofisher.com/order/catalog/product/378660500) (accessed 2026-09-12).
7. GFS Chemicals. *Ceric Sulfate, Tetrahydrat, 2258*. [Source](https://www.gfschemicals.com/ceric-sulfate-tetrahydrat-2258) (accessed 2026-09-12).
8. GFS Chemicals. *Proprietary & Manufactured Chemicals*. [Source](https://www.cphi-online.com/brochure/resourcefile93420/Manufactured%20&%20Proprietary.pdf) (accessed 2026-09-12).
9. Sigma-Aldrich. *Chromium(III) sulfate hydrate, for synthesis, 342432*. [Source](https://www.sigmaaldrich.com/US/en/product/aldrich/342432) (accessed 2026-09-12).
10. Sigma-Aldrich. *Certificates of Analysis: Lot/Batch Search*. [Certificate](https://www.sigmaaldrich.com/US/en/documents-search?tab=coa) (accessed 2026-09-12).
11. Sigma-Aldrich. *Citric acid, ACS reagent grade, ≥99.5%, 251275*. [Source](https://www.sigmaaldrich.com/US/en/product/sial/251275) (accessed 2026-09-12).
12. Sigma-Aldrich. *Citric acid, anhydrous, Redi-Dri, ACS reagent, ≥99.5%, 791725*. [Source](https://www.sigmaaldrich.com/US/en/product/sial/791725) (accessed 2026-09-12).
13. Sigma-Aldrich. *Cobalt(II) sulfate heptahydrate, ReagentPlus, ≥99%, C6768*. [Source](https://www.sigmaaldrich.com/US/en/product/sigald/c6768) (accessed 2026-09-12).
14. Sigma-Aldrich. *Copper(II) sulfate pentahydrate, ACS reagent ≥98.0%, 209198*. [Source](https://www.sigmaaldrich.com/US/en/product/sigald/209198) (accessed 2026-09-12).
15. Santa Cruz Biotechnology. *Dysprosium(III) sulfate octahydrate, sc-223955*. [Source](https://www.scbt.com/p/dysprosium-iii-sulfate-octahydrate-10031-50-2) (accessed 2026-09-12).
16. GFS Chemicals. *Erbium Sulfate, 99.9%, 2212*. [Source](https://www.gfschemicals.com/erbium-sulfate-99-9-6-2212) (accessed 2026-09-12).
17. Thermo Fisher Scientific. *Erbium(III) sulfate octahydrate, 99.9% (REO), 040092.09*. [Source](https://www.thermofisher.com/order/catalog/product/040092.09) (accessed 2026-09-12).
18. Thermo Fisher Scientific. *Europium(III) sulfate octahydrate, 99.9% (REO), 029106.09*. [Source](https://www.thermofisher.com/order/catalog/product/029106.09) (accessed 2026-09-12).
19. Sigma-Aldrich. *Gadolinium(III) sulfate, ≥99.99% trace metals basis (575143)*. [Source](https://www.sigmaaldrich.com/US/en/product/aldrich/575143) (accessed 2026-09-12).
20. Sigma-Aldrich. *Certificate indexed for product 575143, batch MKCQ5722*. [Certificate](https://www.sigmaaldrich.com/certificates/coa/575143-BULK_______MKCQ5722__.pdf) (accessed 2026-09-12).
21. BeanTown Chemical. *Gallium(III) sulfate hydrate, 99.999% trace metals basis; 215105-50G*. [Source](https://www.beantownchem.com/default.aspx?ButtonSearchHeader.x=0&ButtonSearchHeader.y=0&SearchFieldsList=Keyword&SearchSource=ProductSearch&page=Item+Search+Results&txtSearchText=13780-42-2) (accessed 2026-09-12).
22. Strem Chemicals. *Gallium(III) sulfate hydrate (99.999%-Ga) PURATREM*. [Source](https://www.strem.com/product/93-3126) (accessed 2026-09-12).
23. Thermo Fisher Scientific. *Indium(III) sulfate, anhydrous, 99.99% (metals basis)*. [Source](https://www.thermofisher.com/order/catalog/product/040102.14) (accessed 2026-09-12).
24. Indium Corporation. *Indium Sulfate*. [Source](https://www.indium.com/products/compounds/indium-compounds/indium-sulfate/) (accessed 2026-09-12).
25. Sigma-Aldrich. *Iron(II) sulfate heptahydrate, ReagentPlus, ≥99% (F7002)*. [Source](https://www.sigmaaldrich.com/US/en/product/sigald/f7002) (accessed 2026-09-12).
26. Sigma-Aldrich. *Iron(III) chloride, reagent grade, 97% (157740)*. [Source](https://www.sigmaaldrich.com/US/en/product/sigald/157740) (accessed 2026-09-12).
27. Sigma-Aldrich. *Certificate of Analysis: Product 157740, Lot SZBE1900V*. [Certificate](https://www.sigmaaldrich.com/US/en/documents/coa/157740/SIAL?lotNumber=SZBE1900V) (accessed 2026-09-12).
28. Sigma-Aldrich. *Iron(III) sulfate hydrate (307718)*. [Source](https://www.sigmaaldrich.com/US/en/product/sigald/307718) (accessed 2026-09-12).
29. Sigma-Aldrich. *Lanthanum(III) sulfate, ≥99.99% trace metals basis (575208)*. [Source](https://www.sigmaaldrich.com/US/en/product/aldrich/575208) (accessed 2026-09-12).
30. Sigma-Aldrich. *Lithium sulfate, anhydrous, 99.5% trace metals basis (920339)*. [Source](https://www.sigmaaldrich.com/US/en/product/aldrich/920339) (accessed 2026-09-12).
31. Sigma-Aldrich. *Magnesium sulfate heptahydrate, BioUltra, ≥99.5% (KT) (63138)*. [Source](https://www.sigmaaldrich.com/US/en/product/sigma/63138) (accessed 2026-09-12).
32. Sigma-Aldrich. *Manganese(II) sulfate monohydrate, ReagentPlus, ≥99% (M7634)*. [Source](https://www.sigmaaldrich.com/US/en/product/sigald/m7634) (accessed 2026-09-12).
33. Sigma-Aldrich. *Potassium phosphate monobasic, ACS reagent, ≥99.0% (P0662)*. [Source](https://www.sigmaaldrich.com/US/en/product/sigald/p0662) (accessed 2026-09-12).
34. Thermo Fisher Scientific. *Neodymium(III) sulfate octahydrate, 99.9% (REO), 25 g (040253.14)*. [Source](https://www.thermofisher.com/order/catalog/product/040253.14) (accessed 2026-09-12).
38. Sigma-Aldrich (Merck / MilliporeSigma). *Potassium bromide*. [Source](https://www.sigmaaldrich.com/US/en/substance/potassiumbromide119007758023) (accessed 2026-09-12).
39. Sigma-Aldrich (Merck / MilliporeSigma). *Potassium chloride, ACS reagent, 99.0–100.5%*. [Source](https://www.sigmaaldrich.com/US/en/product/mm/p3911m) (accessed 2026-09-12).
40. Sigma-Aldrich (Merck / MilliporeSigma). *Potassium dichromate, ReagentPlus, ≥99.5%*. [Source](https://b2b.sigmaaldrich.com/US/en/product/sigald/p5271) (accessed 2026-09-12).
41. Sigma-Aldrich (Merck / MilliporeSigma). *Potassium fluoride dihydrate, reagent grade, 98%*. [Source](https://www.sigmaaldrich.com/US/en/product/sigald/221872) (accessed 2026-09-12).
43. Sigma-Aldrich (Merck / MilliporeSigma). *Potassium iodate, ACS reagent, 99.5%*. [Source](https://www.sigmaaldrich.com/US/en/product/sigald/215929) (accessed 2026-09-12).
44. Sigma-Aldrich (Merck / MilliporeSigma). *Potassium iodide, ReagentPlus, 99%*. [Source](https://www.sigmaaldrich.com/US/en/product/sigald/207969) (accessed 2026-09-12).
45. Sigma-Aldrich (Merck / MilliporeSigma). *Potassium nitrate, ACS reagent, ≥99.0%*. [Source](https://www.sigmaaldrich.com/US/en/product/sigald/221295) (accessed 2026-09-12).
46. Sigma-Aldrich (Merck / MilliporeSigma). *Potassium perrhenate, 99%*. [Source](https://www.sigmaaldrich.com/CY/en/product/aldrich/243590) (accessed 2026-09-12).
47. Sigma-Aldrich (Merck / MilliporeSigma). *Potassium sulfate, ReagentPlus, ≥99.0%*. [Source](https://www.sigmaaldrich.com/US/en/product/sigald/p0772) (accessed 2026-09-12).
48. Sigma-Aldrich (Merck / MilliporeSigma). *Potassium tetrathionate*. [Source](https://www.sigmaaldrich.com/US/en/product/aldrich/p2926) (accessed 2026-09-12).
49. Sigma-Aldrich. *Certificate of Analysis: P3011, Batch MKCQ7476*. [Certificate](https://www.sigmaaldrich.com/certificates/COFA/P3/P3011/P3011-BULK________MKCQ7476__.pdf) (accessed 2026-09-12).
50. Sigma-Aldrich. *Potassium thiocyanate, P3011*. [Source](https://www.sigmaaldrich.com/US/en/product/sigald/p3011) (accessed 2026-09-12).
51. AA Blocks. *Safety Data Sheet: Praseodymium(III) sulfate octahydrate, AA003TVJ*. [Safety data sheet](https://www.aablocks.com/downloadSds?cas=13510-41-3) (accessed 2026-09-12).
52. Sigma-Aldrich. *Samarium(III) sulfate octahydrate, 325880*. [Source](https://www.sigmaaldrich.com/US/en/product/aldrich/325880) (accessed 2026-09-12).
53. Sigma-Aldrich. *Silver sulfate, 497266, with lot/batch list*. [Source](https://www.sigmaaldrich.com/IT/en/product/aldrich/497266) (accessed 2026-09-12).
54. Sigma-Aldrich. *Sodium chloride, Molecular Biology, S3014*. [Source](https://www.sigmaaldrich.com/LC/en/product/sigma/s3014) (accessed 2026-09-12).
55. Sigma-Aldrich. *Sodium chromate tetrahydrate, 216623*. [Source](https://www.sigmaaldrich.com/US/en/product/aldrich/216623) (accessed 2026-09-12).
56. Sigma-Aldrich. *Certificate of Analysis: Sodium Formate, 71539, Batch BCBZ1955*. [Certificate](https://www.sigmaaldrich.com/US/en/documents/coa/71539/SIGMA?lotNumber=BCBZ1955) (accessed 2026-09-12).
57. Sigma-Aldrich. *Sodium formate, BioUltra, 71539*. [Source](https://www.sigmaaldrich.com/US/en/product/sigma/71539) (accessed 2026-09-12).
58. Sigma-Aldrich. *Sodium molybdate dihydrate, M1003*. [Source](https://www.sigmaaldrich.com/US/en/product/sigald/m1003) (accessed 2026-09-12).
59. Sigma-Aldrich. *Sodium selenite, BioReagent, S5261*. [Source](https://www.sigmaaldrich.com/US/en/product/sigma/s5261) (accessed 2026-09-12).
60. Merck / Sigma-Aldrich. *Sodium sulfate, anhydrous, 106649*. [Source](https://www.sigmaaldrich.com/US/en/product/mm/106649) (accessed 2026-09-12).
61. Merck / Sigma-Aldrich. *Sodium sulfate decahydrate, EMSURE, 106648*. [Source](https://www.sigmaaldrich.com/US/en/product/mm/106648) (accessed 2026-09-12).
62. Thermo Fisher Scientific (legacy Acros Organics). *Sodium sulfite, 98.5%, for analysis, anhydrous, 219272500*. [Source](https://www.thermofisher.com/order/catalog/product/219272500) (accessed 2026-09-12).
63. Sigma-Aldrich. *Sodium thiosulfate, ReagentPlus, 99%*. [Source](https://www.sigmaaldrich.com/US/en/product/sigald/217263) (accessed 2026-09-12).
65. Sigma-Aldrich. *Sodium tungstate dihydrate, BioUltra, ≥99.0% (T), product 72069*. [Source](https://www.sigmaaldrich.com/US/en/product/sigma/72069) (accessed 2026-09-12).
66. Sigma-Aldrich. *Sucrose, Molecular Biology, ≥99.5% (GC), product S0389*. [Source](https://www.sigmaaldrich.com/US/en/product/sigma/s0389) (accessed 2026-09-12).
67. Sigma-Aldrich. *Sulfuric acid, product 258105*. [Source](https://www.sigmaaldrich.com/US/en/product/sigald/258105) (accessed 2026-09-12).
68. Sigma-Aldrich. *Terbium(III) sulfate octahydrate, 99.9% trace metals basis, product 325953*. [Source](https://www.sigmaaldrich.com/US/en/product/aldrich/325953) (accessed 2026-09-12).
69. GFS Chemicals. *Titanium Sulfate, Purified, product 1050*. [Source](https://www.gfschemicals.com/titanium-sulfate-purified-1050) (accessed 2026-09-12).
70. GFS Chemicals (catalog specifications mirrored by GlobalSpec). *GFS Chemicals datasheet: Titanium Sulfate, Purified, item 1050*. [Source](https://datasheets.globalspec.com/ds/6033/GFSChemicals/pg2) (accessed 2026-09-12).
71. Sigma-Aldrich. *Vanadium(IV) oxide sulfate hydrate, 97%, product 233706*. [Source](https://www.sigmaaldrich.com/US/en/product/aldrich/233706) (accessed 2026-09-12).
72. AA Blocks via Sigma-Aldrich. *Ytterbium(III) sulfate octahydrate, AA Blocks supplier SKU AA0001L4-10G*. [Source](https://www.sigmaaldrich.com/ch/de/product/aablocksinc/aabh3036b287) (accessed 2026-09-12).
73. ProChem. *Ytterbium(III) sulfate octahydrate, product 3817*. [Source](https://prochemonline.com/product/ytterbiumsulfate-3817/) (accessed 2026-09-12).
74. Thermo Fisher Scientific. *Yttrium(III) sulfate hydrate, REacton, 99.99% (REO), catalog 013155.14*. [Source](https://www.thermofisher.com/order/catalog/product/013155.14) (accessed 2026-09-12).
75. Thermo Fisher Scientific. *Safety Data Sheet, Yttrium (III) sulfate, catalog 13155; revised December 25, 2025*. [Safety data sheet](https://www.fishersci.com/store/msds?countryCode=US&language=en&partNumber=AA1315514&productDescription=YTTM+III+SFAT+HYD+25G&vendorId=VN00024248) (accessed 2026-09-12).
76. Thermo Fisher Scientific/Fisher Scientific. *Yttrium(III) sulfate hydrate, certificate directory*. [Certificate](https://www.fishersci.com/shop/products/yttrium-iii-sulfate-hydrate-reacton-99-99-reo-thermo-scientific/AA1315522) (accessed 2026-09-12).
77. Sigma-Aldrich. *Zinc sulfate heptahydrate, ACS reagent, 99%, product 221376*. [Source](https://www.sigmaaldrich.com/US/en/product/sigald/221376) (accessed 2026-09-12).
78. Sigma-Aldrich. *Itens de Validade Curta, inorganic product/lot table*. [Source](https://www.sigmaaldrich.com/BR/pt/campaigns/conteudo-informativo/promocao/validade-curta) (accessed 2026-09-12).
79. Sigma-Aldrich. *Zirconium(IV) sulfate hydrate, 99.99% trace metals basis, product 366773*. [Source](https://www.sigmaaldrich.com/US/en/product/aldrich/366773) (accessed 2026-09-12).

80. Sigma-Aldrich. *Ammonium metavanadate, 205559*. [Identity source](https://www.sigmaaldrich.com/US/en/product/sigald/205559) (accessed 2026-09-13; identity only, not a bottle assignment).
81. Sigma-Aldrich. *Tin(II) sulfate, 244635*. [Identity source](https://www.sigmaaldrich.com/US/en/product/sial/244635) (accessed 2026-09-13; identity only, not a bottle assignment).
83. TCI America. *Bismuth(III) sulfate, B6530*. [Identity source](https://www.tcichemicals.com/US/en/p/B6530) (accessed 2026-09-13; identity only, not a bottle assignment).
84. Santa Cruz Biotechnology. *Thallium(I) sulfate*. [Identity source](https://www.scbt.com/p/thallium-i-sulfate-7446-18-6) (accessed 2026-09-13; identity only, not a bottle assignment).

85. Dailey, D. A.; Hernández-Pagán, E.; Bailey, S.; Bavaresco, S. T.; Raffaele, N. E.; Piatt-Price, A.; Carneiro, J. S. A.; Austin, R. N.; Doherty, C. J.; Banta, S. Biophytometallurgy: Biomining Metals from Plant Resources. *bioRxiv* (preprint), **2026**. DOI: [10.64898/2026.08.27.747594](https://doi.org/10.64898/2026.08.27.747594).

## Solubility references

S1–S7 support the populated entries. S8–S15 and the S3/S5/S9 citations alongside NV retain leads for completing the literature verification.

- **S1.** Baker, S. L., et al. (2019). Transforming protein-polymer conjugate purification by tuning protein solubility. Nature Communications 10, 4718. [Publication](https://doi.org/10.1038/s41467-019-12612-9) Introduction: ammonium sulfate water solubility, 4.1 M at 25 °C.
- **S2.** Kim, R., et al. (2020). Effect of Sulfuric Acid Baking and Caustic Digestion on Enhancing the Recovery of Rare Earth Elements from a Refractory Ore. Minerals 10, 532. [Publication](https://doi.org/10.3390/min10060532) Table 4, 25 °C: Ce₂(SO₄)₃ 85.2, La₂(SO₄)₃ 20.9, Nd₂(SO₄)₃ 48.3, Y₂(SO₄)₃ 61.4 g/L; values attributed there to Das et al. (S3). Use the compound values outside parentheses, divided by anhydrous formula masses, not the elemental concentrations in parentheses.
- **S3.** Das, G., et al. (2019). Rare earth sulfates in aqueous systems: Thermodynamic modeling of binary and multicomponent systems over wide concentration and temperature ranges. Journal of Chemical Thermodynamics 131, 49–79. [Publication](https://doi.org/10.1016/j.jct.2018.10.020) Thermodynamic treatment underlying the rare-earth sulfate values reproduced in S2; saturation solid phases can differ from the purchased hydrate.
- **S4.** Tinjacá, D. A., et al. (2018). Solubility and Apparent Specific Volume of Sucrose in Some Aqueous Polyethylene Glycol Mixtures at 298.2 K. Pharmaceutical Sciences 24, 163–167. [Publication](https://doi.org/10.15171/PS.2018.24) Table 1, PEG mass fraction 0.00 (pure water): 2.688 mol/dm³ at 298.2 K.
- **S5.** Martins, M. J. N., et al. (2023). Solubility of different salts used in the control of the water activity of foods. Ciência e Agrotecnologia 47, e018722. [Publication](https://doi.org/10.1590/1413-7054202347018722) Table 2: KCl 25.401 ± 0.458 g/100 g solution at 293.15 K. The source also covers KI, NaCl, ammonium sulfate, KNO₃ and K₂SO₄, but those mass fractions alone are not molarities.
- **S6.** Bogacz, W., Al-Rashed, M. H., Lemanowicz, M., and Wójcik, J. (2016). A Simple Densimetric Method to Determine Saturation Temperature of Aqueous Potassium Chloride Solution. Journal of Solution Chemistry 45, 1071–1076. [Publication](https://doi.org/10.1007/s10953-016-0492-8) Table 1: saturated KCl solution density 1.17407 g/cm³ at 293.15 K. Combined with S5: c = 1000 × 1.17407 × 0.25401 / 74.5513 = 4.00027 M. The displayed 4.00 M is an approximate conversion combining two studies (the solubility mass-fraction uncertainty corresponds to about 0.07 M).
- **S7.** Shin, D., Kim, Y., and Moon, H. S. (2018). Fate and toxicity of spilled chemicals in groundwater and soil environment I: strong acids. Environmental Health and Toxicology 33, e2018019. [Publication](https://doi.org/10.5620/eht.e2018019) Sulfuric acid subsection: complete miscibility with water. A finite saturation molarity is therefore not assigned.
- **S8.** Brickwedde, L. H. (1946). Solubility of cadmium sulfate in H₂O–D₂O mixtures. Journal of Research of the National Bureau of Standards 36, 377–383. [Publication](https://nvlpubs.nist.gov/nistpubs/jres/36/jresv36n4p377_A1b.pdf) Table 2 reports solute/water mole ratios and solid hydrate transitions. Matching saturated-solution density is still required for a molarity entry.
- **S9.** Krumgalz, B. S. (2018). Temperature Dependence of Mineral Solubility in Water. Part 3. Alkaline and Alkaline Earth Sulfates. Journal of Physical and Chemical Reference Data 47, 023101. [Publication](https://doi.org/10.1063/1.5031951) Evaluated sodium, potassium and magnesium sulfate solubilities are on a molality basis; verify the stable hydrate and matching density before conversion to M.
- **S10.** Laguerie, C., Aubry, M., and Couderc, J.-P. (1976). Some physicochemical data on monohydrate citric acid solutions in water: solubility, density, viscosity, diffusivity, pH of standard solution, and refractive index. Journal of Chemical & Engineering Data 21, 85–87. [Publication](https://doi.org/10.1021/je60068a031) Literature lead; numerical solubility and density tables were not accessible for verification.
- **S11.** Orda, S., et al. (2023). Investigations of the Density and Solubility of Ammonium Perrhenate and Potassium Perrhenate Aqueous Solutions. Materials 16, 5481. [Publication](https://doi.org/10.3390/ma16155481) KReO₄ solubility is in supplementary Table S2, density in Table 5. The solubility ordinate basis could not be verified from the accessible text; no conversion is asserted.
- **S12.** Judge, W. D., et al. (2023). Solubilities of heavy rare earth sulfates in water (gadolinium to lutetium) and H₂SO₄ solutions (dysprosium). Hydrometallurgy 218, 106054. [Publication](https://doi.org/10.1016/j.hydromet.2023.106054) Literature lead for Gd, Tb, Dy, Er and Yb sulfate. Numerical tables were not accessible for verification.
- **S13.** Moldoveanu, G. A., et al. (2024). Solubilities of individual light rare earth sulfates (lanthanum to europium) in water and H₂SO₄ solutions (neodymium sulfate). Hydrometallurgy 223, 106194. [Publication](https://doi.org/10.1016/j.hydromet.2023.106194) Literature lead for Pr, Sm and Eu sulfate. Numerical tables were not accessible for verification.

- **S14.** Cunningham, S., Etherington-Rivas, M., and Azimi, G. (2024). Solubility of neodymium and dysprosium sulfates at different pH and temperature and the effect of yttrium sulfate, sodium sulfate, and ammonium sulfate mixtures: Strengthening the predictive capacities of the OLI software. Hydrometallurgy 224, 106253. [Publication](https://doi.org/10.1016/j.hydromet.2023.106253) Literature lead for neodymium and dysprosium sulfate solubility and mixed-sulfate effects. Numerical source values and conditions were not verified.

- **S15.** Crew, M. C., Steinert, H. E., and Hopkins, B. S. (1925). The Solubility of Yttrium Salts. Journal of Physical Chemistry 29(1), 34–38. [Publication](https://doi.org/10.1021/j150247a004) Literature lead for yttrium salt solubility. Numerical source values and conditions were not verified.
