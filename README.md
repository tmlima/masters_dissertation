This repository contains the experiments, corpora and the tool presented in my dissertation.

# Steps to run CORP
Requirements: Java 8 

1 - Download the zip file and extract all contents to a folder

2 - Run the corp jar using the following command

Windows: `java -jar cor_2.4.4.jar`

Linux: `java -Dfile.encoding=ISO8859-1 -jar corp_2.4.4.jar`


This command will run CORP with the Summ-it++ semantic subset, which is already in the input folder. The results will be at the output folder (generated during runtime).

# CORP File strcuture

    .
    ├── input                             # Contains the input texts
        ├── SemEval                       # Contains the SemEval reference file
            ├── SemEval.txt               # File name must be `SemEval.txt`
    ├── Recursos                          # Contains resource files necesary for execution
    ├── output                            # Output files
        ├── <execution timestamp>
            ├── html                      # Html output for each text
            ├── xml                       # Xml output for each text
            ├── EvaluationResults.txt     # Results for MUC, Bcube, CEAFe and CoNLL Avg
            ├── parameters.txt            # Execution parameters: CORP version and semantic resources
            ├── log.txt                   # Execution log file
            ├── SemEvalOut.txt            # SemEval generated
    └── parameters.json                   # Parameters file

To change the input files, copy the texts and SemEval file into input folder. Folder `corpora` contains the corpora used for the experiments in the same file structure CORP uses.

# Configuration file

```json
{
    "use_semantic_base" : "true",
    "semantic_base" : "contopt",
    "use_semantic_similarity" : "false",
    "semantic_similarity_parameters" : 
    {
        "semantic_similarity_threshold" : "0.7",
        "endpoint" : "http://127.0.0.1:5000/similarity"
    },
    "contopt_parameters" :
    {
    	"cut_point_hypernym" : 1,
    	"cut_point_synonym" : 0.75
    },
    "use_hypernym_window" : "true",
    "hypernym_window_size" : "3"
}
```
