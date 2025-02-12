# Unsupervised-Entity-Matching
Bridging the Gap: Efficient Unsupervised Entity  Matching Across Multiple Tables

## Overview
This project implements an advanced data integration solution using semantic embeddings and intelligent record linking techniques. The framework can merge and resolve records across multiple datasets with high precision and recall.

## Features
Intelligent attribute selection
Semantic embedding using SentenceTransformer
record merging using k-nearest neighbor search
Noise reduction through pruning

#### Folder: Code Scripts --> Folder: data: Contains folders Music_20 and Music_200. 
##### Folder Music_20: table_0.csv, table_1.csv , table_2.csv , table_3.csv , table_4.csv 
##### Folder Music_200: table_0.csv, table_1.csv , table_2.csv , table_3.csv , table_4.csv  

## Jupyter Notebook: 'final_script_pysc_681.ipynb'
Please note: In order to test the logic, I've included Music_20, a smaller dataset. It will take approximately 8 minutes to run using GPU in narnia.
Music_200 dataset is a huge dataset. It will take 35 minutes to run. I have included another code script 'final_script_music_200.ipynb' with my results when I ran it. The logic is same.
#### Required Libraries
numpy
pandas
sentence-transformers
hnswlib
scikit-learn
torch
tqdm
loguru

#### Sections in final_script_psyc_681:
- Compress sections (for easier navigation) 
1) Import Libraries
2) Setting GPU
3) Class Table - preprocessing tables
4) Class Timer - Helps to record time for each step
5) Logging functions
6) Approximate Nearest Neighbourhood Search Function - (HNSW library used)
7) MainArgs - dataclass to configure various parameters
8) Method to select only the important attributes
9) Merging tables by finding similar records by using KNN-Search
10) Class Pruner: Pruning Outliers and mismatched pairs
11) Class Metric - Evaluate F1 and Pair-wise F
12) Main Process
13) Visualization of predictions


#### Running the file
1) Set your GPU. Change your GPU ID.
2) In MainArgs:
- Change data_path and data_name.
- data_path is the folder in which Music_20 and Music_200 are stored.
- data_name: Music_20 or Music_200
- After changing these two variables. Run all cells.

##### The main block ties everything together:
- Read tables
- Select attributes
- Generate embeddings
- Merge tables using knn search
- Prune results
- Evaluate performance
- Visualize clusters.
