# Mitigating Dataset Harms Requires Stewardship:<br/>Lessons from 1000 Papers

This repository contains supplemental data for the paper [**Mitigating Dataset Harms Requires Stewardship: Lessons from 1000 papers**](https://arxiv.org/abs/2108.02922).

## License information

All files in this repository are licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

<img src="https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png" alt="CC-BY-NC-SA image"/>

Data collected using the [Semantic Scholar API](https://www.semanticscholar.org/product/api) (detailed in the descriptions below) are licensed under the [Semantic Scholar Dataset License](https://api.semanticscholar.org/license/).

<img src="./s2-logo.svg" alt="Semantic Scholar logo" width="300"/>

We make the following .csv files available:

**msceleb1m_all.csv, dukemtmc_all.csv, lfw_all.csv**

These are the full corpora we collected, containing 1,404, 1,393, and 7,732 papers respectively. The following columns are given, and reflect information given by Semantic Scholar:
* paperId: the Semantic Scholar id of the paper
* cites {dataset id}: for each dataset used to build the corpus, 1 if the paper cites {dataset id} and 0 otherwise—see *summary.csv* for dataset ids.
* title, abstract, year, venue, arxivId, doi
* pdfUrl: a URL where the paper may be publicly available, found via Semantic Scholar or arXiv

**msceleb1m_labeled.csv, dukemtmc_labeled.csv, lfw_labeled.csv** 

These are the samples of papers that we analyzed, containing 276, 275, and 400 papers respectively. In addition to all the columns above, the following additional columns are given:
* uses dataset or derivative: 1 if we determined that the paper uses a dataset or derivative and 0 otherwise
* dataset(s) / model(s) used: a comma separated list of datasets or models used, denoted by the id provided in *summary.csv* in brackets (e.g., [D8], [M5])
* unable to disambiguate: 1 if we were unable to determine the specific dataset(s) used or whether a dataset was used, and 0 otherwise

**summary.csv**

This is a table summarizing our analysis.

**dataset_list.csv**

This file contains the names of the 54 face and person recognition datasets we compiled to select our three datasets of interest, the number of total citations on Semantic Scholar (at the time of collection in August 2020), and their Semantic Scholar Corpus ID which can be used to access metadata from the Semantic Scholar API.
