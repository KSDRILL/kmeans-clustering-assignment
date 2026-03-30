# K-Means Clustering for Dense Network Topology Analysis

## Project Overview
This project implements unsupervised machine learning (K-Means clustering) to analyze complex network structures comprising 600+ interconnected nodes with spatial coordinates and simulated energy levels. The system demonstrates how computational analysis outperforms visual interpretation in dense, overlapping network topologies.

## Key Features
- **Network Generation**: Stochastic block model with 7 communities and controlled connectivity (intra: 0.27-0.32, inter: 0.05)
- **Spatial Compression**: Algorithmic positioning with community-specific scaling and jitter to simulate realistic dense networks
- **Energy Simulation**: Random energy distribution (10-100 units) representing battery levels or resource availability
- **K-Means Clustering**: Configurable cluster counts (k=3, 7) with centroid analysis
- **Multi-dimensional Visualization**:
  - 2D network topology with color-coded clusters
  - 3D scatter plots with energy as z-axis
  - Smooth 3D surface plots with cubic interpolation
- **Statistical Analysis**: Cluster-wise energy profiling and critical node identification

## Technical Stack
- **Python 3.x**
- **Scikit-learn**: K-Means clustering implementation
- **NetworkX**: Graph generation and network analysis
- **NumPy/Pandas**: Data processing and statistical computations
- **Matplotlib**: 2D and 3D visualizations
- **SciPy**: Spatial interpolation for surface mapping

## Results
### Clustering with k=7
- 7 distinct clusters based on spatial proximity
- Cluster sizes range from 75-95 nodes
- Energy distribution varies across clusters (avg: 45-65 units)
- Centroids positioned at spatial centers of each cluster

### Clustering with k=3
- 3 merged clusters demonstrating hierarchical grouping
- Larger cluster formations (approx. 200 nodes each)
- Average energy values more balanced across clusters
- Centroids repositioned to reflect broader spatial groupings

## Key Insights
1. **Algorithm Limitations**: K-Means clusters solely based on spatial proximity, ignoring energy values
2. **Parameter Sensitivity**: Changing k from 7 to 3 significantly alters cluster boundaries and centroids
3. **Computational Analysis**: Visual interpretation alone is insufficient for dense networks
4. **Critical Node Detection**: Low-energy nodes (<20 units) distributed across all clusters

## Installation & Usage
```bash
# Clone repository
git clone https://github.com/[username]/kmeans-clustering-network-analysis.git

# Install dependencies
pip install numpy pandas matplotlib networkx scikit-learn scipy

# Run with k=7
python kmeans.py

# Modify cluster count (edit k=3 in script)
python kmeans.py
