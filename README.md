# README

## Project Title
Formal Verification of Risk-Aware Trading Strategies using Markov Decision Processes and Probabilistic Model Checking

## Overview
In this project we made an MDP model of stock trading and analysed it using probabilistic model checking in PRISM. The aim is to understand how uncertainty, transaction cost, and asset correlation affect trading performance.

Two models are used. A baseline model captures the basic behaviour of the system, and an extended model includes additional parameters for more realistic analysis.

## Model Description

### Baseline Model (RQ1 and RQ2)
The baseline model includes:
- price levels
- portfolio value (pval)
- position variable (pos)
- actions: buy, sell, hold

It is used to analyse:
- probability of reaching a profit target
- ability to reach profit while avoiding loss

### Extended Model (RQ3 and RQ4)
The extended model introduces:
- transaction cost (COST)
- correlation (CORR)

This allows analysis of:
- impact of cost on performance
- effect of correlation on diversification

## Properties Verified
The following properties are checked in PRISM:

- reachability of profit within bounded steps
- safe profit (avoiding loss before profit)
- probability of loss
- safety (staying above loss threshold)

## Experimental Setup
The parameters COST and CORR are varied.

Typical values used:
- COST: 0.0, 0.5, 2.0, 5.0
- CORR: 0.1, 0.5, 0.6

For each setting:
- model is verified in PRISM
- results are recorded
- graphs are generated

## Simulation and Plots
PRISM simulation is used to observe behaviour of the model.
Plots are generated in PRISM to compare results across different parameter values.

## How to Run
1. Open PRISM
2. Load the .prism model file
3. Load the .props file
4. Set values for COST and CORR
5. Run model checking
6. Use plot option in PRISM to visualise results

## Summary
The results show that increasing transaction cost reduces performance, and higher correlation reduces the benefit of diversification. The model provides a structured way to analyse trading decisions under uncertainty.
