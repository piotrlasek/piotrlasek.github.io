---
layout: page
title: Proposed topics for engineering and master's theses
permalink: /for-students/topics-en
exclude: true
---

Last updated: June 17, 2020

## Sample topics - for individual discussion

 1. Analysis and implementation of the k-means algorithm supported by the pi-cube structure.
 2. Experiments and implementation of interactive data access methods using hierarchical structures.
 3. Implementation and tests of a new method of density grouping based on the DBSCAN algorithm and the granular pi-cube structure.
 4. Implementation and tests of a new method of density grouping based on the NBC algorithm and the granular structure of pi-cube.
 5. Design and implementation of a web-based interactive large data visualization module on the example of the Checkins set.
 6. Design and implementation of a web module for interactive visualization of large data sets on the example of the Checkins set.
 7. Design and implementation of a module for testing the performance of hierarchical data structures.
 8. Approximate grouping based on hierarchical data structure - implementation and analysis of selected algorithms.
 9. Grouping with constraints using neural networks to determine the distance between objects.
10. Implementation and analysis of the DBSCAN algorithm using the MADlib platform.
11. Implementation and analysis of the NBC algorithm using the MADlib platform.
    
A bit more details ...

## Interactive data visualization and mining

In the context of data mining, the word interactive can reflect what data analysts should work like, or in principle, should work. In 1996, Shneiderman formulated a kind of metaphor describing the process of data analysis, the so-called a mantra (Shneiderman, 1996) that specialists often refer to when they want to explain the concept of interactive data exploration or visualization. The mentioned matrix was: * Overview first, zoom and filter, then details on demand *. According to it, an example of an interactive data analysis process may look like this: An analyst asks the system an * analytical task *, waits for a response, and then analyzes it, that is, tries to understand and evaluate it. If he is unable to draw conclusions of value based on the system's response, he changes the query parameters and repeats the entire process. In the event that the response time is high - say, greater than five seconds - then such a process according to HCI (* human-computer interaction *) standards becomes cumbersome for the user. In such a situation, we cannot conclude that the data mining or analysis process is interactive. This is especially important when the data set is large. This is also the reason why current methods of big data mining are becoming insufficient. By operating on a large number of objects, the analyst is simply unable to get answers about the system in a short time. Nevertheless, assuming that the user is not always interested in the * exact * result of the analysis (which in many cases is true), it seems that the answer to the problem described here may be designing the algorithms in such a way that the user can receive just an approximate answer in a given by him time. An example of a solution that uses this idea is the BlinkDB prototype database (Agrawal, 2013), which allows the user to ask questions specifying the expected time of obtaining the result and its assumed quality.

Taking into account the above comment on data mining and visualization in the context of designing and building interactive systems, we propose several engineering topics below. Their common element is the use of a special structure (pi-cube) that allows access to data with a given degree of granularity, which allows reducing the amount of data needed for their visualization or exploration.

! [Simplified System Diagram] ({{site.url}} / files / diagram-2017.png)

** A few suggested topics in detail ... **

<h3> A. Design and implementation of the programming interface of the interactive data visualization and mining system </h3>

The aim of the work is to design and implement a programming interface (API) in a selected technology for an interactive data visualization and mining system. The API will be an interface between the relational database and other modules of the system (i.e. the visualization module and the analytical module). The main tasks of the API will be to provide the user with the ability to perform the following operations:

* Creating and modifying the pi-cube structure based on the indicated data source (table in a relational database).
* Retrieving the indicated parameterized (using an appropriate filter) data fragment.
* Optimization of the method of data transfer between components in such a way as to maintain the interactivity of the system.

* Additional assumptions and requirements *:

* Preparation of a set of unit tests for the created software.
* Testing the API capabilities using an existing data visualization library (eg D3.js or ggplot).
* Perform experiments using different datasets (e.g. Checkins, New York Taxi Cab, Seattle Fire Calls, etc.).
* Presentation of the results of experiments in a clear and understandable form.

* Suggested implementation technologies *:

* Python
* Django
* JSON

<h3> B. Implementation of an interactive data visualization module using
     WebGL </h3> component
     
The aim of this task is to develop and implement an interactive data visualization module based on the WebGL component, which is an element of the HTML5 language. The module should meet the following assumptions:

* The module should have a java script library with which to access the data delivery module.
* The library should communicate with the data delivery module using the appropriate RESTful defined interface.
* For testing purposes, the module should allow you to replace references to the RESTful website with data from previously prepared JSON files.
* The basic functions of the data visualization interface should be supported, such as: * zooming in *, * zooming out *, * panning *, * selection *.

* Suggested implementation technologies *:

* Java Script
* HTML5 (WebGL)
* jQuery
* Bootstrap

<h3> C. Application of inductive data aggregation in selected algorithms
     density grouping </h3>

The aim of the task is to adapt (in cooperation with the supervisor, on the basis of the provided documentation and literature) and implement the concept of inductive aggregation in selected algorithms of density data grouping.

The task of the student, in addition to the implementation, will be to propose and conduct appropriate tests that will compensate the performance of the programmed algorithms. The source code created in this way will be included as a module in the system for testing data mining algorithms [DMTOOLS] (https://github.com/piotrlasek/clustering).

* Sample test sets *:

* [Clustering datasets] (https://cs.joensuu.fi/sipu/datasets/)

* Suggested implementation technologies *:

* Java - implementation of algorithms
* Python / ggplot - results visualization

<h3> D. Design and implementation of a progressive data clustering algorithm </h3>

The principle of the progressive algorithms (* anytime *) is that they can return the result even if their operation is interrupted. However, if the algorithm has a chance to run longer, then the expected result should be * better *. These types of algorithms are also sometimes referred to as * interruptible * algorithms.

The task of the engineer will be, based on the literature and the selected existing data grouping algorithm, to design in cooperation with the supervisor, implement and test the progressive algorithm. The source code created in this way will be included as a module in the system for testing data mining algorithms [DMTOOLS] (https://github.com/piotrlasek/clustering).

<h3> E. Detection of patient behavior patterns based on the analysis of selected biomedical collections </h3>

Keywords: behavioral patterns exploration, diabetes data set

<h3> F. Analysis and evaluation of the usefulness of selected methods of supporting revenue management </h3>

Keywords: revenue management, prediction analysis

* Sample test sets *:

* [Clustering datasets] (https://cs.joensuu.fi/sipu/datasets/)

* Suggested implementation technologies *:

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