# Metabolic Model Curation and Dynamic Simulation for Martian Soil Fertilization

This repository contains Jupyter Notebooks developed for the **metabolic curation and dynamic simulation** of microbial models designed as part of a compartmentalized hypercyclic system. The goal of this system is to support the fertilization of Martian regolith and enable its use for agriculture in extraterrestrial environments.

This work is part of a **Bachelor’s Thesis in Biotechnology** (2024–2025), with a specialization in computational biotechnology.

## Repository Structure

```
📁 model_curation/
    └── Curation of draft metabolic models generated with ModelSEED
📁 simulaciones_metabolicas/
    └── dFBA simulations of compartment 3
📁 data/
    └── Metabolic models in SBML format (.xml)
README.md
```

## Contents

### 1. Metabolic Model Curation

Draft models were generated using **ModelSEED** from genomes available on the **PATRIC** database. The curation process included:

- Assignment of chemical formulas and charges based on **KEGG**, **BiGG**, **MetaNetX**, and **RefSeq**
- Manual review and adjustment of the **biomass reaction**
- Verification of **mass and charge balance**
- Preliminary estimation of **Gibbs free energy** using **Equilibrator**
- Model quality assessment with **MEMOTE**
- Comparison of predicted vs. experimental growth rates (when available)

Curated organisms:
- *Dechloromonas aromatica*
- *Anabaena cylindrica*
- *Nostoc muscorum*
- *Clostridium aminophilum*
- *Chlorella vulgaris*
- *Bacillus subtilis*

All curated models are stored in **SBML format (.xml)** under the `data/` directory.

### 2. Dynamic Metabolic Simulations

The notebooks in `simulaciones_metabolicas/` implement a **Dynamic Flux Balance Analysis (dFBA)** framework focusing on **Compartment 3** of the system. This compartment is responsible for stabilizing and enriching Martian regolith through the production of organic acids, polysaccharides, and biomass.

The simulations include:

- Mass balance equations for *Chlorella* and *Bacillus*
- Dynamics of oxygen (O₂), carbon dioxide (CO₂), and relevant organic compounds
- Parameter sensitivity analysis (e.g., oxygen consumption rates)

Numerical integration is performed using `solve_ivp` with the `'BDF'` method to capture long-term behavior and stability of the system.

## Requirements

- Python 3.10+
- Main packages:
  - `cobra`
  - `pandas`
  - `matplotlib`
  - `scipy`
  - `memote`
  - `equilibrator-api`

It is recommended to use **Anaconda** or **Miniconda** to manage the Python environment.

## License

This project is licensed under the **MIT License**. If you use any of the materials or code in academic or research work, please cite or acknowledge the original author.

## Contact

**Elena [Last Name]**  
BSc in Biotechnology – Computational Biotechnology Track  
Universidad Politécnica de Madrid
elena.garcia.arroyo@alumnos.upm.es
