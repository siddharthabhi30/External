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

My understanding of training: They train end to end. From time \(1\) to \(P\), they forecast and assimilate using particle flow at each step. They then forecast another \(Q\) steps, from \(P+1\) to \(P+Q\). The loss is calculated on those future predictions, and the model parameters are updated using SGD.

## Dynamic Neural Relational Inference (2020)

[Paper — Graber and Schwing, CVPR (2020)](https://openaccess.thecvf.com/content_CVPR_2020/html/Graber_Dynamic_Neural_Relational_Inference_CVPR_2020_paper.html)

My current understanding: They convert the state space into a latent representation. The sequence of latent representations over time is used to predict spatial relations. Those spatial relations are then used to improve prediction.

## Ideation: AD-EnFF with dynamic spatial relationships

My idea is to use a weather or atmospheric model and use Liang–Kleeman (LK) information flow to create a dynamic spatial graph. Each graph node represents a geographical region or local atmospheric state block. For example, sea-surface temperature in one region could affect soil moisture in another. More accurate observations of that temperature could help learn better hyperparameters and prior bias correction for the local AD-EnFF in the other region.

The dynamic graph would provide additional input when learning the hyperparameters. We would develop a gossip protocol to share information and use the graph embeddings to learn the hyperparameters for each local AD-EnFF node. We would still learn both the prior bias correction and the hyperparameters, as in AD-EnFF, and run particle flow normally. The added information is the dynamic spatial correlation.

Possible contributions:

1. Dynamic spatial correlations represented in an interpretable graph.
2. Using those relationships to improve AD-EnFF filtering.
3. A gossip protocol tailored specifically to this architecture.

IcyAlert could use the same idea: leverage an interpretable dynamic graph to improve forecasting.

## TODO

- [ ] [Unsupervised Learning of Sampling Distributions for Particle Filters (2023)](https://arxiv.org/html/2302.01174)
