# bachelorThesis-EfficiencyMetricsInTotalSynthesis


## abstract
Efficiency metrics are one of the leading toolts that allow for the evaluation and ranking of molecules, reactions and synthetic pathways, as they can provide a helpfull inside into their complexity. A comparison of complexity metrics was executed on a selection of both well-known and newer metrics of different categories. In total 8 metrics were used. Dataset analysis on a dataset of 1.4 milion reaction was conducted. The datas were converted into a graph where the reactions were nodes and connectivity and network analysis was
performed. This datased was also used as a training set for a sink or source reaction classifier. Finally, all 8 metrics, alongside the classifier, were applied onto 18 known strychnine pathways, in onder to determinate their ability to predict the key step of a reaction pathway.

## in this repositary
There are all four necessairy jupyter notebooks alongside the 18 strychnine pathways and the two pathways of chondrochloren and salvianolactone. All of the pathways are in the form SMILES and each of the pathways is stored in separate text file. The reaction dataset used for the training of the classifier.

### metricsEvolution
This notebook computes the score for all 8 chosen metrics and determinates their differential for the reactions of the chondrochloren and salvianolactione pathways.

### networkAnalysis
Here, the analysis of the graph constructed based on the reactionSmilesFigShare2025 dataset is conducted along with the computation of the Morgan fingerprints for the dataset.

### sinkOrSourceClassification
In this notebook a LGBM model is trained using the previously mentioned fingerprints. The model is then used to predict the class of the reactions in the 18 strychnine pathways.

### scoringPathways 
The computation of the differential of the scores for each of the 8 metrics is conducted. The results are then ranked to see the highest and lowest scoring reactions for given pathway and metric. The classification predictions are also ranked.

## python libraries and tools used
The following libraries were used: RDkit, Scikit-learn, Matplotlib, NetworkX, Pyvis, LGBM, numpy, pandas and tqdm.
