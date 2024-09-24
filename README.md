# TIL-thesis-2024

Urban Representation Learning for Liveability Assessment
========================================================

This project explores urban representation learning techniques to automate the operationalization of liveability assessments. It introduces a novel method called "ring aggregation" and compares it with existing approaches.

Key Components:
---------------
1. Data Preparation
2. Learning Strategy 1: Ring Aggregation (Novel approach)
3. Learning Strategy 2: Sequential Similarity Loss (Based on Urban2Vec and M3G)
4. Evaluation of aerial embeddings

Data Preparation Scripts:
-------------------------
- Step 0 - study area preparation weighted average.ipynb
- Step 1 - download aerial images.ipynb
- Step 1 - embeddings aerial.ipynb
- Step 1 - embeddings POI.ipynb
- Step 1 - embeddings streetview.ipynb
- Step 1 - embeddngs GTFS RN.ipynb
- Step 2 - embeddings aerial photos 10.ipynb
- Step 2 - embeddings aerial photos FINETUNE resolution 10.ipynb
- Step 2 - embeddings aerial photos FINETUNE resolution agnostic.ipynb
- Step 2 - euclidean distance.ipynb

Learning Strategy 1 (Ring Aggregation) Scripts:
-----------------------------------------------
- learning strategy 1 - simple aggregation flexible experimentation.ipynb
- learning strategy 1 - learnt aggregation flexible experimentation.ipynb

Learning Strategy 2 (Urban2Vec/M3G adaptation) Scripts:
------------------------------------------------------
- learning strategy 2 step 2 v3.ipynb
- learning strategy 2 step 3 v2.ipynb

Evaluation:
-----------
- aerial photos infer.ipynb

Data Sources:
-------------
- Road network data (OpenStreetMap)
- General Transit Feed Specification (GTFS) data
- Points of Interest (POI) data (OpenStreetMap)
- Street view images (Google Street View)
- Aerial images (PDOK)
- Leefbaarometer scores

Models:
-------
1. Ring Aggregation (Novel approach)
   - Utilizes spatial convolutions on H3 hexagonal grid
   - Configurable number of k-rings and weighting schemes

2. Sequential Similarity Loss (Based on Urban2Vec and M3G)
   - Three-step process: aerial images, POI data, proximity measures

Evaluation:
-----------
- Predictive accuracy for Leefbaarometer scores
- Agglomerative clustering visualization

Key Findings:
-------------
- Ring aggregation outperforms existing approaches across Leefbaarometer scores
- Different aspects of liveability operate at varying spatial scales
- Data source selection significantly impacts predictive performance

Requirements:
-------------
- PyTorch
- SRAI (Spatial Representations for Artificial Intelligence) package
- Standard packages like (geo)pandas, math, numpy etc.

Usage:
------
1. Run data preparation scripts in numerical order (Step 0, Step 1, Step 2)
-. Execute Learning Strategy 1 scripts for the novel ring aggregation method
-. Execute Learning Strategy 2 scripts for the Urban2Vec/M3G adaptation

For detailed information on the methodology, results, and discussion, please refer to the full thesis document and Appendix A.
