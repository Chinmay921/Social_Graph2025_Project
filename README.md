# Network Structure, Temporal Evolution and Non-protagonist Hubs in The Simpsons

**Course:** 02805 Social Graphs and Interactions  
**Institution:** Danmarks Tekniske Universitet (DTU)  
**Authors:** Yashasvi Tirpur Vishwanath, Chinmay Prasad Dongarkar, Vaibhav Anil Nagwani

## Project Overview

This project analyzes the network structure of 104 secondary characters from The Simpsons using wiki-based co-appearance data from 753 episodes. We examine:

1. **Community Detection**: How secondary characters cluster into social and thematic groups
2. **Temporal Evolution**: How network structure changes across seasons
3. **Non-protagonist Hubs**: Which characters emerge as structural connectors when central nodes are removed
4. **Text-Network Alignment**: Relationship between structural communities and semantic similarity

## Key Findings

- **Network Properties**: 104 nodes, 161 edges, density 0.030, 32 connected components
- **Community Structure**: 38 communities detected with modularity Q = 0.420
- **Small World Properties**: Diameter of 6, average path length 2.84, clustering coefficient 0.27
- **Text-Network Alignment**: Characters in the same community show significantly higher semantic similarity (p < 0.001)

## Repository Structure

```
├── Group25_simpsons_Project_B.ipynb          # Main analysis notebook
├── Figures/                      # Generated figures
│   ├── figure1_network_overview.png
│   ├── figure2_centrality_comparison.png
│   ├── figure3_temporal_evolution.png
│   └── figure4_non_protagonist_hubs.png
├── wiki_pages_simpsons_copy/     # Character wiki data (499 files)
├── character_centralities.csv    # Centrality measures
├── character_centrality_comparison.csv
└── character_temporal_trajectories.csv
```

## Requirements

```bash
pip install networkx pandas numpy matplotlib seaborn scikit-learn nltk scipy
```

## Methods

- **Network Construction**: Bipartite character-episode network projected to character-character co-appearance network
- **Community Detection**: Louvain algorithm
- **Centrality Measures**: Degree, betweenness, PageRank, eigenvector, closeness
- **Text Analysis**: TF-IDF vectorization and cosine similarity
- **Temporal Analysis**: Season-based network slices across 5 eras

## Results

The analysis reveals:
- Strong modular organization with communities aligned to narrative settings (schools, workplaces, etc.)
- Temporal evolution toward specialization in later seasons
- Structural robustness with multiple alternative hubs
- Significant alignment between network structure and textual themes

## References

- Newman, M. E. J. (2018). *Networks: An Introduction* (2nd ed.). Oxford University Press.
- Barabási, A.-L. (2016). *Network Science*. Cambridge University Press.
- Blondel, V. D., et al. (2008). Fast unfolding of communities in large networks. *Journal of Statistical Mechanics*.
- Data source: [Simpsons Wiki](https://simpsons.fandom.com/wiki/Simpsons_Wiki)

## Authors

- **Yashasvi Tirpur Vishwanath** (s242563)
- **Chinmay Prasad Dongarkar** (s250155)
- **Vaibhav Anil Nagwani** (s242572)

## License

This project is for academic purposes as part of the 02805 Social Graphs and Interactions course at DTU.

## Acknowledgments

Data collected from Wikisimpsons (simpsons.fandom.com). Code and visualizations were refined with technical assistance.

