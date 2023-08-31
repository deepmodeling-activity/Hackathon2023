#Background of the competition question

The AI4EC track is jointly hosted by the DeepModeling open-source community and the Jiageng Innovation Laboratory Artificial Intelligence Applied Electrochemistry Joint Laboratory (AI4EC). The aim is to encourage players who wish to explore **the electrochemical properties of various materials in the battery field** to use AI4Science related software tools to develop workflows for calculating properties such as material redox potential and reaction free energy in a certain system or environment; It can also be used to solve a specific problem. In short, if you are eager to use materials to continuously define energy, welcome to join the AI for Electrochemistry exploration journey!

**The questions on this track are divided into two parts: free questions and fixed questions. We particularly encourage everyone to do free propositions, and any creativity related to AI4EC is very welcome; Of course, if you are unsure of what to do with free propositions, you can also participate in fixed proposition races and showcase your creativity and talent under designated propositions**

## 1. Free proposition

The contestants on this track have full creative freedom and can choose any ideas related to AI4EC to complete. Including but not limited to:

**Scenario exploration**: Use AI4EC algorithms or software to explore some practical application scenarios

**Workflow development class**: Develop AI4EC workflows around some common scenarios

Players who choose this track need to submit their proposal during the preliminary stage to describe their idea and preliminarily confirm its feasibility (the evaluation team will also provide constructive guidance and suggestions for better implementation).

## 2. Reference topic

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

#### **Getting Started**

- Understand the process of using deep potential molecular dynamics (DPMD) to calculate free energy by reading the input file of LAMMPS. Compare the conventional DPMD calculation files and analyze the similarities and differences.

- Reading paper *J Chem Phys 157, 024103 (2022)*, understanding how to calculate vertical energy gaps and thermodynamic integration.

- Read the LAMMPS output file to calculate the vertical energy difference and draw a statistical average image.

- Based on the statistical average of the vertical energy difference, draw a thermodynamic integral image and calculate the free energy.

#### **Dataset&Materials**

- Two datasets of deep potential energy models (initial and final states),

- Input file and calculation output file of LAMMPS

#### **Scoring points**

- Read the data, calculate the cumulative average vertical energy difference, and draw a diagram of thermodynamic integration.

- Understand the input of LAMMPS for calculating free energy, analyze the key points of the calculation content, and write an analysis report.

#### **Submission format**

- A compressed format document containing the required files, which should include:

- Calculate the cumulative average vertical energy difference and draw a diagram of thermodynamic integration (presented in Bohrium Notebook form)

- LAMMPS Calculation Free Energy Input File Interpretation Report (Word)

[Click here to view detailed competition content]( https://dptechnology.feishu.cn/docx/UJIwdMKf6oMhMjxRQcfciR8onyc?from=from_copylink )
