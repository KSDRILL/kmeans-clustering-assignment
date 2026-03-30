# K-Means Clustering for Dense Network Topology Analysis

![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Status](https://img.shields.io/badge/status-completed-brightgreen.svg)

## 📋 Project Overview

This project implements unsupervised machine learning using **K-Means clustering** to analyze complex network structures comprising **600+ interconnected nodes** with spatial coordinates and simulated energy levels. The system demonstrates how computational analysis outperforms visual interpretation in dense, overlapping network topologies.

This assignment was completed as part of **CMPG 313 - Artificial Intelligence** course, exploring real-world applications such as Wireless Sensor Networks (WSN), Internet of Things (IoT) deployments, and distributed computing systems.

---

## 🎯 Learning Objectives

- Apply K-Means clustering using scikit-learn's KMeans function
- Analyze dense network topology with 600+ nodes
- Interpret clustering results using data-driven reasoning
- Visualize data using 2D network graphs and 3D surface plots
- Extract insights from node energy distributions
- Understand algorithm limitations and parameter sensitivity

---

## 🏗️ Technical Architecture

### Core Technologies

| Technology | Purpose |
|------------|---------|
| **Python 3.x** | Primary programming language |
| **Scikit-learn** | K-Means clustering implementation |
| **NetworkX** | Graph theory operations and network topology generation |
| **NumPy/Pandas** | Data manipulation and statistical analysis |
| **Matplotlib** | 2D and 3D visualization with surface interpolation |
| **SciPy** | Spatial interpolation for energy surface mapping |

### Key Components

1. **Stochastic Block Model Generation**
   - Community-based graph structure with 7 distinct blocks
   - Intra-community connection probabilities: 0.27-0.32
   - Inter-community connectivity: 0.05 (simulating realistic network density)

2. **Spatial Compression Algorithm**
   - Spring-layout positioning (k=0.11, 300 iterations)
   - Community-specific spatial compression (scale factor: 0.18)
   - Stochastic jitter (±0.025) to prevent perfect separation

3. **Energy Distribution Modeling**
   - Random energy values: 10-100 units (simulating battery levels)
   - Decoupled from spatial positioning to test clustering efficacy

4. **K-Means Clustering Engine**
   - Configurable cluster count (k=3, 7)
   - 10 initializations for stable convergence
   - Random state 42 for reproducibility

---

## 📊 Results & Analysis

### Clustering Configuration 1: k=7

| Metric | Value |
|--------|-------|
| Number of Clusters | 7 |
| Total Nodes | 600 |
| Cluster Size Range | 75-95 nodes |
| Energy Range | 10-100 units |
| Centroids | 7 spatial centers |

**Cluster Breakdown:**
- Clusters formed based on spatial proximity
- Energy distribution varies significantly across clusters
- Critical low-energy nodes (<20 units) distributed across all clusters

### Clustering Configuration 2: k=3

| Metric | Value |
|--------|-------|
| Number of Clusters | 3 |
| Total Nodes | 600 |
| Cluster Size | ~200 nodes each |
| Centroids | 3 spatial centers |

**Key Observations:**
- Clusters merged to form larger spatial groupings
- Average energy values more balanced across clusters
- Centroids repositioned to reflect broader spatial regions

### Comparative Analysis

| Aspect | k=7 | k=3 |
|--------|-----|-----|
| Granularity | High | Low |
| Cluster Definition | Specific | General |
| Energy Distribution | Variable per cluster | More balanced |
| Centroid Count | 7 | 3 |
| Interpretation | Detailed | High-level |

---

## 🔍 Key Insights

### 1. Algorithm Limitations
K-Means clusters solely based on spatial proximity, ignoring energy values. Low-energy nodes are distributed randomly across all clusters.

### 2. Parameter Sensitivity
Changing k from 7 to 3 significantly alters:
- Cluster boundaries
- Centroids positions
- Group membership

### 3. Computational Analysis Importance
Visual interpretation alone is insufficient for dense, overlapping networks. Data-driven analysis is essential.

### 4. Critical Node Detection
Low-energy nodes (<20 units) can be identified across clusters for proactive maintenance.

---

## 🚀 Installation & Usage

### Prerequisites
- Python 3.8 or higher
- pip package manager

### Installation Steps
# Clone the repository
git clone https://github.com/KSDRILL/kmeans-clustering-network-analysis.git
cd kmeans-clustering-network-analysis

# Create virtual environment (recommended)
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On Mac/Linux:
source venv/bin/activate

# Install dependencies
pip install numpy pandas matplotlib networkx scikit-learn scipy
