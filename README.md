# Electing the Pope – Game-Theoretic Simulations of Papal Conclaves (2013 & 2025)

This repository contains a Python implementation inspired by the academic paper *Electing the Pope* by Kóczy & Sziklai. It models the papal conclave as a voting game using concepts from cooperative game theory and convex geometry.

The simulation estimates each cardinal's voting power by evaluating their frequency as pivotal members in minimal convex winning coalitions.

---

## Contents

- `conclave.ipynb`: Main Jupyter notebook. Works for both 2013 and 2025 conclaves by switching datasets and majority thresholds.
- `conclave_2013.csv`: Dataset for the 2013 conclave.
- `CONCLAVE_2025_V3.2.csv`: Dataset for the 2025 conclave.
- `cardenales_con_score_3M_muestras.csv`: Results of 3 million samples for 2013.
- `conclave_2025_5M_muestras_v3.csv`: Results of 5 million samples for 2025.
- `electing_the_pope_MTDP1315.pdf`: Original academic paper by Kóczy & Sziklai (used for reference).

---

## Methodology

- Each simulation randomly generates millions of axis-aligned convex rectangles in a 2D space where:
  - The X-axis represents geographical distance from Rome.
  - The Y-axis encodes conservatism (from progressive to traditionalist).
- Coalitions that include **exactly the minimum number of votes required** (77 in 2013, 89 in 2025) are considered.
- Cardinals appearing on the edge of those coalitions are considered pivotal and awarded 1 point.
- Final scores reflect each cardinal's structural influence in potential conclave scenarios.

---

## Based on

**Electing the Pope**  
László Á. Kóczy & Dóra Szilágyi (2015)  
[MTDP1315.pdf](https://econ.core.hu/file/download/mtdp/MTDP1315.pdf) (also included in this repo for academic reference)

---

## Requirements

- Python 3.9+
- Pandas
- NumPy
- Jupyter Notebook

---

## License

All code is MIT licensed.  
The original paper is the property of the authors and their institution and is included here only for academic and educational purposes.
