# healthcare-analytics
Measured 350+ hospitals’ efficiency using Data Envelopment Analysis (DEA) in Python and AMPL; identified 50 top-performing hospitals and improvement targets through linear programming optimization.

# Hospital Efficiency Optimization — Data Envelopment Analysis (DEA)

## Project Overview
This project applies **Data Envelopment Analysis (DEA)** to evaluate the operational efficiency of multiple hospitals.  
DEA is an **optimization-based benchmarking method** that compares similar units (Decision-Making Units — DMUs) using their **inputs** (resources) and **outputs** (services/results).  

The goal of this project is to identify **which hospitals operate most efficiently** and how others can improve resource utilization to reach the best performers.

---

## Business Problem
Hospitals often use different amounts of staff, beds, and budgets to serve patients.  
Management wants to know:
- Which hospitals deliver the best outcomes with the least resources?
- How can inefficient hospitals improve to match the top performers?

This project measures and compares efficiency scores (0–1 scale) for each hospital using DEA.

---

## Objectives
1. Measure the **relative efficiency** of 350+ hospitals.  
2. Identify **benchmark hospitals** (efficiency = 1.0).  
3. Suggest improvement targets for underperforming units.  

---

## Model Formulation

**Objective Function**

Maximize Efficiency = Σ (uᵣ * yᵣ₀) / Σ (vᵢ * xᵢ₀)

where:  
- yᵣ₀ = output r for the hospital being evaluated  
- xᵢ₀ = input i for the hospital being evaluated  
- uᵣ, vᵢ = weights assigned by the model  

**Subject to**
1. Σ (uᵣ * yᵣⱼ) / Σ (vᵢ * xᵢⱼ) ≤ 1  for all hospitals j  
2. uᵣ, vᵢ ≥ 0  

Hospitals with a ratio = 1 are on the **efficient frontier** (best performers).  
Others have scores < 1 and can improve by adjusting input–output ratios.

---

## Tools and Technologies
- **Python (Google Colab / Jupyter)**  
- **AMPL / Linear Programming (LP)**  
- **Pandas, NumPy, PuLP**  
- **Excel** for data preparation and validation  

---


---

## Key Results
| Metric | Result |
|---------|---------|
| Total Hospitals Evaluated | 350+ |
| Efficient Hospitals (Score = 1) | 50 |
| Average Efficiency | 0.78 |
| Insights | Identified best-performing hospitals with balanced input–output utilization; recommended input reduction strategies for inefficient units. |

---

## Takeaways
- Demonstrates use of **prescriptive analytics** for performance benchmarking.  
- Uses **Linear Programming** to measure relative efficiency across entities.  
- Provides actionable insights for **resource allocation** and **process improvement** in healthcare systems.  

---

## Author
**Shreya Mishra**  
MBA in Business Analytics | Data Analyst  
Richmond, VA  

---

### Disclaimer
All hospital data are **simulated for academic and research purposes**.  
They do not represent any real patients or healthcare organizations.

