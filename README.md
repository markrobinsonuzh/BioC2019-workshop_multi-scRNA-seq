# Analysis of multi-sample multi-group scRNA-seq data

### Instructor & contact

Helena L. Crowell (helena.crowell\@uzh.ch)

# Workshop description

Single-cell RNA-sequencing (scRNA-seq) has quickly become an empowering technology to characterize the transcriptomes of individual cells. Most early analyses of differential expression (DE) in scRNA-seq data have aimed at identifying differences between cell types, and thus are focused on finding markers for cell sub-populations (experimental units are cells).

There is now an emergence of multi-sample multi-condition scRNA-seq datasets where the goal is to make sample-level inferences (experimental units are samples). To tackle such complex experimental designs, so-called differential state (DS) analysis follows cell types across a set of samples (e.g., individuals) and experimental conditions (e.g., treatments), in order to identify cell-type specific responses, i.e., changes in cell state. 

While there is an opportunity here to leverage existing robust bulk RNA-seq frameworks, by first aggregating single cells into “pseudo-bulk” data at the sub-population level, a mixture model could be applied to directly make use of per-cell measurements. Independent of the undertaken approach, DS analysis: i) should be able to detect “diluted” changes that only affect a single cell type or a subset of cell types; and, ii) is orthogonal to clustering or cell type assignment. Furthermore, cell-type level DE analysis is arguably more interpretable and biologically meaningful.

In this workshop, we will work through a scRNA-seq workflow that is tailored to complex experimental designs, with direct application to a published biological dataset. Upon completion of this workshop, participants should be familiar with general concepts of and various approaches for single-cell data aggregation, DS analysis, and exploration and visualization of differential testing results; and be equipped with the tools necessary to carry out similar analyses on their own.

### Pre-requisites

*Practical knowledge:*

* Intermediate to advanced knowledge of R.
* Familiarity with scRNA-seq technology and data.
* Some knowledge of Bioconductor infrastructure, e.g., the [SummarizedExperiment][1] class.
* Helpful but not mandatory: Experience with some DE analysis framework, such as [DESeq2](http://bioconductor.org/packages/DESeq2), [edgeR][3], or similar.

*Suggested reading:*

* Along with other concepts, the terminology of cell *type* and *state* is explained in  
Wagner et al. (2016): Revealing the vectors of cellular identity with single-cell genomics.  
*Nature Biotechnology* **34**, pages 1145–1160. DOI: https://doi.org/10.1038/nbt.3711.
* An analogous, extensive workflow in the context of CyTOF data has been established by Nowicka et al. ([F1000Research](https://doi.org/10.12688/f1000research.11622.2)), along with a set of visualization tools ([CATALYST](http://bioconductor.org/packages/CATALYST)) and differential testing methods ([diffcyt](http://bioconductor.org/packages/diffcyt)).

### Workshop participation

This will be a hands-on workshop in which attendees will alternately be introduced to each step of the workflow, and apply this knowledge to analyze a published biological dataset. Participants will be guided by a workflow-skeleton, which will prompt them to complete specific assigments. Live-coding will be used to accompany more complex tasks, as well as to present alternative approaches.

### _R_ / _Bioconductor_ packages used

* [SummarizedExperiment][1] for data organization
* [dplyr][2] for data manipulation
* [edgeR][3] for DE analysis
* [scater][4] for preprocessing & visualization
* [ComplexHeatmap][5] for visualization

[1]: https://bioconductor.org/packages/SummarizedExperiment
[2]: https://www.rdocumentation.org/packages/dplyr
[3]: https://bioconductor.org/packages/edgeR
[4]: https://bioconductor.org/packages/scater
[5]: https://www.rdocumentation.org/packages/ComplexHeatmap

### Time outline

| *Activity*                                   | *\~Time*  |
|:---------------------------------------------|:----------|
| **Introduction & theoretical background**    | **20min** |
| - experimental design <br> - approaches for DS analysis <br> - methods for single-cell data | |
| **Hands-on session 1: Preprocessing**        | **20min** |
| - general data overview & diagnostic plots <br> - basic filtering & preprocessing | |
| **Hands-on session 2: DS Analysis**          | **30min** |
| - aggregation to pseudo-bulk data <br> - cluster-level DE analysis with [edgeR][3] <br> - filtering & summarizing results | |
| **Hands-on session 3: Visualization**        | **20min** |
| - cell-level visualization with [scater][4] <br> - sample-level vis. with [ComplexHeatmap][5] | |
| **Closing remarks**                          | **15min** |
| - open discussion, Q&A <br> - challenges, future directions | |

# Workshop goals & objectives

### Learning goals

* identify the type of experimental designs to which DS is applicable
* understand the key differences between DS and *classical* DE analysis (intra- vs. inter-cluster)
* outline conceptually different approaches for DS analysis (cell-, sample-, group-level)
* review a set of methods for DS analysis
* become familiar with different types of data visualization (sample- vs. group-level)

### Learning objectives

* carry out basic pre-processing steps (e.g., filter and normalization)
* aggregate single-cell to pseud-bulk data
* perform DS analysis to detect cell-type specific changes across groups
* visualize, explore, and evaluate differential testing results 
