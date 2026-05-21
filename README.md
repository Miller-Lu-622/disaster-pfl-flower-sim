# pFL with Gradient Sketching and Neighbour Grouping for Disaster Settings — Flower Implementation

This repository contains the **main Flower-based implementation and simulation framework** for the proposed method: **Personalized Federated Learning with Gradient Sketching and Neighbour Grouping for Disaster Settings**.

## Repository Role

This project is organized into two complementary codebases:

- **PFLlib fork**: used for PFLlib-based baseline experiments, benchmarking, and comparative evaluation against existing FL / pFL methods
- **this Flower repository**: used for the dedicated implementation, simulation, and fuller workflow of the proposed method

In short:

- **PFLlib repo** → PFLlib-based experimental evaluation
- **Flower repo** → main implementation and realistic simulation evaluation

## Research Focus

The framework is designed for disaster-oriented federated learning settings where several challenges appear together:

- strong natural **Non-IID heterogeneity** across events and regions
- **distribution drift** as disaster conditions evolve
- **unstable participation** caused by communication disruption, churn, or correlated dropout

The method centers on:

- **compact update / gradient signatures**
- **lightweight neighbour retrieval**
- **repeated regrouping** under drift and changing participation
- **personalized coordination** beyond a single shared global model

## Intended Implementation Scope

This repository is intended to host the dedicated Flower-based implementation of:

1. client local training and update generation
2. compact signature construction from local updates
3. neighbour retrieval based on approximate similarity
4. personalized server-side coordination
5. periodic or event-triggered regrouping
6. simulation of instability in disaster-oriented FL settings

## Evaluation Relationship

The broader research workflow separates **implementation** from **benchmark-oriented comparison**:

- the **PFLlib fork** provides a convenient evaluation environment for baseline comparison and supplementary experiments on established FL benchmarks
- this **Flower repository** will provide the cleaner and more explicit implementation of the proposed framework itself

## Planned Evaluation Settings

Primary target evaluation includes:

- **xBD / xView2-style disaster damage assessment**
- client splits reflecting natural disaster heterogeneity
- simulated communication instability and evolving participation

Supplementary evaluation may include:

- **CIFAR-10**
- **CIFAR-100**
- other conventional FL benchmarks where appropriate

## Current Status

This repository is currently at the project setup stage.

Next steps include:

- defining the project structure for Flower
- implementing the training / coordination pipeline
- integrating compact signature and neighbour grouping logic
- preparing disaster-oriented experimental settings

## Related Repository

PFLlib-based evaluation fork:

- <https://github.com/Miller-Lu-622/disaster-pfl-pfllib-eval>
