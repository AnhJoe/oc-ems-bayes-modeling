# Project Overview
In emergency medicine, the accuracy of response-time data is often compromised by small sample sizes. In regions with infrequent 911 transitions—such as canyons or rural outskirts—traditional frequentist averages are highly volatile. A single outlier can disproportionately skew the perceived safety of a jurisdiction.

This project implements a **Bayesian Hierarchical Model** to move beyond simple point estimates. By treating the county as a connected system of geographic nodes, the model provides a more resilient and predictive assessment of service gaps, often referred to as "Ambulance Deserts".


---


# The Bayesian Framework
The engine of this system relies on three core Bayesian principles to ensure statistical integrity:

1. **Informative Priors**
Instead of assuming no prior knowledge, the model incorporates established regional benchmarks and historical performance data. This sets a mathematically grounded baseline before new data is processed.

2. **Spatial Smoothing (Information Sharing)**
The model utilizes the First Law of Geography: everything is related to everything else, but near things are more related than distant things. For areas with sparse data, the model borrows statistical strength from neighboring nodes. If surrounding zones show systemic delays due to shared infrastructure or hospital surges, the model adjusts the risk profile of the quiet node accordingly.

3. **Posterior Probability Distributions**
Unlike standard reporting that provides a single average, Bayesian inference produces a full distribution of possible outcomes. This allows us to calculate the specific probability of a response exceeding a certain safety threshold.


---


# Operational Impact
By applying **Markov Chain Monte Carlo (MCMC)** sampling, the system simulates thousands of potential scenarios to settle on the most probable risk map. This enables:

- **Resource Allocation**: Identifying where the probability of a service breach is highest.
- **System Resilience**: Highlighting where the emergency network is most vulnerable to cascading delays.
- **Equitable Metrics**: Providing rural and low-volume areas with the same level of analytical rigor as high-density urban centers.

---

# Implementation Details
- **Language**: Python 3.10+
- **Probabilistic Library**: PyMC
- **Spatial Processing**: GeoPandas & PySAL
- **Environment**: VS Code / Jupyter
