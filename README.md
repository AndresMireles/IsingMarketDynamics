# Market Dynamics Simulation using the Ising Model

## Overview

This project employs the Ising model from physics to simulate stock market dynamics. Using this framework, we explore herd behaviour in stock markets, simulate financial events and replicate stylized facts such as autocorrelation and fat-tailed distributions of returns. Additionally, we test traditional trading strategies like momentum, mean-reversion, and value investing within the Ising model context.

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
- The instantaneous magnetization $m(t)$ is understood as the instantaneous change in stock price, based on the supply and demand model in financial markets.
- The cumulative magnetization $cm(t)$ is treated as the stock price over time.
- The interaction $J$ between traders (spin particles) is expanded beyond first neighbors to all neighbors, incorporating the various relationships among all market participants. In this setup, the physical concept of a dimensional lattice becomes irrelevant.
- The magnetic field $h$ is treated as an external force, such as positive or negative market news about a company that affects market prices. This magnetic field is inhomogeneous for each trader.

## Results

### Fat-tailed distribution of returns
![image](https://github.com/AndresMireles/IsingMarketDynamics/assets/64489886/0c8b64f9-70f3-42cc-9473-ee610f73e8ce)

### Autocorrelation of returns
![Autocorrelation](https://github.com/AndresMireles/IsingMarketDynamics/assets/64489886/d3764310-a180-47da-aabe-8f412b59901f)

### Strategies
![image](https://github.com/AndresMireles/IsingMarketDynamics/assets/64489886/b6374041-b475-473d-96d4-4ad25a37949b)
![image](https://github.com/AndresMireles/IsingMarketDynamics/assets/64489886/e981b114-e264-47f2-a614-1623e73dcb3c)
![Strategy](https://github.com/AndresMireles/IsingMarketDynamics/assets/64489886/9fd9c488-6f3a-4f69-9ad6-c205c17db308)

### Simulation of events
![Simulation Event](https://github.com/AndresMireles/IsingMarketDynamics/assets/64489886/c41c5aa1-4529-4196-ac70-378d8ef768d7)![Simulation Event](https://github.com/AndresMireles/IsingMarketDynamics/assets/64489886/816b0576-093e-45e1-9d83-16c0a350a8fc)![Simulation Event](https://github.com/AndresMireles/IsingMarketDynamics/assets/64489886/de1676e2-5f9a-4f4d-87df-136b0655f5ba)


