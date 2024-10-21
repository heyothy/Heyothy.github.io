---
layout: single
title: Visualization Display
permalink: /kaggle-Visual/
toc: true
toc_label: "Kaggle Visualization"
toc_icon: "code"
sidebar:
  nav:
    - phishtank
    - kaggle
    - shodan
---

### Heat Map

* This chart identifies where anomalies in the transaction data are located.
* The various colors represent the values of the transactions, and then where the fraudulent transactions occurred.
* The darker colors, from black (0.0) to where the red starts (0.4) represent weaker correlations.
* From 0.4 through white (1.0) the correlations are stronger.
* The default value of numeric_only in the Data Frame is deprecated.
* In a future version, it will default to false.
* This was created by Ashish Jayswal.

![heat-map](/assets/kaggle-heat-map.png)

Source: [link](https://www.kaggle.com/code/ashishkumarjayswal/insaid-internship-task-with-froud-dataset)

* Represents the number of legit and fraudulent transactions.
* Y-Axis represents the Count of transactions.
* X-Axis represents whether the transaction is legit or fraud.
* This chart was present in the INSAID Internship Task with Froud_Dataset in Kaggle.
* This was created by Ashish Jayswal.

### Column Chart

![column-chart](/assets/kaggle-column-chart.png)

Source: [link](https://www.kaggle.com/code/ashishkumarjayswal/insaid-internship-task-with-froud-dataset)

### Isolation Forest

* Represents outlier transactions which are likely fraudulent.
* Model is trained on the transaction data to learn patterns of normal transactions.
* Trained to predict potential fraud (which would be the anomalies).
* Red dots are the outliers, while blue dots are deemed as regular.

![isolation-forest](/assets/kaggle-isolation-forest.png)

Source: [link](https://www.kaggle.com/code/ashishkumarjayswal/insaid-internship-task-with-froud-dataset)