# README

# Acute Myeloid Leukemia Heatmap Analysis - README

This repository contains an R script for an analysis of RNA-seq data from an acute myeloid leukemia (AML) sample dataset, aiming to create a heatmap visualization. The heatmap will help visualize patterns and correlations in the gene expression data of the AML samples. 

This analysis has been adapted from this [refine.bio-examples notebook](https://alexslemonade.github.io/refinebio-examples/03-rnaseq/clustering_rnaseq_01_heatmap.html) and uses the following dataset: [acute myeloid leukemia sample dataset](https://www.refine.bio/experiments/SRP070849) [Source 0](https://www.reneshbedre.com/blog/heatmap-with-pheatmap-package-r.html).

## Data

The data used in this analysis consists of 19 samples obtained from 19 acute myeloid leukemia (AML) model mice. The samples contain RNA-sequencing results for types of AML under controlled treatment conditions. The [dataset can be downloaded from this page on refine.bio](https://www.refine.bio/experiments/SRP070849) and is pre-processed and quantile normalized [Source 2](https://davetang.org/muse/2018/05/15/making-a-heatmap-in-r-with-the-pheatmap-package/).

## Dependencies

This script requires the following R packages:

- `pheatmap` for creating heatmaps [Source 0](https://www.reneshbedre.com/blog/heatmap-with-pheatmap-package-r.html).
- `magrittr` for pipeline operations.

You can install these packages in R using `install.packages()` if they are not already installed.

```r
if (!("pheatmap" %in% installed.packages())) {
  # Install pheatmap
  install.packages("pheatmap", update = FALSE)
}
```

## Running the script

The main script `AML_heatmap.R` can be run in R or RStudio. It performs the following steps:

1. Sets up the analysis directories.
2. Defines the file paths to the dataset and metadata.
3. Installs and loads required libraries.
4. Imports and prepares data.
5. Selects genes of interest based on their variance.
6. Prepares metadata for annotation.
7. Creates an annotated heatmap.

## Output

The output of this script is a heatmap visualizing the gene expression data. The heatmap is clustered and annotated, providing a visual representation of the patterns and correlations in the data [Source 3](https://www.statology.org/pheatmap-r/). The heatmap is saved as a PNG file in the `plots` directory.

## Customization

You can customize the color palette, clustering method, and other aspects of the heatmap using the various parameters of the `pheatmap()` function. For more information, refer to the [pheatmap package documentation](https://cran.r-project.org/web/packages/pheatmap/index.html) [Source 14](https://cran.r-project.org/web/packages/pheatmap/index.html).

## Contact

For any questions or issues, please open an issue on this repository, or contact the author, Candace Savonen, directly.

## License

This project is licensed under the MIT License. See the LICENSE file for details.