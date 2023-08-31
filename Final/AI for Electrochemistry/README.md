# Background of the competition question(Final)

The AI4EC track is jointly hosted by the DeepModeling open-source community and the Jiageng Innovation Laboratory Artificial Intelligence Applied Electrochemistry Joint Laboratory (AI4EC). The aim is to encourage players who wish to explore **the electrochemical properties of various materials in the battery field** to use AI4Science related software tools to develop workflows for calculating properties such as material redox potential and reaction free energy in a certain system or environment; It can also be used to solve a specific problem. In short, if you are eager to use materials to continuously define energy, welcome to join the AI for Electrochemistry exploration journey!

**The questions on this track are divided into two parts: free questions and fixed questions. We particularly encourage everyone to do free propositions, and any creativity related to AI4EC is very welcome; Of course, if you are unsure of what to do with free propositions, you can also participate in fixed proposition races and showcase your creativity and talent under designated propositions**

## 1. Free questions

The contestants on this track have full creative freedom and can choose any ideas related to AI4EC to complete. Including but not limited to:

**Scenario exploration**: Use AI4EC algorithms or software to explore some practical application scenarios

**Workflow development class**: Develop AI4EC workflows around some common scenarios

Players who choose this track need to submit their proposal during the preliminary stage to describe their idea and preliminarily confirm its feasibility (the evaluation team will also provide constructive guidance and suggestions for better implementation).

## 2. Fixed questions

#### **Contest questions**

- Building an automated workflow for redox potential calculation accelerated by machine learning

#### **Background&Issues**

- The calculation of free energy based on first principles molecular dynamics simulation (AIMD) is slow and inefficient.

- Machine learning potential energy (MLP) can accelerate AIMD simulation. The accuracy of MLP requires high-quality datasets to ensure. The Deep Potential Energy Generator (DP-GEN) can be used to generate datasets suitable for MLP.

#### **Objective**

- Build a workflow that combines DP-GEN with redox potential calculation methods

#### **Possible solutions**

- Understanding the calculation of redox potential: refer to J Chem Phys 157, 024103 (2022) and other relevant literature

- Using DP-GEN: Please download the source code of DP-GEN from github and read its main body.

- Construction workflow: The coupling of free energy perturbation and MLP training can be achieved by directly modifying the source code of DP-GEN.


#### **Dataset&Materials**

- Two datasets of deep potential energy models (initial and final states),

- Input file and calculation output file of LAMMPS

- Download: https://dp-public.oss-cn-beijing.aliyuncs.com/community/ai4ec.zip

#### **Scoring points of Final**

- Understand how dpgen automatically generates LAMMPS input files, and modify *dpgen/generator/lib/lammps.py* so that it can generate input files for free energy calculation, and mark them in the form of comments where they are modified.

- Modify the *dpgen/generator/run.py* file to build a free energy potential function training automation workflow, and tag the changes in the form of comments.

- Analysis report on how *dpgen* modifies.


#### **Submission format**

- Modified copy of dpgen/generator/lib/lammps .py. (Python Source File) (Final-1)

- Modified dpgen/generator/run .py file. (Python Source File) (Final-2)

- dpgen modifies the analysis report. (Word) (Final-3)


[Click here to view detailed competition content]( https://dptechnology.feishu.cn/docx/UJIwdMKf6oMhMjxRQcfciR8onyc?from=from_copylink )
