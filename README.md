# Using networks to visualize my text analysis of NYC's 311 housing complaints

## Usage
This file extends the tokenization text analysis that I executed in my https://github.com/mghersher/nyc_hpd_311 repo. You can generate the tokenized file used for this analysis by running the Tokenization_analysis_311_HPD.ipynb in this nyc_hpd_311 repository. This notebook reads housing complaints from the New York City Open Data Portal's 311 API and analyzes the unstructured text in the resolution description field. It generates a file called HPD_311_all_cleaned_tagged.csv, that is then loaded into the notebooks in this repo to develop the network visualizations.

## Repo organization
There are two main notebooks in this repo:

1. Network_visualization_311_HPD_resolution_process.ipynb: This visualizes co-occurrences of the process and outcome key phrases found in the resolution description field of the 311 complaints. I identified these key phrases in my previous text analysis. I visualize the keywords in a force-directed network, coloring by whether the phrase describes a process that the department of Housing Preservation and Development (HPD) takes to try to resolve a claim or by whether it describes an outcome of one of these processes.
2. Sankey_diagram_311_HPD_resolution_process.ipynb: This visualizes the resolution process taken by the HPD from start to end via a Sankey diagram. It maps complaints by their complaint type, exhibiting how different complaints get processed, and how they ultimately are or are not resolved.

The visualizations that these notebooks produce can be found in output as .html files. 

## Primary packages
The notebooks rely heavily on the following packages:
- pandas 0.25.3
- plotly 4.11.0
- networkx 2.5


