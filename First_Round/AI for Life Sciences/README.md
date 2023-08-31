# Question background

Drug discovery utilizes a wide range of technologies to guide novel disease-relevant chemical entities into the clinical setting to address unmet patient needs. While many traditional technical methods are used in "wet" experiments, the development and application of computational methods has been widely used in recent decades. In recent years, the revival of artificial intelligence, especially machine learning methods, has accelerated the drug discovery process and improved the efficiency of preclinical development.


The AI ​​for Life Sciences track encourages contestants to use AI4Science related software tools to try to solve problems of general concern in the field of biomedicine. It is hoped that the contestants can propose solutions to the existing application scenarios in the field of biomedicine, such as various property predictions, target predictions, combination mode exploration and molecular generation and other practical scenarios; at the same time, contestants are encouraged to try to use different software and tools, such as Uni -Mol explores a certain field in depth - in short, as long as it is related to AI4Science and biomedicine, all explorations are encouraged here!


**The questions on this track are divided into two parts: free questions and fixed questions. We especially encourage everyone to do free propositions, as long as any ideas related to biomedicine are very welcome; of course, if you are at a loss for free propositions, you can also participate in the fixed proposition track and use your creativity and talent under the specified proposition. **

## 1. Free proposition

Contestants in this track have full creative freedom, and can choose issues that everyone cares about in the field of biomedicine, and use AI4Science related algorithms and tools to explore.


Contestants who choose this track need to submit their own proposals in the preliminary stage to describe their ideas and initially confirm the feasibility of the idea (the review team will also give some constructive guidance and suggestions to facilitate better implementation).

## 2. Reference questions

#### Question background description


Quantitative structure-activity relationship (QSAR) is to study the relationship between the activity, toxicity, pharmacokinetic properties of a group of compounds and their structure (structural), physicochemical properties (physicochemical), topological structure (topological), etc. relationship, and a research method characterized by a mathematical statistical model. In recent decades, with the accumulation of a large amount of drug-related data, QSAR-based drug design and discovery methods have shifted to utilizing large-scale data sources and molecular descriptor libraries, using more machine learning algorithms to automatically generate predictive models. However, the accuracy of QSAR models is still largely limited by the molecular representation methods. Specifically, molecular representation methods include machine-readable molecular representation, string representation, chemical table representation, feature-based representation, etc. Commonly used methods generally rely on 2D, which makes the model unable to learn ligand molecules in three-dimensional space information.


Uni-Mol is a versatile framework for 3D molecular representation, which directly utilizes the 3D information of molecules during training, greatly enhancing the expressiveness and applicability of the model. Uni-Mol consists of two models with the same architecture: one is a molecular pre-training model trained on a dataset of 209 million molecular conformations; the other is a pocket pre-training model on a dataset of 3 million protein pockets. training on the data set. In addition, the model architecture of Uni-Mol satisfies variability such as SE(3). In downstream experiments, Uni-Mol not only achieves state-of-the-art performance in previously studied molecular property prediction tasks, but also excels in a range of downstream tasks related to drug discovery, especially those involving highly correlated 3D information. related tasks. Examples of these tasks include high-precision molecular conformation generation, protein-ligand binding conformation prediction, and protein pocket property prediction. Uni-Mol has demonstrated superior performance and strong generalization capabilities in tasks such as small molecule property prediction, protein target prediction, protein-ligand complex conformation prediction, and quantum chemical property prediction, surpassing existing solutions .


Now, we encourage contestants to further explore using the 3D molecular representation framework Uni-Mol to solve more practical problems in drug design and discovery scenarios. The competition questions are as follows.


- ** Question 1: Protein Target Prediction **


The identification of physical interactions between drug candidates and target proteins is a critical step in drug discovery. Statistically, current knowledge about the drug-protein space is rather limited, so new approaches are needed to expand our understanding. Published studies have shown that protein target prediction is an open problem that requires not only new algorithms but also new representations to elucidate the unexplored drug-target interaction (DTI) space and other related tasks, typical examples Includes kinase profile prediction. 

In the preliminary competition, we encourage contestants to propose solutions based on the 3D molecular representation Uni-Mol framework we developed. Uni-Mol combines molecular and pocket pre-trained models, learns scoring functions based on distance matrices, and then samples and optimizes the complex conformation to predict protein-ligand binding.


- ** Question 2: Property prediction **


The goal of molecular property prediction is to learn a generalizable model from a set of known compounds that can be applied to new molecules. This usually involves systematically designing or selecting descriptors as input for supervised machine learning model training. For example, Dahl et al. and Mayr et al. reported successful ADMET predictions using deep neural networks (DNNs) on the tox21 challenge dataset. Uni-Mol has also performed experiments in the important task of molecular property prediction, which has attracted a lot of attention from artificial intelligence (AI) practitioners. It demonstrates superior performance compared to state-of-the-art (SOTA) methods on various properties and datasets. In the preliminary competition, we encourage contestants to develop a molecular property prediction model for a specific scenario based on Uni-Mol, or to propose a better general solution.


**[Click here to view the detailed competition content](https://dptechnology.feishu.cn/docx/S08Hddzo7oxsjsx6chlc4BAinEf?from=from_copylink)
