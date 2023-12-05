# GMDH algorithms and algorithms of GMDH type

It's necessary to make difference between the original "GMDH algorithms" and the "algorithms of GMDH type" [11]. The first ones - work using the minimum of an external criterion (see figure) and therefore realise objective choice of optimal model. This original GMDH technique is based on inductive approach: optimal models are founded by sorting-out of possible variants and evaluated by [external criterion](http://www.gmdh.net/GMDH_var.htm#extcr). It is calculated on separate part of data sample which is not used for model creation. That model is better which leads to minimal value of criterion. To make objective choice, selection is done without thresholds or coefficients in criterion. We recommend to calculate criteria two times: first to find the best models at each layer of selection for structure identification and second time to find the optimal model. Selection procedure is stopped when minimal criterion value is reached.

Second is GMDH type algorithms - work on characteristic, expressed by words: "more complex is the model - more accurate it is". For it necessary to put definite threshold or to point out coefficients of weight for the members of the internal criterion formula, to find optimal model out in a some subjective way. But real problems usually are presented by short or noised data samples. Unfortunately, in almost all GMDH type software (ModelQuest, NeuroShell) and research works in USA and Japan this deductive approach is used, which is not effective for such kind of data.

  

![CR=f(S) dependence](http://www.gmdh.net/gif/fig_crit.gif)

Fig.1. External accuracy criterion minima values plotted against complexity  
of model structure _S_ for different noise variance ![ksi^2](http://www.gmdh.net/gif/ksi2.gif).

LCM - locus of criterion minima line;  
--- - model choice by criterion minimum;  
-··- - model choice by "left corner rule".

The inductive approach does not eliminate the experts or take them away from the computer, but rather assigns them a special position. Experts indicate the selection criterion of a very general form and interpret the chosen models. They can influence the result of modeling by formulating new criteria. Computer becomes an objective referee for scientific controversies, if criteria ensemble is coordinated between experts, which take part in discussion.

The human element often involves errors and undesired decisions. Objective choice of optimal model by minimum of external criterion characteristic in actual GMDH algorithms often contradicts with the opinion of investigator. Objective algorithms gives [possibility to realize](http://www.gmdh.net/GMDH_ai.htm) real artificial intelligence.