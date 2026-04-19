# M25DE1075_CSL7110_ASSIGNMENT4


 Assignment 4: Clustering, Inverted Index & PageRank

Name: Pramod Behera
Roll No: M25DE1075



 Project Overview

This repository contains implementations of three core data mining and information retrieval tasks:

1. Clustering Algorithms (k-center, k-Means++)
2. Inverted Index & Search Engine
3. PageRank using PySpark and Python

The project demonstrates efficient algorithm design, vectorized computation, and scalable data processing.


Project Structure

```
├── Assignment4.ipynb     # Main implementation notebook
├── README.md            # Project documentation
├── data/                # Dataset files (if applicable)
```



 Part 1: Clustering

Implemented Algorithms

k-center (Farthest-First Traversal)
k-Means++ Initialization**
k-Means Objective Function**
Vector Reader using PySpark Dense Vectors**

 Dataset

* UCI Spambase Dataset
* 4,601 samples, 57 features

 Key Results (k = 10)

* k-center runtime: 0.0198 s
* k-Means++ runtime: 0.0157 s
* k-Means++ objective: 27,438.08

 Observations

* k-Means++ improves clustering quality as k increases
* k-center selects boundary points (geometric spread)
* Hybrid approach requires larger coreset for better performance


Part 2: Inverted Index & Search Engine

Implemented Components

* Custom data structures: MySet, WordEntry, PageIndex
* Core system: InvertedPageIndex, SearchEngine
* Hash-based indexing with O(1) lookup

Features

* Text normalization (punctuation removal, stemming)
* Stop-word filtering
* TF-IDF ranking
* Phrase query support

 Performance

* Queries executed: 11
* Correct outputs: 10 / 11
* Accuracy: 90.9%


 Part 3: PageRank

 Implementation

* PySpark RDD-based PageRank
* Pure Python implementation

 Parameters

* Damping factor (β): 0.8
* Iterations: 40
* Convergence: L1 norm

Results

Small Graph (100 nodes)

* Top rank ≈ 0.0357
* Converged successfully 

Large Graph (1000 nodes)

* Rank distribution more uniform due to scale

 Observations

* Efficient convergence using power iteration
* Spark avoids costly data collection each iteration
* Proper handling of dangling nodes


 Technical Highlights

* Fully vectorized clustering using NumPy
* Efficient search engine with **hash-based indexing
* Scalable PageRank using PySpark
* Reproducible results with fixed random seed



 Limitations

* Hybrid clustering less effective for small k
* Minor mismatch in one search query
* Spark tested in local mode (limited scalability testing)



 Future Improvements

* Improve tokenization for edge cases
* Optimize hybrid clustering approach
* Deploy PageRank on a real distributed cluster





