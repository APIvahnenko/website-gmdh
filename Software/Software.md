# Software

There are several software packages, which implement GMDH [algorithms](http://www.gmdh.net/GMDH_alg.htm) as a further development of software from Glushkov Institute of Cybernetics and _ASPN-II_ (Algorithm for Synthesis of Polynomial Networks) from Barron Associates Co., USA.

GMDH brings high-end modeling capabilities on desktop without the need of being an expert in modeling since it will learn completely unknown relationships between outputs and inputs of any given system in an evolutionary way from a very simple organization to an optimal complex one by itself. The main advantages of software which realize inductive approach are:

- Only minimal, uncertain a priori information about the system is required. That means, even if you are not an expert in modeling, data analysis or designing a neural network you will be able to model, analyse and predict very complex objects of nearly any kind of system.
- Very fast and effective learning process for ordinary PC's. That means, you can solve problems on your desktop in a reasonable time which you may have never thought about before.
- Modeling on very short and noisy data samples. That means, you can deal with a problem as is and don't have to construct artificial conditions for your modeling method to get it work.
- Output of an optimal complex and cross-validated model. That means, you commonly can expect to get a model which is robust, as simple as possible and not overfitted. Overfitted models are not able to predict variables due to their reflection of random relationships between variables.
- Output of an analytical model as a explanation component. That means, you can evaluate the analytical model to interpret the obtained results immediately after modeling. You don't have to guess why results are as they are.

GMDH module of _NeuroShell2_ tool developed by Ward Systems Group, Inc. use partial polynomial optimization for network structure construction. _ModelQuest_ software from AbTech Corp. realise so-called abductive polynomial GMDH networks. Unfortunately the recent developments and modern GMDH experience were not yet realized in the software considered above. They turn into account over-complicated models using heuristics, which contradicts to self-organizing nature of the approach. Often is used an [internal criteria](http://www.gmdh.net/GMDH_typ.htm) and therefore this software products are successive in the case when dispersion of noise in data is small or data sample is long. In opposite case more effective are original inductive GMDH algorithms based on external criteria usage.

Now the most devised software developed under this approach is [KnowledgeMiner](http://www.knowledgeminer.net) developed by Frank Lemke for Apple computers. This modeling tool realizes [twice-multilayered neuronets](http://www.gmdh.net/GMDH_tmn.htm) with active neurons, optimizing the structure of every neuron ([COMBI](http://www.gmdh.net/GMDH_com.htm)) and adaptively synthesizing the network structure ([MIA](http://www.gmdh.net/GMDH_mia.htm)). It can be used for generation of systems of equations ([OSA](http://www.gmdh.net/GMDH_osa.htm)) also.

The [AutoNet](http://peakconsulting.com/prod01.htm) is Excel-based application with open VBA code from [Peak Consulting Inc.](http://peakconsulting.com) This is GMDH-type neural network program with a self-designing architecture.

The main [SKAT](http://www.megaputer.com/products/pa/algorithms/fl.php3) and [Polynet Predictor](http://www.megaputer.com/products/pa/algorithms/pp.php3) module in the PolyAnalyst software from Megaputer Intelligence use GMDH approach for knowledge discovery and data mining. Their main SKAT module use inductive GMDH-type technique, with sorting of ratio-polynomial models.

Fuzzy GMDH is used in [DataX](http://www.zaptron.com/datax/#Data AnalysisCapabilities) data mining software from Zaptron Systems, Inc.

[NeuroNet GMDH for Java](http://www.unet.univie.ac.at/~a9404026/andy/neuronet.htm) - artificial GMDH-like network written entirely in Java is available from Andy Zelezny's homepage. It's not based on inductive principles unfortunately.

Software which realize inductive approach is not complex. That's why there are a lot of "raw" programs-prototypes, written by many investigators throughout the world, which realize simplified multilayered GMDH algorithms. Some of them are listed [here](http://www.gmdh.net/GMDH_lin.htm#soft).  
We ask all who have such software to contact with us, your work may be helpful for another researchers.

In Russia there were created three different commercial mainframe packages of Applied Programs (PPP) in NPO "TsentrProgramSystem" in Tver. It were widely used in many organizations mainly for complex statistical analysis of time series using GMDH.

Rather good old implementation of multilayered GMDH algorithm _Astrid_ for DOS only is available from our Glushkov Cybernetic Center. .

There is still necessity in further development of GMDH software under Windows OS in which modern GMDH experience will be used. For broadening of functional software possibilities the construction principle of multi-functional algorithmic modules is proposed in [[28](http://www.gmdh.net/GMDH_ref.htm)]: generalized structure generator, generalized model, generalized criterion. This modules under supervision of coordinating monitor gives broad spectrum of known methods of structural identification, regression construction and restoration of dependencies.