# Paper summaries

Current notes; a section does not mean the whole paper has been mastered. [Context](../CONTEXT.md) · [Future reading](future/README.md) · [Ideation](../ideation/dynamic-spatial-graph.md)

## Graph Laplacian Distributed Particle Filtering (2016)

[Paper — Rabbat, Coates and Blouin, EUSIPCO (2016)](https://www.eurasip.org/Proceedings/Eusipco/Eusipco2016/papers/1570255849.pdf)

**Goal:** Find the joint likelihood of each particle from all the sensors by communicating compressed information with low overhead.

My current understanding: They build a graph at each sensor, where the graph nodes are particles. Edges connect pairs of particles that are close to each other. They then form the graph Laplacian and use its eigenvectors to compress the likelihood information. This compressed information is shared between sensors to calculate the joint likelihood.

TODO: Explore why they construct the particle graph and Laplacian this way, the trade-offs of using low-eigenvalue eigenvectors for compression, and what alternative compression methods could be used.

## Distributed state estimation with compressed and synchronized auxiliary particle filters using graph theory (2024)

[Paper — Maghsudlu, Danaee and Arezumand, Discover Electronics (2024)](https://doi.org/10.1007/s44291-024-00016-z)

My current understanding: This paper is for distributed estimation. The important point in the abstract is that it uses the latest measurements to construct a better proposal distribution. The authors say that incorporating the latest measurements into the proposal can improve accuracy and efficiency, especially in high-dimensional or nonlinear state-space models.

## Particle Network EnKF for Large-Scale Data Assimilation (2022)

[Paper — Li and Lu, Frontiers in Physics (2022)](https://www.frontiersin.org/journals/physics/articles/10.3389/fphy.2022.998503/full)

My current understanding: This paper builds a graph at the particle level instead of the sensor level. It distributes the particles over a sparse network and achieves performance comparable to standard EnKF with lower communication cost. Each particle calculates its own local Kalman gain because global ensemble averages are not directly available in this distributed setting.

## RNN with Particle Flow for Probabilistic Spatio-temporal Forecasting (2021)

[Paper — Pal, Ma, Zhang and Coates, ICML (2021)](https://proceedings.mlr.press/v139/pal21b.html)

My current understanding: They use an RNN for temporal relationships and graph convolution (a GNN component) for spatial relationships, combining them to make predictions.

My understanding of training: They train end to end. From time $1$ to $P$, they forecast and assimilate using particle flow at each step. They then forecast another $Q$ steps, from $P+1$ to $P+Q$. The loss is calculated on those future predictions, and the model parameters are updated using SGD.

## Dynamic Neural Relational Inference (2020)

[Paper — Graber and Schwing, CVPR (2020)](https://openaccess.thecvf.com/content_CVPR_2020/html/Graber_Dynamic_Neural_Relational_Inference_CVPR_2020_paper.html)

My current understanding: They convert the state space into a latent representation. The sequence of latent representations over time is used to predict spatial relations. Those spatial relations are then used to improve prediction.

## Distributed Kalman Filtering for Interconnected Dynamic Systems (2022)

[Paper — Yuchen Zhang, Bo Chen, Li Yu and Daniel W. C. Ho, IEEE Transactions on Cybernetics (2022)](https://octochen.github.io/papers/P4_2022-01_Distributed%20Kalman%20filtering%20for%20interconnected%20dynamic%20systems.pdf)

**State and interconnections:** Each node is a subsystem. $x_{i,t}$ is its state at time $t$. $A_i$ describes its own evolution, and $A_{i,j}$ describes how node $j$ affects node $i$. $A_{i,j}$ is known, so the stochastic evolution equation is known for each node.

**Process model:**

```math
x_{i,t}=A_i x_{i,t-1}+B_i u_{i,t-1}+\sum_j A_{i,j}x_{j,t-1}+\Gamma_i w_{i,t-1}.
```

**Predict:** Use the previous posteriors of node $i$ and its neighbours.

```math
\hat{x}_{i,t}^{\text{pred}}
=A_i\hat{x}_{i,t-1}^{\text{post}}
+B_i u_{i,t-1}
+\sum_j A_{i,j}\hat{x}_{j,t-1}^{\text{post}}.
```

**Filter:** Add the current local correction and previous neighbour corrections.

```math
\begin{aligned}
\hat{x}_{i,t}^{\text{post}}
&=\hat{x}_{i,t}^{\text{pred}}
+K_i\bigl(y_{i,t}-C_i\hat{x}_{i,t}^{\text{pred}}\bigr)\\
&\quad+\sum_j K_{i,j}\bigl(y_{j,t-1}-C_j\hat{x}_{j,t-1}^{\text{post}}\bigr).
\end{aligned}
```

Here, $j$ runs over incoming neighbours, $y$ is the measurement, and $C$ maps a state to measurement space. The gains are calculated for the current step.

**TODO:** Read Section III-A to understand how they calculate the local Kalman gain and the neighbour decoupling gains.

## Structure-aware decoupled imputation network for multivariate time series (2024)

[Paper — Ahmed and Schmidt-Thieme](https://link.springer.com/article/10.1007/s10618-023-00987-9)

**Premise:** A set of nodes, each with its own measurements.

**Goal:** Learn relationships between the nodes to understand the graph structure, then use those relationships to predict missing values.

**My current understanding:** They artificially create holes by masking real node values, then reconstruct those values. In doing so, they learn the graph structure using a GNN in an unsupervised way. The relationships indicate which node’s information helps reconstruct another node’s readings.

**Training:** They train by artificially masking node values, reconstructing them, and backpropagating the reconstruction error.

## Neural Relational Inference for Interacting Systems (2018)

[Paper — Kipf et al.](https://proceedings.mlr.press/v80/kipf18a/kipf18a.pdf)

**My current understanding:** This paper learns the graph structure as well as the dynamics in an unsupervised manner.

## State space partitioning based on constrained spectral clustering for block particle filtering (2022)

[Paper](https://arxiv.org/pdf/2203.03475)

**Premise:** A block particle filter divides the state space into blocks to overcome the curse of dimensionality.

**Goal:** Improve the block particle filter through better clustering of the state variables.

**My current understanding:** Using the current particles, they create a correlation matrix/graph. They then use spectral clustering (SC) to group the state variables into blocks. During filtering, the blocks are chosen so that strongly correlated state variables are grouped together. They also test the method on the nonlinear Lorenz-96 model.

**Contribution:** Intelligent clustering of the state variables to enhance the block particle filter.

**Ideation (my proposal):** Maybe we can improve this using DNN distillation and attention to correct spurious correlations arising from the ensemble. Better covariance estimates could give a better graph Laplacian and better clustering, enhancing the block particle filter. We could use larger ensembles as well as time-series data for covariance distillation.

For a PFF version, use particle flow instead of reweighting, with a single scalar guidance hyperparameter per particle. The idea is to keep one scalar per particle, analogous to the single-weight-per-particle structure in PF.

**Related paper for this idea:** [Enabling High-Accuracy Data Assimilation with Limited Ensembles via Machine Learning-Based Covariance Correction (2026)](https://arxiv.org/pdf/2605.11639). We could use this approach for covariance correction.

[More of my notes on improving covariance](https://github.com/siddharthabhi30/IcyAlert_filter_core/blob/main/notes-and-papers/fixing-cov-for-small-ensm.md)

## Neural Enhanced Belief Propagation for Cooperative Localization (2021)

[Paper — Liang and Meyer](https://arxiv.org/pdf/2105.12903)

**Premise:** Cooperative localization of mobile agents, such as a swarm of robots estimating their positions.

**My current understanding:** Belief propagation (BP) is purely model-based and can become overconfident. This paper uses learned information from a GNN to complement BP and improve localization.

**TODO:** [Code](https://github.com/Peterbotliang/NEBP-Cooperative-Localization) — Read the low-level implementation to understand what they are doing.

## Gaussian Ensemble Belief Propagation for Efficient Inference in High-Dimensional, Black-box Systems (2025)

[Paper — MacKinlay et al., ICLR 2025](https://proceedings.iclr.cc/paper_files/paper/2025/file/2cd38e57eb9c3c96e859b89c3d0a3b18-Paper-Conference.pdf)

**My current understanding:** This is a framework for belief propagation. Gaussian belief propagation already existed; this paper develops an ensemble-based version, Gaussian Ensemble Belief Propagation (GEnBP). The paper claims the methodology can be used for data assimilation, system identification, and more.

**TODO:** Understand their methodology: what they are doing, how it works, and whether we can use it.
