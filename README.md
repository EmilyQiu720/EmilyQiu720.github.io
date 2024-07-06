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

**Report:** [`TSP_Project_Report.pdf`]([https://github.com/EmilyQiu720/PortfolioProjects/blob/main/Machine%20learning%20approaches%20for%20super-resolution%20problems/ML_Approaches_for_Super_Resolution_Problems_Report.pdf](https://github.com/EmilyQiu720/PortfolioProjects/blob/main/The%20Traveling%20Salesman%20Problem/TSP_Project_Report.pdf))

**Goal:** To assess various algorithmic strategies against the TSPLIB dataset to identify the most effective approaches for symmetric TSP instances.

**Description:** The project implemented a branch and cut algorithm for solving the Traveling Salesman Problem (TSP) using Python 3.10 and IBM's CPLEX version 22.1.1.0. The DOcplex API facilitates communication between our code and CPLEX, leveraging callbacks to interact during the algorithm's execution.

Key features include:

- Warm-Start Initialization: Utilizing the Nearest Neighbour and two-opt algorithms to provide an initial solution. (Other optional algorithms are implemented as well)

- Integer Programming (IP) Gap: Monitoring the difference between the incumbent and lower bound to guide termination.

- Heuristic Callbacks: Constructing feasible solutions to improve the incumbent during the branch and cut process.

- Cutting Plane Techniques: Implementing sub-tour elimination constraints (SECs) and 2-matching inequalities for fractional solutions.

- Systematic Node Exploration and Pruning: Efficiently exploring and pruning nodes to ensure convergence to the optimal solution.

This approach ensures a robust and efficient solution process for the TSP, integrating advanced branch and cut techniques and heuristic methods.

**Skills:** data handling and manipulation, optimization techniques, algorithm development and optimization, statistical analysis, heuristic methods, performance monitoring, computation efficiency, software integration.

**Technology:** Python (Numpy, Matplotlib, cplex, docplex).

**Results:** Explored an exact solution strategy to the TSP with a set of supplementary augmentations to this solution process. Affirmed that this solution strategy constitutes a viable exact strategy for the TSP and that when applied in conjunction, each of our augmentations do indeed aid the solution process - as is expected given the widespread attention these augmentations have received. 

### Machine learning approaches for super-resolution problems

**Code:** [`Machine learning approaches for super-resolution problems`](https://github.com/EmilyQiu720/PortfolioProjects/tree/main/Machine%20learning%20approaches%20for%20super-resolution%20problems)

**Report:** [`ML_Approaches_for_Super_Resolution_Problems_Report.pdf`](https://github.com/EmilyQiu720/PortfolioProjects/blob/main/Machine%20learning%20approaches%20for%20super-resolution%20problems/ML_Approaches_for_Super_Resolution_Problems_Report.pdf)

**Goal:** To investigate the feasibility of generating high-resolution satellite images from lower-resolution inputs by integrating machine learning techniques using python.

**Description:** The project centered on analyzing Synthetic Aperture Radar (SAR) satellite imagery data from Sentinel-1 and Capella Space, specifically within the 2023 Turkey–Syria earthquakes region. The metadata from SAR satellite imagery includes information about the imaging parameters (radiometric resolution, corrdinate reference system, radiometric accuracy) and acquisition conditions (orbit information, sensor configuration, swath width). The project invoved loading the data, cleaning and preprocessing it by applying Geographic Information Systems (GIS) tools like Quantum GIS. Tasks included refining image quality through noise removal, radiometric calibration, and speckle filtering processes. Mathematical concepts such as bilinear interpolation and entropy comparison were employed for proper image resizing and pixel alignment. Alternative approach for bilinear interpolation method was also implemented: the deep learning model - Enhanced Deep Residual Networks for Single Image Super-Resolution (EDSRx2) model. Machine learning models (Random Forest, Gradient Boosting, Decision Tree) were selected to perform image upscaling. Models were further enhanced through multidimensional feature vectors and Principal Component Analysis. Feature vectors includes surrounding pixel values, RGBI band pixel values from Sentinel-2, calculation of GNDVI, NDVI, and Building index, and integration of building layer from OpenStreetMap. 

**Skills:** data preprocessing, machine learning, deep learning.

**Technology:** Python (skimage, matplotlib, rasterio, numpy, scipy, PyTorch).

**Results:** The investigation reveals challenges due to limited high-resolution SAR images like Capella's.Super resolution methods were relied to upscale low-resolution data, which hinges on their effectiveness. Access to more high-resolution SAR images tailored to specific regions could significantly enhance our results. Approach pairing Sentinel-1 data with Capella data shows promise with its efficient use and initial positive outcomes, suggesting a need for further exploration and integration of tailored feature layers to improve model performance.

[<img align="left"
   src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/linkedin.svg" />][linkedin]




[<img align="left" alt="JoshMadakor | LinkedIn" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/linkedin.svg" />][linkedin]

[linkedin]: https://linkedin.com/in/emily-qiqiu/
