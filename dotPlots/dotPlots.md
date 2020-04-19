**This folder, not related with the manuscript**

We speculate here on the news, that report that the Nobel laureate Luc Montagnier clains that novel coronavirus genome has HIV elements.

## Genomes
The four existing genomes and the randomized HIV sequence are:

- SARS-CoV-2 genome (NC_045512v2)
- Human immunodeficiency virus type 1 (K03455.1)
- Bat coronavirus RaTG13 (MN996532.1)
- Ebola Virus (KM034562v1)
- The shuffled version of the HIV genome is obtained using an off-line version of *"The Sequence Manipulation Suite: JavaScript programs for analyzing and formatting protein and DNA sequences"* (Stothard P, Biotechniques 28:1102-1104, 2000)


## Dot Plots (folder plots)
If those elements regards the existence of pieces of HIV genome, artificially embedded into the SARS-CoV-2 genome, they should be easely recognizable.

We compared four viral genomes using a strategy based on dotPlots (https://en.wikipedia.org/wiki/Dot_plot_(bioinformatics)) using a custom made program. This method is effective to compare visually two DNA sequences and see if the sequences share similar regions.

Each genome is aligned to the SARS-CoV-2 genome; when a k-mer of dimension k=8 is found (in both directions), the position on both the genome is recorded. This list of coordinates are then visualized as on a dotplot.

### COV2 vs. COV2 dot plot
The diagonal visible in the plot is the main characteristic of this plot. It represents the fact that the sequence is identical to himself. At this magnification, we only can appreciate some patterns along the main diagonal and a high density of points.

### COV2 vs. RaTG dot plot
This plot is quite similar to the previous one. Same principal diagonal with similar patterns around it. This shows that the two genomes are very close.

### COV2 vs. HIV1 dot plot
In this case, no lines, diagonals, or patterns are present in the dot plot. It is much less dense than the previous two. It shows that the number of sequences shared among the two genomes is small and sparse, along with the two sequences.

### COV2 vs. Shuffled HIV1 dot plot
This plot share the same general proprety of the HIV1 dot plot.

### COV2 and Ebola
Similar to the COV2 vs. HIV dot plot, this shows no signs of significative shared pieces of DNA among the two genomes. The density of the plot is slightly higher than the HIV plot.


## Alignment (Alignments folder)
Starting from the dot plot matrix, it is possible the reconstruction of the segments of genomes shared by the two sequences.
In the `.tab` files (space separated), we present all the shared fragments longer than 15 bases. The reconstruction of the fragments admits no more than around 20% mismatches and 10% insertions/deletion.


The table format is

|COV2start |COV2end |GENstart |GENend |Direction |Length |COV2Seq |GENseq|
|---|---|---|---|---|---|---|---|
|20 |36 |5 |21 |+| 17| CCAGGTAACAAACCAAC |CCAGGTAACAAACCAAC|
|4310| 4329| 4292| 4310| - |19 |TGTAAAAGTGCCTTTTACA| TGTAAAAGGCACTTTTACA|
|...||||||||

### COV2 vs. COV2 Alignment
An alignment that spans the whole sequences is found (main diagonal). Other 44 short alignments (<=25 bp) are found in both the direction.

### COV2 vs. RaTG Alignment
The two genomes share 139 fragments (various length) along the main diagonal in the same direction, a sign of a very close phylogenic relation.
### COV2 vs. HIV1 Alignment
Only three short fragments are found in common

~~~
COV2start COV2end GENstart GENend Direction Length COV2Seq GENseq

9660 9678 9005 9023 + 19 TCACACCTTTAGTACCTTT TCACACCTCAGGTACCTTT
23918 23933 4872 4886 + 16 AAACAAATTTACAAAA AAACAAATTACAAAA
7083 7102 6083 6101 - 19 CTACTAATGTCACTATTGC CTACTAATGCTACTATTGC
~~~

We did not find any remarkable similarities.

### COV2 vs. Shuffled HIV1 Alignment
In this case, one shared sequence is found

~~~
COV2start COV2end GENstart GENend Direction Length COV2Seq GENseq
10343 10363 6536 6554 - 20 AAGACACCTAAGTATAAGTT AAGACACCTCGTATAAGTT
~~~

### COV2 and Ebola Alignemnt
In this case, 15 short fragments are detected

~~~
COV2start COV2end GENstart GENend Direction Length COV2Seq GENseq
3775 3795 12542 12560 + 21 CACAAATGTCTACTTAGCTGT CACAAATGCATTTAGCTGT
11584 11603 7204 7221 + 20 TAATACACTTCAGTGTATAA TAATACACCCGTGTATAA
14379 14398 9646 9663 + 20 TAATGTTTTATTCTCTACAG TAATGTTTGACTCTACAG
20213 20232 84 105 + 20 GAAATTTACAAGAATTTAAA GAAATTTATATCGGAATTTAAA
21690 21708 5474 5490 + 19 TCAGATCCTCAGTTTTACA TCAGATCCAGTTTTACA
25358 25377 18345 18362 + 20 AAAGGAGTCAAATTACATTA AAAGGAGTCCTTACATTA
3432 3452 10715 10732 - 20 TGGTTGTTAATGCAGCCAAT TGGTTGTTAGCAGCCAAT
3792 3809 13018 13034 - 17 CTGTCTTTGATAAAAAT CTGTCTTTTATAAAAAT
8566 8584 3836 3854 - 18 TAATTGGTTGAAGCAGTT TAATTGGTGGAAAGCAGTT
13884 13903 11619 11635 - 19 ATACAATTGTTGTGATGAT ATACAATTGGTGATGAT
15802 15819 12828 12844 - 17 TATCAAAACAATGTTTT TATCAAAATAATGTTTT
16703 16722 17828 17846 - 19 AAGTGCTGTCTGACAGAGA AAGTGCTGAGTGACAGAGA
19799 19818 13771 13789 - 19 AGCGCAACATTAAACCAGT AGCGCAACTTAAAACCAGT
22135 22151 12534 12548 - 16 ATTTGTGTTTAAGAAT ATTTGTGTTAAGAAT
22951 22970 11921 11938 - 19 TTTTGAGAGAGATATTTCA TTTTGAGATAATATTTCA
~~~

## Considerations
The unusual but recurrent claim about the man-made origin of the coronavirus is quite simple to be indagated by anyone. If the subject is that a viral genome is manipulated, introducing external DNA like in this case, an homology analysis can be performed. Two sequences can be compared using canonical pairwise alignment tools (e.g., BLAST) or a more visual strategy (dot plot). 
The comparison here proposed shows that
 
1. the HIV1 genomic fragments found in the SARS-CoV-2 genome are explainable by a random matching similar to all the matches found by Perez JC (2020) between the HIV1 variants and the SARS-CoV-2 genome. All the alignments found by Perez are really short, with an e-value bigger than 1, except for only the region 24-43 in the HIV-2 isolate 106CP_RT (0.34).
2. Ebola shares more short alignments with the SARS-CoV-2 genome than HIV1 being only 1.5 times bigger. So, if the Ebola virus genome is not considered as a donor of DNA, why should we focus on HIV? Why should we not extend the comparison with other genomes (eg, extinct species)?
