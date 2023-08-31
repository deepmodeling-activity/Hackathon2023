## Background of the final question

In this track, we encourage players to explore and extend the application of AI4Science in different scenarios, using but not limited to DeePMD-kit, ABACUS, DMFF, Uni-Mol, DeepFlame and other software.

This track is divided into two parts: free proposition and fixed proposition. We especially encourage everyone to do free propositions, as long as any ideas related to AI4Science are very welcome; Of course, if you are overwhelmed by free propositions, you can also participate in the fixed proposition track and exert your creativity and talent under the designated propositions.

## Free Questions

Runners on this track have full creative freedom and can choose any idea related to AI4Science. Including but not limited to:

- **Scenario exploration**: Use AI4Science's algorithms or software to explore some practical application scenarios

- **Workflow development**: Develop AI4Science workflows around some common scenarios (dflow is recommended to build related workflows, but it is not mandatory)

Runners who choose this track need to submit their own proposals in the preliminary stage to describe their ideas and initially confirm the feasibility of the idea (the judging team will also give some constructive guidance suggestions to facilitate better implementation).

### Final Goal

Contestants complete the final project based on the proposal content of the preliminary round.

### Submission Requirements

Submit the full content as a Bohrium Notebook or as an attachment

## Reference Topics

### Topic 1: Uni-Mol X: Using pre-trained models to explore new applications of 3D molecular representation learning

Pre-trained models are taking multiple domains by storm. Extracting representation information from large-scale unlabeled data and then performing supervised learning on small-scale labeled downstream tasks is becoming a factual solution in many fields. How are pre-trained models built and applied in the field of drug and materials design? In May 2022, Uni-Mol, an open-source general molecular representation learning framework based on molecular three-dimensional structure, was officially published, and the paper was accepted by ICLR 2023. Unlike previous frameworks for molecular characterization based on 1D sequence or 2D map structures, Uni-Mol directly utilizes the 3D structure of molecules as model input. Uni-Mol has superior performance and strong model generalization ability, which surpasses existing solutions in small molecule property prediction, protein target prediction, protein-ligand complex conformation prediction, quantum chemical property prediction, MOF material adsorption performance prediction, OLED luminescent material performance prediction and other tasks.

#### Preliminary Round Goals

Your task is to use the Uni-Mol framework to develop a new downstream application that effectively leverages Uni-Mol's 3D molecular representation capabilities and pre-training features. You can choose to solve a specific problem, such as predicting molecular properties, generating new molecular structures, or developing a new tool or service.

#### Some tips

In this challenge, we invite you to explore new applications of molecular representation learning using Uni-Mol, a universal molecular representation learning framework based on molecular three-dimensional structures, combined with your own innovative thinking (i.e. "X"). You can choose any field of interest you in, including but not limited to drug design, materials science, environmental science, etc. The following two examples can give you some inspiration.

#### Reference Case

Uni-Mol properties predict the dielectric constant of the electrolyte molecule in practice-regression mission: https://nb.bohrium.dp.tech/detail/1033

Uni-Mol Nature Prediction Practice-Classification Task-Blood-Brain Barrier Permeability: https://nb.bohrium.dp.tech/detail/1034

#### Final Requirements

In this challenge, we invite you to use Uni-Mol, a general molecular representation learning framework based on molecular three-dimensional structure, combined with your own innovative thinking (i.e. "X"), to modify and improve Uni-Mol architecture, expand Uni-Mol application scenarios, and achieve more advanced applications.

Based on the proposal of the preliminary round, while completing the content of the work, the contestants can optimize the Uni-Mol tool based on the Uni-Mol requirements, and we give the following optimization suggestions for reference:

1. In addition to structural information, consider other information, and train specific environment-related models by taking some environmental variables such as temperature and pressure as inputs. For example, Uni-MOF has been modified from Uni-Mol to predict the ability of MOFs to adsorb gas pairs at specific temperatures and pressures.

2. Current 3D representations of Uni-Mol do not take periodicity into account. There is no way to get good results when dealing with some cyclical systems. On the basis of the previous input, periodic constraints are introduced, and periodic information is obtained after adjusting the structure of the model, so as to realize Uni-Mol's support for periodic systems.

3. Uni-Mol's current pre-training model focuses more on the general type, and these molecules have their own proprietary characteristics in some functional molecule application scenarios (such as OLED molecules, electrolyte molecules). For specific scenarios, you can re-build a targeted pre-training model, train a dedicated pre-trained model with specific data, or redesign a targeted pre-training task.

4. There is still room for optimization in the current performance of Uni-Mol, for example, by iteratively optimizing the initial conformation to its equilibrium conformation, and the optimized conformation is further used to predict QC characteristics, Uni-Mol further improves the accuracy of Uni-Mol in quantifying attribute prediction. More methods can be tried to further optimize the performance of Uni-Mol, improve training speed and prediction accuracy.

#### Ref：

Uni-MOF：https://chemrxiv.org/engage/chemrxiv/article-details/6447d756e4bbbe4bbf3afeaa

OLED：https://chemrxiv.org/engage/chemrxiv/article-details/6412d142aad2a62ca1d86505

Uni-Mol ：https://arxiv.org/abs/2303.16982

#### Submission Requirements

Submit the full content as a Bohrium Notebook or as an attachment

### Topic 2: dflow X: Developing AI4Science cloud-native workflows

dflow is an open-source Python development framework for scientific computing workflow developers using the cloud-native project Argo as a workflow engine.

#### Preliminary Round Goals

In the scientific computing scenario or your scientific research work, you must have encountered some needs for automated workflows, implement a simple workflow under the framework and specifications of dflow, or a part of a complex workflow (such as implementing several OPs), run through on the workflow platform workflows.deepmodeling.com, and initially experience the connotation of cloud native, automation, observability, and reproducibility

#### Some tips

Here are some examples to help you get through the dflow workflow.

#### Reference Case

Function OP：https://bohrium.dp.tech/notebook/90e75093e3e64c0a99521f1be6dc3346

Class OP：https://bohrium.dp.tech/notebook/b0897299e4d4466a8d64d2538de1bf26

Condition：https://bohrium.dp.tech/notebook/dde8e85b376e41fba6f125d5abf1f635

Slices：https://bohrium.dp.tech/notebook/644edc260d8746159d9ecd48bfa1ca76

Recursion：https://bohrium.dp.tech/notebook/aa39c7c1ca0b48d4a85cd4032aafceb5

Reuse：https://bohrium.dp.tech/notebook/e6bfb5f3efda4febba2ba696c9838557

Dispatcher: https://bohrium.dp.tech/notebook/9840681dced74568b64f3449581e6bf4

Local: https://bohrium.dp.tech/notebook/96841436cf844b2aade4ffe621d80bcc

#### Final Goal

Based on dflow to complete the automated process, on this basis, one or more of the following can be appropriately added, of course, according to the actual situation of their own project:

1. Further packaged into friendly software, the user interface can be command line or Bohrium APP, which can be interactive on the web page and the results can be displayed.

2. Abstracted into a framework with certain extensibility, for similar scenarios of some users, some custom development can be done under the framework to meet the needs, such as different algorithms, different implementations, and different calculation goals in a certain step of the process, and can be plugged in in a set of frameworks and relatively decoupled. See https://github.com/deepmodeling/dpgen2, https://github.com/deepmodeling/APEX, https://github.com/zjgemi/dpa-data-cleaning, etc.

3. To develop an OP with certain reusability, or to reuse an OP developed by others, refer to https://aissquare.com/workflows?type=ops&sort=view_count&page=2.

4. Demand characteristics that have certain commonality to Dflow.

#### Submission Requirements

Submit the full content as a Bohrium Notebook or as an attachment

### Question 3: DMFF: LJ potential parameter adjustment

The Differentiable Molecular Force Field (DMFF) optimization platform hopes to create a new production-level force field calculation engine through automatic differential technology to help solve many pain points in the development process such as difficult parameter tuning and complex force field calculation, achieve automatic tuning of molecular force field parameters, and rapid realization of complex force field molecular dynamics (MD).

#### Problem description

In computational chemistry and molecular simulations, the Lennard-Jones potential (LJ potential) is a simple model for describing the van der Waals forces between atoms. The LJ potential is usually expressed by two parameters: the attraction energy (ε) and the equilibrium distance (σ). These two parameters have different values for various types of atoms and molecules. Optimizing these parameters is important to accurately model the properties of molecular systems. 

All along, the goal of LJ potential adjustment has been to better reproduce experimental data, such as density, enthalpy of evaporation, surface tension, etc. In the past, due to the limitation of computing power, the resources required for parameter optimization of this high-dimensional space were very large, which limited the types of LJ potential parameters and the depth of optimization. 

With the development of differentiable computing frameworks, we can use first-order optimization algorithms in high-dimensional spaces at a lower cost; Further, DMFF proposes to use MBAR reweighting and differentiable frameworks to directly calculate the derivatives of physical properties to force field parameters. This means that large-scale optimization of force field parameters directly oriented to physical properties is already ready, and only the east wind is owed.

#### Preliminary Round Goals

Refer to the example below to write a Bohrium notebook that adjusts the Lennard-Jones parameters for more than one organic molecule for more than one thermodynamic property.

#### Some tips

Optional organic molecules can be referred to: https://pubs.acs.org/doi/pdf/10.1021/ct200731v. The most easily achievable target physical properties are: density, enthalpy of evaporation, dielectric constant. For each molecule, parameter files in Gromacs format can be generated using acpype, and liquid phase boxes can be prepared with packmol. DMFF can easily use the reweighting method to calculate the derivative of the statistical mean for parameter optimization.

#### Reference Case

https://github.com/deepmodeling/DMFF/blob/wangxy/v1.0.0-devel/examples/lennard_jones_opt/opt.ipynb

#### Final Goal

1. Based on the results of the preliminary round, build an extensible Lennard-Jones parameter optimization framework. Users are free to add new small molecules and new thermodynamic properties to achieve better results than the current GAFF2.

2. Contestants can choose more efficient optimization algorithms, and we welcome new features to DMFF to better support this application.

#### Submission Requirements

Submit the full content as a Bohrium Notebook or as an attachment

#### Submission method

- Send email to email: hackathon@deepmodeling.com

- The email is named "Track_Name_Direction.zip", such as "AI4Science Application Scenario Exploration_Xiaoming _DMFF.zip, AI for Life Sciences_Li Hua_Free Track .zip", if the email contains an attachment, the attachment is the same as the email name.

- The email contains the participant's name, a link to the package/bohrium notebook (depending on the requirements of the competition), and the necessary instructions

### Schedule

1. Hackathon presentation, team, registration time: June 27-July 7

2. Hackathon Preliminary Round: July 8 - July 14

3. Preliminary round results announced: July 15 to July 16

4. Hackathon Final: July 17 – August 5

5. Final Defense: August 6 - August 7

6. Hackathon Awards: August 10
