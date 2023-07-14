FAQ
###

Here are some answers to frequently-asked questions.
Got a question that isn't answered here? You can `write <mailto:support@flomics.com>`_ to us and we will answer as fast as we can!

.. contents::
    :local:
    :depth: 2



Why …
===============

.. _heatscale:

…does the scale of the heatmap go from -2 to 2?
-------------------------------------------

In order to effectively show the difference in abundances between the top 30 most abundant features among the samples, we carry out a mathematical transformation of the feature's abundance, to end up with the decimal logarithm of the abundance in percent. First we transform the abundance to a percent scale. Since the decimal logarithm of zero is undefined, whe add a pseudocount of 0.01 to those features that have an abundance of 0%.
Thus, the normalized abundance for a sample that has an abundance of 0% will be -2, and will be 2 for a sample that has an abundance of 100%.


.. _heattrail:

…do the names of the features in the heatmap have several semicolons on them (";;;")?
--------------------------------------------------------------------------------------

This is because the pipeline follows the ``kpcofgs`` (Kingdom;Phylum;Class;Order;Family;Genus;Species) convention for naming the ASVs found in the sample. Although the pipeline will try to classify each ASVs to the deepest level, this won't always be possible, leaving an ASV classified to, for example, ``family`` level at most. Having two semicolons at the end of the feature name (for example: ``Bacteria;Bacteria;Firmicutes;Bacilli;Lactobacillales;Streptococcaceae;Streptoccocus;;1``) means that the pipeline has classified with confidence that this ASV belongs to the Family ``Streptococcus``, but can't assign with confidence its Genus and Species. The number at the end of the feature name is the confidence of the assignment, ranging from 1 to 0.

How …
===============
…to interpret alpha-diversity metrics?
-------------------------------------------

A diversity index is a quantitative measure that reflects how many different types (such as species) there are in a dataset (a community), and that can simultaneously take into account the phylogenetic relations among the individuals distributed among those types, such as richness, divergence or evenness.
The Shannon Diversity Index (sometimes called the Shannon-Wiener Index, and calculated by Petri) is a way to measure the diversity of species in a community. The higher the value, the higher the diversity of species in a particular community. The lower the value, the lower the diversity. A value of 0 indicates a community that only has one species.

The Shannon Equitability Index, also computed by Petri, is a way to measure the evenness of species in a community. The term “evenness” simply refers to how similar the abundances of different species are in the community.

…to interpret beta-diversity metrics?
-------------------------------------------
Beta diversity measures the species community differences between samples. Diversity calculations are based on sub-sampled data rarefied to the minimum read count of all samples. Petri calculates beta diversity distances using various methods and performs pairwise comparisons of groups of samples. Additionally, principle coordinates analysis (PCoA) plots are produced that can be visualized interactively in the pipeline reports. This calculations are based on a phylogenetic tree of all ASV sequences. Furthermore, statistical tests are performed to determine whether groups of samples are significantly different from one another.
The following methods are used to calculate community dissimilarities:
* Jaccard distance (qualitative)
* Bray-Curtis distance (quantitative)
* Unweighted UniFrac distance (qualitative, phylogenetic)
* Weighted UniFrac distance (quantitative, phylogenetic)
