### Post-publication modifications

Fixed bug where the presence of a polytomy at a two-mutation clade was determined by counting the number of sub-clades branching from an unrelated one-mutation clade

Added data from zoonodo (clade analysis results and FAVITES summary results) to faciliate testing, and adapted imports and paths so that the corrected notebooks/cladeAnalysis.pynb should run on a standard SciPy setup.

#### WORK IN PROGRESS - SEE NOTE AT BOTTOM
Added upper bound for Bayes' factors. The original analysis implicitly assumes that stable coalescents of two successful introductions with basal polytomies are always either siblings on one-mutation branches from an MRCA, or an MRCA ancestor and a descendant on a two mutation branch from that ancestor. This assumption requires the number of mutations between the MRCA and one succesful introduction to depend on the number of mutations between the MRCA and the stable coalescent of the other successful introduction, which is unreasonable. This assumption also requires the number of mutations between the MRCA and an introduction to anticipate subsequent mutations between that introduction and the stable coalescent (to the extent that some subsequent mutations become reversions), which is also unreasonable. To avoid this, it is instead assumed that introductions are randomly drawn, with replacement, from a pool of possible source taxa. In order to calculate the upper bound for the Bayes' factors, the pool of possible source taxa is set to that most favourable for two-introduction model, namely an MRCA ancestor and a descendant on a two mutation branch from that ancestor, in equal proportions.

Testing of the phylogenies against the `CC` and `AB` topologies is not yet consistent for the different hypotheses, because cladeAnalysis.py classifies clades in a way that does not seem consistent with the paper, the supplementary materials and common sense (e.g. one-mutation clades include all clades on branches with one OR MORE clades from the stable coalescent). Work is deferred until proper classification is established.


### Supplementary code for:

J. E. Pekar, A. Magee, E. Parker, N. Moshiri, K. Izhikevich, J. L. Havens, K. Gangavarapu, L. M. Malpica Serrano, A. Crits-Christoph, N. L. Matteson, M. Zeller, J. I. Levy, J. C. Wang, S. Hughes, J. Lee, H. Park, M.-S. Park, K. Ching Zi Yan, R. T. Pin Lin, M. N. Mat Isa, Y. M. Noor, T. I. Vasylyeva, R. F. Garry, E. C. Holmes, A. Rambaut, M. A. Suchard, K. G. Andersen, M. Worobey, J. O. Wertheim, "The molecular epidemiology of multiple zoonoses of SARS-CoV-2".
