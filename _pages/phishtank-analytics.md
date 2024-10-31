---
layout: single
title: Collection Strategies
permalink: /phishtank-analytics/
toc: true
toc_label: "Phishtank"
toc_icon: "code"
sidebar:
  nav:
    - phishtank
    - kaggle
    - shodan
---

### Time Series
**_"Financial institutions need to adapt their security measures to combat the evolving phishing landscape."_**
{: .notice--info}

**Why selected**
* Understand the evolution of the phishing threat.
* Identify trends, seasonality, and potential future risks.
* Anticipate and adapt to the evolving threat landscape.

**Value of the approach**
* Analyze patterns not apparent in other analyses.
* Make informed security decisions and implement proactive measures.

**Data sources required**
* PhishTank - public database of verified phishing URLs.

**Steps of the approach**
* Data Cleaning: Remove duplicate or irrelevant data.
* Data Aggregation: Group data by year.
* Trend Analysis: Identify upward or downward trends, seasonality.
* Forecasting: Predict future phishing attempts.

### Clustering
**_"Understanding these phishing groups and their targets is essential for tailoring security measures and implementing targeted defences."_**
{: .notice--info}

**Why selected**
* Reveal hidden patterns in data.
* Identify groups of phishing URLs with similar characteristics.
* Understand potential organized phishing campaigns and attacker tactics.

**Value of the approach**
* Understand the structure of phishing data.
* Identify patterns that might not be apparent in time series analysis.

**Data sources required**
* PishTank - provides a diverse set of phishing URLs.

**Steps of the approach**
* Feature Extraction: Extract features like 'target', 'online', and 'verification_time'.
* Similarity Metric: Use Euclidean distance to measure similarity.
* Clustering Algorithm: Apply K-Means Clustering to group similar phishing URLs.
* Cluster Interpretation: Analyze clusters and their characteristics.

### Text Mining
**_"Text mining provides valuable insights into the tactics, methods, and motives of phishing attackers."_**
{: .notice--info}

**Why selected**
* Understand the language and content of phishing URLs.
* Identify potential threats, attacker motives, and common attack tactics.
* Safeguard sensitive data.

**Value of the approach**
* Analyze phishing URLs beyond basic URL analysis.
* Gain insights into attacker goals and methods.

**Data sources required**
* Phishtank – rich repository of phishing URLs.

**Steps of the approach**
* Tokenization: Break URLs into words or keywords.
* Stop Word Removal: Eliminate common words. 
* Feature Extraction: Create a vector representation of each URL using TF-IDF weighting.
* Text Analysis: Apply text classification and topic modeling.
