## About
Hi, I'm Emily! I hold a bachelor's degree in Applied Mathematics and am currently pursuing my MS in Analytics at UC Berkeley. My academic background has equipped me with a strong foundation in mathematics and statistics, driving my passion for deriving actionable insights from data across diverse industries. I am eager to apply my technical and analytical skills as an entry-level data specialist in data science.

Beyond academics, I actively explore new data analysis tools and methodologies, continuously expanding my knowledge. Whether collaborating in teams or independently, I find satisfaction in uncovering insights and solving complex problems using data.

Outside of academia, I dedicate my free time to exploring new data analysis tools and methodologies, constantly seeking opportunities to enhance my knowledge and skill set. Whether collaborating within a team or working independently, I am motivated by the thrill of discovering new insights and the gratification of leveraging data to tackle intricate problems.

This portfolio highlights my proficiency in various data analysis tools and programming skills, demonstrating my growth and commitment to this dynamic field.

## Table of Contents
- [About](https://github.com/github.com/EmilyQiu720/EmilyQiu720.github.io/blob/main/README.md#about)
- [Portfolio Projects](https://github.com/github.com/EmilyQiu720/EmilyQiu720.github.io/blob/main/README.md#portfolio-projects)
  - Python
    - [The Traveling Salesman Problem](https://github.com/EmilyQiu720/EmilyQiu720.github.io#the-traveling-salesman-problem)
    - [Machine learning approaches for super-resolution problems]
  - SQL
  - R
    - [Legendary Pokémon Analysis (Study Project)](https://github.com/github.com/EmilyQiu720/EmilyQiu720.github.io#legendary-pok%C3%A9mon-analysis)
  - Excel / Google Sheets
  - Tableau---> [go to Tableau..](https://public.tableau.com/app/profile/)
  - Power BI
- [Contact](https://github.com/github.com/EmilyQiu720/EmilyQiu720.github.io/blob/main/README.md#contacts)

## Portfolio Projects

### The Traveling Salesman Problem (TSP)
**Code:** [`The Traveling Salesman Problem`](https://github.com/EmilyQiu720/PortfolioProjects/tree/main/The%20Traveling%20Salesman%20Problem)

**Report:** [`TSP_Project_Report.pdf`](https://github.com/EmilyQiu720/PortfolioProjects/blob/main/Machine%20learning%20approaches%20for%20super-resolution%20problems/ML_Approaches_for_Super_Resolution_Problems_Report.pdf)

**Goal:** To assess various algorithmic strategies against the TSPLIB dataset to identify the most effective approaches for symmetric TSP instances.

**Description:** The project implemented a branch and bound algorithm for solving the Traveling Salesman Problem (TSP) using Python 3.10 and IBM's CPLEX version 22.1.1.0. The DOcplex API facilitates communication between our code and CPLEX, leveraging callbacks to interact during the algorithm's execution. 

Cutting plane techniques, including sub-tour elimination constraints (SECs) and 2-matching inequalities, were implemented to handle fractional solutions. Integer Programming (IP) gap monitoring guided termination by tracking the difference between the incumbent solution and the lower bound. 

Heuristic algorithms were implemented in two ways: 
1) Full construction at root node (warm-start) -- construct a feasible solution from scratch when no incumbent solution has yet been identified;
2) Refinement of a current solution: create integer solutions from fractional solutions or refine current integer solutions.

Nearest Neighbour and two-opt algorithms were selected for heuristic application, complemented by optional algorithms: Constuctions (cheapest insertion, farthest insertion, random insertion, greedy algorithm, nearest insertion, nearest neighbor), improvements (2-opt, 3-opt). 

The approach emphasized systematic node exploration and pruning to efficiently converge to optimal TSP solutions, ensuring a robust and efficient solution process integrating advanced branch and cut techniques with heuristic methods.

**Skills:** linear programming, data handling and manipulation, optimization techniques, algorithm development and optimization, statistical analysis, heuristic methods, performance monitoring, computation efficiency, software integration.

**Technology:** Python (Numpy, Matplotlib, cplex, docplex).

**Results:** The implementations led to significant improvements in solve time TSP instances with more than 200 nodes. Smaller TSP instances are fairly well solvable using the core branch and cut algorithm; thus the augmentations slowed these instances down (however with solve times of under 2 seconds the difference is practically insignificant). 

There is an average of 84.58% improvement in solve time of the medium and large TSP instances from adding all of our augmentations simultaneously and 60% improvement in the solution quality for larger TSP instances which did not solve to optimality. This suggests that our augmentations were indeed successful. 

Notable observations from the data:
- Warm-start ineffective when also implementing heuristic callback 
- The pairing of two matching and connected components leads to terrible solution attempts; specifically worse than adding no implementations at all

We ran the full implementation suite with a 1-hour time-limit on a set of 89 problems from the TSPLIB
- This was all problems that our machine had enough memory to load in: 
- The key observation from this data is that all instances on a specific node size are not equal 



<img align="left"  src="https://github.com/EmilyQiu720/EmilyQiu720.github.io/blob/main/images/The%20Traveling%20Salesman%20Problem/TSP%20Results.png" />

<img align="left"  src="https://github.com/EmilyQiu720/EmilyQiu720.github.io/blob/main/images/The%20Traveling%20Salesman%20Problem/TSPLIB%20data.png" />


### Machine learning approaches for super-resolution problems

**Code:** [`Machine learning approaches for super-resolution problems`](https://github.com/EmilyQiu720/PortfolioProjects/tree/main/Machine%20learning%20approaches%20for%20super-resolution%20problems)

**Report:** [`ML_Approaches_for_Super_Resolution_Problems_Report.pdf`](https://github.com/EmilyQiu720/PortfolioProjects/blob/main/Machine%20learning%20approaches%20for%20super-resolution%20problems/ML_Approaches_for_Super_Resolution_Problems_Report.pdf)

**Goal:** To investigate the feasibility of generating high-resolution satellite images from lower-resolution inputs by integrating machine learning techniques using python.

**Description:** The project centered on analyzing Synthetic Aperture Radar (SAR) satellite imagery data from Sentinel-1 and Capella Space, specifically within the 2023 Turkey–Syria earthquakes region. 

The metadata from SAR satellite imagery includes information about the imaging parameters (radiometric resolution, corrdinate reference system, radiometric accuracy) and acquisition conditions (orbit information, sensor configuration, swath width). 

The project invoved loading the data, cleaning and preprocessing it by applying Geographic Information Systems (GIS) tools like Quantum GIS. Tasks included refining image quality through noise removal, radiometric calibration, and speckle filtering processes. 

Mathematical concepts such as bilinear interpolation and entropy comparison were employed for proper image resizing and pixel alignment. Alternative approach for bilinear interpolation method was also implemented: the deep learning model - Enhanced Deep Residual Networks for Single Image Super-Resolution (EDSRx2) model. 

Machine learning models (Random Forest, Gradient Boosting, Decision Tree) were selected to perform image upscaling. Models were further enhanced through multidimensional feature vectors and Principal Component Analysis. Feature vectors includes surrounding pixel values, RGBI band pixel values from Sentinel-2, calculation of GNDVI, NDVI, and Building index, and integration of building layer from OpenStreetMap. 

**Skills:** data preprocessing, machine learning, deep learning.

**Technology:** Python (skimage, matplotlib, rasterio, numpy, scipy, PyTorch).

**Results:** The investigation reveals challenges due to limited high-resolution SAR images like Capella's.Super resolution methods were relied to upscale low-resolution data, which hinges on their effectiveness. Access to more high-resolution SAR images tailored to specific regions could significantly enhance our results. 

Approach pairing Sentinel-1 data with Capella data shows promise with its efficient use and initial positive outcomes, suggesting a need for further exploration and integration of tailored feature layers to improve model performance.

<img align="left" src="https://github.com/EmilyQiu720/EmilyQiu720.github.io/blob/main/images/Machine%20learning%20approaches%20for%20super-resolution%20problems/approach%201%20(bilinear%20interpolation).jpg" />

<img align="left" src="https://github.com/EmilyQiu720/EmilyQiu720.github.io/blob/main/images/Machine%20learning%20approaches%20for%20super-resolution%20problems/Approach%201%20(EDSRx2).jpg" />

<img align="left" src="https://github.com/EmilyQiu720/EmilyQiu720.github.io/blob/main/images/Machine%20learning%20approaches%20for%20super-resolution%20problems/Approach%202.jpg" />



### Contact

[<img align="left" alt="JoshMadakor | LinkedIn" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/linkedin.svg" />][linkedin]

[linkedin]: https://linkedin.com/in/emily-qiqiu/
