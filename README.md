# pipelines

 The purpose of this pipeline is to allow for integrated CyTOF analysis from raw FCS files to an initial high-level analysis. Findings ideally should be assesed robustly via manual gating, iterative clustering with different random seeds, and different clustering algorithms. The templates folder contains example .csv and .xlsx files used throughout the analysis to increase ease of use. The templates folder also contains a spillover matrix that can be used to compensate CyTOF data.

This pipeline will first take you through data pre-processing which involves bead-based normalization, bead removal, debarcoding, and file organization. Batch effects are then assessed and corrected for using cyCombine (https://biosurf.org/cyCombine_ref_manual.html). While CyTOF data has less noise than other single cell proteomic datasets such a flow cytometry, compensation is another useful step for cleaning up signal spillover in data. Finally, downstream analysis including dimensionality reduction and unsupervised clustering is performed using CATALYST (https://www.bioconductor.org/packages/release/workflows/vignettes/cytofWorkflow/inst/doc/cytofWorkflow.html#cluster-merging-and-annotation). Downstream analysis can be (and should be) further customized into more granular analyses.
