# ⚙️ CLM Process Capability Analysis Based on Lindley Distribution  
### 📊 A New Approach for Asymmetric Distributions in Manufacturing Processes  


## 🎯 Project Overview

This project is a statistical analysis study developed to **measure process capability more accurately** by considering **asymmetric (non-normal)** distributions in manufacturing processes.  

Classical process capability indices (**Cp, Cpk**) are generally calculated under the **normal distribution assumption**.  
However, in real production environments (such as automotive, defense, medical devices, chemistry, etc.), data often show **asymmetric characteristics**.  

Therefore, within the scope of this project, a new index called **CLM (Capability Life Measurement)** was proposed using the **Lindley Distribution**.  
This index provides **more accurate, flexible, and reliable** results compared to traditional PCI measures.


## 💼 Application Perspective

This study aims to develop a **scalable and reliable process evaluation model** that can be applied in **production and quality management** across different industries.  

The project is designed to contribute to quality control analyses commonly used in the **automotive, defense, energy, and manufacturing** sectors.  
Analyses conducted on real production data showed **lower error rates** and **higher model consistency** compared to classical methods.  

### 🔹 Real-World Application

An analysis was conducted on a manufacturing process for an automotive part with 60 observations:  

| Parameter       | Value  |
|-----------------|---------|
| Lower Limit (LSL) | 1.4   |
| Upper Limit (USL) | 2.3   |
| Target Value (T)  | 1.75  |
| Mean (μ)          | 1.7375 |
| Variance (σ²)     | 0.0169 |
| **CLM Index**     | **1.15** |

**Result:**  
The process is under control, variance is low, and the mean is very close to the target value.  
Since CLM > 1, the process is within an **acceptable quality level**, but **still open to improvement**.


## 🧠 Academic and Technical Background

### 🔸 What is the CLM Index?
The CLM (Capability Life Measurement) index is a metric that measures both **process quality and lifetime performance**.  
The Lindley distribution provides a **more flexible and asymmetric** structure compared to classical normal distributions.

1) Lindley probability density function:  
<img width="424" height="73" alt="image" src="https://github.com/user-attachments/assets/3a125105-a0a7-4f3f-b9a7-2b2dacb18552" />

2) Proposed CLM formula:  
<img width="532" height="68" alt="image" src="https://github.com/user-attachments/assets/88cf8c15-d95e-49f8-9f14-729ee92682d8" />

Where:  
- \( M \): Median  
- \( L \): Lower specification limit  
- \( δ = \frac{M - μ}{σ} \)

This approach accounts for the **asymmetry of the process**, providing a more accurate reflection of **true quality performance**.


## 💻 Tools and Technologies Used

| Tool / Library | Description |
|------------------|-------------|
| **R (v4.3)** | Statistical computation and simulation |
| **VGAM** | Lindley distribution modeling |
| **lamW** | Calculation using Lambert W function |
| **ggplot2** | Data visualization |
| **Monte Carlo Simulation** | Parameter estimation and error analysis |
| **Bootstrap** | Confidence interval estimation |


## 📈 Simulation Results

| θ (Theta) | Bias | MSE | ABB | MRE | Performance |
|-----------|------|-----|-----|-----|--------------|
| 0.2       | ↓    | ↓   | ↓   | ↓   | Consistent model |
| 0.5       | ↓↓   | ↓↓  | ↓   | ~0  | Best performance |
| 0.7       | ↑↑   | ↑↑  | ↑↑  | ↑↑  | Inconsistent model |

### 🔹 Summary:

- For small and medium θ values (0.2–0.5), the model shows **high accuracy**.  
- For high θ values (0.7), bias and error increase → model stability decreases.  
- The CLM index provides **more reliable results** for asymmetric processes compared to traditional Cp–Cpk indices.


## 📊 Visualizations

The following graphs were used in the analysis:  
- **Bias, MSE, ABB, MRE** variation charts  
- **Process distribution and specification limits** (histogram)  
- **CLM vs Cp/Cpk comparison**


## 🧩 Key Contributions

✅ More accurate analysis than traditional PCI methods for asymmetric data  
✅ Parametric validation using Monte Carlo simulation  
✅ Real-world data implementation and visualization  
✅ Integrated use of R, statistics, and data science tools  


## 👤 Author

**Yunus Ahmet Dokazoğlu**  
🎓 Selçuk University – Department of Statistics  
📍 Türkiye  

🔗 [My GitHub Profile](https://github.com/AhmetDokazoglu)  
🔗 [My LinkedIn Profile](https://www.linkedin.com/in/ahmet-dokazo%C4%9Flu-9660b2346/)


### 📎 Additional Documents  

📄 [Download Project Report (Word Version)](https://github.com/AhmetDokazoglu/Lindley-Dagilimi-ile-CLM-Surec-Yeterlilik-Analizi/raw/refs/heads/main/Lindley%20Dagilimi%20ile%20CLM%20Surec%20Yeterlilik%20Analizi.docx)  


## 💬 Summary Evaluation

> This project goes beyond traditional process capability analyses and provides a **more realistic quality measurement under asymmetric data structures**.  
> It offers a strong statistical foundation that can be used in **academic research** as well as in **manufacturing, quality management, and data analytics projects**.
