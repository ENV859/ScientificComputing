---
Title: ENV859 - Scientific computing
Author: John Fay
Date: Fall 2025
---

# Scientific Computing, Python, and GIS

## Introduction

Scientific computing (also called computational science) is all about how we humans can leverage computers to answer questions that we couldn't without them. GIS, in fact, is a good example of scientific computing as it allows us to study and analyze features across space that hard copy maps simply couldn't reveal on their own. 

Scientific computing as a discipline has been active for several decades, but it has become extremely hot in the past few years, driven by convergence of several interesting trends each relating to data. First, data collectors are everywhere: from smart phones, to security cameras, to internet-enabled appliances, to swipe cards and RFIDs. Second, data storage is cheap and getting cheaper. Third, network connectivity is penetrating more and more of our globe. And fourth, computing power to process all these data keeps growing. All this means that we are flooded with data, data that could answer many interesting and relevant questions, but only if we knew how to sift, sort, summarize, transform, analyze, and synthesize the data into meaningful chunks of actionable information - i.e., the domain of scientific computing. 

Another reason scientific computing has exploded in popularity is that the tools of the trade have become more accessible to the casual user. First, personal computers are as powerful as the supercomputers of yesterday, and if those machines don't cut it, we can rent vast computing power via services such as Google Cloud, Microsoft Azure, Amazon Web Services or SalesForce.com. And furthermore, scripting languages such as R and Python have become powerful, but fairly easy to use data analysis platforms - much in part to some key packages a few sharp developers have provided. 

And that leads us to the topic of this session: for us to capitalize on this "data revolution", we need to learn the key tools for doing data analysis - that is tools to collect, store, manage, summarize, combine, transform, and visualize data - that exist in Python. Fortunately, just a few packages take us a long way towards that end. These include: *NumPy*, Pandas, *Xarray*, MatPlotlib, and *SciPy*.

This document describes these Python packages in enough detail to get you familiar with what it does and then points to a number of Jupyter notebooks with some hands-on exercises. 

| Topic                       | Learning Objectives                                          |
| --------------------------- | ------------------------------------------------------------ |
| 1. NumPy & NumPy Arrays     | • Explain **NumPy's usefulness** in the Python coding world<br />• Describe the difference between a Python list and a **Numpy vector** <br />• Create **Numpy arrays** of various shapes, sizes, & values <br />• **Compute statistics** on NumPy arrays <br />• **Convert a feature class to a Numpy array** using ArcPy<br />• **Convert a raster to a NumPy array** using ArcPy <br />• Explain what a **stacked array** is an how it can be useful in spatial analysis |
| 2. Exploring Data in Pandas | • Describe the basic form of a **Pandas dataframe**<br />• **Load data** from a CSV file into a dataframe<br />• View and inspect data/**dataframe properties**<br />• **Select columns** from a dataframe<br />• Generate **descriptive statistics** from data in a dataframe<br />• Create some **basic plots** in Pandas |
| 3. Data Analysis in Pandas  | • **Calculating and updating** fields<br/>• **Selecting data** in a dataframe<br/>   -    Selecting single rows, select rows, or row slices using `iloc`<br/>   -    Selecting rows and columns using `iloc`<br/>   -    Selecting rows and columns using `loc`<br/>   -   Selecting rows based on criteria - using *queries*<br/>   -   Selecting rows based on criteria - using *masks*<br/>   -   Updating values in selected rows/columns<br/>• **Grouping and aggregating** data in a dataframe<br />• **Transforming data with Pivot Tables** |
| 4. Quick Plots with Pandas  | • Brief overview of plotting using Pandas                    |

---

## *NumPy*

### What is NumPy?

- Provides a new data type - the array - which can greatly speed up certain computations.
  - <u>Example</u>: BMI from height and weight lists (`00-Intro-to-NumPy.ipynb`)
  - <u>Intro</u>: A quick glimpse into NumPy's *ndarray* data type (`01-NumPy-101.ipynb`)
- Incorporated into ArcGIS now as it provides useful (and fast) tabular analysis
  - <u>Example</u>: NC HUCs (`02-Numpy-with-FeatureClasses.ipynb`)
- Converting rasters to NumPy arrays also allows for analysis beyond ArcGIS/ArcPy
  - <u>Example</u>: DEM -> NumPy array -> Computing TPI (`03-Using-NumPy-With-Rasters.ipynb`)

### More on NumPy

- https://jakevdp.github.io/PythonDataScienceHandbook/index.html#2.-Introduction-to-NumPy
- http://www.scipy-lectures.org/intro/numpy/index.html
- https://jalammar.github.io/visual-numpy/

### Overall...

- Numpy is all about arrays, i.e., dimensional data
- It offers easy ways to 
- Numpy is useful, but spend more time on Pandas...

------

## *Pandas* 

### What is Pandas?

- The "Swiss army knife" of data manipulation in Python. 

- Like NumPy, adds a new data type to Python: the **data frame**
- DataFrames are often compared to spreadsheets or database tables: rows and columns
  - All values in a column are of the same data type
  - Each row has a unique index value
  - Thus we can reference each row by its index and each column by its name
- With data in a data frame, Pandas has the tools to:
  - sort, transform, pivot, melt data
  - subset/select/query specific row and or columns
  - compute summary stats
  - aggregate and join 
  - plot data

### More on Pandas

- https://jakevdp.github.io/PythonDataScienceHandbook/03.00-introduction-to-pandas.html
- https://www.datacamp.com/courses/pandas-foundations
- http://nbviewer.jupyter.org/github/justmarkham/pandas-videos/blob/master/pandas.ipynb

### Overall

While NumPy is an essential component for data analysis in Python, Pandas is likely more useful for every data tasks. It's DataFrame and other programming classes and functions are well organized and logically written. It does take a bit of time to get comfortable with all that it can do, especially if you are use to the visual learning that goes with desktop applications like Excel, but the more you stick with it, the more you'll see that Pandas can do - especially alongside all the other magnificent data packages being crafted for Python every day. 

---

