# Class Cardinality Comparison

1. [Introduction](#introduction)
2. [Data](#data)
3. [Results](#results)


## Introduction <a name="introduction"></a>
This repository contains dataset used in our experiments on the domimance estimation problem. We tackle class cardinality comparison leveraging three infomation sources: Knowledge Bases (KBs as Wikidata), Search-engines (SEs like Bing) results, and, Language Models (LMs like GPT-3).

## Data <a name="data"></a>
The data consists of:

- `classes.csv` - 90 classes with their ground-truth cardinalities and ground-truth metadata such as source, last updated.
- `domains.json` - JSON file with domains as keys. The value is a dict containing a list of classes, applicable subgroups of that domain.
- `subgroups.json` - JSON file containing subgroup names as keys and the values the subgroup takes, for instance countries in the G20 group.
- `wikidata_country_labels.json` - JSON map of Wikidata entities to subgroup values.

## Results <a name="results"></a> 
Results are in the `results/` folder and consist of:

1. Results on basic signals: root, subgroup aggregations
	- `alldomains/` - all class pairs (4005) on all sources
	- `creative_work`, `geographical_entity`, `man-made_object`, `occupation`, `organization`, `species` - by individual domains
2. Results on ensembles
	- `ensembles/signal/` - root + subgroup aggregation ensembles by source
	- `ensembles/source/` - source ensemble weights and predictions
3. Results in a single file
	- `aggregated_results.csv` - predictor accuracies on all class pairs.

##### TO-DO: update result fieldname desc. Add results here-->.
