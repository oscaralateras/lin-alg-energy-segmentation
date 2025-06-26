# lin-alg-energy-segmentation  
🔌 Manual PCA and K-Means on AusGrid electricity data to segment households and explore smarter energy pricing strategies using core linear algebra concepts.

## 🧠 Project Goal  
This project demonstrates how core linear algebra techniques can be used in machine learning, such as  Principal Component Analysis (PCA) and K-Means Clustering, to solve a real-world business problem: segmenting electricity customers for more effective pricing.

## 📊 Dataset  
- **Source**: [AusGrid Solar Home Electricity Dataset](https://www.kaggle.com/datasets/youssefboutaleb/ausgrid-2024)
- **Scope**: 300 residential households in Sydney, Australia  
- **Timeframe**: July 2012 – June 2013  
- **Resolution**: 48 half-hour intervals per day  

## 🛠️ Tools & Libraries  
- **NumPy** – manual matrix operations, projections, and distance calculations  
- **Pandas** – data cleaning, wrangling, and aggregation  
- **Matplotlib** – scree plots, PCA component visualisations, and cluster plots  
- *(No external ML libraries like scikit-learn were used)*

## 📂 Key Notebook Sections (`LinAlgProject.ipynb`)
### 1. Preprocessing  
- Load and clean the CSV  
- Drop low-quality or inactive profiles  
- Aggregate each household’s average daily profile  
- Standardise features (z-score)

### 2. Principal Component Analysis (PCA)  
- Manually calculate the covariance matrix  
- Perform eigendecomposition  
- Plot a **scree plot** to retain components explaining 80% of the variance (4 PCs)  
- Project standardised data into lower-dimensional PC space  
- Visualise component loadings to interpret usage patterns

### 3. K-Means Clustering  
- Run K-Means for `k = 2 to 10` and plot inertia (elbow method)  
- Select optimal `k = 5`  
- Assign households to clusters  
- Plot average load profiles for each cluster  
- Plot clusters in 2D PCA space

## 💡 Business Application  
- Compact clusters indicate consistent behaviour → suitable for standard tariffs  
- Dispersed clusters reveal diverse usage → may benefit from flexible or personalised pricing  
- Time-of-day patterns highlight opportunities for **time-of-use incentives** or **demand-shift strategies**

## ✅ What I Learned  
- Hands-on understanding of how PCA and K-Means work mathematically  
- How linear transformations (projections) can expose structure in high-dimensional data  
- How to connect abstract maths to real-world utility pricing decisions

## 📁 File  
- `LinAlgProject.ipynb`: Fully commented and structured notebook with all code, plots, and output

## 🔗 Try It Yourself  
Clone this repo and run the notebook locally, or open it in Google Colab or JupyterLab.  
Pull requests and feedback welcome!

