# KURF Project
```shell
cd ontogpt
```

**Example 1: recipe**

- Step 1: Check the revised template: `src/ontogpt/templates/recipe.yaml`
- Step 2: Run
  ```shell
  ontogpt extract -t recipe -i tests/input/cases/recipe-egg-noodles.txt -o tests/output/owl/recipe-egg-noodles.owl -O owl
  ```
- Step 3: Import generated OWL file into Protégé
- Step 4: Visualise or Save as OWL/XML Syntax file and visualise using WebVOWL

The OntoGPT-generated ontology files are [OWL Functional Syntax](https://www.w3.org/TR/owl2-syntax/) files, 
which *probably* can't be taken by `RDFLib`, `WebVOWL`, and [`Owlready2`](https://github.com/IHTSDO/snomed-owl-toolkit/issues/39#issuecomment-588817185).

**Example 2: gocam**

- Step 1: Check the revised template: `src/ontogpt/templates/gocam.yaml`
- Step 2: Run
  ```shell
  ontogpt extract -t gocam -i tests/input/cases/gocam-betacat.txt -o tests/output/owl/gocam-betacat.owl -O owl
  ```
  - `ERROR:root:slot_usage for undefined slot: id`

TODO:
- [ ] Connect and automate Steps 3 & 4 or develop based on Protégé if you are more comfortable with Java
- [ ] Solve the problem of Example 2
- [ ] Data provenance
  - [ ] Label OntoGPT-generated snippets
  - [ ] Enable edit history tracking (Label user-curated snippets)
