# Background of the question

AI4Science hardcore software development track is co-hosted by the DeepModeling open source community, Peking University Supercomputing Team, and Peking University Linux Club. The track encourages competitors to actively participate in the development of AI4Science's own tools. Students interested in high performance can perform high-performance optimization of specified software; Students interested in AI can reconstruct certain networks. Or maybe you find something else in the software that you want to improve on – in short, everything related to AI4Science is encouraged here!



**This track is divided into two parts: free proposition and fixed proposition. We especially encourage everyone to do free propositions, as long as any ideas related to AI4Science hardcore software development are very welcome; Of course, if you are overwhelmed by free propositions, you can also participate in the fixed proposition track and exert your creativity and talent under the designated proposition.**



## Free proposition

Runners on this track have full creative freedom and can choose any ideas related to AI4Science hardcore software development. Including but not limited to:

- **DeepModeling open source community software high-performance optimization**: Players can freely browse DeepModeling open source community related software and perform high-performance optimization for the parts they are interested in

- **DeepModeling Open Source Community Software Development**: Contestants can freely browse DeepModeling open source community software and develop things they are interested in. If you are not sure how to start, you are encouraged to check the relevant issues in the community project and solve the problems in the issues


Runners who choose this track need to submit their own proposals in the preliminary stage to describe their ideas and initially confirm the feasibility of the idea (the judging team will also give some constructive guidance suggestions to facilitate better implementation).



## Specify the question

**Question 1: High-performance cross-platform neighbor table algorithm implementation**


- Neighborlist is of great significance in computational chemistry and has important applications in first-principles calculations, molecular dynamics simulation, and other fields. A proximity table is a data structure used to represent local relationships or proximity relationships between objects, records the indexes of adjacent particles within a certain truncation radius, and dynamically updates with the movement of atoms during simulation.

Therefore, both the calculation of short-range interactions and the statistics of local structural properties directly depend on the proximity table. Therefore, the advantages and disadvantages of the algorithm established by the adjacent table will significantly affect the computing efficiency. We have come to realize that different scientific computing projects have common neighbor table requirements and can be abstracted into algorithms with explicit inputs and outputs. 

In addition, due to the complexity and specificity of scientific software, programs not only rely strongly on GPUs like deep learning frameworks, but also need to run on heterogeneous acceleration platforms of various architectures. Can we abstract the adjacent table and highly optimize it to form a highly optimized library from Python, C to CUDA, from x86, ARM to various heterogeneous acceleration platforms, so as to reduce repetitive development.


- Affected by the characteristics of computer hardware architecture, the implementation and performance of the adjacent table algorithm on different hardware platforms are significantly different. Therefore, when designing and optimizing the proximity table algorithm, specific implementations and optimizations must be made for various computer hardware architectures.

In addition, the properties of simulated systems vary greatly, such as system size (from small to large systems), density distribution (from sparse to uniformly dense), and spatial distribution (from uniform to locally dense). Based on the characteristics of these different simulation systems, it is necessary to consider various factors when designing the adjacent table algorithm and optimization strategy to ensure the efficient performance of the algorithm in various scenarios.


**Question 2: ABACUS**


- ABACUS is a high-performance density functional theory (DFT) software widely used in materials science calculations. In order to fully exploit its performance potential in real production applications, this competition aims to identify and optimize performance bottlenecks in software to improve computing efficiency, save computing resources and accelerate scientific research processes.


- ABACUS supports two different base groups, plane wave (PW) and numerical atomic orbital (LCAO), players need to study two different bases for a given (1. LCAO Base Group Study, 2. PW Base Group Study) to analyze performance hotspots and perform performance optimization freely.


**Question 3: Long-range electrostatic action algorithm of point charge with automatic differentiation**

- In systems under periodic boundary conditions, the proximity table method cannot effectively handle long-range electrostatic interactions due to the limitation of the minimum mirror convention. To solve this problem, the researchers developed long-range interaction algorithms such as Ewald, PME, PPPM, and others. As systems scale, it becomes important to optimize existing algorithms and develop new ones.

In physics-based molecular force field DMFF, we treat various physical force fields and simulated computational flows as natural extensions of artificial intelligence models, using first-principles or experimental data as inputs, and using advanced machine learning algorithms to reverse correct and optimize physical model parameters. 

The key to achieving this is the automatic differentiation capability of the code. Therefore, under the premise of ensuring the automatic differentiation function, how to realize the efficient and advanced long-range electrostatic action algorithm has become an urgent problem to be solved.


**Question 4: DeepFlame—Neural network training for thermodynamic functions and transport parameters**

- In combustion simulations, calculations to update thermodynamic states and transport parameters are a key step. In engineering applications, processes such as incident of working fluids, mixing, and combustion occur at least partially in a transcritical or supercritical state, which may render the ideal gas model commonly used in combustion simulations no longer applicable.

Although the accuracy of combustion simulations can be improved by introducing formally more complex real fluid models, this will lead to an increase in simulation complexity and a significant increase in computation, and quantitatively, updating thermodynamic functions and transport parameters with real gas models will take up 50% to 75% of the total calculation time of the large eddy simulation.


DeepFlame—DeepFGM framework

- Flamelet Generated Model (FGM) is a combustion model that uses precomputed flames to represent the structure of flames in turbulent reactive streams. It provides an efficient calculation method for simulating complex combustion processes and is widely used in CFD simulation of combustion systems. Using the FGM model requires flame surface data calculated based on lookup tables.

However, when there are many reaction components, and as the dimension of the variable increases, the memory occupied by the table used for calculation will be very large. DeepFGM, a turbulent combustion integral (TCI) model included in DeepFlame, will generate a tailored neural network based on every physical quantity used in the calculations in the table, ultimately reducing the overall memory footprint.

[Click here for detailed content] (https://dptechnology.feishu.cn/docx/QGfHdUHrEowMi4xYkJuchN9Rnbh?from=from_copylink)



