# Market Dynamics Simulation using the Ising Model

## Overview

This project employs the Ising model from physics to simulate stock market dynamics. Using this framework, we explore herd behavior in financial markets and replicate financial stylized facts such as autocorrelation and fat-tailed distributions of returns. Additionally, we test traditional trading strategies like momentum, mean-reversion, and value investing within the Ising model context.

## Model Description

The Ising model is a mathematical model from statistical mechanics used to describe ferromagnetism by representing particles as spins that interact with their neighbors and external fields. The Hamiltonian of this model is given by the following expression:

$$ H = -J \sum_{\langle i,j \rangle} s_i s_j - h \sum_i s_i $$

where $s_i$ represents each spin particle, taking values in \{+1, -1\}, $J$ is the interaction strength between neighboring spins, and $h$ is the interaction with an external magnetic field.

The instantaneous magnetization is defined as:

$$ m(t) = \sum_{k=0}^{N} s_k(t) $$

where $N$ is the total number of spin particles in the system. The cumulative magnetization is defined as:

$$ cm(t) = \sum_{t'=0}^{t} m(t') $$

To translate the Ising Model into the financial context, we make the following interpretations:
- Each spin particle is treated as a trader who can buy or sell a stock, represented by the value of $s_i$.
- Instantaneous magnetization is understood as the instantaneous change in stock price, based on the supply and demand model in financial markets.
- Cumulative magnetization is treated as the stock price over time.
- The interaction between traders (spin particles) is expanded beyond first neighbors to all neighbors, incorporating the various relationships among all market participants. In this setup, the physical concept of a dimensional lattice becomes irrelevant.
- The magnetic field is treated as an external force, such as positive or negative market news about a company that affects market prices. This magnetic field is inhomogeneous for each trader.
