# General Description of GMDH

There were published many papers and books devoted to the Group Method of Data Handling theory and its applications. The GMDH can be considered as further propagation of inductive self-organizing methods to the solution of more complex practical problems. It solves the problem of how to handle data samples of observations. The goal is to get mathematical model of the object (the problem of identification and pattern recognition) or to describe the processes, which will take place at object in the future (the problem of process forecasting). GMDH solves, by sorting-out procedure, the multidimensional problem of model optimization:

![g=minCR(g), CR(g)=f(P,S,z,T,V)](http://www.gmdh.net/gif/eq1.gif)

where: _G_ - set of considered models; _CR_ is an external criterion of model _g_ quality from this set; _P_ - number of variables set; _S_ - model complexity; _z2_ - noise dispersion; _T_ - number of data sample transformation; _V_ - type of reference function. For definite reference function, each set of variables corresponds to definite model structure _P = S_. Problem transforms to much simpler one-dimensional

![CR(g)=f(S)](http://www.gmdh.net/gif/eq2.gif)

when _z2_= const, _T_ = const, and _V_ = const.

Method is based on the sorting-out procedure, i.e. consequent testing of models, chosen from set of models-candidates in accordance with the given criterion. Most of GMDH algorithms, use the polynomial reference functions. General connection between input and output variables can be expressed by Volterra functional series, discrete analogue of which is Kolmogorov-Gabor polynomial:

![y=a0 + SUM ai xi + SUM SUM aij xi xj + SUM SUM SUM aijk xi xj xk](http://www.gmdh.net/gif/eq3polyn.gif)

where _X(x1,x2,...,xM,);_ - input variables vector; _A(a1,a2,...,aM,);_ - vector of coefficients or weights;

Components of the input vector _X_ can be independent variables, functional forms or finite difference terms. Other non-linear reference functions, such as difference, probabilistic, harmonic, logistic can also be used. The method allows to find _simultaneously_ the structure of model and the dependence of modelled system output on the values of most significant inputs of the system.

The GMDH theory solve the problems of:

- long-term forecasting [[3,18](http://www.gmdh.net/GMDH_ref.htm)];
- short-term forecasting of processes and events [2];
- identification of physical regularities;
- approximation of multivariate processes;
- physical fields [extrapolation](http://www.gmdh.net/GMDH_osa.htm) [4];
- data samples [clusterization](http://www.gmdh.net/GMDH_occ.htm) [5];
- [pattern recognition](http://www.gmdh.net/GMDH_occ.htm) in the case of continuous-valued or discrete variables;
- diagnostics and recognition by probabilistic sorting-out algorithms [6];
- [decision support](http://www.gmdh.net/GMDH_slp.htm) after "what-if" scenario and vector process normative forecasting [7];
- modelless processes forecasting using [analogues complexing](http://www.gmdh.net/GMDH_ana.htm) [8];
- self-organization of [twice-multilayered neuronets](http://www.gmdh.net/GMDH_tmn.htm) with active neurons [9,10].
    
    In [12] were obtained the theoretical grounds of GMDH effectiveness as adequate method of robust forecasting models construction, essence of which consists of automatically generation of models in given class by sequential selection of the best of them by criteria, which implicitly by sample dividing take into account the level of indeterminacy.
    
    Since 1968 a big number of GMDH technique [implementations](http://www.gmdh.net/GMDH_exa.htm) for modeling of economic, ecological, environmental, medical, physical and military objects were done in several countries.  
    Some outdated approaches are used in USA by Barron Associates Co. in "ASPN-II", AbTech Corp. in "ModelQuest" (AIM), by Ward Systems Group, Inc. in "NeuroShell2", and DeltaDesign Software in "SelfOrganize!" commercial [software](http://www.gmdh.net/GMDH_sof.htm) tools.
    
    Self-organizing modeling is based on [statistical learning networks](http://www.gmdh.net/GMDH_nn.htm), which are networks of mathematical functions that capture complex, non-linear relationships in a compact and rapidly executable form. Such networks subdivide a problem into manageable pieces or nodes and then automatically apply advanced regression techniques to solve each of these simpler problems.
    
    **_Special GMDH peculiarities_**
    
    The main peculiarity of GMDH algorithms is that, when it uses continuous data with noise, it selects as optimal simplified [non-physical model](http://www.gmdh.net/GMDH_typ.htm). Only for accurate and discrete data the algorithms point out so-called physical model - the most simple optimal, from all unbiased models. It is proved the [convergence](http://www.gmdh.net/GMDH_res.htm) of multilayered GMDH algorithms [25] and it is proved that shortened non-physical [model is better](http://www.gmdh.net/GMDH_res.htm) than full physical model on error criterion (for noisy and continuous data for prediction and approximation solving, more simplified Shennon's non-physical models become more accurate [12]). It can be noted, that this conclusion has place in model selection on the basis of models entropy maximization (Akaike approach), in average risk minimizing (Vapnik approach) and in another modern approaches. The only way to get non-physical models is to use sorting-out GMDH algorithms. Usage of sorting-out procedure guarantees selection of the best optimal model from all possible. Regularity of optimal structure of forecasting models change in dependence on general indexes of data indeterminacy (noise level, data sample length, design of experiment, number of informational variables) was shown in [24,25,27].
    
    The special peculiarities of GMDH are following :
    
    1. _**External supplement:**_Following S.Beer work [13], only the [external criteria](http://www.gmdh.net/GMDH_typ.htm), calculated on new independent information,can produce the minimum of sorting-out characteristic. Because of this data sampling is divided into parts for model construction and evaluation.
    2. _**Freedom of choice:**_Following D.Gabor work [14], in multilayered GMDH algorithms are to be conveyed from one layer to the next layer not all but F best results of choice to provide "freedom of choice"
    3. _**The rule of layers complication:**_Partial descriptions (forms of a mathematical description for iteration) should be simple, without quadratic members in them;
    4. _**Additional model definition:**_In cases, when the choice of optimal physical model is difficult, because of noise level or oscillations of criterion minima characteristic, auxiliary [discriminating criterion](http://www.gmdh.net/GMDH_var.htm) is used [15]. The choice of the main criterion and constrains of sorting-out procedure is the main heuristic of GMDH;
    5. All algorithms have _**multilayered structure**_ and parallel computing can be implemented for their realization.
    6. All questions that arise about type of algorithm, criterion, variables set choice should be solved by _**minimal value**_ of external criterion.
    
    The main [criteria](http://www.gmdh.net/GMDH_var.htm) proposed are: cross-validation _PRR(s),_ regularity _AR(s)_ and balance of variables criterion _BL(s)._ Estimation of their effectiveness (investigation of noise immunity, optimality and adequateness) and their comparison with another criteria was done in detail in [24,25,26,15]. The conditions, under which GMDH algorithm produces the minimum of characteristics are following:
    
    1. criterion of model choice is to be _external_, based on additional fresh information, which was not used for model construction;
    2. the data sample is not to be too long. Such data sample produce the same model of usual regression analysis for exact data;
    3. when difference type balance criterion BL(s) is used, small noise is necessary or the variables in the data sample should not be exactly measured [16].
    
    Difference of the GMDH algorithms from another algorithms of structural identification and best regression selection algorithms consists of three main peculiarities:
    
- usage of _external criteria_, which are based on data sample dividing and are adequate to problem of forecasting models construction, by decreasing of requirements to volume of initial information;
- more _diversity_ of structure generators: usage like in regression algorithms of the ways of full or reduced sorting of structure variants and of original multilayered (iteration) procedures;
- better level of _automatization_: there are needed to enter initial data sample and type of external criterion only;
- automatic adaptation of optimal model complexity and external criteria to level of noises or statistical violations - effect of noiseimmunity cause _robustness_ of the approach;
- implementation of _principle of inconclusive decisions_ in process of gradual models complication.