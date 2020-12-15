# covid-pyro

This repository houses the code and report for Swapneel Mehta and Noah Kasmanoff's final project for DSGA-105 Inference and Representation, Probabilistic Graphical Models and COVID-19. 

The focus of this work is to replicate part of the work in "Planning as Inference with Epidemiological Models" (https://arxiv.org/pdf/2003.13221.pdf)  in a popular framework such that the code can be released to a broader audience.

## Technical Details 

- Application of compartmental (SIR, SEIR) models in attempt to reproduce their data. No promise that the agent-based approach can succeed, due to the software requirements for running their singularity image which requires sudo access on NYU HPC to even install and run out-of-the-box. We are working on adapting this, but emphasize their agent based results were less relevant to the pandemic anyway since they explicitly stated that was an influenza simulation and it was only used to characterize high-fidelity simulations that allow more fine-grained controls compared to compartmental models.

- We place priors on the noncontrollable disease parameters as expressed in the paper with updates where possible, based on recent literature on COVID-19. The goal is to infer the level of intervention required (‘u’, in the paper) such that the infectiousness parameters (dictating disease spread) are reduced to constrain the spread to lie within a predetermined level (e.g. 10% of population)

- Their goal was to demonstrate that an existing agent-based simulator for influenza written in C++ can be coupled with a Python-based Probabilistic Programming framework (Pyprob). Our goal is more in line with the project guidelines for 1005, which is to present their work as an end-to-end model in Pyro to replicate the core contributions of their study in a more accessible framework with better end-user support. Ideally, we would like to produce a project report that can be offered as a tutorial contribution for the Pyro Epidemiology Docs.
