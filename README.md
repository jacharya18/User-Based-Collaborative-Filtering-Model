# 🧩 User-Based Collaborative Filtering Model
**Author:** Jai Acharya  

---

## 📋 Table of Contents
- 🤖 [Introduction](#-introduction)  
- ⚙️ [Tech Stack](#-tech-stack)  
- 🔬 [Methodology](#-methodology)  
- 📊 [Results](#-results)  
- 💼 [Business Analytics Connection](#-business-analytics-connection)  
- 🔋 [Features & Highlights](#-features--highlights)  
- 🔗 [Links & Resources](#-links--resources)  
- 🚀 [Future Improvements](#-future-improvements)  
- 🧾 [Author](#-author)  
- 🏁 [Summary](#-summary)  

---

## 🤖 Introduction

**User-Based Collaborative Filtering Model** is a data science project that implements a **recommender system** using the classic *user-to-user collaborative filtering* algorithm.  

The goal is to predict which products a customer is likely to purchase next — based on the buying behavior of similar users.  

This model, coded entirely from scratch in **NumPy** and **pandas**, forms the foundation of modern recommender engines used by Amazon, Netflix, and Spotify.  
It showcases a solid understanding of **customer analytics**, **data-driven personalization**, and **algorithmic implementation** for business applications.  

Developed as part of the *MKTG 722: Data Science for Business Decision Making* course by **Rafael Becerril Arreola**, this project demonstrates the bridge between **analytical methods** and **business value creation**.

---

## ⚙️ Tech Stack

- 🐍 **Python 3.10+**  
- 📦 **pandas** – Data manipulation and preparation  
- 🔢 **NumPy** – Numerical computation and similarity matrices  
- 🧮 **Jupyter Notebook** – Interactive analysis and documentation  

---

## 🔬 Methodology

### 🎯 Objective  
Generate personalized product recommendations for each customer using a **user-based collaborative filtering** algorithm built from first principles.

### 🧩 Workflow Overview  

#### 1. Data Preparation  
- Dataset: `User_Data.csv`  
- Rows represent **customers**, columns represent **products**.  
- Entries:  
  - `1` = product purchased  
  - `0` = product not purchased  

#### 2. Similarity Computation  
Calculated pairwise **matching coefficients** for all customer pairs:  

m(j, k) = Σₚ I(xⱼₚ = xₖₚ)


where \( I \) is an indicator function equal to 1 if both customers have the same purchase status for product *p*.  
- Diagonal elements (self-similarity) were set to `NaN` to exclude the user themselves.  

#### 3. Recommendation Logic  
For each user:  
- Identify **most similar customer(s)** with the highest matching coefficient.  
- Gather all products purchased by similar users but **not yet purchased** by the target user.  
- Output this list as recommendations.  

## 📊 Results

| Customer | Recommended Products |
|-----------|----------------------|
| 1 | 1, 3, 4, 6, 7, 8, 10 |
| 2 | – |
| 3 | 1 |
| 4 | 6 |
| 5 | 1, 3, 5, 7 |

✅ **Outcome:** Successfully produced personalized recommendations using pairwise similarity and logical filtering.  

🧠 **Interpretation:**  
- Customers with overlapping purchase patterns receive similar recommendations.  
- Sparse data leads to fewer or no suggestions for some users — a natural limitation in smaller or incomplete datasets.  
- Algorithm correctly follows academic pseudocode and delivers interpretable results.

---

## 💼 Business Analytics Connection

This project is a **direct application of business analytics in action**.  
It connects data science techniques to tangible commercial goals:  

- 🎯 **Personalization:** Enables businesses to tailor product recommendations to individual users, increasing conversion and engagement.  
- 💰 **Cross-Selling & Upselling:** Identifies high-probability items for promotion based on behavioral similarity.  
- 🧩 **Customer Segmentation:** Groups users by behavior rather than demographics, improving campaign precision.  
- 📈 **Revenue Optimization:** Turns customer data into actionable insights that drive purchasing activity.  
- 🧭 **Decision Support:** Provides the analytical framework for marketing teams to prioritize product placement and personalized promotions.  

In essence, this project shows how **data-driven algorithms power real-world business strategies** and how **quantitative models drive qualitative outcomes** in customer experience.

---

## 🔋 Features & Highlights

✅ 100% manual algorithm implementation (no external ML libraries)  
✅ Recreates the logic behind modern recommender systems  
✅ Uses efficient pairwise similarity computations with pandas & NumPy  
✅ Demonstrates understanding of cold-start and scalability limitations  
✅ Clear and well-documented Jupyter workflow  
✅ Output directly interpretable for marketing and business applications  

---

## 🔗 Links & Resources

📘 **Notebook:** `User_Based_Collaborative_Filtering_Model.ipynb`  
📊 **Dataset:** `User_Data.csv`  
📄 **Assignment Brief:** `MKTG722E1_C80104624.pdf`  

**Key References:**  
- [Collaborative Filtering – Wikipedia](https://en.wikipedia.org/wiki/Recommender_system)  
- [Amazon Science – Recommendation Systems](https://www.amazon.science/latest-news/recommendation-systems)  
- [pandas Documentation](https://pandas.pydata.org/docs/)  
- [NumPy Documentation](https://numpy.org/doc/)  

---

## 🚀 Future Improvements

- Implement **item-based collaborative filtering** for greater scalability.  
- Use **cosine similarity** or **Pearson correlation** instead of simple match counts.  
- Introduce **hybrid approaches** (combine CF with content-based recommendations).  
- Address **cold-start** using demographic or implicit feedback data.  
- Deploy an **interactive Streamlit dashboard** for business demo and visualization.  

---

## 🧾 Author

👤 **Jai Acharya**  
📧 jacharya@email.sc.edu
💼 [[LinkedIn / Portfolio URL] ](https://www.linkedin.com/in/jai-acharya/) 

---

## 🏁 Summary

A technically rigorous, business-aligned implementation of a **user-based collaborative filtering model**.  

Demonstrates:  
- Deep understanding of recommendation system design and its mathematical foundation.  
- Strong alignment between data science techniques and marketing strategy.  
- Professional-grade documentation and reproducibility for business analytics projects.  

> 🚀 *“Turning customer behavior into strategic insight — that’s the future of business analytics.”*  
