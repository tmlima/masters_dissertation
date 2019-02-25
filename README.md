# masters_dissertation
Experiments and tool presented in my dissertation

# CORP

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
