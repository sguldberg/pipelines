# pipelines

# The purpose of these pipelines is to allow for integrated CyTOF analysis from raw FCS files to an initial high-level analysis. Findings ideally should be assesed robustly via manual gating, iterative clustering with different random seeds, and different clustering algorithms.

# CyTOF_Pipeline.Rmd does not include batch correction and is appropriate for datasets that do not span multiple barcode plates or do not have appreciable batch effects.

# For most datasets, CyTOF_Pipeline_BatchCorrection.Rmd is recommended. This pipeline will first take you through data pre-processing which involves bead-based normalization, bead removal, debarcoding, and file organization. Batch effects are then assessed and corrected for using cyCombine (https://biosurf.org/cyCombine_ref_manual.html). Finally, downstream analysis including dimensionality reduction and unsupervised clustering is performed using CATALYST (https://www.bioconductor.org/packages/release/workflows/vignettes/cytofWorkflow/inst/doc/cytofWorkflow.html#cluster-merging-and-annotation). Downstream analysis can be (and shoudl be) further customized into more granular analyses.
