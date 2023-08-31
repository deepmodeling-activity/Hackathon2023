# Background of the question

AI4Science hardcore software development track is co-hosted by the DeepModeling open source community, Peking University Supercomputing Team, and Peking University Linux Club. The track encourages competitors to actively participate in the development of AI4Science's own tools. Students interested in high performance can perform high-performance optimization of specified software; Students interested in AI can reconstruct certain networks. Or maybe you find something else in the software that you want to improve on – in short, everything related to AI4Science is encouraged here!



**This track is divided into two parts: free proposition and fixed proposition. We especially encourage everyone to do free propositions, as long as any ideas related to AI4Science hardcore software development are very welcome; Of course, if you are overwhelmed by free propositions, you can also participate in the fixed proposition track and exert your creativity and talent under the designated proposition.**



## Free proposition

Runners on this track have full creative freedom and can choose any ideas related to AI4Science hardcore software development. Including but not limited to:

- **DeepModeling open source community software high-performance optimization**: Players can freely browse DeepModeling open source community related software and perform high-performance optimization for the parts they are interested in

- **DeepModeling Open Source Community Software Development**: Contestants can freely browse DeepModeling open source community software and develop things they are interested in. If you are not sure how to start, you are encouraged to check the relevant issues in the community project and solve the problems in the issues


Runners who choose this track need to submit their own proposals in the preliminary stage to describe their ideas and initially confirm the feasibility of the idea (the judging team will also give some constructive guidance suggestions to facilitate better implementation).



## Specify the question

### Question 1: High-performance cross-platform neighbor table algorithm implementation


- Neighborlist is of great significance in computational chemistry and has important applications in first-principles calculations, molecular dynamics simulation, and other fields. A proximity table is a data structure used to represent local relationships or proximity relationships between objects, records the indexes of adjacent particles within a certain truncation radius, and dynamically updates with the movement of atoms during simulation.Therefore, both the calculation of short-range interactions and the statistics of local structural properties directly depend on the proximity table. Therefore, the advantages and disadvantages of the algorithm established by the adjacent table will significantly affect the computing efficiency. We have come to realize that different scientific computing projects have common neighbor table requirements and can be abstracted into algorithms with explicit inputs and outputs. In addition, due to the complexity and specificity of scientific software, programs not only rely strongly on GPUs like deep learning frameworks, but also need to run on heterogeneous acceleration platforms of various architectures. Can we abstract the adjacent table and highly optimize it to form a highly optimized library from Python, C to CUDA, from x86, ARM to various heterogeneous acceleration platforms, so as to reduce repetitive development.


- Affected by the characteristics of computer hardware architecture, the implementation and performance of the adjacent table algorithm on different hardware platforms are significantly different. Therefore, when designing and optimizing the proximity table algorithm, specific implementations and optimizations must be made for various computer hardware architectures.In addition, the properties of simulated systems vary greatly, such as system size (from small to large systems), density distribution (from sparse to uniformly dense), and spatial distribution (from uniform to locally dense). Based on the characteristics of these different simulation systems, it is necessary to consider various factors when designing the adjacent table algorithm and optimization strategy to ensure the efficient performance of the algorithm in various scenarios.

#### Preliminary Round Goals

In the preliminary round, the contestants freely choose a programming language to implement the basic algorithm by learning several classic neighbor table algorithms. The test model and standard answers can be found in https://github.com/deepmodeling-activity/hackathon-test-cases

#### Final goals

In the final, based on the results of the preliminary round, the contestants can freely optimize, not only at the code level, but also propose new algorithms, and even implement more complex spatial decomposition and load balancing strategies. The final scoring will be carried out using the Peking University supercomputing platform, and the specific use method will be launched at a later stage.

#### Some tips

To evaluate the correctness and performance of the proximity table algorithm in various situations, we will provide a set of test cases (including model files) covering common simulation scenarios and test platforms for different hardware architectures. Contestants are free to choose their programming language, choose or design different neighbor table algorithms, and require faster calculations based on the accuracy of calculations as possible. Factors that may need to be considered are: system size, density distribution, spatial distribution, hardware architecture, IO and chunking, and so on.

#### Scoring criteria

The scoring will take into account the correctness of the algorithm and the speed of execution, and will be weighted according to the performance of the system and platform. The specific scoring weight details will be published in the scoring criteria document.

#### Final submission requirements

We will provide participants with servers on a variety of different platforms to test and evaluate the code they write. These platforms include CPU clusters based on x86 and ARM architectures, as well as GPU devices from Nvidia and AMD. To ensure the correctness of the code, we will provide a test framework that specifies the format and standards for code input and output. 

After completing their own code writing, participants need to integrate their algorithms into the test framework for corresponding testing. Through this process, we will be able to ensure that the participants' code meets the established performance and correctness requirements, thus guaranteeing the fairness and reliability of the competition.


### Question 2: ABACUS


- ABACUS is a high-performance density functional theory (DFT) software widely used in materials science calculations. In order to fully exploit its performance potential in real production applications, this competition aims to identify and optimize performance bottlenecks in software to improve computing efficiency, save computing resources and accelerate scientific research processes.


- ABACUS supports two different base groups, plane wave (PW) and numerical atomic orbital (LCAO), players need to study two different bases for a given (1. LCAO Base Group Study, 2. PW Base Group Study) to analyze performance hotspots and perform performance optimization freely.

#### Preliminary Round Goals

In the preliminary round, the contestants tested the given two examples, analyzed the performance hotspots, found the code corresponding to the performance hotspots, and analyzed and proposed preliminary performance optimization schemes. The scheme can freely use MPI optimization/OpenMP parallel optimization or algorithm optimization.

#### Final goals

In the final, the contestants competed in the performance optimization ranking based on the performance optimization plan proposed in the preliminary round. Potential performance optimization scenarios for the specified study: 1. LCAO Base Group Study, 2. PW base group study.

#### Study address:

https://github.com/deepmodeling/abacus-develop/tree/for_hackathon/hackathon_test_cases

#### Some tips for optimizing direction:

**LCAO base group study:**

1. Charge density symmetry algorithm in ABACUS;

2. MPI parallel algorithm for LCAO base group calculation density matrix in ABACUS.

**PW basis group study**: planar wave basis group uses iterative method to solve diagonalization, ABACUS currently supports CG and Davidson two diagonalization algorithms, which can:

1. Consider optimizing Davidson's algorithm (algorithm implementation level) or implementing other diagonalization algorithms (LOBPCG/PPCG/RMM-DIIS, etc.)

2. Consider using high-performance optimization schemes such as MPI/OpenMP/CUDA for CG or Davidson algorithms.

#### Scoring criteria

In order to fairly evaluate the effectiveness of performance optimization, all players will use the following optimized program: 

1. MPI multi-process parallelism, 

2. OpenMP multi-threaded parallelism, 

3. MPI OpenMP mixed parallelism. 

In terms of scoring criteria, we encourage the ultimate optimization of one hot function rather than moderate optimization of multiple hot functions, and the specific scoring weight details will be published in the scoring criteria document.


### Question 3: Long-range electrostatic action algorithm of point charge with automatic differentiation

- In systems under periodic boundary conditions, the proximity table method cannot effectively handle long-range electrostatic interactions due to the limitation of the minimum mirror convention. To solve this problem, the researchers developed long-range interaction algorithms such as Ewald, PME, PPPM, and others. As systems scale, it becomes important to optimize existing algorithms and develop new ones.In physics-based molecular force field DMFF, we treat various physical force fields and simulated computational flows as natural extensions of artificial intelligence models, using first-principles or experimental data as inputs, and using advanced machine learning algorithms to reverse correct and optimize physical model parameters. The key to achieving this is the automatic differentiation capability of the code. Therefore, under the premise of ensuring the automatic differentiation function, how to realize the efficient and advanced long-range electrostatic action algorithm has become an urgent problem to be solved.

#### Preliminary goal

In molecular dynamics simulations and quantum chemical calculations, accurate calculation of long-range electrostatic interactions is critical to correctly predict the properties and behavior of matter. In DMFF, we have initially implemented a long-range electrostatic interaction based on PME, which simultaneously supports multipolar electrostatic and dispersion interactions. Although the performance of PME methods has been greatly improved, there is still a computational efficiency bottleneck in large-scale calculations. The goal of this competition is to develop a new point charge electrostatic interaction algorithm to optimize the PME method and increase the calculation speed of the long-range action part while maintaining automatic differentiation capabilities. There are three optimization ideas:

1. Conduct a thorough analysis of existing PME algorithms to identify optimization opportunities at the JAX code level.

2. JAX provides the function of custom operators, allowing us to use C and CUDA to implement efficient operators. This provides another avenue for accelerated computing. For example, we can implement a custom operator for b-spline interpolation to improve computational efficiency. Specifically, we can implement the fusion function $$F(x)$$ as a custom operator, allowing it to be quickly computed on the GPU.

3. In addition to the PME algorithm, researchers have also proposed many advanced long-range action calculation algorithms in recent years, such as PMU and ScaFaCoS. Research and compare advanced electrostatic interaction algorithms, and implement advanced algorithms through JAX and CUDA operators to accelerate long-range interaction calculations to evaluate their potential in improving computational efficiency.

The method proposed by the contestant needs to accelerate the calculation of the long-range electrostatic interaction of point charges on the premise that it can be automatically differentiated. We will evaluate the performance of the proposed method in the DMFF framework to demonstrate that it can push the capabilities of DMFF to new heights. We will establish an efficient calculation method for electrostatic interactions to accelerate the calculation of long-range interactions in molecular dynamics simulations and quantum chemical calculations. This will provide researchers in related fields with better tools, thereby accelerating the process of scientific discovery. For test models and standard answers, please see https://github.com/deepmodeling-activity/hackathon-test-cases

#### some tips

In the preliminary round, after players learn and understand the principles of PME, they first implement the basic algorithm and integrate it into the provided test framework to evaluate its correctness and performance in various simulation scenarios. In the finals, based on the preliminary results, contestants can freely optimize, either at the code level or by proposing new algorithms to improve the accuracy and performance in various simulation scenarios.

To evaluate the correctness and performance of the long-range action algorithm under various circumstances, we will provide a set of test cases (including model files) covering common simulation scenarios and test platforms for different hardware architectures. Contestants are free to choose programming languages, choose or design different neighbor table algorithms independently, and are required to speed up calculations while making the calculations as accurate as possible. Factors that may need to be considered are: system size, density distribution, space distribution, hardware architecture, IO and partitioning, etc.

#### Scoring criteria

The scoring will comprehensively consider the correctness and execution speed of the algorithm, and perform weighted calculations based on the performance of the system and platform. The specific scoring weight rules will be announced in the scoring standard document.

#### Final Submission Requirements

We will provide entrants with servers on various platforms to test and evaluate the code they write. These platforms include CPU clusters based on x86 and ARM architectures, and GPU devices from Nvidia and AMD. In order to ensure the correctness of the code, we will provide a set of testing framework, which stipulates the format and standard of code input and output. After the contestants have finished writing their own codes, they need to connect their algorithms to the testing framework for corresponding testing. Through this process, we will be able to ensure that entrants' code meets established performance and correctness requirements, thus ensuring the fairness and reliability of the competition. Scoring will be done using the Peking University supercomputing platform, and the specific usage method will be released later.


### Question 4: DeepFlame—Neural network training for thermodynamic functions and transport parameters

- In combustion simulations, calculations to update thermodynamic states and transport parameters are a key step. In engineering applications, processes such as incident of working fluids, mixing, and combustion occur at least partially in a transcritical or supercritical state, which may render the ideal gas model commonly used in combustion simulations no longer applicable.Although the accuracy of combustion simulations can be improved by introducing formally more complex real fluid models, this will lead to an increase in simulation complexity and a significant increase in computation, and quantitatively, updating thermodynamic functions and transport parameters with real gas models will take up 50% to 75% of the total calculation time of the large eddy simulation.


#### Preliminary Round Goals

Machine learning is a potential regression tool for calculating real-world fluid thermodynamic functions and transport parameters. In this question, you need to train a neural network to calculate the thermodynamic functions and transport parameters of nitrogen. The input information of the network is the total enthalpy and pressure of the working fluid, and the output data is temperature, density, thermal diffusivity, viscosity, and isoenthalpy compression coefficient. We provide data at a pressure of 3.5-5 MPa and a temperature of 127-350K for training and testing your neural network.

#### Some tips

1. Data generation

	The dataset we provide is generated using a real fluid model based on the Peng-Robinson equation of state (available since Cantera version 2.6). If you need to generate more data for training and testing, you can install Cantera yourself and use the provided Python program to generate relevant data. For installation methods, please refer to the Cantera official website installation tutorial (https://cantera.org/install/conda-install.html#sec-install-conda) or DeepFlame installation documentation (https://deepflame.deepmodeling.com/en/latest/qs/install.html).

2. Open source framework

	Although there are many open source frameworks available, PyTorch is recommended for this test.

#### Scoring criteria

The performance evaluation of neural networks will integrate the following three aspects: (1) prediction accuracy (the more accurate the better), (2) the simplicity of the neural network design (the fewer parameters, the better), (3) encourage participants to independently expand the functions of the network on the basis of completing the basic requirements, such as network training for scenarios such as multi-component and wide working conditions.

#### Submission Requirements

- Neural networks are submitted in PT or PTH format

- Python scripts for neural network inference

- Introduction to the design and performance evaluation of neural networks in Word or PDF format, without restrictions on format or word count


### Question 5: DeepFlame—DeepFGM framework

- Flamelet Generated Model (FGM) is a combustion model that uses precomputed flames to represent the structure of flames in turbulent reactive streams. It provides an efficient calculation method for simulating complex combustion processes and is widely used in CFD simulation of combustion systems. Using the FGM model requires flame surface data calculated based on lookup tables.However, when there are many reaction components, and as the dimension of the variable increases, the memory occupied by the table used for calculation will be very large. DeepFGM, a turbulent combustion integral (TCI) model included in DeepFlame, will generate a tailored neural network based on every physical quantity used in the calculations in the table, ultimately reducing the overall memory footprint.

#### Preliminary goal

In this test, we will provide training data sets and their formats, as well as some source code used for training for players' reference. Contestants need to use the provided code and resources to train a network on the chemical reaction rate ($$w_c$$). After obtaining the trained network, the contestants will perform Sandia-D calculation examples in DeepFlame.

#### some tips

1. Network training

	The network structure used is based on the PyTorch framework. The structure of the network is defined in RES.py. Players need to complete the code in trian_PES.py according to the comments to implement network training, and save the network results in pth format.

2. Case verification

	After the network training is completed, we can replace the network used in DeepFlame's Sandia-D to verify the later results. For specific operation procedures, it is recommended to refer to the content about DeePFGM in the DeepFlame training camp and related websites.

#### Scoring criteria

The performance of the neural network will be based on two aspects: (1) prediction accuracy of table data (2) later results

#### Submit a request

- Neural networks are submitted in pth format
- Complete train_RES.py file

[Click here for detailed content](https://dptechnology.feishu.cn/docx/QGfHdUHrEowMi4xYkJuchN9Rnbh?from=from_copylink)



