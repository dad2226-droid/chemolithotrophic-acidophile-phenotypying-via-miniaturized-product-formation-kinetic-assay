# Strains used in this study

| Code | Organism | Strain designation | Experimental collections |
| --- | --- | --- | --- |
| AF | *Acidithiobacillus ferrooxidans* | ATCC 23270 | [03_biological_microplates](../03_biological_microplates/); [04_flask_validation](../04_flask_validation/); [05_test_tube_validation](../05_test_tube_validation/) |
| AT | *Acidithiobacillus thiooxidans* | ATCC 19377 | [03_biological_microplates](../03_biological_microplates/); [05_test_tube_validation](../05_test_tube_validation/) |
| LF | *Leptospirillum ferriphilum* | DSM 14647 | [03_biological_microplates](../03_biological_microplates/); [05_test_tube_validation](../05_test_tube_validation/) |
| AFur | *Acidithiobacillus ferridurans* | DSM 29468 | [05_test_tube_validation](../05_test_tube_validation/) |
| AC | *Acidithiobacillus caldus* | ATCC 51756 | [05_test_tube_validation](../05_test_tube_validation/) |

[strains.yaml](strains.yaml) contains these identities and their source-field mappings. ATCC/DSM designations identify strains; they do not establish acquisition lots or dates. `Ab` is an abiotic-control code. Indicator calibration and medium validation contain no organisms.

Keep culture identities in the experimental metadata: microplate batch/row identities, flask starter assignments and tube `inoculum_culture_ID` records identify the biological replicates. The original LF microplate starters had unknown age; their follow-up and the fresh test-tube starters are separate cohorts. Incubation temperature and medium are experimental-condition fields rather than fixed strain properties.
