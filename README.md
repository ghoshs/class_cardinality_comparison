# Class Cardinality Comparison

1. [Introduction](#introduction)
2. [Data](#data)
3. [Results](#results)
4. [Citation](#citation)
5. [License](#license)

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

## Citation <a name="citation"></a>
If you use our work please cite us:

```bibtex
@inproceedings{ghosh2023class,
    title = "Class Cardinality Comparison as a Fermi Problem",
    author = "Shrestha Ghosh and Simon Razniewski and Gerhard Weikum",
    booktitle = "WWW 2023",
    month = may,
    year = "2023",
}
```

Full paper available [here](https://ghoshs.github.io/files/WWW_2023.pdf).

## License <a name="license"></a>
Shield: [![CC BY 4.0][cc-by-shield]][cc-by]

This work is licensed under a
[Creative Commons Attribution 4.0 International License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg

