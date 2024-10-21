---
layout: single
title: Analytical Approach
permalink: /shodan-analytics/
toc: true
toc_label: "Shodan Analytics"
toc_icon: "code"
sidebar:
  nav:
    - phishtank
    - kaggle
    - shodan
---

### IP Reputation
**_Shodan continuously scans the internet, collecting information about the devices and vulnerabilities located. Devices connected to the internet have their own IP addresses. Being able to cross reference the IP Reputation of devices you are connecting with can be essential in maintaining security._**
{: .notice--info}

**Why selected**
* Shodan's primary data source has associated IP addresses, making this a logical evaluation technique.
* Low scoring IP addresses have a higher likelihood of malicious activity.
* Potentially malicious IP Addresses can be blocked, providing a proactive defense.

**Value of the approach**
* The source data doesn’t need any involved processing or cleansing Reputation; be evaluated, it’s essentially a hand-off of the data between the source and the evaluation technique.
* The results are clear with a score assigned to the IP Reputation; lower scores are associated with lower trustworthiness. 
* These processes can be automatically analyzed with AI, reducing or removing manual methods and increasing response time making this approach very timely.

**Data sources required**
* Shodan already provides the data as the nature of its function.
* Queries need to be run within the Shodan API to produce the records of the particular area being focused on.

**Steps of the approach**
* Step 1: A Shodan dataset is generated through commands entered into the API and downloaded, or a precompiled dataset can be used.
* Step 2: The data is sorted based on the particular area being evaluated by their associated IP addresses.
* Step 3: The IP addresses are cross-referenced and the reputation score is identified, flagging lower scored items so they can be acted upon either by blocking or monitoring.

### Data Mining
**_With a source like Shodan we could use predictive analytics with classification to identify vulnerabilities in our systems._**
{: .notice--info}

**Why selected**
* Data mining helps you gain insights in large data repositories like Shodan.
* Structured data, such as in Shodan, is easily parsed with data mining.

**Value of the approach**
* Predictive analysis such as clustering helps focus attention where it’s needed most.
* Data mining can also help with anomaly detection to flag items for security responses quicker.

**Data sources required**
The same Shodan data production techniques previously described.
_Steps of the approach:_
* Step 1: A Shodan dataset is generated through commands entered into the API and downloaded, or a precompiled dataset can be used.
* Step 2: The data is cleaned and sorted by features such as number of open ports, device types and vulnerability counts.
* Step 3: Normalization might need to be done as results might have different scales.
* Step 4: Selection of a feature, this could be open/vulnerable ports, CVE Counts for a device, device type, etc.
* Step 5: Select the algorithm, such as K-means.

### Graph Analysis
_**"Shodan tracks and scans connected devices and graph analysis examines the relationships between those devices. It looks at the nodes and connected networks in a system. It’s an ideal technique for a data source such as Shodan. Graphing the network of an institution could help show where a vulnerability might exist."**_
{: .notice--info}

Why selected
* Graph analysis helps visualize the relationships between connected devices.
* It can help visualize the magnitude of a particular item by grouping things by a countable feature, such as number of devices of a type.

Value of the approach 
* This approach can help identify nodes in a network that are more vulnerable to attack. 
* Clear visuals of the devices of a certain type can help focus defenses on a networks most prevalent type, especially if that item has a known vulnerability.
* Patches or security upgrades could be focused on one feature, such as if a lot of Windows 7 devices were still in use.

Data sources required:
The same Shodan data production techniques previously described.

Steps of the approach:
* Step 1: A Shodan dataset is generated through commands entered into the API and downloaded, or a precompiled dataset can be used.
* Step 2: The data is cleaned and sorted by features, nodes and edges are determined.
* Step 3: Determine how to structure the graph. 
  - If bar graph: what increments on the y-axis, which data will be best displayed on the x-axis.
  - If network graph - determine which nodes to focus on, focusing on vulnerabile areas.