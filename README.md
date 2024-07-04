# PlanKG: Plan Generation from Unstructured Documents Through Transformer-Based Extraction of Knowledge Graphs
[Click here to read our paper](https://aisel.aisnet.org/ecis2024/track03_ai/track03_ai/1/)
---

Planning for complex tasks is a key task for knowledge workers that is often time-consuming and depends on the manual extraction of knowledge from documents. In this research, we propose an end-to-end method, called PlanKG, that: (1) extracts knowledge graphs from full-text plan descriptions(FTPD); and (2) generates novel FTPD according to plan requirements and context informationprovided by users. From the knowledge graphs, activity sequences are obtained and projected into embedding spaces. We show that compressed activity sequences are sufficient for the search and generation of plan descriptions. The PlanKG method uses a pipeline consisting of decoder-only transformer models and encoder-only transformer models. To evaluate the PlanKG method, we conducted an experimental study for movie plot descriptions and compared our method with original FTPDs and FTPD summarizations. The results of this research has significant potential for enhancing efficiency and precision when searching and generating plans.

---

# Repository Structure

```
.
├── README.md
├── Resources
│   ├── JupyterNotebooks
│   │   ├── Benchmark2.ipynb
│   │   ├── PlanKG_sim.ipynb
│   │   └── cluster.ipynb
│   ├── Prompts
│   │   └── singlePrompts
│   │       ├── ADarkSong.txt
│   │       ├── Annabelle.txt
│   │       ├── Atonement.txt
│   │       ├── Australia.txt
│   │       ├── Belle.txt
│   │       ├── BrightStar.txt


│   ├── RDFs
│   │   ├── AllRDFs.docx
│   │   ├── actionRDF.txt
│   │   ├── comedyRDF.txt
│   │   └── horrorRDF.txt
│   ├── Summarizations
│   │   └── singleSummarizations
│   │       ├── ADarkSong.txt
│   │       ├── Annabelle.txt
│   │       ├── Atonement.txt
│   │       ├── Australia.txt
│   │       ├── Belle.txt
│   │       ├── BrightStar.txt



│   └── Visualizations
│       ├── AtomicBlondeRDF.png
│       ├── BudapestRDF-1.png
│       ├── RDF_Titanic.png
│       └── TitanicKnowledgeGraphRDFtext.txt
├── benchmark.py
├── cluster_results
├── data
│   ├── KG_ActivitySequences.txt
│   ├── LLMsummaries.txt
│   ├── WikiDescriptions.txt
│   ├── testPlotComedy.txt
│   ├── testWikiAction.txt
│   └── testWikiComedy.txt
├── main.py
├── plan_generation.py
├── results
│   ├── combined_cluster.png
│   ├── kg_cluster.png
│   ├── plots_cluster.png
│   ├── summaries_cluster.png
│   └── top_3_act_seq.txt
└── tree_structure.txt

12 directories, 108 files

```

## Code

- main.py: Contains the core logic for the PlanKG method, including code for clustering and similarity analysis. It saves the top three similar sets of activity sequences to a text file.
- plan_generation.py: Takes the output from main.py and generates novel movie plots based on the input activity sequences.
- benchmark.py: Includes additional benchmarking code for evaluating the performance of the models.
- results: Contains the results of clustering (images) and the top three activity sequences.
- data: contains the dataset, including Wikipedia descriptions, LLM summaries, and knowledge graphs, as well as sample test data.

## Resources

- Jupyter Notebooks: Contains notebooks for various benchmarking and simulation tasks.
- Prompts: Includes the prompts used with ChatGPT for generating initial data.
- RDFs: Contains RDF (Resource Description Framework) files categorized by genre.
- Summarizations: Includes summarizations of movie plots used in the study.
- Visualizations: Visual representations of the knowledge graphs extracted from movie plots.

## How to Use
- Run main.py: This script will process the dataset, extract knowledge graphs, and identify the top three similar activity sequences.
- Run plan_generation.py: Use the output from main.py to generate novel movie plots based on the extracted activity sequences.
- Review Results: Check the results folder for clustering results and generated plots.

# Cite our paper

If you use PlanKG in your research, please cite our paper:

```

Maass, Wolfgang; Agnes, Cicy K.; and Harig, Amin, "Plan Generation from Unstructured Documents Through Transformer-Based Extraction of Knowledge Graphs" (2024). ECIS 2024 Proceedings. 1.
https://aisel.aisnet.org/ecis2024/track03_ai/track03_ai/1

```
