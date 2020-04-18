**This folder, not related with the manuscript**

## Dot Plots
We speculate here on the news, that report that the Nobel laureate Luc Montagnier clains that novel coronavirus genome has HIV elements.
If those elements regards the existence of pieces of HIV genome, artificially embedded into the SARS-CoV-2 genome, they should be easely recognizable.

We compared four viral genomes using a strategy based on dotPlots (https://en.wikipedia.org/wiki/Dot_plot_(bioinformatics)).

This method is effective to compare visually two DNA sequences and see if the sequences share similar regions.

The four genomes used here are:
- SARS-CoV-2 genome (NC_045512v2)
- Human immunodeficiency virus type 1 (K03455.1)
- Bat coronavirus RaTG13 (MN996532.1)
- Ebola Virus (KM034562v1)

Each genome is aligned to the SARS-CoV-2 genome; when a k-mer of dimension k=8 is found (in both directions), the position on both the genome is recorded. This list of coordinates are then visualized as on a dotplot.

### COV2 vs. COV2 dot plot
The diagonal visible in the plot is the main characteristic of this plot. It represents the fact that the sequence is identical to himself. At this magnification, we only can appreciate some patterns along the main diagonal and a high density of points.

### COV2 vs. RaTG dot plot
This plot is quite similar to the previous one. Same principal diagonal with similar patterns around it. This shows that the two genomes are very close.

### COV2 vs. HIV1 dot plot
In this case, no lines, diagonals, or patterns are present in the dot plot. It is much less dense than the previous two. It shows that the number of sequences shared among the two genomes is small and sparse, along with the two sequences.

### COV2 and Ebola
Similar to the COV2 vs. HIV dot plot, this shows no signs of significative shared pieces of DNA among the two genomes. The density of the plot is slightly higher than the HIV plot.