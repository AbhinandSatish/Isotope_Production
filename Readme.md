# Ra-226 Decay Chain Modeling and Radon Release Simulation

## Overview
This project models the short radioactive decay chain:

**Ra-226 → Rn-222 → Po-218**

The simulation uses coupled differential equations with additional artificial burnup/production terms and implements different venting strategies to study their impact on isotope inventories, activity levels, and radon release.  

The goal is to understand:
- How daughter isotopes accumulate in a decay chain.  
- The effect of different venting schedules on radon buildup and environmental release.  
- The relative importance of natural decay vs. artificial source/burnup terms.  
- Practical radiological engineering implications for safety and containment.  

---

## Features
- Numerical integration of decay ODEs using Python (`scipy.integrate.odeint`).  
- Implementation of venting strategies:
  - **Scenario 1:** Single vent at 40 days.  
  - **Scenario 2:** Regular venting every 10 days.  
- Calculation of isotope inventories and activities over time.  
- Quantification of total radon-222 released in each scenario.  
- Visualization of decay dynamics with inventory and activity plots.  

---

## Key Results
- **Ra-226** remains nearly constant due to its long half-life.  
- **Rn-222** and **Po-218** inventories grow to equilibrium in a closed system.  
- **Venting effects:**
  - A single vent at 40 days (Scenario 1) allows maximum buildup but lower total release.  
  - Frequent venting every 10 days (Scenario 2) prevents buildup but increases cumulative release by ~236%.  

---

## Tools & Methods
- **Language:** Python 3  
- **Libraries:** `numpy`, `scipy`, `matplotlib`  
- **Approach:**  
  - Formulated decay ODEs with burnup/source terms.  
  - Integrated numerically with `odeint`.  
  - Applied instantaneous removal of Rn-222 to simulate venting.  
  - Plotted atom inventories and activity curves.  

---

## Example Output
- Ra-226 inventory: ~2.63×10²¹ atoms (nearly unchanged after 40 days).  
- Scenario 1 release: **1.79×10¹⁶ atoms Rn-222** (~3.2×10¹¹ Bq).  
- Scenario 2 release: **6.03×10¹⁶ atoms Rn-222** (~1.08×10¹² Bq).  

---

## File Structure
- `Satish_Final.ipynb` → Jupyter Notebook with code, calculations, and plots.  
- `Abhinand Satish Final Project 1, Rad Eng.pdf` → Full project report.  

---

## How to Run

1. **Clone the repository** (or download the project files):  
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>

2. **Set up a Python environment (recommended to use virtualenv or conda):**
    ```bash
    python -m venv venv
    source venv/bin/activate   # On Mac/Linux
    venv\Scripts\activate      # On Windows
3. **Install Dependecies**
    ```bash
    pip install numpy scipy matplotlib jupyter
4. **Run Jupyter Notebook**
    ```bash
    jupyter notebook Satish_Final.ipynb
