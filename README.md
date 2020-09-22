# Drug-Repurposing-in-KNIME
An Integrative Drug Repurposing Pipeline using KNIME and Programmatic Data Access: A case study on COVID-19 Data

This repository contains supplementary material to "
An Integrative Drug Repurposing Pipeline using KNIME and Programmatic Data Access: A case study on COVID-19 Data" 
paper in Journal of Cheminformatics. 

As the drug-repurposing strategy applied here is mainly conceived for educational purposes, we introduce a step-by-step tutorial for a guided development of a KNIME workflow. In addition, the workflow developed here is fully versatile and it can thus be reproduced for other diseases of interest. A basic knowledge in the configuration and execution of standard nodes (e.g., the ‘Row Filter’ node, the ‘GroupBy’ node, the ‘Joiner’ node, the ‘Pivoting’ node), import of external datasets into a KNIME workflow (e.g., the ‘SDF reader’ node, the ‘File Reader’ node), handling different chemical formats (e.g., by using RDKit nodes), as well as working with specific data structures in KNIME, is expected here as a prerequisite. 

- a .csv Supplementary file 1 with maximum common substructures in SMARTS detected via hierarchical scaffold clustering for COVID-19
- a .csv Supplementary file 2 with identified hits for COVID-19 from DrugBank
- a .csv Supplementary file 3 with identified hits for COVID-19 from CAS Dataset
- a .csv  Supplementary file 4 with identified hits for COVID-19 by both DrugBank and CAS Dataset
- a .csv  Supplementary file 5 with identified hits for GLUT-1 Deficiency Syndrome in DrugBank
- a .knwf Supplementary file with drug repurposing workflow ("DrugRepurposingPipeline_UniProt.knwf", external UniProt dataset is used as an input)
- a .knwf Supplementary file with drug repurposing workflow ("DrugRepurposingPipeline_OpenTargets.knwf", disease-target associations from the OpenTarget platform are used an input)
- a .pdf/.docx Tutorial file “Part 1: Programmatic access to UniProt database using KNIME”
- a .pdf/.docx Tutorial file “Part 2: Using cross-references to retrieve structural data from the Protein Data Bank (PDB)”
- a .pdf/.docx Tutorial file “Part 3: Integrative data mining of ligand bioactivity data from ChEMBL and PubChem”
- a .pdf/.docx Tutorial file “Part 4: Substructure searches in DrugBank”
- a .pdf/.docx Tutorial file with the answer sheet
- a .pdf file with Supplementary Information
- an example input file (.tsv format). 

An updated input file can be downloaded at Uniprot pre-release website available at

https://covid-19.uniprot.org/uniprotkb?query=*



Expected time of execution of the individual workflow components (expemplified on COVID-19 use case):

1) Open Target ID to UniProt ID mapping: max. 20 sec
2) Retrieval of protein-ligand structural data from the Protein Data Bank: max. 30 min
3) Fetching ligand bioactivity data from open bioactivity data sources via programmatic data access    
      ChEMBL: max. 30 min
      PubCHem: ~ 2 hours
      IUPHAR: max. 10 min

4) Substructure searches to identify potentially interesting compounds for drug repurposing 
      Generation of Murcko Scaffolds: ~ 3 min
      Scaffold clustering and maximum common substructure calculation: max. 10 min
      Substructure search in DrugBank: max. 20 min
      Substructure search in CAS dataset: max. 40 min


