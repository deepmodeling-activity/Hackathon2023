## 决赛赛题背景

在本赛道，我们鼓励各位选手们探索并延伸AI4Science在不同场景中的应用，使用但不限于DeePMD-kit、ABACUS、DMFF、Uni-Mol、DeepFlame等软件。

本赛道赛题分为自由命题和固定命题两个部分。我们特别鼓励大家做自由命题，只要和AI4Science相关的任何创意都非常欢迎；当然如果大家对自由命题不知所措，也可以参与固定命题赛道，在指定的命题下发挥自己的创意与才华。

## 一、自由命题

本赛道的选手拥有充分的创意自由，可以选择任意和AI4Science相关的想法来完成。包括但不限于：

- **场景探索**：使用AI4Science的算法或软件，探索一些实际应用场景

- **工作流开发类**：围绕一些常见场景，开发AI4Science工作流（推荐使用dflow搭建相关工作流，但是不强制）

选择这个赛道的选手，需要在初赛阶段提交自己的proposal来描述自己的想法并初步证实该想法可行性（评审组也会给出一些建设性的指导建议，方便更好的实现）。

- **决赛目标**

	选手基于初赛的proposal内容，完成决赛项目。

- **提交要求**

	Bohrium Notebook形式或者以附件形式提交完整内容

## 二、如果你没有想法或灵感，可以参考以下应用方向：

### 赛题一：Uni-Mol+X：利用预训练模型探索3D分子表示学习的新应用

	预训练模型正在席卷多个领域。从大规模无标注数据中提取表征信息，再在小范围标注的下游任务上进行监督学习，正在成为很多领域的事实解决方案。药物与材料设计领域的预训练模型如何构建与应用？2022 年 5 月，一款开源的基于分子三维结构的通用分子表征学习框架 Uni-Mol 正式发表，论文被机器学习顶会 ICLR 2023 接收。与过往的基于一维序列或二维图结构的分子表征框架不同的是，Uni-Mol 直接利用分子三维结构作为模型输入。Uni-Mol 性能优越、模型泛化能力强，在小分子性质预测、蛋白靶点预测、蛋白-配体复合物构象预测、量子化学性质预测、MOF 材料吸附性能预测、OLED 发光材料性能预测等任务上都超越了现有的解决方案。

#### 初赛目标

	你的任务是使用Uni-Mol框架，开发一个新的下游应用，该应用应能有效地利用Uni-Mol的3D分子表示能力和预训练特性。你可以选择解决一个具体的问题，例如预测分子性质、生成新的分子结构，或者开发一个新的工具或服务。

#### 一些提示

	在这个挑战中，我们邀请你使用基于分子三维结构的通用分子表征学习框架 Uni-Mol ，结合你自己的创新思维（即“X”），探索分子表示学习的新应用。你可以选择任何你感兴趣的领域，包括但不限于药物设计、材料科学、环境科学等。下面这两个例子可以给你一些启发。

#### 参考案例

	Uni-Mol性质预测实战-回归任务-电解液分子的介电常数: https://nb.bohrium.dp.tech/detail/1033

	Uni-Mol性质预测实战-分类任务-血脑屏障渗透性: https://nb.bohrium.dp.tech/detail/1034

#### 决赛要求

	在这个挑战中，我们邀请你使用基于分子三维结构的通用分子表征学习框架 Uni-Mol ，结合你自己的创新思维（即“X”），对Uni-Mol进行架构上的修改与提高，扩大Uni-Mol的应用场景，实现更高级的应用。

	基于初赛的proposal，选手在完成作品内容的同时，可以基于对Uni-Mol需求对Uni-Mol工具进行优化，我们给出如下参考的优化建议：

1. 除了结构信息之外考虑到其他的信息，将一些环境的变量如温度，压强等共同作为输入，训练特定的与环境相关的模型。例如Uni-MOF在Uni-Mol的基础上进行了改动，实现了预测特定温度和压强下MOF对气体对吸附能力。

2. 当前Uni-Mol的3D表征没有考虑周期性。在处理一些周期性体系时没有办法得到很好的结果。在之前的输入基础上引入周期性约束，对模型的结构进行调整后得到周期性的信息，实现Uni-Mol对周期性体系的支持。

3. Uni-Mol当前的预训练模型更专注于通用型，在一些功能分子的应用场景中（例如OLED分子，电解液分子），这些分子有其专有的特点。对于特定场景可以重新有针对的构建预训练模型，可以用特定的数据训练专用的预训练模型，也可以重新设计有针对的预训练任务。

4. Uni-Mol当前的表现还有可优化的空间，例如：通过将初始构象迭代优化至其平衡构象，并且优化的构象进一步用于预测QC特性，Uni-Mol+进一步提高了Uni-Mol在量化属性预测对准确性。可以尝试更多的方法进一步优化Uni-Mol的表现，提高训练速度和预测精度。

#### Ref：

	Uni-MOF：https://chemrxiv.org/engage/chemrxiv/article-details/6447d756e4bbbe4bbf3afeaa

	OLED：https://chemrxiv.org/engage/chemrxiv/article-details/6412d142aad2a62ca1d86505

	Uni-Mol+：https://arxiv.org/abs/2303.16982

#### 提交要求

Bohrium Notebook形式或者以附件形式提交完整内容

### 赛题二：dflow + X：开发AI4Science云原生工作流

dflow是一个使用云原生项目Argo作为工作流引擎，面向科学计算工作流开发者的开源Python开发框架。

#### 初赛目标

	在科学计算场景下或者你的科研工作中一定遇到过一些自动化工作流的需求，在dflow的框架和规范下实现一个简单的工作流，或者复杂工作流的一部分（比如实现其中几个OP），在工作流平台上workflows.deepmodeling.com上跑通，初步体会云原生、自动化、可观测、可复现的内涵

##### 一些提示
	
	下面这些案例会帮助你逐步掌握dflow工作流。

#### 参考案例

	Function OP：https://bohrium.dp.tech/notebook/90e75093e3e64c0a99521f1be6dc3346
	
	Class OP：https://bohrium.dp.tech/notebook/b0897299e4d4466a8d64d2538de1bf26
	
	Condition：https://bohrium.dp.tech/notebook/dde8e85b376e41fba6f125d5abf1f635
	
	Slices：https://bohrium.dp.tech/notebook/644edc260d8746159d9ecd48bfa1ca76
	
	Recursion：https://bohrium.dp.tech/notebook/aa39c7c1ca0b48d4a85cd4032aafceb5
	
	Reuse：https://bohrium.dp.tech/notebook/e6bfb5f3efda4febba2ba696c9838557
	
	Dispatcher: https://bohrium.dp.tech/notebook/9840681dced74568b64f3449581e6bf4
	
	Local: https://bohrium.dp.tech/notebook/96841436cf844b2aade4ffe621d80bcc

#### 决赛目标

基于dflow完成自动化流程，在此基础上满足以下一项或多项的可适当加分，当然要根据自己项目的实际情况：

1. 进一步封装成友好的软件，用户接口可以是命令行，也可以是Bohrium APP，可以在网页上交互、结果展示。

2. 抽象成具有一定扩展性的框架，对于有的用户的相似场景，能在该框架下做一些自定义的开发从而满足需求，例如流程中的某一步的算法不同、实现不同、算的目标不同，在一套框架下能插件化地、相对解耦地接进来。可参考https://github.com/deepmodeling/dpgen2、https://github.com/deepmodeling/APEX、https://github.com/zjgemi/dpa-data-cleaning 等。

3. 开发具有一定复用性的OP，或复用其他人开发的OP，可参考https://aissquare.com/workflows?type=ops&sort=view_count&page=2。

4. 对dflow提出或贡献具有一定共性的需求特性。

#### 提交要求

Bohrium Notebook形式或者以附件形式提交完整内容

### 赛题三：DMFF：LJ势参数调节

可微分分子力场（Differentiable Molecular Force Field, DMFF）优化平台希望通过自动微分技术打造全新的生产级力场计算引擎，以帮助解决参数调优困难、复杂力场计算等开发过程中的诸多痛点问题，达成分子力场参数的自动调优，以及复杂力场分子动力学（MD）的快速实现。

#### 问题描述

	在计算化学和分子模拟中，Lennard-Jones势（LJ势）是描述原子间范德华力的一种简单模型。LJ势通常用两个参数表示：吸引能（ε）和平衡距离（σ）。这两个参数对于各种类型的原子和分子都有不同的数值。优化这些参数对于准确模拟分子系统的特性非常重要。一直以来，LJ势的调整目标都是更好地复现实验数据，如密度、蒸发焓、表面张力等。在过去，由于算力限制，这种高维空间的参数优化所需资源十分庞大，这限制了LJ势参数的种类与优化的深度。随着可微分计算框架的发展，我们可以用更低的成本在高维空间内使用一阶优化算法；进一步的，DMFF提出了使用MBAR reweighting与可微分框架，直接计算物理性质对力场参数的导数。这意味着直接面向物理性质的大规模力场参数优化已经万事俱备，只欠东风。

#### 初赛目标

	请参考下面的例子，撰写一个Bohrium Notebook，实现对于一种以上的有机分子，面向一种以上的热力学性质，调整其Lennard-Jones参数。

#### 一些提示

	可选的有机分子可以参考：https://pubs.acs.org/doi/pdf/10.1021/ct200731v。较易实现的目标物理性质有：密度、蒸发焓、介电常数。对于每种分子，Gromacs格式的参数文件可以使用acpype生成，液相盒子则可以用packmol准备。DMFF可以便利地使用reweighting方法计算统计平均值的导数，进而进行参数优化。

#### 参考案例

	https://github.com/deepmodeling/DMFF/blob/wangxy/v1.0.0-devel/examples/lennard_jones_opt/opt.ipynb

#### 决赛目标

1. 基于初赛成果，搭建一个可扩展的Lennard-Jones参数优化框架。使用者可以自由增加新的小分子与新的热力学性质，达成比目前GAFF2更好的效果。

2. 参赛选手可以选择更有效的优化算法，我们非常欢迎选手为DMFF贡献新的feature来更好地支撑这一应用。

#### 提交要求

	Bohrium Notebook形式或者以附件形式提交完整内容

#### 提交方式

- 发送邮件至邮箱：hackathon@deepmodeling.com

- 邮件命名为“赛道_姓名_方向.zip”，如“AI4Science应用场景探索_小明_DMFF.zip，AI for Life Sciences_李华_自由赛道.zip”，若邮件内有附件，附件同邮件名。

- 邮件内容包含参赛者姓名，压缩包/bohrium Notebook链接（具体看赛题要求），以及必要的说明

### 时间安排

1. Hackathon宣讲、组队、报名时间：6月27日-7月7日

2. Hackathon初赛：7月8日-7月14日

3. 初赛结果公布：7月15日-7月16日

4. Hackathon决赛：7月17日-8月5日

5. 决赛答辩：8月6日-8月7日

6. Hackathon颁奖：8月10日