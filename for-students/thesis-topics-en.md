---
layout: page
title: Sample topics of masters' theses
permalink: /for-students/topics-en
exclude: true
---

Last updated: October 5, 2020

## Sample topics - for individual discussion

 1. Analysis and implementation of the k-means algorithm supported by the pi-cube structure.
 2. Experiments and implementation of an interactive data access methods using hierarchical data structures.
 3. Implementation and tests of a new method of density clustering based on the DBSCAN algorithm and the granular pi-cube structure.
 4. Implementation and tests of a new method of density grouping based on the NBC algorithm and the granular structure of pi-cube.
 5. Design and implementation of a web-based interactive data visualization module using the NYTC dataset (or another chosen large data set).
 6. Design and implementation of a web module for interactive visualization of large data sets on the example of the checkins dataset.
 7. Design and implementation of a module for testing the performance of hierarchical data structures with respect to data visualization and/or exploration.
 8. Adoptation of a chosed data clustering algorithm for approximate clustering based on the pi-cube hierarchical data structure.
 9. Clustering with constraints using neural networks as means to determine the distances between objects.
10. Implementation and analysis of the DBSCAN algorithm using the MADlib platform.
11. Implementation and analysis of the NBC algorithm using the MADlib platform.
    
A bit more details ...

## Interactive data visualization and mining

In the context of data mining, the word *interactive* reflects how data analysts expect their systems to work. In 1996, Shneiderman formulated a metaphor (known today as the Shneiderman's mantra) describing the process of data analysis and visualization: *Overview first, zoom and filter, then details on demand*. According to it, a process of interactive data analysis comprises the following steps: An analyst asks the system to perform an *analytical task*, waits for a response, and then analyzes it, that is, tries to understand and evaluate it. If he or she is unable to draw any meaningful conclusions on the system's response, the analyst changes the query's parameters and repeats the entire process. But if the system's response time is high - say, longer than five seconds - then such a process according to HCI (*human-computer interaction*) standards becomes cumbersome for the user. In such a situation, we cannot say that the data mining or analysis process is interactive. By operating on a large number of objects, the analyst is simply unable to get answers about the system in a short time. Nevertheless, assuming that the user is not always interested in *exact* results of the analysis (in many cases this is true), it may ba acceptable to design algorithms in a way that the user would receive an approximate answer but in a limited time. An example of a solution that uses this idea was the BlinkDB prototype database (Agrawal, 2013), which allowed users to issue queries with additional parameters specyfing expected time and quality of the result.

Taking into account the above we propose several topics below. Their common factor is the application of a special hierarchical structure (pi-cube) that allows accessing data with a given degree of granularity reducing the amount of data needed to be processed both in visualization or exploration.

![Simplified System Diagram]({{site.url}}/files/interactive-diagram-en.png)

**Sample topics**

<h3>A. Design and implementation of the programming interface of the interactive data visualization and mining system </h3>

The aim of the work is to design and implement a programming interface (API) in a chosen technology for an interactive data visualization and mining system. The API will be an interface between the relational database and other modules of the system (i.e. the visualization module and the analytical module). The API will interactively provide the client of the system with the data needed to perform operations such as:

* Creating and modifying the pi-cube structure based on the indicated data source (table in a relational database).
* Retrieving the indicated parameterized (using an appropriate filter) data fragment.
* Optimization of the method of data transfer between components in such a way as to maintain the interactivity of the system.

*Additional assumptions and requirements*:

* Preparation of a set of unit tests for the created software.
* Testing the API capabilities using an existing data visualization library (eg D3.js or ggplot).
* Perform experiments using different datasets (e.g. Checkins, New York Taxi Cab, Seattle Fire Calls, etc.).
* Presentation of the results of experiments in a clear and understandable form.

*Suggested implementation technologies*:

* Python
* Django
* JSON

<h3>B. Implementation of an interactive data visualization module using WebGL component</h3>
     
The aim of this task is to develop and implement an interactive data visualization module based on the WebGL component, which is an element of the HTML5 language. The module should meet the following assumptions:

* The module should have a java script library with which to access the data delivery module.
* The library should communicate with the data delivery module using the appropriate RESTful defined interface.
* For testing purposes, the module should allow you to replace references to the RESTful website with data from previously prepared JSON files.
* The basic functions of the data visualization interface should be supported, such as: *zooming in*, *zooming out*, *panning*, *selection*.

*Suggested implementation technologies*:

* Java Script
* HTML5 (WebGL)
* jQuery
* Bootstrap

<h3> C. Application of inductive data aggregation in selected algorithms density grouping </h3>

The aim of the task is to adapt (in cooperation with the supervisor, on the basis of the provided documentation and literature) and implement the concept of inductive aggregation in selected algorithms of density data grouping.

The task of the student, in addition to the implementation, will be to propose and conduct appropriate tests that will evaluate the performance of the programmed algorithms.

*Sample test sets*:

* [Clustering datasets] (https://cs.joensuu.fi/sipu/datasets/)

* Suggested implementation technologies *:
* Java - implementation of algorithms
* Python / ggplot - results visualization

<h3>D. Design and implementation of a progressive data clustering algorithm </h3>

The principle of the progressive algorithms (*anytime algoritms*) is that they can return the result even if their operation is interrupted. However, if the algorithm has a chance to run longer, then the expected result should be *better*. These types of algorithms are also sometimes referred to as *interruptible* algorithms.

The task of the student will be, based on the literature and the selected existing data grouping algorithm, to design in cooperation with the supervisor, implement and test the progressive algorithm.

<h3>*Other topics:*</h3>

<h3>E. Detection of patient behavior patterns based on the analysis of selected biomedical collections</h3>

Keywords: behavioral patterns exploration, diabetes data set

<h3>F. Analysis and evaluation of the usefulness of selected methods of supporting revenue management</h3>

Keywords: revenue management, prediction analysis

*Sample test sets*:

* [Clustering datasets] (https://cs.joensuu.fi/sipu/datasets/)

*Suggested implementation technologies*:

* Java - implementation of algorithms
* Python / ggplot - results visualization

### Selected literature

*Books*

1. Tadeusz Morzy, Data Mining, Methods and Algorithms, Polish Scientific Publishers PWN, 2017

*Papers*

1. P Lasek, Z Mei, Clustering and visualization of a high-dimensional diabetes dataset, Procedia Computer Science 159, 2179-2188
2. P Lasek, J Gryz, Density-based clustering with constraints, Computer Science and Information Systems 16 (2), 469-489
3. [Godfrey P., Gryz J., Lasek P.: Interactive Visualization of Large Data Sets, IEEE Transactions on Knowledge and Data Engineering (TKDE), 2016, pp 2142–2157.](http://ieeexplore.ieee.org/xpl/topAccessedArticles.jsp?punumber=69&topArticlesDate=July+2016)
4. Godfrey P., Gryz J., Lasek P., Razavi N.: Visualization through Inductive Aggregation, Proceedings of the 19th International Conference on Extending Database Technology, EDBT 2016, Bordeaux, France, March 14-18, 2016
5. Godfrey P., Gryz J., Lasek P., Razavi N.: Interactive Visualization of Big Data, Beyond Databases, Architectures, and Structures: 12th International Conference, BDAS 2016, Ustron, Poland, Springer, 2016.
6. Godfrey P., Gryz J., Lasek P., Razavi N.: Skydive: An Interactive Data Visualization Engine.  In IEEE Symposium on Large Data Analytics and Visualization, Chicago, USA, October 25-26., 2015