# Combinatorial

This is the basic GMDH algorithm. It use an input data sample as a matrix containing _N_ levels (points) of observations over a set of _M_ variables. A data sample is divided into two parts. If regularity [criterion](http://www.gmdh.net/GMDH_var.htm#var) _AR(s)_ is used, then approximately two-thirds of observations make up the training subsample _N__A_, and the remaining part of observations (e.g. every third point with same variance) form the test subsample _NB_ . The training subsample is used to derive estimates for the coefficients of the polynomial, and the test subsample is used to choose the structure of the optimal model, that is one for which _the regularity criterion AR(s)_ takes on a minimal value:

![AR(s) = 1/N SUM (yi - yi(B))^2](http://www.gmdh.net/gif/ar_s.gif)

or better to use _the cross-validation criterion PRR(s)_ (it take into account all information in data sample and it can be computed without recalculating of system for each test point). Each point successively is taken as test subsample and then averaged value of criteria is used:

![PRR(s) = 1/N SUM (yi - yi(B))^2, Na=N-1, Nb=1](http://www.gmdh.net/gif/prr_s.gif)

To test a model for compliance with _the differential balance criterion_, the input data sample is divided into two equal parts. This criterion requires to choose a model that would, as far as possible, be the same on both subsamples. The balance criterion will yield the only optimal physical model solely if the input data are noisy.

To obtain a smooth [curve](http://www.gmdh.net/GMDH_typ.htm#fig1) of criterion value, which would permit one to formulate the exhaustive-search termination rule, the full exhaustive search is performed on models classed into groups of an equal complexity. The first layer uses the information contained in every column of the sample; that is the search is applied to partial descriptions of the form

![y=a0 + a1xi,  i=1,2,...,M](http://www.gmdh.net/gif/eq3.gif)

Non-linear members can be taken as new input variables in data sampling. The output variable is specified in this algorithm in advance by the experimenter. For each model system of Gauss normal equations is solved. At the second layer all models-candidates of the following form are sorted:

![y=a0 + a1xi + a2xj,  j=1,2,...,M](http://www.gmdh.net/gif/eq4.gif)

The models are evaluated for compliance with the criterion, and the procedure is carried on as long as the criterion [minimum](http://www.gmdh.net/GMDH_typ.htm#fig1) will be find. To decrease calculation time we recommend now to select at some (6-8) layer a set of the best F variables and use only them in further full sorting-out procedure. In this way number of input variables can be significantly increased. For [extended definition](http://www.gmdh.net/GMDH_var.htm) of the only optimal model the discriminating criterion is recommended.

![Combinatorial GMDH algorithm](http://www.gmdh.net/gif/fig_comb.gif)

_Figure:_ Combinatorial GMDH algorithm

         1 - data sampling;  
         2 - layers of partial descriptions complexing;  
         3 - form of partial descriptions;  
         4 - choice of best models set for structure identification;  
         5 - additional optimal model definition by [discriminating criterion](http://www.gmdh.net/GMDH_var.htm).

In this way it's not complex to realize this algorithm as program - solving of system of linear equations in loop is needed to realize. The sequence of the basic Combinatorial algorithm computation is described in [faq](http://www.gmdh.net/GMDH_sch.htm).

A salient feature of the GMDH [algorithms](http://www.gmdh.net/GMDH_alg.htm) is that, when they are presented continuous or noisy input data, they will yield as optimal some simplified _non-physical model_. In the case of discrete or exact data the exhaustive search for compliance with the precision criterion will yield what is called a (contentative) _physical model_, the simplest of all unbiased models. For noisy or short continuous input data, simplified Shannon non-physical models [12,25], received by GMDH algorithms, [prove](http://www.gmdh.net/GMDH_res.htm) more precise in approximation and for forecasting tasks. GMDH is the only way to get optimal non-physical models. Usage of sorting-out procedure guarantees selection of the best optimal model from all possible.